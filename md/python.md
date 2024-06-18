Using Autoplot in the Python Environment, using JPype.

Audience: Autoplot users who would like to use the software to read data
into Python, and to use other Autoplot codes from these environments

See also: [help.jython](help.jython.md "wikilink") which is the Java-based
version of Python which is used to script Autoplot.

# Introduction

**More recent versions of Python (e.g 3.8 on Linux) are not able to use
these steps. Updates to this documentation are coming. See
<https://github.com/autoplot/python/blob/master/README.rst>**

Both IDL and MATLAB make it extremely easy to use Java code in these
environments. Autoplot is able to read data from a variety of input
sources using compact URIs to specify data locations, making it useful
accessing digital data. For example, it's difficult to read data from an
Excel worksheet into IDL, but since Autoplot can read this data, it
becomes just as easy to read data from this source as it is a table of
ASCII data. Further, Matlab can read data from CDF files, but its
low-level CDF interface makes Autoplot attractive, because you can
access data with just several lines of code. Last, Autoplot can
automatically retrieve and manage data from remote sites via FTP and
HTTP, so this mechanism can be used in IDL and MATLAB as well.

Autoplot contains a number of codes that are useful, in addition to
reading data. For example, Autoplot is able to write data to a number of
data formats, and this code is useful in Matlab as well.

JPype is a Python library that bridges Java to native Python, and it is
used to provide this functionality to Python as well.

# Getting Started

First we need to connect the Autoplot code to the environment. In these
examples, "Unix\>" is used to indicate commands entered into a Unix BASH
shell, and "\>\>\>" a (native) Python 2.6 session.

## Installing JPype

JPype is the bridge that allows Python to talk to Java codes, and
Autoplot. First we'll have to install it.

```
Unix> # go to SourceForge `<https://sourceforge.net/projects/jpype/>` and download JPype.  File is JPype-0.5.4.2.zip 
Unix> # unzip it
Unix> cd  JPype-0.5.4.2
Unix> export JAVA_HOME=/usr/local/jdk1.8
Unix> python setup.py build 
Unix> python setup.py install --home=~ 
Unix> ls ~/lib64/python/ 
Unix> export PYTHONPATH=~/lib64/python 
Unix> python
>>> from jpype import startJVM, JPackage     # verify that we can import it without ImportError
```
### Ubuntu Linux Notes

I had to install python-dev:

  - sudo apt-get install python-dev

The "egg" was installed in \~/lib/python, not \~/lib64/python.

### Mac notes

On a Mac, you have to do some other bits.

  - the jpype build refers to a bunch of -I folders, and you need to
    make links from the actual locations to these names.
  - cd /Library/Java/, sudo ln -s
    JavaVirtualMachines/jdk1.8.0\_31.jdk/Contents/Home Home
  - export JAVA\_HOME=/Library/Java/Home
  - "jni\_md.h" needs to be linked
  - the "startJVM" command below will need to be pointed at
    libjvm.dylib.

## Using pip

Larry at The University of Iowa succeeded in using pip to install:

```
yum -y install python-pip
pip2.6 install jpype1
```
## Using condas

Using Anaconda and Spyder, I was able to add jpype and then run the
scripts from the command line:

```
./conda install -c conda-forge jpype1
```
## Connecting the Jar File

In either case, you'll need to download the Autoplot "single jar"
release that is available along with each release of the software. For
example, the release at <http://autoplot.org/jnlp/latest/> has a link to
a single jar version here:
<http://autoplot.org/jnlp/latest/autoplot.jar>. This 25 megabyte jar
file is similar to a .so file from C and Fortran, and contains compiled
code and also needed resources. Note this is a full Autoplot and can be
used from the command line, bypassing the mechanism normally used to
launch Autoplot. If this seems large, consider that this contains code
to read NetCDF, OpenDAP, CDF, Excel, and many other forms of data.

### Connecting to Python

Python is able to add the jar after the session is started, with the
plugin jpype. You'll have to use your JRE location (Java 7 is required),
and autoplot.jar can be downloaded from
<http://autoplot.org/latest/autoplot.jar>

```
>>> from jpype import *
>>> startJVM(getDefaultJVMPath(),'-Djava.class.path=/tmp/autoplot.jar')
>>> org= JPackage("org")
>>> apds = org.autoplot.idlsupport.APDataSet()
QDataSetBridge v2.1.0
APDataSet v1.5.0
```
If you are using Spyder, note Spyder keeps the Python session open, and
you only need to start the JVM once. So here is a code which addresses
the issue:

```
try:
   startJVM('/usr/local/jdk1.8/jre/lib/amd64/server/libjvm.so','-Djava.class.path=/tmp/autoplot.jar')
except:
   print 'JVM already started'
```
At <https://github.com/autoplot/python>, we have a project which hopes
to make use in Python as easy as possible. This can be downloaded and
added to Python by hand, or using pip, it's:

```
pip install autoplot
```
This will make things more like use in Matlab, where the jar file is
downloaded and JVM automatically started:

```
>>> from autoplot import javaaddpath
>>> org= javaaddpath('`<http://autoplot.org/devel/autoplot.jar>`')
>>> apds = org.autoplot.idlsupport.APDataSet()
```
## First Read of Data

Suppose you have been using the Autoplot URI (data address)
<http://autoplot.org/data/swe-np.xls?column=data&depend0=dep0> to read
data into Autoplot.

```
>>> apds.setDataSetURI( '`<http://autoplot.org/data/swe-np.xls?column=data&depend0=dep0>`' )
>>> apds.doGetDataSet()

>>> print( apds.toString() )
```
<http://autoplot.org/data/swe-np.xls?column=data&depend0=dep0>  
```
data: data[dep0=288] (dimensionless)
dep0: dep0[288] (days since 1899-12-30T00:00:00.000Z) (DEPEND_0)

>>> vv= apds.values()
>>> print( vv[0] )
3.4716999530792236
```
## QDataSet in this Interface

This interface is meant to provide access to anything that can be
represented within Autoplot and its internal data model,
[QDataSet](QDataSet.md "wikilink").

QDataSet is meant to be a simple, uniform data interface that is adapted
to many different syntaxes, including Java, Python, C, IDL and MATLAB.
However, it's more of a guide than a specification, and since Python
(and IDL and Matlab) are slow when many commands are executed, we
provide access to data via arrays rather than individual values as in
Java. Also, we provide access to timetags and other independent data
through the one object. This should simplify use in the environments.
For example, we say:

```
dep0Name= apds.depend(0)
x= apds.values( dep0Name )
```
or

```
x= apds.values( apds.depend(0) )
```
Another difference is that the apds is mutable, meaning its state can be
changed, whereas QDataSets are generally immutable. For example, you can
tell the apds what your preferred units are, affecting what is returned
by the values() command.

# DataSet Properties

You can access the dataset properties like so:

```
dsp= apds.properties( )
print dsp.get('NAME')

yp= apds.properties( 'dep0' )
print yp.get('UNITS') 
```
or

```
print apds.property( 'dep0', 'UNITS' )
```
# The Rest of the Reader Interface

What are the X values? They are in some strange unit that the data
source chooses. In this example it is "days since
1899-12-30T00:00:00.000Z". We can specify what units we want:

```
apds.setPreferredUnits( 'hours since 2007-01-17T00:00' )
import numpy as np
import matplotlib.pyplot as plt
plt.plot( apds.values('dep0'), apds.values(), '.-' ) 
plt.show( ) 
```
Here are some example units strings: seconds since 2010-01-01T00:00,
days since 2010-01-01T00:00, Hz, MHz. Note Autoplot's units are not
fully developed, and conversions are not always possible.

We also can work with fill data:

```
apds.setFillDouble( -999 )
```
This will convert whatever fill is in the dataset to this value. This
saves the developer the time of reading what the fill, validmin, and
validmax are in the QDataSet.

The Autoplot package provides a means to read the time values as
datetime64.

```
vv= to_ndarray( apds, 'DST' )
tt= toDateTime( apds, 'Epoch' )
plt.plot( tt, vv )
```
# Access other Autoplot classes

Other classes Autoplot uses can be accessed. For example,

```
import jpype
jpype.startJVM( jpype.getDefaultJVMPath(),'-Djava.class.path=/tmp/autoplot.jar' )
org= jpype.JPackage("org")
sc= org.autoplot.ScriptContext
x= sc.getCompletions( '`<http://autoplot.org/data/somedata.cdf>`?')
```
lists all the variables in the CDF file.

#### Format datasets from Python

Here's how we can use Autoplot's formatting to export data:

```
from autoplot import *
org= javaaddpath('`<http://autoplot.org/jnlp/devel/autoplot.jar>`')
dsu= org.das2.qds.DataSetUtil
ops= org.das2.qds.ops.Ops   # note these must point to a Java class, unlike Matlab.
ds= dsu.asDataSet( ops.link( ops.timegen('1999-01-01T00:00Z', '1s', 200 ), ops.randomu( 0, 200 ) ) )
sc= org.autoplot.ScriptContext
sc.formatDataSet( ds, '/tmp/foo.xls' )
```
TODO: use a NumPy array. This doesn't work for me.

#### adapt NumPy

Here's with a numpy array. The trick here is you have to convert it to a
list first.

``` python
import numpy,jpype
from autoplot import javaaddpath
org= javaaddpath( 'http://autoplot.org/jnlp/latest/autoplot.jar' )

nn= numpy.zeros( (20) )
aa= jpype.JArray(jpype.JFloat,1)(nn.tolist())
dataset= org.das2.qds.ops.Ops.dataset
ds= dataset(aa)
sc= org.autoplot.ScriptContext
sc.formatDataSet( ds, '/tmp/oneD.cdf' )
```
`
```
I had trouble with the two-D case (numpy.zeros(20,30)).

## Static methods in Python

```
fs= org.das2.util.filesystem.FileSystem
afs= fs.create('`<https://emfisis.physics.uiowa.edu/Flight/RBSP-B/L4/>`') 
fsm= org.das2.fsm.FileStorageModel
afsm= fsm.create(afs,'$Y/$m/$d/rbsp-b_WFR-waveform-magnitude_emfisis-L4_$Y$m$d_v$(v,sep).cdf')
dru= org.das2.datum.DatumRangeUtil
dr= dru.parseTimeRange('2014-02')
ff= afsm.getFilesFor( dr )      # this will download all files in the interval
for f in ff: print f.toString()
```
# Problems

See <http://autoplot.org/idl#Problems>.

  - JPype doesn't let you call overloaded methods, so setFillValue()
    doesn't work. Instead use setFillDouble and setFillFloat, which are
    available in the latest devel release.

# See Also

Here is the nightly test which tells all:
<http://jfaden.net/jenkins/job/autoplot-test024/>

We've made a pip package which include javaaddpath to make it more like
Matlab, where the autoplot.jar download is handled. See
<https://github.com/autoplot/python/>

# Complete Python Examples

This example assumes you have jpype and matplotlib installed:

```
javalib= '/usr/local/jdk1.8/jre/lib/amd64/server/libjvm.so' # you will need to set this to your JVM

from jpype import *
import urllib
urllib.urlretrieve( '`<http://autoplot.org/jnlp/latest/autoplot.jar>`', '/tmp/autoplot.jar' )
startJVM( javalib,'-Djava.class.path=/tmp/autoplot.jar')
org= JPackage("org")
apds= org.autoplot.idlsupport.APDataSet()
t= '2018-01-17'
apds.setDataSetURI( '`<http://cdaweb.gsfc.nasa.gov/sp_phys/data/ace/swepam/level_2_cdaweb/swe_k0/$Y/ac_k0_swe_$Y$m$d_v$v.cdf?Np&timerange=>`' + t );
apds.doGetDataSet()
apds.setPreferredUnits( 'hours since '+t )
print apds.toString()
```
`#&nbsp;`&lt;http://cdaweb.gsfc.nasa.gov/sp_phys/data/ace/swepam/level_2_cdaweb/swe_k0/$Y/ac_k0_swe_$Y$m$d_v$v.cdf?Np&amp;timerange=2018-01-17&gt;  
```
# Np: Np[Epoch=288] (#/cc)
# Epoch: Epoch[288] (cdfEpoch) (DEPEND_0)
import numpy as np
import matplotlib.pyplot as plt
plt.plot( apds.values('Epoch'), apds.values(), '.-' )
plt.show()
```
Here's a Juno example which was crashing Python with an old version of
jpype:

```
javalib= '/usr/local/jdk1.8/jre/lib/amd64/server/libjvm.so' # you will need to set this to your JVM

from jpype import *
import urllib
urllib.urlretrieve( '`<http://autoplot.org/jnlp/devel/autoplot.jar>`', '/tmp/autoplot.jar' )
startJVM( javalib,'-Djava.class.path=/tmp/autoplot.jar')
org= JPackage("org")
apds= org.autoplot.idlsupport.APDataSet()  
apds.loadDataSet( 'vap+das2Server:`<http://jupiter.physics.uiowa.edu/das/server?dataset=Juno/FGM/ElectronCyclotron&start_time=2017-02-01T00:00:00.000Z&end_time=2017-02-04T00:00:00.000Z>`' )
apds.setPreferredUnits( 'hours since 2017-02-01T00:00:00.000' )
import numpy as np
import matplotlib.pyplot as plt
plt.plot( apds.values('ds_1'), apds.values('fce'), '.-' )
plt.show()
```
I believe this has something to do with the length of the data. If I
load just the first 100000 points, it's fine. plt.plot( xx\[0:\],
yy\[0:\] ) gives a message about "signed integer is greater than
maximum". plt.plot(xx,yy) hangs. TODO: This Juno source is
password-protected anyway, so switch to an open a smaller dataset. See
also <https://sourceforge.net/p/autoplot/bugs/2012/> .

# Error Messages

'No matching overloads found.' this happens when you forget the (), for
example with apds= org.autoplot.idlsupport.APDataSet().

