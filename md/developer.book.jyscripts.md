# .jy scripts

Jython is Python written for Java. In the same way that Python can be
used to call C code, Jython can call Java code, and Autoplot provides
routines that can be used in Jython scripts to create new and useful
functionality. For example, suppose we have a plot of one day's worth of
data, formatted the way we like, it is easy to write a script that
creates images for the entire mission:

```
trs= generateTimeRanges( '$Y-$m-$d','2000' )
for tr in trs:
   dom.timeRange= DatumRangeUtil.parseTimeRange(tr)
   writeToPng( '/tmp/%s.png' % tr )
```
These scripts are conventionally named with a .jy extension, and can be
run by entering the location of the .jy script in the address bar. This
allows one user to deliver functionality to another user via a script on
a website the same way data URIs can be used.

Note that these scripts have the same access you do on a system, so a
script can accidentally delete data, and malicious scripts could damage
your system. For this reason, always review scripts before running them,
unless they come from a trusted source.

<http://autoplot.org/cookbook> has a number of example scripts, and more
are found in the Autoplot source:
<https://svn.code.sf.net/p/autoplot/code/autoplot/trunk/Autoplot/src/scripts/>

# commonly used functions

A number of functions are often used in scripts, and this section hopes
to introduce them. A more complete reference is available here:
[developer.scripting](developer.scripting.md "wikilink")

## commonly used functions

<table>
<thead>
<tr class="header">
<th><p>code</p></th>
<th><p>function</p></th>
<th><p>example</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><b>DatumRangeUtil.parseTimeRange(time)</b><br />
time,string indicating time range</p></td>
<td><p>parses a string timerange to the internal form which many functions need.</p></td>
<td><p>tr='2014-Jan'<br />
drtr= DatumRangeUtil.parseTimeRange( tr )</p></td>
</tr>
<tr class="even">
<td><p><b>generateTimeRanges(format,timerange)</b><br />
format,format for output times<br />
timerange,the span to cover</p></td>
<td><p>generates a list of string timeranges that cover an interval.</p></td>
<td><p>trs= generateTimeRanges( '$Y-$m-$d','2000' )</p></td>
</tr>
<tr class="odd">
<td><p><b>writeToPng(file)</b><br />
file, the file name</p></td>
<td><p>export the current canvas out to a png image file.</p></td>
<td><p>writeToPng( '/tmp/foo.png' )</p></td>
</tr>
<tr class="even">
<td><p><b>putProperty(dataset,String,Object)</b><br />
dataset<br />
String,property name<br />
Object,the object depends on property</p></td>
<td><p>set the dataset property. If the dataset is not writable, a copy is returned. If the value can be coerced to the correct type, it will be.</p></td>
<td><p>ds= ripples(40,40)<br />
ds= putProperty( ds, QDataSet.TITLE, 'Fake Data' )<br />
plot(ds)</p></td>
</tr>
<tr class="odd">
<td><p><b>getParam(name,deflt[,label[,constraints]])</b><br />
String,tag<br />
Object,default value<br />
[String,label for the parameter]<br />
constraints is an array of enumerated values.</p></td>
<td><p>get an input parameter for the script. This will create a GUI when shift is held with the execute button, or when the script is run from the address bar.</p></td>
<td><p>name= getParam('sc','A','RBSP Spacecraft',['A','B'])<br />
print(name)</p></td>
</tr>
<tr class="even">
<td><p><b>getDataSet(uri[,mon])</b><br />
file, the filename URI.<br />
[monitor, a progress monitor]</p></td>
<td><p>read in the data for the given URI.</p></td>
<td><p>ds= getDataSet( '<a href="http://autoplot.org/data/autoplot.cdf?Magnitude">http://autoplot.org/data/autoplot.cdf?Magnitude</a>' )<br />
plot( ds )</p></td>
</tr>
<tr class="odd">
<td><p><b>formatDataSet(ds,file)</b><br />
ds, the dataset to format<br />
file, the filename URI.</p></td>
<td><p>format the data to the given filename and implied file format. Options can be provided with optional arguments following a question mark.</p></td>
<td><p>ds= getDataSet( '<a href="http://autoplot.org/data/autoplot.cdf?Magnitude">http://autoplot.org/data/autoplot.cdf?Magnitude</a>' )<br />
formatDataSet( ds, '/tmp/mag.txt?header=rich' )</p></td>
</tr>
<tr class="even">
<td><p><b>datum(o)</b><br />
o, an object which can be converted to a datum (numerical value and unit)</p></td>
<td><p>convert the object to a Datum.</p></td>
<td><p>ds= datum('4Kg')<br />
t=datum('2018-08-07T15:22Z')</p></td>
</tr>
<tr class="odd">
<td><p><b>datumRange(o)</b><br />
o, an object which can be converted to a datum range (two numerical values and unit)</p></td>
<td><p>convert the object to a DatumRange, or an interval in a dimension.</p></td>
<td><p>ds= datumRange('4.2-6.8 Kg')<br />
t=datumRange('2018-08-07')</p></td>
</tr>
<tr class="even">
<td><p><b>dataset(o)</b><br />
o, an object which can be converted to a data set</p></td>
<td><p>convert the object to a dataset</p></td>
<td><p>ds= dataset('4.2 Kg')<br />
ds=dataset([1,2,3,4,5])<br />
ds=dataset([1,2,3,4,5],units='eV')</p></td>
</tr>
</tbody>
</table>

## math operators

Jython provides operator overloading, and the following operators are
available. Since QDataSet carries units around, these operators are
generally aware of fill data and units. The units are presently simple
names, so often units are dropped in operations. For example '5 cm' / '1
s' doesn't result in '5 cm/s' but the unit is dropped and the result is
dimensionless.

<table>
<thead>
<tr class="header">
<th><p>operator</p></th>
<th><p>function</p></th>
<th><p>example</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><b>+,-,/,*</b></p></td>
<td><p>add, subtract, multiply, divide</p></td>
<td><p>ds1= getDataSet( '<a href="http://www.autoplot.org/data/image/Capture_00158.jpg?channel=greyscale">http://www.autoplot.org/data/image/Capture_00158.jpg?channel=greyscale</a>' )<br />
ds2= getDataSet( '<a href="http://www.autoplot.org/data/image/Capture_00159.jpg?channel=greyscale">http://www.autoplot.org/data/image/Capture_00159.jpg?channel=greyscale</a>' )<br />
result= abs( ds2- ds1 )</p></td>
</tr>
<tr class="even">
<td><p><b>**</b></p></td>
<td><p>exponent</p></td>
<td><p>ds= linspace(-5,5,100)<br />
plot(ds**2)</p></td>
</tr>
<tr class="odd">
<td><p><b>-</b></p></td>
<td><p>negation</p></td>
<td><p>ds= linspace(-5,5,100)<br />
ds= -ds<br />
plot(ds)</p></td>
</tr>
</tbody>
</table>

## predefined objects

There are a set of variables that are often useful that are defined any
time a script is started. They are:

<table>
<thead>
<tr class="header">
<th><p>name</p></th>
<th><p>data type</p></th>
<th><p>function</p></th>
<th><p>example</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>monitor</p></td>
<td><p>ProgressMonitor</p></td>
<td><p>shows progress for data loads or script processing.</p></td>
<td><p>ds= getDataSet( '<a href="http://autoplot.org/data/sst.mnmean.nc?sst">http://autoplot.org/data/sst.mnmean.nc?sst</a>', monitor )</p></td>
</tr>
<tr class="even">
<td><p>dom</p></td>
<td><p>Application</p></td>
<td><p>the current state of the application</p></td>
<td><p>plot(rand(20))<br />
dom.plotElements[0].style.color=Color.RED</p></td>
</tr>
<tr class="odd">
<td><p>PWD</p></td>
<td><p>String</p></td>
<td><p>the present working directory, typically the location of the script.<br />
Note this can refer to local directories or http sites.<br />
If the editor is not saved to a file, PWD is not defined.</p></td>
<td><p>print PWD<br />
print URI(PWD).path</p></td>
</tr>
</tbody>
</table>

## QDataSet properties

Here are QDataSet properties that are often used:

<table>
<thead>
<tr class="header">
<th><p>QDataSet property</p></th>
<th><p>data type</p></th>
<th><p>function</p></th>
<th><p>example</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DEPEND_0</p></td>
<td><p>QDataSet</p></td>
<td><p>provide the independent dataset that is indexed by the first dimension</p></td>
<td><p>ds=ripplesSpectrogramTimeSeries(100)<br />
ttag= ds.property( QDataSet.DEPEND_0 )<br />
print extent(ttag)</p></td>
</tr>
<tr class="even">
<td><p>DEPEND_1</p></td>
<td><p>QDataSet</p></td>
<td><p>provide the independent dataset that is indexed by the first dimension</p></td>
<td><p>ds=ripplesSpectrogramTimeSeries(100)<br />
energy= ds.property( QDataSet.DEPEND_1 )<br />
plot(energy)</p></td>
</tr>
<tr class="odd">
<td><p>UNITS</p></td>
<td><p>Units</p></td>
<td><p>provide the units object for the data</p></td>
<td><p>ds=ripplesSpectrogramTimeSeries(100)<br />
ds= putProperty( ds, QDataSet.UNITS, Units.MeV)<br />
plot(ds)</p></td>
</tr>
<tr class="even">
<td><p>TITLE</p></td>
<td><p>String</p></td>
<td><p>one-line description of the data, used for plot titles</p></td>
<td><p>ds=ripplesSpectrogramTimeSeries(100)<br />
ds= putProperty( ds, QDataSet.TITLE, 'Fake Data')<br />
plot(ds)</p></td>
</tr>
<tr class="odd">
<td><p>LABEL</p></td>
<td><p>String</p></td>
<td><p>short description of the data, used for axis labels</p></td>
<td><p>ds=ripplesSpectrogramTimeSeries(100)<br />
ds= putProperty( ds, QDataSet.LABEL, 'Fake Data')<br />
plot(ds)</p></td>
</tr>
</tbody>
</table>

# Jython vs Python

  - differences in the libraries. Many Python libraries are implemented
    in native code, and are not available in Jython. For example, SciPy
    is not available in Jython.
  - Jython binds to any Java object trivially. For example, the Apache
    Commons Math library is bundled in the Autoplot distribution, and
    can be used directly from Autoplot scripts.
  - Jython is Python 2.2, and will soon be Python 2.7, the last version
    before Python 3.0.
  - Autoplot provides a good editor for Jython, for example using Java
    introspection to provide completions.

# comparison to SciPy

Both SciPy and Autoplot's scripting were developed with a common goal:
to provide a familiar environment where scientists familiar with IDL and
Matlab can develop code using Python. Because of this, two environments
have similar code. In one case study, a SciPy code several hundred lines
long was ported to Autoplot within minutes.

The differences come from how data is modeled. SciPy and IDL use arrays
to model data, whereas Autoplot uses QDataSet. Because of this, Autoplot
can perform similar functions that are more abstract and typically
require shorter and simpler code.

(This section should have a side-by-side comparison between scripts in
the environments...)

# QDataSet

Instead of representing data in arrays, Autoplot's scripting uses
QDataSet to represent data. QDataSet is an interface to the data, and
different implementations are used to provide efficiency. For example,
in IDL when you say ds\[\*,10\] to look at a slice of ds, a new array is
created and the data is copied. In Autoplot a new dataset is created
that is backed by the same data internally, and the data is never
copied.

QDataSets have metadata which make them more abstract, and make
interfaces simplier. For example, in IDL to plot YY which is a function
of XX, you would say plot, XX, YY. With QDataSet you would already have
the association of YY\[XX\] and you can just say plot(YY).

# script and console tabs

Autoplot provides an editor and output console to assist in using
scripts.

The console tab has an "AP\>" prompt that allows commands be entered
interactively. For example,

```
AP> plot('`<http://autoplot.org/data/autoplot.cdf?Magnitude>`')
AP> ds= dom.dataSourceFilters[0].controller.dataSet   # get the data read in
AP> print max(ds)
```
Note that the feature "Server" provides a similar interface, but via
telnet into a port.

The script editor is a simple editor that provides syntax highliting and
completions. For example, enter QDataSet.<TAB> and see that completions
like "QDataSet.DEPEND\_0" are shown.

![jythonScriptHoverLookup.jpg](jythonScriptHoverLookup.jpg
"jythonScriptHoverLookup.jpg")

There is a selection for the script context, and when the context is
"Data Source" (for .jyds scripts) commands that control the application
are not available. When the context is "Application" all commands are
available. Note when a script is run here and there is an error, a red
squiggle is drawn under (or near) the failure and the Python session is
left open. With this you can inspect the current value of symbols by
highliting the symbol and hovering over the highlite until the tooltip
containing the value appears.

