Using Autoplot in the MATLAB Environment

Audience: Autoplot users who would like to use the software to read data
into MATLAB, and to use other Autoplot codes from these environments

# Introduction

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

# Getting Started

First we need to connect the Autoplot code to the environment. In these
examples, "Unix\>" is used to indicate commands entered into a Unix BASH
shell, and "MATLAB\>" an MATLAB v7.7 session.

You can verify the Java version by calling the Java method:

```
>> java.lang.System.getProperty('java.version')
ans =
1.8.0_181
```

## Connecting the Jar File

In either case, you'll need to download the Autoplot "single jar"
release that is available along with each release of the software. For
example, the development release at <http://autoplot.org/jnlp/latest/>
has a link to a single jar version here:
<http://autoplot.org/jnlp/latest/autoplot.jar>. For MATLAB, you don't
need to download the file, but to be consistent with IDL, we will
download it to /tmp/autoplot.jar or some location appropriate for your
workstation. This 30 megabyte jar file is similar to a .so file from C
and Fortran, and contains compiled code and also needed resources. Note
this is a full Autoplot and can be used from the command line, bypassing
the mechanism normally used to launch Autoplot. If this seems large,
consider that this contains code to read NetCDF, OpenDAP, CDF, Excel,
and many other forms of data.

### Connecting to MATLAB

MATLAB is able to add the jar after the session is started, with the
command "javaaddpath":

```
MATLAB> javaaddpath( '/tmp/autoplot.jar' )
```

Note this can be a URL, like

```
MATLAB> javaaddpath( '`<http://autoplot.org/jnlp/latest/autoplot.jar>`' )
```

Note older versions of Matlab use Java 6 and will not work with Autoplot
version v2015a\_5 and newer.

Now we can test to see that the jar file is connected:

```
MATLAB> apds  = org.autoplot.idlsupport.APDataSet;
APDataSet v1.6.5
Java Version 1.8.0_181
disabling HTTP certificate checks.
```

## First Read of Data

![Autoplot can be used to read data into IDL and
MATLAB](idlMatlabInterface.png
"Autoplot can be used to read data into IDL and MATLAB")

Suppose you have been using the Autoplot URI (data address)
<http://www.autoplot.org/data/swe-np.xls?column=data&depend0=dep0> to
read data into Autoplot.

```
MATLAB> apds.setDataSetURI( '`<http://www.autoplot.org/data/swe-np.xls?column=data&depend0=dep0>`' )
MATLAB> apds.doGetDataSet
```

Note there's a bug where MATLAB is unable to read AbstractPreferences,
and you see an error message associated with this. This message can be
ignored. Note the default autoplot\_data/fscache must always be used.

```
MATLAB> apds
apds =
```
<http://www.autoplot.org/data/swe-np.xls?column=data&depend0=dep0>  
```
data: data[dep0=288] (dimensionless)
dep0: dep0[288] (days since 1899-12-30T00:00:00.000Z) (DEPEND_0)
```

```
MATLAB> plot( apds.values )
```

## QDataSet in this Interface

This interface is meant to provide access to anything that can be
represented within Autoplot and its internal data model,
[QDataSet](QDataSet.md "wikilink").

QDataSet is meant to be a simple, uniform data interface that is adapted
to many different syntaxes, including Java, Python, C, IDL and MATLAB.
However, it's more of a guide than a specification, and since both IDL
and MATLAB are slow when many commands are executed, we provide access
to data via arrays rather than individual values as in Java. Also, we
provide access to timetags and other independent data through the one
object. This should simplify use in the environments. We say:

```
dep0Name= apds.depend(0)
x= apds.values( dep0Name );
```

or

```
x= apds.values( apds.depend(0) );
```

Another difference is that the apds is mutable, meaning its state can be
changed, whereas QDataSets are generally immutable. For example, you can
tell the apds what your preferred units are, affecting what is returned
by the values() command.

# DataSet Properties

You can access the dataset properties like so:

```
dsp= apds.properties( )
dsp.get('NAME')
```
  
```
yp= apds.properties( 'dep0' )
yp.get('UNITS') 
```

or

```
apds.property( 'dep0', 'UNITS' )
```

# The Rest of the Reader Interface

What are the X values? They are in some strange unit that the data
source chooses. In this example it is "t1970", which is the number of
non-leap seconds since 1970-Jan-01T00:00. We can specify what units we
want:

```
apds.setPreferredUnits( 'hours since 2007-01-17T00:00' )
plot( apds.values('dep0'), apds.values() ) 
```

Here are some example units strings: seconds since 2010-01-01T00:00,
days since 2010-01-01T00:00, Hz, MHz. Note Autoplot's units are not
fully developed, and conversions are not always possible.

We also can work with fill data:

```
apds.setFillValue( -999 )
```

This will convert whatever fill is in the dataset to this value. This
saves the developer the time of reading what the fill, validmin, and
validmax are in the QDataSet.

# Access other Autoplot classes

Other classes Autoplot uses can be accessed. For example,

```
sc= org.autoplot.ScriptContext;
x= sc.getCompletions( 'vap+cdfj:`<http://autoplot.org/data/somedata.cdf>`?')
```

lists all the variables in the CDF file.

#### Format datasets from MATLAB

Here's how we can use Autoplot's formatting to export data:

```
dsu= org.das2.qds.DataSetUtil;
ds= dsu.asDataSet( rand( 200,1 ) )    % adapt Matlab array to QDataSet.  
sc= org.autoplot.ScriptContext;
sc.formatDataSet( ds, '/tmp/foo.cdf?randata' )
```

The extension is used to control the output format.

## Static methods in Matlab

```
Matlab> afs= org.das2.util.filesystem.FileSystem.create('`<https://emfisis.physics.uiowa.edu/Flight/RBSP-B/L4/>`')
Matlab> afsm= org.das2.fsm.FileStorageModel.create(afs,'$Y/$m/$d/rbsp-b_WFR-waveform-magnitude_emfisis-L4_$Y$m$d_v$(v,sep).cdf')
Matlab> dr= org.das2.datum.DatumRangeUtil.parseTimeRange('2014-02')
Matlab> ff= afsm.getFilesFor( dr );
Matlab> print ff(0).toString()
```

# Problems

There are some technical issues with all this.

Also:

  - It seems clear that you'd want to be able to use Autoplot to verify
    data, so applot should accept apds as an argument.
  - Filters are not readily accessible in IDL and MATLAB, and it would
    nice to show how these could be used.

# See Also

Here is the nightly test which tells all:
<http://jfaden.net/jenkins/job/autoplot-test024/>. See Test024.java,
which uses Java (instead of Matlab) to call the interface.

# Complete MATLAB Examples

```
javaaddpath( '`<http://autoplot.org/jnlp/latest/autoplot.jar>`' )
apds= org.autoplot.idlsupport.APDataSet;
t= '2019-01-17';
apds.setDataSetURI( strcat( '`<https://cdaweb.gsfc.nasa.gov/sp_phys/data/ace/swepam/level_2_cdaweb/swe_k0/$Y/ac_k0_swe_$Y$m$d_v$v.cdf?Np&timerange=>`', t ) );
apds.doGetDataSet;
apds.setPreferredUnits( 'hours since 2019-01-17' );
plot( apds.values( apds.depend(0) ), apds.values );
```

Read Emfisis waveform files:

```
javaaddpath( '`<http://autoplot.org/jnlp/latest/autoplot.jar>`' )
apds= org.autoplot.idlsupport.APDataSet;
apds.setDataSetURI( '`<https://emfisis.physics.uiowa.edu/Flight/RBSP-A/L2/2013/10/03/rbsp-a_WFR-waveform-continuous-burst_emfisis-L2_20131003T17_v1.3.2.cdf?BuSamples>`' );
apds.doGetDataSet;
apds.setPreferredUnits( 'seconds since 2013-10-03T17:00' );
plot( apds.values( apds.depend(1) ), apds.slice(1) );
```

We wish to easily write Excel files (.xls). This script allows us to do
this with Autoplot:

```
javaaddpath( '`<http://autoplot.org/jnlp/latest/autoplot.jar>`' )
SC= org.autoplot.ScriptContext; 
```
  
```
tt= org.das2.qds.ops.Ops.labels( {  'experiment_1', 'experiment_2' } );  %  There's a warning about "No constructor 'org.das2.qds.ops.Ops' with matching signature found."  This is new.
ll= org.das2.qds.ops.Ops.labels( { 'ch1','ch2','ch3','ch4','ch5','ch6' } );
ds= org.das2.qds.ops.Ops.rand(2,6);
ds= org.das2.qds.DataSetUtil.asDataSet( ds );
ds= org.das2.qds.ops.Ops.link( tt, ll, ds );
SC.formatDataSet( ds, '/tmp/mydata.xls?sheet=sh1' );
```
  
```
ds= rand(2,6);
ds= org.das2.qds.DataSetUtil.asDataSet( ds );
ds= org.das2.qds.ops.Ops.link( tt, ll, ds );
SC.formatDataSet( ds, '/tmp/mydata.xls?sheet=sh2&append=T' );
```

# Previous Documentation

  - Some older scripts show how to pass data to Autoplot from IDL and
    MATLAB through a pipe:
    [1](http://autoplot.svn.sourceforge.net/viewvc/autoplot/autoplot/trunk/VirboAutoplot/src/external/)
  - <http://autoplot.org/wiki/index.php?title=developer&oldid=3660#IDL.2FMATLAB>

