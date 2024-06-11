Using Autoplot in the IDL and MATLAB Environments

Audience: Autoplot users who would like to use the software to read data
into IDL and MATLAB, and to use other Autoplot codes from these
environments

# Note

This document was split into separate versions for IDL and Matlab. The
two documents are very similar, but this was done to avoid confusion.
See [idl](idl "wikilink") and [matlab](matlab "wikilink").

# Introduction

Both IDL and MATLAB make it extremely easy to use Java code in these
environments. Autoplot is able to read data from a variety of input
sources using compact URIs to specify data locations, making it useful
accessing digital data. For example, it's difficult to read data from an
Excel worksheet into IDL, but since Autoplot can read this data, it
becomes just as easy to read data from this source as it is a table of
ASCII data. Further, IDL can read data from CDF files, but its low-level
CDF interface makes Autoplot attractive, because you can access data
with just several lines of code. Last, Autoplot can automatically
retrieve and manage data from remote sites via FTP and HTTP, so this
mechanism can be used in IDL and MATLAB as well.

Autoplot contains a number of codes that are useful, in addition to
reading data. For example, Autoplot is able to write data to a number of
data formats, and this code is useful in IDL as well.

Last, IDL and MATLAB adapt to Java code in such a way that code looks
very similar in both languages. For example, where in IDL you would
have:

`sc= OBJ_NEW('IDLjavaObject$ScriptContext', 'org.virbo.autoplot.ScriptContext')`  
`x= sc->getCompletions( 'vap+cdfj:`<http://autoplot.org/data/somedata.cdf>`?')`

in MATLAB you would have:

`sc= org.virbo.autoplot.ScriptContext`  
`x= sc.getCompletions( 'vap+cdfj:`<http://autoplot.org/data/somedata.cdf>`?')`

For this reason, examples are shown in IDL within this document.

# Getting Started

First we need to connect the Autoplot code to the environment. This is,
not surprisingly, the biggest difference between IDL and MATLAB. In
these examples, "Unix\>" is used to indicate commands entered into a
Unix BASH shell, "MATLAB\>" an MATLAB v7.7 session, and "IDL\>" an IDL
v7.0 session.

## Connecting the Jar File

In either case, you'll need to download the Autoplot "single jar"
release that is available along with each release of the software. For
example, the development release at <http://autoplot.org/jnlp/v2015a_5/>
has a link to a single jar version here:
<http://autoplot.org/jnlp/v2015a_5/autoplot.jar>. For MATLAB, you don't
need to download the file, but to be consistent with IDL, we will
download it to /tmp/autoplot.jar or some location appropriate for your
workstation. This 20 megabyte jar file is similar to a .so file from
C/Fortran and contains compiled code and also needed resources. Note
this is a full Autoplot and can be used from the command line, bypassing
the mechanism normally used to launch Autoplot. If this seems large,
consider that this contains code to read: NetCDF, OpenDAP, CDF, Excel,
and many other forms of data.

I'm using <http://autoplot.org/jnlp/v2015a_5/autoplot.jar> for the demo
here, and also at the latest release is found at
<http://autoplot.org/jnlp/latest/autoplot.jar>.

Note sometimes you'll see this called a jumbojar, which is the name we
use for our software and all the libraries it needs, combined into one
jar file.

### Connecting to MATLAB

MATLAB is able to add the jar after the session is started, with the
command "javaaddpath":

`MATLAB> javaaddpath( '/tmp/autoplot.jar' )`

Note for MATLAB, this can be a URL, like
<http://autoplot.org/jnlp/v2015a_5/autoplot.jar>

Now we can test to see that the jar file is connected:

`MATLAB> apds  = org.virbo.idlsupport.APDataSet;`  
`QDataSetBridge v1.8.01`  
`APDataSet v1.3.2`

### Connecting to IDL

For IDL, the jar file must be connected to the IDL process before
starting the session. This must be a fully-qualified path, because it
will work **inconsistently** if it's not. Using bash:

`Unix> export CLASSPATH=/tmp/autoplot.jar`

And we can test to see that the jar file is connected:

`IDL> apds= OBJ_NEW('IDLjavaObject$APDataSet', 'org.virbo.idlsupport.APDataSet')`  
`% QDataSetBridge v1.7.01`  
`% APDataSet v1.2.3`

## First Read of Data

I'll show a first read of data in both MATLAB and IDL. ![Autoplot can be
used to read data into IDL and MATLAB](idlMatlabInterface.png
"Autoplot can be used to read data into IDL and MATLAB")

### MATLAB

`MATLAB> apds.setDataSetURI( '`<http://www.autoplot.org/data/swe-np.xls?column=data&depend0=dep0>`' )`  
`MATLAB> apds.doGetDataSet`

Note there's a bug where MATLAB is unable to read AbstractPreferences,
and you see an error message associated with this. This message can be
ignored. Note the default autoplot\_data/fscache must always be used.

`MATLAB> apds`  
`data: data[dep0=287] (dimensionless)`  
`dep0: dep0[287] (t1970) (DEPEND_0)`  
`MATLAB> plot( apds.values )`

### IDL

Here's the code in IDL. Remember, the CLASSPATH variable must be set in
the Unix environment as described above.

`IDL> apds->setDataSetURI, '`<http://www.autoplot.org/data/swe-np.xls?column=data&depend0=dep0>`'`  
`IDL> apds->doGetDataSet`  
`IDL> print, apds->toString()`  
`data: data[dep0=287] (dimensionless)`  
`dep0: dep0[287] (t1970) (DEPEND_0)`  
`IDL>  plot, apds->values()`

This shows a first look at getting data.

## QDataSet in this Interface

This interface is meant to provide access to anything that can be
represented within Autoplot and its internal data model,
[QDataSet](QDataSet "wikilink").

QDataSet is meant to be a simple, uniform data interface that is adapted
to many different syntaxes, including Java, Python, C, IDL and MATLAB.
However, it's more of a guide than a specification, and since both IDL
and MATLAB are slow when many commands are executed, we provide access
to data via arrays rather than individual values as in Java. Also, we
provide access to timetags and other independent data through the one
object. This should simplify use in the environments. For example,
instead of:

`apds->property( QDataSet.DEPEND_0 ).values()`

we say:

`dep0Name= apds->depend(0)`  
`x= apds->values( dep0Name )`

or

`x= apds->values( apds->depend(0) )`

Another difference is that the apds is mutable, meaning its state can be
changed, whereas QDataSets are generally immutable. For example, you can
tell the apds what your preferred units are, affecting what is returned
by the values() command.

# DataSet Properties

You can access the dataset properties like so:

`dsp= apds->properties( )`  
`print, ( dsp->get('TITLE') )->toString()    ; unfortunately IDL doesn't quite equate Java strings with IDL strings, so you need "toString()"`  
  
`yp= apds->properties( 'ds_2' )`  
`print, ( yp->get('LABEL') )->toString()`

or

`print, ( apds->property( 'ds_2', 'LABEL') )->toString()`

# The Rest of the Reader Interface

What are the X values? They are in some strange unit that the data
source chooses. In this example it is "t1970", which is the number of
non-leap seconds since 1970-Jan-01T00:00. We can specify what units we
want:

`apds->setPreferredUnits, 'hours since 2007-01-17T00:00' `  
`plot( apds->values('dep0'), apds->values() ) `

(Problem: there's an inconsistency here between ooffice calc and what
I'm getting. It almost looks like the autoplot xls export shifts to the
local time. Use a different data source, like CDF.) Here are some
example units strings: seconds since 2010-01-01T00:00, days since
2010-01-01T00:00, Hz, MHz. Note Autoplot's units are not fully
developed, and conversions are not always possible.

We also can work with fill data:

`apds->setFillValue, -999`

This will convert whatever fill is in the dataset to this value. This
saves the developer the time of reading what the fill, validmin, and
validmax are in the QDataSet.

# Access other Autoplot classes

Other classes Autoplot uses can be accessed. For example,

`sc= OBJ_NEW('IDLjavaObject$ScriptContext', 'org.virbo.autoplot.ScriptContext')`  
`x= sc->getCompletions( 'vap+cdfj:`<http://autoplot.org/data/somedata.cdf>`?')`

lists all the variables in the CDF file.

#### Format datasets from MATLAB/IDL

Here's how we can use Autoplot's formatting to export data:

`dsu= OBJ_NEW('IDLjavaObject$DataSetUtil', 'org.virbo.dataset.DataSetUtil' )`  
`ds= dsu->asDataSet( randomu( s, 200 ) )    ; adapt IDL array to QDataSet. This is not the Autoplot function randomu, but IDL's.`  
`sc= OBJ_NEW('IDLjavaObject$ScriptContext', 'org.virbo.autoplot.ScriptContext' )`  
`sc->formatDataSet, ds, '/tmp/foo.xls'`

The extension is used to control the output format. Note formatting to
CDF is still done via the C-based plugin, not the Java plugin, and
cannot be used. Note also that error feedback is poor, see
<https://sourceforge.net/tracker/?func=detail&aid=3430015&group_id=199733&atid=970682>.
We should consider adding a wrapper for often-used functions to simplify
this as well.

There's an asynchronous version of the loader, so that multiple things
can be loaded at once, and progress feedback is provided. (I need to
remind myself how this is done.)

## Static methods in IDL

It's a little non-trivial to use static methods in IDL, but it is
possible. Here is an example showing use of the FileSystem and
FileStorageModel objects, note the $Static$ part in the OBJ\_NEW part:

`Unix> export CLASSPATH=/tmp/autoplot.jar`  
  
`IDL> fs= OBJ_NEW( 'IDLJavaObject$Static$FileSystem', 'org.das2.util.filesystem.FileSystem' ) ; provide access to the create command`  
`IDL> afs= fs.create('`<http://emfisis.physics.uiowa.edu/Flight/RBSP-B/L4/>`') ; create a filesystem object`  
`IDL> fsm= OBJ_NEW( 'IDLjavaObject$Static$FileStorageModel', 'org.das2.fsm.FileStorageModel' )`  
`IDL> afsm= fsm.create(afs,'$Y/$m/$d/rbsp-b_WFR-waveform-magnitude_emfisis-L4_$Y$m$d_v$(v,sep).cdf')`  
`IDL> dru= OBJ_NEW( 'IDLjavaObject$DatumRangeUtil', 'org.das2.datum.DatumRangeUtil' )`  
`IDL> dr= dru.parseTimeRange('2014-02')`  
`IDL> ff= afsm.getFilesFor( dr )`  
`IDL> for i=0,n_elements(ff)-1 do print, ff[i]->toString()`

# Problems

There are some technical issues with all this.

Also:

  - The CLASSPATH problem in IDL is nasty, because you might have
    multiple jar files when autoplot and other libraries are needed. I
    assume this can be done.
  - It seems clear that you'd want to be able to use Autoplot to verify
    data, so applot should accept apds as an argument.
  - Filters are not readily accessible in IDL and MATLAB, and it would
    nice to show how these could be used.

# See Also

Here is the nightly test which tells all:
<http://jfaden.net:8080/hudson/job/autoplot-test024/>

IDL command applot sends data to Autoplot for display:
[developer.applot](developer.applot "wikilink")

This looks promising for use with native Python, using jpype to bridge
to Autoplot, so that it can be used to read data. See
<https://sourceforge.net/p/autoplot/feature-requests/365/>

# Complete IDL Examples

Remember,

`Unix> export CLASSPATH=/tmp/autoplot.jar`

And here's the first IDL program:

`apds= OBJ_NEW('IDLjavaObject$APDataSet', 'org.virbo.idlsupport.APDataSet')`  
`apds->setDataSetURI, '`<http://www.autoplot.org/data/swe-np.xls?column=data&depend0=dep0>`'`  
`apds->doGetDataSet`  
`apds->setPreferredUnits, 'hours since 2007-01-17T00:00' `  
`plot, apds->values( apds->depend(0) ), apds->values()`

Accessing aggregated data

`apds= OBJ_NEW('IDLjavaObject$APDataSet', 'org.virbo.idlsupport.APDataSet')`  
`t= '2011-01-17'`  
`apds->setDataSetURI, '`<http://cdaweb.gsfc.nasa.gov/istp_public/data/ace/swe/$Y/ac_k0_swe_$Y$m$d_v$v.cdf?Np&timerange=>`' + t`  
`apds->doGetDataSet`  
`apds->setPreferredUnits, 'hours since '+t `  
`plot, apds->values( apds->depend(0) ), apds->values(), xtitle='hours since '+t`

Using slice to get at irregular data

`apds  = OBJ_NEW('IDLjavaObject$APDataSet', 'org.virbo.idlsupport.APDataSet')`  
`casargs= "-lfdr+ExEw+-mfdr+ExEw+-mfr+13ExEw+-hfr+ABC12EuEvEx+-n+hfr_snd+-n+lp_rswp+-n+bad_data+-n+dpf_zero+-n+mfdr_mfr2+-n+mfr3_hfra+-n+hf1_hfrc+-a+-b+30+-bgday="`  
`tt= "start_time=2010-01-11T11:15:00.000Z&end_time=2010-01-11T21:45:00.000Z"`  
`KEY= '1234567' ; request key from the RPWS group`  
`ds= 'das2_1/cassini/cassiniLrfc'`  
`apds->setDataSetURI, 'vap+das2server:`<http://www-pw.physics.uiowa.edu/das/das2Server?dataset='+ds+'&key='+KEY+'&'+tt+'&'+casargs>` `  
`apds->doGetDataSet`  
`print, apds->toString() `  
`help, apds->slice( 3 )`  
`plot, apds->slice( 3 ), /ylog`

# Complete MATLAB Examples

Sarah couldn't write .xls files on her Mac. This script allows her to do
this with Autoplot:

`javaaddpath( '`<http://autoplot.org/jnlp/devel/autoplot.jar>`' )`  
`Ops = org.virbo.dsops.Ops;`  
`Util= org.virbo.dataset.DataSetUtil;`  
`SC= org.virbo.autoplot.ScriptContext; `  
  
`tt= Ops.labels( {  'experiment_1', 'experiment_2' } );`  
`ll= Ops.labels( { 'ch1','ch2','ch3','ch4','ch5','ch6' } );`  
`ds= rand(2,6);`  
`ds= Util.asDataSet( ds );`  
`ds= Ops.link( tt, ll, ds );`  
`SC.formatDataSet( ds, '/tmp/forSarah.xls?sheet=sh1' );`  
  
`ds= rand(2,6);`  
`ds= Util.asDataSet( ds );`  
`ds= Ops.link( tt, ll, ds );`  
`SC.formatDataSet( ds, '/tmp/forSarah.xls?sheet=sh2&append=T' );`

# Previous Documentation

  - Some older scripts show how to pass data to Autoplot from IDL and
    MATLAB through a pipe:
    [1](http://autoplot.svn.sourceforge.net/viewvc/autoplot/autoplot/trunk/VirboAutoplot/src/external/)
  - <http://autoplot.org/wiki/index.php?title=developer&oldid=3660#IDL.2FMATLAB>
