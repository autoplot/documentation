Using Autoplot in the IDL Environment

Audience: Autoplot users who would like to use the software to read data
into IDL, and to use other Autoplot codes from these environments

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

# Getting Started

First we need to connect the Autoplot code to the environment. In these
examples, "Unix\>" is used to indicate commands entered into a Unix BASH
shell, and "IDL\>" an IDL v7.0 (or newer) session.

You can verify the Java version by calling a Java method:

`IDL> System= obj_new( 'IDLJavaObject$Static$System', 'java.lang.System' )`  
`IDL> print, System.getProperty( 'java.version' )`  
`1.8.0_131`

You will need at least Java version 1.7.0, and 1.8.0\_102 or better is
needed to access CDAWeb and other https sites. You will need at least
IDL 7.0, and soon 8.4 will be required.

## Connecting the Jar File

In either case, you'll need to download the Autoplot "single jar"
release that is available along with each release of the software. For
example, the release at <http://autoplot.org/jnlp/latest/> has a link to
a single jar version here:
<http://autoplot.org/jnlp/latest/autoplot.jar>. We will download it to
/tmp/autoplot.jar or some location appropriate for your workstation.
This 30 megabyte jar file is similar to a .so file from C/Fortran and
contains compiled code and also needed resources. Note this is a full
Autoplot and can be used from the command line, bypassing the mechanism
normally used to launch Autoplot. If this seems large, consider that
this contains code to read NetCDF, OpenDAP, CDF, Excel, and many other
forms of data.

Note this jar file requires Java 7 and will only work with IDL 8.4 and
newer.

Notes:

  - sometimes you'll see this called a jumbojar, which is the name we
    use for our software and all the libraries it needs, combined into
    one jar file.
  - Latest versions of Autoplot require Java 7, and older versions of
    IDL may still use Java 6. IDL 8.4 is okay, 8.1 will not work with
    v2015a\_6 or newer.
  - IDL 8.1 allows obj.method() as well as obj-\>method(), and this form
    is used here.

### Connecting to IDL

For IDL, the jar file must be connected to the IDL process before
starting the session. This must be a fully-qualified path, because it
will work **inconsistently** if it's not. Using bash:

`Unix> wget -N `<http://autoplot.org/jnlp/latest/autoplot.jar>  
`Unix> export CLASSPATH=autoplot.jar`

And start up a new IDL session and we can test to see that the jar file
is connected:

`IDL> apds= OBJ_NEW('IDLjavaObject$APDataSet', 'org.autoplot.idlsupport.APDataSet')`  
`% APDataSet v1.6.2`  
`% Java Version 1.7.0_25`

## First Read of Data

Suppose you have been using the Autoplot URI (data address)
<http://www.autoplot.org/data/swe-np.xls?column=data&depend0=dep0> to
read data into Autoplot. ![Autoplot can be used to read data into IDL
and MATLAB](idlMatlabInterface.png
"Autoplot can be used to read data into IDL and MATLAB")

Here's the code in IDL. Remember, the CLASSPATH variable must be set in
the Unix environment as described above.

`IDL> apds.setDataSetURI, '`<http://www.autoplot.org/data/swe-np.xls?column=data&depend0=dep0>`'`  
`IDL> apds.doGetDataSet`  
`IDL> print, apds.toString()`  
`data: data[dep0=287] (dimensionless)`  
`dep0: dep0[287] (t1970) (DEPEND_0)`  
`IDL>  plot, apds.values()`

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
object. So we say:

`dep0Name= apds.depend(0)   ; This returns the name of the DEPEND_0 property.`  
`x= apds.values( dep0Name )`

or

`x= apds.values( apds.depend(0) )`

Another difference is that the apds is mutable, meaning its state can be
changed, whereas QDataSets are generally immutable. For example, you can
tell the apds what your preferred units are, affecting what is returned
by the values() command.

# DataSet Properties

You can access the dataset properties like so:

`dsp= apds.properties( )`  
`p= dsp.get('NAME')`  
`print, p.toString()    ; unfortunately IDL doesn't quite equate Java strings with IDL strings, so you need "toString()"`  
  
`yp= apds.properties( 'ds_2' )`  
`p= yp.get('LABEL')`  
`print, p.toString()`

or

`ll= apds.property( 'ds_2', 'NAME')`  
`print, ll.toString()`

# The Rest of the Reader Interface

What are the X values? They are in some strange unit that the data
source chooses. In this example it is "t1970", which is the number of
non-leap seconds since 1970-Jan-01T00:00. We can specify what units we
want:

`apds.setPreferredUnits, 'hours since 2007-01-17T00:00' `  
`plot( apds.values('dep0'), apds.values() ) `

Here are some example units strings: seconds since 2010-01-01T00:00,
days since 2010-01-01T00:00, Hz, MHz. Note Autoplot's units are not
fully developed, and conversions are not always possible.

We also can work with fill data:

`apds.setFillValue, -999`

This will convert whatever fill is in the dataset to this value. This
saves the developer the time of reading what the fill, validmin, and
validmax are in the QDataSet.

Last, we can add a filter process string:

`apds.setFilter, '|slice1(0)'`

Presently this must be done before the getDataSet call. Future versions
should allow it at any time.

## Length and Slice to access non-qubes

IDL and Matlab have 3-D arrays, but do not support "ragged" arrays of C
and Java, which is also the structure of QDataSets. For example,
qds\[0,\*,\*\] may have size \[50,20\], but qds\[1,\*,\*\] has size
\[40,30\]. For example, the CASSINI RPWS instrument uses this feature of
C and Java (and QDataSet) to represent data from different modes.
Autoplot uses the name "qube" to refer to datasets which are N-D arrays
like you would see in IDL.

To access these ragged arrays, the "slice" method is called instead of
the values method. This will extract data from one slice of the dataset
(qds\[0,\*,\*\]) at a time. (It is guaranteed that slices are qubes.)
The lengths method returns the size of each qube after slicing. The
following code makes the ragged array into a regular array. It also
utilitizes "rank()" which returns the number of indices in the dataset,
and isQube which checks for ragged or qube, and lengths which returns
all the dimensions.

`apds= OBJ_NEW('IDLjavaObject$APDataSet', 'org.autoplot.idlsupport.APDataSet')`  
`apds.loadDataSet( 'vap+inline:ripplesJoinSpectrogramTimeSeries(10)' )`  
`if apds.rank() eq 3 and not apds.isQube() then begin`  
`  n = apds.length()`  
`  ndim = lonarr(n, 2)`  
`  for i = 0, n-1 do ndim[i,*] = apds.lengths(i)`  
` `  
`  data = dblarr(n, max(ndim[*,0]), max(ndim[*,1]))`  
`  for i = 0, n-1 do begin`  
`    temp = apds.slice(i)`  
`    data[i,0:ndim[i,0]-1,0:ndim[i,1]-1] = temp`  
`  endfor`  
`endif else begin`  
`  data = apds.values()`  
`endelse`  
  
`help, data`

# Access other Autoplot classes

Other classes Autoplot uses can be accessed. For example,

`sc= OBJ_NEW('IDLjavaObject$ScriptContext', 'org.autoplot.ScriptContext')`  
`x= sc.getCompletions( 'vap+cdfj:`<http://autoplot.org/data/somedata.cdf>`?')`

lists all the variables in the CDF file.

#### Accessing Aggregation in IDL

`agg= OBJ_NEW('IDLjavaObject$Agg', 'org.autoplot.aggregator.AggregatingDataSourceFactory' )`  
`fsm= agg.getFileStorageModel('`<http://autoplot.org/data/agg/efi/$Y/po_k0_efi_$Y$m$d_v$v.cdf>`')`  
`ops= OBJ_NEW('IDLJavaObject$Static$Ops', 'org.das2.qds.ops.Ops' )   ; note static is explained below`  
`ff= fsm.getBestNamesFor( ops.datumRange('1999-12-30/2000-01-04') )   ; wait for 2018-07-18 release`  
`print, fsm.getRoot() + ff[0]`

#### Format datasets from IDL

Here's how we can use Autoplot's formatting to export data:

`setenv, 'CLASSPATH=autoplot.jar'`  
  
`sc= OBJ_NEW('IDLjavaObject$ScriptContext', 'org.autoplot.ScriptContext')`  
`ops= OBJ_NEW('IDLjavaObject$Static$Ops', 'org.das2.qds.ops.Ops' )`  
`units= OBJ_NEW('IDLjavaObject$Static$Units', 'org.das2.datum.Units' )`  
  
`tt= ops.dataset( dindgen(100), units.lookupUnits( 'seconds since 1970-01-01T00:00Z' ) )`  
`dd= ops.dataset( randomn(s,100) )`  
`dd.putProperty, 'DEPEND_0', tt`  
  
`sc.formatDataSet, tt, '/tmp/foo.cdf?tt'`  
`sc.formatDataSet, dd, '/tmp/foo.cdf?dd&append=T'`  

The extension is used to control the output format. Note also that error
feedback is poor, see <https://sourceforge.net/p/autoplot/bugs/768/>. We
should consider adding a wrapper for often-used functions to simplify
this as well.

There's an asynchronous version of the loader, so that multiple things
can be loaded at once, and progress feedback is provided. (TODO:
document this.)

## Static methods in IDL

It's a little non-trivial to use static methods in IDL, but it is
possible. Here is an example showing use of the FileSystem and
FileStorageModel objects, note the $Static$ part in the OBJ\_NEW part:

`Unix> wget -N `<http://autoplot.org/jnlp/latest/autoplot.jar>  
`Unix> export CLASSPATH=autoplot.jar`  
  
`IDL> fs= OBJ_NEW( 'IDLJavaObject$Static$FileSystem', 'org.das2.util.filesystem.FileSystem' ) ; provide access to the create command`  
`IDL> afs= fs.create('`<https://emfisis.physics.uiowa.edu/Flight/RBSP-B/L4/>`') ; create a filesystem object`  
`IDL> fsm= OBJ_NEW( 'IDLjavaObject$Static$FileStorageModel', 'org.das2.fsm.FileStorageModel' )`  
`IDL> afsm= fsm.create(afs,'$Y/$m/$d/rbsp-b_WFR-waveform-magnitude_emfisis-L4_$Y$m$d_v$(v,sep).cdf')`  
`IDL> dru= OBJ_NEW( 'IDLjavaObject$DatumRangeUtil', 'org.das2.datum.DatumRangeUtil' )`  
`IDL> dr= dru.parseTimeRange('2014-02')`  
`IDL> ff= afsm.getFilesFor( dr )`  
`IDL> for i=0,n_elements(ff)-1 do print, ff[i].toString()`

And to echo the Java version:

`IDL> System= obj_new( 'IDLJavaObject$Static$System', 'java.lang.System' )`  
`IDL> print, System.getProperty( 'java.version' )`  
`1.8.0_131`

Sometimes we don't want an XWindows dependence caused by login prompt
windows. Set headless property in this case.

`IDL> System= obj_new( 'IDLJavaObject$Static$System', 'java.lang.System' )`  
`IDL> System.setProperty('java.awt.headless','true')`  
`IDL> apds= OBJ_NEW('IDLjavaObject$APDataSet', 'org.autoplot.idlsupport.APDataSet')`  
`IDL> apds.loadDataSet, 'vap+das2Server:`<http://jupiter.physics.uiowa.edu/das/server?dataset=Juno/FGM/MagComponents&start_time=2017-02-01T00:00:00.000Z&end_time=2017-02-04T00:00:00.000Z>`'`

## Other Examples

This github directory shows an example where Autoplot is used to
download files. See ap\_get\_file.pro:

` `<https://github.com/autoplot/dev/tree/master/demos/2021/20210202>

# Problems

Also:

  - The CLASSPATH problem in IDL is nasty, because you might have
    multiple jar files when autoplot and other libraries are needed. I
    assume this can be done.
  - It seems clear that you'd want to be able to use Autoplot to verify
    data, so applot should accept apds as an argument.

New 2017-March:

  - Java 1.8.102 is required to access CDAWeb, which is beyond the
    version included with recent IDLs. Use:
      - idlde -vm /usr/local/jdk1.8.0\_121/bin/ (NO--THE ON-LINE
        DOCUMENTATION IS WRONG AND THIS REFERS TO THE IDL VIRTUAL
        MACHINE)
      - Link the IDL to a new JRE, as described here:
        <http://www.harrisgeospatial.com/Support/HelpArticles/TabId/185/ArtMID/800/ArticleID/13555/Changing-the-Java-version-used-with-the-IDL-8-Workbench.aspx>
        (LINK IS BROKEN\!)
  - CLASSPATH can be set within the IDL session, with "setenv,
    'CLASSPATH=autoplot.jar'"

# See Also

Here is the nightly test which tells all:
<http://jfaden.net/jenkins/job/autoplot-test024/>

IDL command applot sends data to Autoplot for display:
[developer.applot](developer.applot "wikilink")

# Complete IDL Examples

Remember,

`Unix> export CLASSPATH=/tmp/autoplot.jar`

And here's the first IDL program:

`apds= OBJ_NEW('IDLjavaObject$APDataSet', 'org.virbo.idlsupport.APDataSet')`  
`apds.setDataSetURI, '`<http://www.autoplot.org/data/swe-np.xls?column=data&depend0=dep0>`'`  
`apds.doGetDataSet`  
`apds.setPreferredUnits, 'hours since 2007-01-17T00:00' `  
`plot, apds.values( apds.depend(0) ), apds.values()`

Accessing aggregated data

`apds= OBJ_NEW('IDLjavaObject$APDataSet', 'org.virbo.idlsupport.APDataSet')`  
`t= '2011-01-17'`  
`apds.setDataSetURI, '`<http://cdaweb.sci.gsfc.nasa.gov/istp_public/data/ace/swepam/level_2_cdaweb/swe_k0/$Y/ac_k0_swe_$Y$m$d_v$v.cdf?Np&timerange=>`' + t`  
`apds.doGetDataSet`  
`apds.setPreferredUnits, 'hours since '+t `  
`plot, apds.values( apds->depend(0) ), apds.values(), xtitle='hours since '+t`

Using slice to get at irregular data

`apds  = OBJ_NEW('IDLjavaObject$APDataSet', 'org.virbo.idlsupport.APDataSet')`  
`casargs= "-lfdr+ExEw+-mfdr+ExEw+-mfr+13ExEw+-hfr+ABC12EuEvEx+-n+hfr_snd+-n+lp_rswp+-n+bad_data+-n+dpf_zero+-n+mfdr_mfr2+-n+mfr3_hfra+-n+hf1_hfrc+-a+-b+30+-bgday="`  
`tt= "start_time=2010-01-11T11:15:00.000Z&end_time=2010-01-11T21:45:00.000Z"`  
`KEY= '1234567' ; request key from the RPWS group`  
`ds= 'das2_1/cassini/cassiniLrfc'`  
`apds.setDataSetURI, 'vap+das2server:`<http://www-pw.physics.uiowa.edu/das/das2Server?dataset='+ds+'&key='+KEY+'&'+tt+'&'+casargs>` `  
`apds.doGetDataSet`  
`print, apds.toString() `  
`help, apds.slice( 3 )`  
`plot, apds.slice( 3 ), /ylog`

Using Autoplot to get a file from the web

`; Copy and paste these lines to the IDL command prompt.`  
  
`setenv, 'CLASSPATH=autoplot.jar'  ; download from `<http://autoplot.org/latest/autoplot.jar>  
`pm= OBJ_NEW( ) ; like null in Java or None in Jython `  
  
`url= OBJ_NEW( 'IDLJavaObject$URL', 'java.net.URL', '`<https://emfisis.physics.uiowa.edu/events/rbsp-a/misc-support-files/rbspa-half-orbit-periods2.txt>`' )`  
  
`DataSetURI= OBJ_NEW( 'IDLJavaObject$Static$DataSetURI', 'org.autoplot.datasource.DataSetURI' )`  
`ff= DataSetURI.downloadResourceAsTempFile(url,pm)`  
`print, ff.toString()`  
  
`openr, lun, ff.toString(), /get_lun`  
`line = "" `  
  
`WHILE NOT EOF(lun) DO BEGIN & $`  
`  READF, lun, line & $`  
`  print, line`  
`ENDWHILE`

# Previous Documentation

  - Some older scripts show how to pass data to Autoplot from IDL and
    MATLAB through a pipe:
    [1](http://autoplot.svn.sourceforge.net/viewvc/autoplot/autoplot/trunk/VirboAutoplot/src/external/)
  - <http://autoplot.org/wiki/index.php?title=developer&oldid=3660#IDL.2FMATLAB>
