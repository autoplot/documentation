Purpose: We need a document describing commands available when
scripting. This will cover commands available when no imports are used.

Audience: Scientists and software people wanting to use Autoplot for
scripting.

Note: Some of the non-technical aspects of this page are being migrated
to [scripting](scripting.md "wikilink").

See also [scripting](scripting.md "wikilink"),
<http://autoplot.org/data/jyds>, and <http://autoplot.org/data/tools/>.
See also <https://github.com/autoplot/dev>, where many working scripts
have been developed.

Here's the Javadoc for Autoplot codes:
<http://www-pw.physics.uiowa.edu/~jbf/autoplot/javadoc2018/>

More scripts in the SVN repository:
[1](https://autoplot.svn.sourceforge.net/svnroot/autoplot/autoplot/trunk/Autoplot/src/scripts/)
(All scripts before and including areaSelect.py have been verified to
work with current DOM).

# Introduction to Scripting

Autoplot uses the popular language Python (actually Jython, which is
Java-based) to provide scripting for various applications. For example,
a script can load the data from two data sources and combine them to
make a new dataset. Scripts can also be used to run Autoplot
automatically, for example, to create a series of images called a
pngwalk. Autoplot creates the scripting environment where the user's
commands are executed, and adds useful commands to the environment.
Also, Autoplot's <em>data model</em>, or data representation, is adapted
so that arithmetic operators can be used directly on the data as if they
were number arrays in IDL or Matlab. (But unlike IDL and Matlab, they
carry with them descriptive metadata and physical units.)

For example, consider this script:

``` python
ds1= getDataSet( 'http://autoplot.org/data/image/Capture_00158.jpg?channel=greyscale' )
ds2= getDataSet( 'http://autoplot.org/data/image/Capture_00159.jpg?channel=greyscale' )
result= abs( ds2- ds1 )
```
`
```

It should be fairly clear what the script does: load in two grayscale
views of images, and then assign the absolute difference to the variable
result. This variable could then be plotted, for example, or we might
look for the greatest difference.

Scripting is used in two contexts: the Data Source Context and the
Application Context. In the "Data Source" context, the output of the
script is expected to be named `result` or `data`, and this script
variable is plotted in the canvas tab. In the "Application" context,
Jython commands may be used to manipulate the content of the canvas. The
command line argument "--script" allows scripts to be run in the
application context, so that new applications can be created.

## Script Editor

Autoplot provides a editor GUI for working with scripts. Selecting
Options-\>Enable Feature-\>Script Panel will reveal a tab named "script"
where scripts may be entered and executed. The editor provides simple
completions for this environment. To see completions, enter TAB or
ctrl-space. (Note TAB can use reset to the TAB character whitespace with
a preference.)

Note the completions use a trick to work, and that is to refactor the
script to an equivalent script which can be executed immediately. This
works by reducing the script to just imports and constructor calls, and
to a number of routines which are known to be quick. Of course this
doesn't always work, but provides pretty good results. However, because
of this, some parts of the code can not support completions, like
callbacks from Java code (def boxSelected). It's also possible that a
constructor call is very slow, which would hang completions, but this
assumption has been effective. Last, there may be some side effects that
occur as well, like GUIs created. The completions are getting more
attention than before as many more people are using the editor, and this
code is maturing. ![ScriptEditor.jpg](ScriptEditor.jpg
"ScriptEditor.jpg")

## Data Source Context

Here scripts can load in data and return a new dataset (or datasets).
This is the "data source context" and these are files that can be used
as if they were datasets. If the above script were saved in the file
"<http://www.autoplot.org/data/imageDiff.jyds>," then
<http://www.autoplot.org/data/imageDiff.jyds?result> would refer to this
dataset. This allows scientists to publish operations done to data as
well as data itself. Note these scripts are unaware of the Autoplot
application, they can load and operate on data, but they cannot plot it.
Commands available in this context are described below under the section
"Ops"

Script examples:
[2](https://autoplot.svn.sourceforge.net/svnroot/autoplot/autoplot/trunk/JythonDataSource/src/)
and [cookbook\#Scripting](cookbook.md#scripting "wikilink").

## Application Context

These scripts access the application itself. Take for example the
following application:

```
plot( 'vap+cdaweb:ds=AC_H2_MFI&id=Magnitude&timerange=2010-01-01' )
trs= generateTimeRanges( '$Y-$m-$d', '2010-January' )
for tr in trs:
   dom.timeRange= DatumRangeUtil.parseTimeRange(tr)
   writeToPng( '/tmp/%s.png' % tr )
```

This script would run the application through each day of the month
January 2010, making images of each day. All commands are available in
this context.

Examples are available at
[3](https://autoplot.svn.sourceforge.net/svnroot/autoplot/autoplot/trunk/Autoplot/src/scripts/)
and [cookbook\#Scripting](cookbook.md#scripting "wikilink"). [This
javadoc](http://apps-pw.physics.uiowa.edu/hudson/job/autoplot-javadoc2017/lastSuccessfulBuild/artifact/doc/org/autoplot/ScriptContext.html)
describes the commands available in this Jython Application Context.

## Building Scripts

### Use of Progress Monitor

All scripts have a progress monitor that can be used to provide feedback
to users. This is the variable 'monitor' and is used like so:

```
import java.lang.Thread
monitor.setTaskSize(200)                     # the number of steps (arbitary units)
monitor.started()                            # the task is started.  
```
  
```
for i in xrange(200):
   if ( monitor.isCancelled() ): break       # if not called, the cancel button will be insensitive
   monitor.setProgressMessage('at %d' % i)   # this describes actions done to perform the task.  
   monitor.setTaskProgress(i)
   java.lang.Thread.sleep(100);
```
  
```
monitor.finished()     # indicate the task is complete
```

A well-written script will use the monitor to effectively convey
information to the user. Imagine the scientist is the CEO of a company,
and the script is the Manager of a process. The process is implemented
by a Worker. All three parties use the progress monitor. The Worker
calls setProgressMessage and setTaskProgress to convey the state of the
task. The Worker checks isCancelled to see if they can abort the
process. The Manager calls setLabel to convey the overall goal of the
progress. Typically Autoplot will play the role of the Manager, setting
the label "loading data" or "executing script", but it is acceptable for
the script to take on this role as well, since it can be more
descriptive.

### Getting Input

```
s= getParam( 's', 'deflt', 'label to describe' )   # gets a string parameter, with default value "deflt"
f= getParam( 'f', 2.34, 'label to describe' )      # gets a float parameter, with default value 2.34
i= getParam( 'i', 100, 'array size' )              # gets an integer parameter.  Be careful--user input of a real is truncated, so 100 is quite different than
f= getParam( 'f', 100.0, 'volume' )                # gets a float parameter. 
e= getParam( 'e', 'RBSPA', 'spacecraft', [ 'RBSPA', 'RBSPB' ] )   # enumeration with the values given
b= getParam( 'v', 'F', 'apply correction', [ 'T', 'F' ] )         # booleans are just enumerations with the values 'T' and 'F'
```

![jydsEditor2.jyds.png](jydsEditor2.jyds.png "jydsEditor2.jyds.png")

Autoplot will look for this in scripts and automatically add to GUI. The
type is determined by the default value. Types are shown above, and
there are also "Datums" which are a physical quantity (like 5Hz),
"DatumRanges" which span a range from min datum to max datum, often used
for time ranges, "URIs" which locate data, and "URLs" which locate web
resources. Note files are not a type, and URLs can be used for this
purpose with the "file:" prefix.

This is mostly used for .jyds scripts that create new datasets, but all
script types can use this command. The jyds plugin creates a GUI by
simplifying the script to just getParam calls and trivial commands, so
please let us know if this is not working for you.

Enumerations are supported as well, where a list of possible values is
enumerated. For example:

```
sensor= getParam( 'sensor', 'left', 'sensor antenna', ['left','right'] )
```

will get the parameter sensor, which can be either left or right (with
left as the default). When a GUI is created, a droplist of possible
values is used instead of a text entry field.

Last, booleans are allowed, and a checkbox is used when a GUI is
produced:

```
correct= getParam( 'correct', 'T', 'perform correction on the data', [ 'T', 'F' ] )
```

Note you cannot use the result as a boolean in the Jython code. You must
compare it to 'T'.

Application-context scripts can use get param as well. When the execute
button is pressed the default values are used, but when shift-Execute is
pressed a dialog for controlling the parameters is shown. Scripts can be
run from the command line as well, and would look like:

```
java -cp autoplot.jar org.autoplot.JythonMain /tmp/myscript.jy sensor=right correct=T
```

or if the Autoplot GUI is needed:

```
java -cp autoplot.jar org.autoplot.AutoplotUI --script /tmp/myscript.jy sensor=right correct=T
```

Positional arguments are read in as arg\_1, arg\_2, etc.

#### Creating a GUI from a script

Autoplot works by making a simplified version of the script, and then
running it with getParam replaced with a function that tallies the
calls. This trick causes confusion when sometimes functions can be used
and sometimes not. These functions can be used:

```
 "range", "xrange", "getParam", "lower", "upper"
```

so

```
 x= getParam( 'sc', 1, 'spacecraft ID", range(40) )
```

works, but this won't:

```
 x= getParam( 'sc', 1, 'spacecraft ID", findgen(40) )
```

#### Finer control of Parameters

Finer controls can be used when the fourth argument to getParam is a
dictionary. For example,

```
x= getParam( 'sc', 1, 'spacecraft ID', { 'labels':['rbsp-a','rbsp-b'], 'values':[1,2] } )
```

allows additional labels to be added to the selections. You can also
have examples, using:

```
x= getParam( 'name', 'Jim', 'Operator Name', { 'examples':['Jim','Terry','Sally'] } )
```

Other constaints will be coming, like minimum and maximum values for
numeric data.

### Handling Exceptions

Often a process will typically execute, but we know exceptional cases
may occur and we want to invoke special code to handle them. For
example, we may open a sequence of files, and if one is misformatted, we
want to log it to a file and carry on with processing other files.

In Jython we use try/exception blocks, something like:

```
try: 
  plot( uri )
  writeToPng( '/tmp/pngs/%s.png' % uri )
except Exception, ex:
  ERROR.write( '# unable to plot ' + uri + ' because of ' + str(ex) )
```

Note most of the functions called are actually Java procedures and throw
Java exceptions. Unfortunately, the Jython catch needs a second catch
for Java exceptions, and a second `except` block is needed:

```
try: 
  plot( uri )
  writeToPng( '/tmp/pngs/%s.png' % uri )
except Exception, ex:
  ERROR.write( '# unable to plot ' + uri + ' because of ' + str(ex) )
except java.lang.Exception, ex:
  ERROR.write( '# unable to plot ' + uri + ' because of ' + str(ex) )
```

Or, if you don't need to inspect the exception:

```
try: 
  plot( uri )
  writeToPng( '/tmp/pngs/%s.png' % uri )
except:
  ERROR.write( '# unable to plot ' + uri )
```

#### Throwing (or Raising) Exceptions

Sometimes we want our process to stop and let the user know that
something went wrong, so we throw an exception. This is done like so:

```
if ( ds.length()==0 ):
  raise Exception("Dataset is empty")
```

### Adding to the Tools menu

Application-context scripts can be added to the Autoplot GUI by adding
them to HOME/autoplot\_data/putting them in the
HOME/autoplot\_data/bookmarks/tools.xml, which can be added graphically
with Tools-\>"Manage and Browse Tools", and when a tool is run for the
first time a dialog showing the script and its control panel also has a
checkbox for adding the script to the Tools menu.

&lt;http://autoplot.org/data/tools/&gt;`&nbsp;shows&nbsp;some&nbsp;example&nbsp;scripts.`

### PWD is often defined

PWD is allowed in scripts to refer to folder containing the script. This
is a string containing the URI location of the script, be it on a local
hard drive or a remote web folder. This will always end with a slash,
and will often start with "<http://>" or "<file://>". The script editor
tab allows a script to be composed without saving it to a file. In this
case PWD is not defined.

# Commands

These are commands that are available to scripts in Autoplot. Autoplot's
scripting environment is Jython (Python in Java) with a set of codes
that are automatically imported to keep scripts simple.

The Java types that each command takes are indicated, because it's
easier to produce this document and if these commands are used in Java
instead if Jython, the types must be followed. Jython is able to make
some conversions to correctly combine data.

# Application Context Commands

These are extra commands that are added when running in the script
context that control the Autoplot application itsself, such as
writeToPng. These commands are not available in JythonDataSources (Data
Source Context), which load data to make a new data set.

## getViewWindow

```
public static java.awt.Window getViewWindow()
```

return the Window for the application, to be used for dialogs. See
createGui(), which creates the view.

## setCanvasSize

```
public static void setCanvasSize(int width,
                                int height)
```

set the size of the canvas. This is only used when the GUI is not used,
and in headless mode, otherwise the GUI controls the size of the canvas.

Parameters:

  - width - the width of the canvas
  - height - the height of the canvas

<div id="plot">

</div>

## plot

A number of plot commands are available.

### plot the URI

```
public static void plot(java.lang.String surl)
```

bring up the autoplot with the specified URL.

Parameters:

  - surl - a URI or vap file

### plot one URI against another

```
public static void plot(java.lang.String surl1,
                       java.lang.String surl2)
```

plot one URI against another. No synchronization is done, so beware.
Introduced for testing non-time axis TSBs.

Parameters:

  - surl1 - the independent variable dataset (generally used for X)
  - surl2 - the dependent variable dataset (generally used for Y, but
    can be rank 2).

### plot the URI at position

```
public static void plot(int chNum,
                       java.lang.String surl)
```

bring up the autoplot with the specified URL. This may be a little
confusing, because it replaces the datasource with the given number,
which would typically correspond to the position on the page.

Parameters:

  - chNum - the data source number to reset the URI.
  - surl - a URI to use

### plot the URI at position with this label

```
public static void plot(int chNum,
                       java.lang.String label,
                       java.lang.String surl)
```

bring up the autoplot with the specified URL.

Parameters:

  - chNum - the data source number to reset the URI.
  - label - for the plot.
  - surl - a URI to use

### plot this dataset

```
public static void plot(org.virbo.dataset.QDataSet ds)
```

plot the dataset in the first dataSource node.

Parameters:

  - ds - QDataSet to plot

### plot one dataset against another

```
public static void plot(org.virbo.dataset.QDataSet x,
                       org.virbo.dataset.QDataSet y)
```

plot the dataset in the first dataSource node.

Parameters:

  - x - QDataSet for the independent parameter
  - y - QDataSet for the dependent parameter

### plot one dataset Z against X and Y

```
public static void plot(org.virbo.dataset.QDataSet x,
                       org.virbo.dataset.QDataSet y,
                       org.virbo.dataset.QDataSet z)
```

plot the dataset in the first dataSource node.

Parameters:

  - x - QDataSet for the independent parameter for the X values
  - y - QDataSet for the independent parameter for the Y values
  - z - Rank 1 or Rank 2 QDataSet for the dependent parameter

### plot one dataset in this position

```
public static void plot(int chNum,
                       org.virbo.dataset.QDataSet ds)
```

plot the dataset in the specified dataSource node.

Parameters:

  - ds - dataset to plot.

### plot one dataset against another in this position

```
public static void plot(int chNum,
                       org.virbo.dataset.QDataSet x,
                       org.virbo.dataset.QDataSet y)
```

plot the dataset in the specified dataSource node.

Parameters:

  - x - QDataSet for the independent parameter for the X values
  - y - QDataSet for the independent parameter for the Y values

### plot one dataset Z against X and Y in this position

public static void plot(int chNum,

```
                       org.virbo.dataset.QDataSet x,
                       org.virbo.dataset.QDataSet y,
                       org.virbo.dataset.QDataSet z)
```

plot the dataset in the specified dataSource node.

Parameters:

  - x - QDataSet for the independent parameter for the X values
  - y - QDataSet for the independent parameter for the Y values
  - z - Rank 1 or Rank 2 QDataSet for the dependent parameter

### plot this URI at this position

```
public static void plot(int chNum,
                       java.lang.String label,
                       org.virbo.dataset.QDataSet ds)
```

bring up the autoplot with the dataset

Parameters:

  - chNum - the data source number to reset the URI.
  - label - for the plot.
  - ds - the dataset to use.

### plot X vs Y with this label at this position

```
public static void plot(int chNum,
                       java.lang.String label,
                       org.virbo.dataset.QDataSet x,
                       org.virbo.dataset.QDataSet y)
```

plot the dataset in the specified dataSource node.

Parameters:

  - x - QDataSet for the independent parameter for the X values
  - y - QDataSet for the independent parameter for the Y values

### plot one dataset Z against X and Y in this position with this label

```
public static void plot(int chNum,
                       java.lang.String label,
                       org.virbo.dataset.QDataSet x,
                       org.virbo.dataset.QDataSet y,
                       org.virbo.dataset.QDataSet z)
```

plot the dataset in the specified dataSource node.

Parameters:

  - label - the label for the dependent parameter
  - x - QDataSet for the independent parameter for the X values
  - y - QDataSet for the independent parameter for the Y values
  - z - Rank 1 or Rank 2 QDataSet for the dependent parameter

## plotx

The plotx command is now just "plot".

The plotx command is an experimental plot command that is written for
use only in the Jython environment.

```
xx= linspace( 0, 4*PI, 100 )
yy= sin( xx )
plotx( xx, yy, title='sin' )
```

Its control tries to match IDL's plot command, with named parameters
like:

```
xtitle ytitle ztitle  ='Label' the label for each axis
xlog ylog zlog        =True for log plots
yrange                =[-10,10] 
title                 ='Title' title for the plot
renderType            ='scatter', 'series', 'nnSpectrogram', etc.
symsize               =5.0 symbol size in pixels
linewidth             =3.0 line thickness in pixels
color                 ='0xFF0000' or 'RED'
symbol                ='STAR', 'CROSS', 'TRIANGLES', 'EXES', 'DIAMONDS'
```

## dataset

The dataset command takes its argument and converts it to a QDataSet,
the internal model. For example, dataset(\[1,2,3\],units='s') takes the
Jython array and makes a rank 1 QDataSet with three elements, with
metadata indicating its units are seconds. Other metadata can be
specified:

```
title       = title if plotted
label       = left-side label, or spectrogram label if plotted
name        = internal identifier, and Jython-safe name for the data
units       = units for the data.
validMin    = extent for valid data
validMax    = extent for valid data
typicalMin  = suggestions for axis range
typicalMax  = suggestions for axis range
scaleType   = 'log' or 'linear' suggestion for axis type
```

Note these are converted to the proper type for the property. For
example, when the string 's' is used for the units, internally it is
converted to the canonical representation of the unit (Units.seconds)

## setStatus

```
public static void setStatus(java.lang.String message)
```

set the autoplot status bar string. Use the prefixes "busy:", "warning:"
and "error:" to set icons.

Parameters:

  - message - message to display, possibly with "busy:" "warning:" or
    "error:" prefix.

## addTab

```
public static void addTab(java.lang.String label,
                         javax.swing.JComponent c)
```

add a tab to the running application. A new tab will be added with the
label.

Parameters:

  - label - the label for the component.
  - c - the component to add.

## setRenderStyle

```
public static void setRenderStyle(java.lang.String name)
```

  - Set the style used to render the data using a string identifier:
    spectrogram, series, scatter, histogram, fill\_to\_zero, digital

Parameters:

  - name - string name of the plot style.

## peekAt

```
public static void peekAt(java.lang.Object o)
                  throws java.io.IOException
```

This is intended to be used with a debugger. The developer should put a
breakpoint at the out.write statement, and then call peekAt from the
script.

Parameters:

  - o - any object we want to look at.

## writeToPng

```
public static void writeToPng(java.lang.String filename)
```

write out the current canvas to a png file. TODO: bug 3113441: this has
issues with the size. It's coded to get the size from the DOM, but if it
is fitted and has a container it must get size from the container. Use
writeToPng( filename, width, height ) instead for now. See
writeToPdf(String filename), which appears to have a fix for this that
would affect how this is resolved.

Parameters:

  - filename - The name of a local file

## writeToPng

```
public static void writeToPng(java.lang.String filename,
                             int width,
                             int height)
```

write out the current canvas to a png file. TODO: bug 3113441: this has
issues with the size. It's coded to get the size from the DOM, but if it
is fitted and has a container it must get size from the container. Use
writeToPng( filename, width, height ) instead for now. See
writeToPdf(String filename), which appears to have a fix for this that
would affect how this is resolved.

Parameters:

  - filename - The name of a local file
  - width - the width in pixels of the png
  - height - the height in pixels of the png

## writeToPng

```
public static void writeToPng(java.io.OutputStream out)
```

write out the current canvas to stdout. This is introduced to support
servers. TODO: this has issues with the size. See writeToPng(filename).

Parameters:

  - OutputStream - out

## writeToPdf

```
public static void writeToPdf(java.lang.String filename)
```

write out the current canvas to a pdf file. TODO: this has issues with
the size. See writeToPng(filename). It looks like this might be handled
here

Parameters:

  - filename - the local file to write the file.

## writeToPdf

```
public static void writeToPdf(java.io.OutputStream out)
```

write out the current canvas to a pdf to the output stream. This is to
support servers. TODO: this has issues with the size. See
writeToPng(filename). It looks like this might be handled here

Parameters:

  - out - the OutputStream

## writeToBufferedImage

```
public static java.awt.image.BufferedImage writeToBufferedImage(Application applicationIn)
```

creates a BufferedImage from the provided DOM. This blocks until the
image is ready. TODO: this has issues with the size. See
writeToPng(filename). It looks like this might be handled here

Parameters:

  - applicationIn -

## getTimeRangesFor

```
public static java.lang.String[] getTimeRangesFor(java.lang.String surl,
                                                 java.lang.String timeRange,
                                                 java.lang.String format)
```

return an array of URLs that match the spec for the time range provided.
For example,

```
uri= '`<http://cdaweb.gsfc.nasa.gov/istp_public/data/polar/hyd_h0/$Y/po_h0_hyd_$Y$m$d_v01.cdf?ELECTRON_DIFFERENTIAL_ENERGY_FLUX>`'
xx= getTimeRangesFor( uri, '2000-jan', '$Y-$d-$m' )
for x in xx:
   print x
        
```

This is also available in the Data Source Context (.jyds files).

Parameters:

  - surl - an Autoplot uri with an aggregation specifier.
  - timeRange - a string that is parsed to a time range, such as "2001"
  - format - format for the result, such as "%Y-%m-%d"

Returns:

  - a list of URLs without the aggregation specifier.

## generateTimeRanges

```
public static java.lang.String[] generateTimeRanges(java.lang.String spec,
                                                   java.lang.String srange)
                                            throws java.text.ParseException
```

Given a spec to format timeranges and a range to contain each timerange,
produce a list of all timeranges covering the range formatted with the
spec. For example, generateTimeRanges( "%Y-%m-%d", "Jun 2009" ) would
result in 2009-06-01, 2009-06-02, ..., 2009-06-30.

This is also available in the Data Source Context (.jyds files).

Parameters:

  - spec - such as "%Y-%m". Note specs like "%Y%m" will not be parsable.
  - srange - range limiting the list, such as "2009"

Returns:

  - a string array of formatted time ranges, such as \[ "2009-01",
    "2009-02", ..., "2009-12" \]

## setTitle

```
public static void setTitle(java.lang.String title)
```

set the title of the focus plot.

Parameters:

  - title -

## createGui

```
public static void createGui()
```

create a model with a GUI presentation layer. If the GUI is already
created, then this does nothing.

## getApplicationModel

```
public static ApplicationModel getApplicationModel()
```

returns the internal application model (the object that does all the
business). This provides access to the internal model for power users.
Note the applicationModel provides limited access, and the DOM now
provides full access to the application.

Returns:

  - ApplicationModel object

## isModelInitialized

```
public static boolean isModelInitialized()
```

provide way to see if the model is already initialized (e.g. for clone
application)

Returns:

  - true if the model is already initialized.

## bind

```
public static void bind(java.lang.Object src,
                       java.lang.String srcProp,
                       java.lang.Object dst,
                       java.lang.String dstProp)
```

binds two bean properties together. Bindings are bidirectional, but the
initial copy is from src to dst. In MVC terms, src should be the model
and dst should be a view. The properties must fire property change
events for the binding mechanism to work. Example:

```
bind( dom.plots[0], "title", dom.plots[0].getYaxis(), "label" )
dom.plots[0].title= 'My Data'
```

Parameters:

  - src - java bean such as model.getPlotDefaults()
  - srcProp - a property name such as "title"
  - dst - java bean such as model.getPlotDefaults().getXAxis()
  - dstProp - a property name such as "label"

## dumpToQStream

```
public static void dumpToQStream(org.virbo.dataset.QDataSet ds,
                                java.io.OutputStream out,
                                boolean ascii)
```

serializes the dataset to a QStream, a self-documenting, streaming
format useful for moving datasets.

```
ds= getDataSet('`<http://autoplot.org/data/somedata.cdf?BGSEc>`')
from java.lang import System
dumpToQStream( ds, System.out, True )
        
```

Parameters:

  - ds - The dataset to stream. Note all schemes should be streamable,
    but some bugs exist that may prevent this.
  - output - stream, such as "System.out"
  - ascii - use ascii transfer types, otherwise binary are used.

## dumpToDas2Stream

```
public static void dumpToDas2Stream(org.virbo.dataset.QDataSet ds,
                                   boolean ascii)
```

serializes the dataset to a das2stream, a well-documented, open,
streaming data format. (that's a joke.) Das2Streams are the legacy
stream format used by the Plasma Wave Groups's server, and can serialize
a limited set of QDataSets. QStreams were introduced to allow streaming
of any QDataSet, see dumpToQStream. Currently, to keep the channel open,
the stream is created in a buffer and then the buffer is sent. TODO:
write a stream-producing code that doesn't close the output stream.
(TODO: does it still do this?)

Parameters:

  - ds - QDataSet
  - ascii - use ascii transfer types, otherwise binary are used.

## dumpToDas2Stream

```
public static void dumpToDas2Stream(org.virbo.dataset.QDataSet ds,
                                   java.lang.String file,
                                   boolean ascii)
```

serializes the dataset to a das2stream, a well-documented, open,
streaming data format. (that's a joke.) Currently, to keep the channel
open, the stream is created in a buffer and then the buffer is sent.
TODO: write a stream-producing code that doesn't close the output
stream.

Parameters:

  - ds -
  - file - the file target for the stream.
  - ascii - use ascii transfer types.

## formatDataSet

```
public static void formatDataSet(org.virbo.dataset.QDataSet ds,
                                java.lang.String file)
                         throws java.lang.Exception
```

Export the data into a format implied by the filename extension. See the
export data dialog for additional parameters available for formatting.
For example:

```
ds= getDataSet('`<http://autoplot.org/data/somedata.cdf?BGSEc>`')
formatDataSet( ds, 'vap+dat:`<file:/home/jbf/temp/foo.dat?tformat=minutes&format=6.2f>`')
        
```

Parameters:

  - ds - QDataSet
  - file - local file name that is the target, and optionally contains
    format-specific parameters, described below.

### parameters

These parameters are format-specific, and are appended with file?params.
For example,
formatDataSet(ripplesTimeSeries(20),'/tmp/data.dat?header=rich')

#### ascii

  - header=rich format with rich ascii headers
  - tformat=Millisecond the resolution of timetags
  - format=%5.2f for format specifier for non-timetags.

#### CDF

  - type=float use floats to store data
  - timeType=epoch use legacy Epoch data, instead of TT2000.
  - append=T open and insert the data, so that multiple parameters live
    in one file, instead of writing a new file.

#### qds, d2s

  - type=binary use binary instead of ascii transfer types.

#### HDF5

  - type=float use floats to store data
  - \!\!TODO: does ISTP work?

#### wav

  - scale=T scale the data to use the dynamic range

#### bin

  - type=float use floats to store data
  - byteOrder=big use big-endian floats instead of little-endian.

## getDocumentModel

```
public static Application getDocumentModel()
```

get the document model (DOM). This may initialize the model, in which
case defaults like the cache directory are set.

## save

```
public static void save(java.lang.String filename)
```

save the current state as a .vap file

Parameters:

  - filename - local file where the vap should be saved.

## getCompletions

```
public static java.lang.String[] getCompletions(java.lang.String file)
```

return a list of completions. I was talking to Tom N. who was looking
for this to get a list of CDF variables, and realized this would be
useful in the IDL context as well as python scripts. This will perform
the completion for where the carot is at the end of the string.

This is also available in the Data Source Context (.jyds files).

Parameters:

  - file, - for example "<http://autoplot.org/data/somedata.cdf>?"

Returns:

  - list of completions, containing the entire URI.

## load

```
public static void load(java.lang.String filename)
```

load the .vap file. This is implemented by calling plot on the URI.

Parameters:

  - filename - the vap file to load

## reset

```
public static void reset()
```

reset the application to its initial state.

## setLayout

```
public static void setLayout( nrows ) 
public static void setLayout( nrows, ncolumns ) 
```

reset to a multi-plot layout.

## fixLayout

```
public static void fixLayout(  ) 
```

remove empty gaps in the plot.

## close

```
protected static void close()
```

called when the application closes so if we reopen it will be in a good
state.

# Ops

These are QDataSet operators imported from org.virbo.dsops.Ops.
Parenthesis enclosing an operator indicate the operator is overloaded to
this function, so for example a.add(b) is usually replaced with a+b.

Note that there's a bit of "coercion" supported to make two dataset
arguments have the same geometry. For example, you can add two
10-element rank 1 datasets, but you can also add a 10-element rank 1
dataset to a rank 0 dataset. In other words, \[1,2,3,4\]+\[1,1,1,1\] is
equivalent to \[1,2,3,4\] + 1 because the 1 is coerced to \[1,1,1,1\].
Also Python arrays and numbers are automatically converted to QDataSets.
Note a dataset must sometimes be explicitly made, and to force python to
coerce to it, use the dataset() command to convert it:

```
print [1,2,3,4]
print dataset([1,2,3,4])  
print total(dataset([1,2,3,4]))
print total(2 + dataset([1,2,3,4]) )
#(This is in the autoplot2011 version only.)
```

## abs

```
public static QDataSet abs(QDataSet ds1)
```

element-wise abs. For vectors, this returns the length of each element.
Note jython conflict needs to be resolved.

Parameters:

  - ds1 -

Returns:

## accum

```
public static QDataSet accum(QDataSet accumDs,
                            QDataSet ds)
```

return an array that is the running sum of each element in the array,
starting with the value accum. Result\[i\]= accum + total( ds\[0:i+1\] )

Parameters:

  - accum - the initial value of the running sum. Last value of Rank 0
    or Rank 1 dataset is used, or may be null.
  - ds - each element is added to the running sum

Returns:

  - the running of each element in the array.

See Also:

  - diff

## accum

```
public static QDataSet accum(QDataSet ds)
```

return an array that is the running sum of each element in the array,
starting with the value accum. Result\[i\]= total( ds\[0:i+1\] )

Parameters:

  - ds - each element is added to the running sum

Returns:

  - the running sum of each element in the array.

See Also:

  - diff

## acos

```
public static QDataSet acos(QDataSet ds)
```

element-wise arccos.

Parameters:

  - ds -

Returns:

## add (+)

```
public static QDataSet add(QDataSet ds1,
                          QDataSet ds2)
```

add the two datasets have the same geometry.

Parameters:

  - ds1 -
  - ds2 -

Returns:

## and

```
public static QDataSet and(QDataSet ds1,
                          QDataSet ds2)
```

element-wise logical and function. non-zero is true, zero is false.

Parameters:

  - ds1 -
  - ds2 -

Returns:

## asin

```
public static QDataSet asin(QDataSet ds)
```

element-wise arcsin.

Parameters:

  - ds -

Returns:

## atan

```
public static QDataSet atan(QDataSet ds)
```

element-wise atan.

Parameters:

  - ds -

Returns:

## atan2

```
public static QDataSet atan2(QDataSet dsy,
                            QDataSet dsx)
```

element-wise atan2, 4-quadrant atan.

Parameters:

  - dsy -
  - dsx -

Returns:

## autoHistogram

```
public static QDataSet autoHistogram(QDataSet ds)
```

One pass auto-scaling histogram. See also histogram.

Parameters:

  - ds -

Returns:

## boxcar

```
public static QDataSet boxcar(QDataSet ds, int size) 
```

run boxcar average over the dataset, returning a dataset of same
geometry. Points near the edge are simply copied from the source
dataset. The result dataset contains a property "weights" that is the
weights for each point.

Parameters:

  - ds - rank 1 dataset
  - size - size of the boxcar

Returns:

  - dataset

## bundle

```
public static QDataSet bundle(QDataSet ds1,
                             QDataSet ds2)
```

bundle the two datasets, adding if necessary a bundle dimension. This
will try to bundle on the second dimension, unlike join. This will also
isolate the semantics of bundle dimensions as it's introduced.

Parameters:

  - ds1 -
  - ds2 -

Returns:

## ceil

```
public static QDataSet ceil(QDataSet ds1)
```

element-wise ceil function.

Parameters:

  - ds1 -

Returns:

## circle

```
public static QDataSet circle(double radius)
public static QDataSet circle(String radius)
public static QDataSet circle(QDataSet radius)
```

return a dataset with X and Y forming a circle, introduced as a
convenient way to indicate planet location.

Parameters:

  - radius the radius, a rank 0 dataset, maybe with units, or a string
    parsed into a rank 0 dataset.

Returns:

  - QDataSet that when plotted is a circle.

## collapse0

```
public static QDataSet collapse0(QDataSet ds)
```

reduce the dataset rank by averaging data over the 0th dimension. If
there is fill in the reduction, then the result is fill.

## collapse1

reduce the dataset rank by averaging data over the 1st dimension. If
there is fill in the reduction, then the result is fill.

## collapse2

reduce the dataset rank by averaging data over the 2nd dimension. If
there is fill in the reduction, then the result is fill.

## collapse3

reduce the dataset rank by averaging data over the 3rd dimension. If
there is fill in the reduction, then the result is fill.

## concatenate

```
public static QDataSet concatenate(QDataSet ds1,
                                  QDataSet ds2)
```

concatenates the two datasets together, appending the datasets on the
zeroth dimension. The two datasets must be QUBES have similar geometry
on the higher dimensions. If one of the datasets is rank 0 and the
geometry of the other is rank 1, then the lower rank dataset is promoted
before appending. If the first dataset is null and the second is
non-null, then return the second dataset. This was briefly known as
"join."

Parameters:

  - ds1 - null, or a rank n dataset with dimensions any1,a1,a2,...
  - ds2 - A rank n dataset with dimensions any2,a1,a2,...

Returns:

  - a rank n dataset with dimensions any1+any2,a1,a2, or just ds2 when
    ds1 is null.

See also: join

## Constants

PI = 3.141592653589793

E = 2.718281828459045

## contour

```
public static QDataSet contour(QDataSet tds,
              QDataSet vv)
```

contour the data in rank 2 table tds at rank 0 vv. The result is a rank
2 bundle of \[:,'x,y,z'\] where i is the contour number. The result will
have DEPEND\_0 be an monotonically increasing sequence with jumps
indicating new contours.

Parameters:

  - tds - rank 2 table
  - vv - rank 2 bundle

Returns:

## convertUnitsTo

```
public static DatumRange   convertUnitsTo(DatumRange dr, Units u)
public static Datum    convertUnitsTo(Datum d, Units u)
public static QDataSet     convertUnitsTo(QDataSet ds, Units u)
```

convert the data units to the given units, which must be convertible.

Parameters:

  - ds - datum, datum range, or dataset, e.g. '5 to 50MHz'
  - vv - the new units. e.g. 'Hz'

Returns:

  - data in the new units, e.g. '5000000 to 50000000 Hz'

## copysign

```
public static QDataSet copysign(QDataSet magnitude,
                               QDataSet sign)
```

returns a dataset with the same geometry, but having the floating-point
magnitude of the first argument with the sign of the second argument.

Parameters:

  - magnitude - dataset containing magnitude
  - sign - dataset with compatible geometry

Returns:

  - Dataset with the magnitude and sign combined.

See Also:

  - signum

## cos

```
public static QDataSet cos(QDataSet ds)
```

element-wise cos.

Parameters:

  - ds -

Returns:

## cosh

```
public static QDataSet cosh(QDataSet ds)
```

element-wise cosh.

Parameters:

  - ds -

Returns:

## createEvent

```
public static QDataSet createEvent(java.lang.String timeRange,
                                  int rgbcolor,
                                  java.lang.String annotation)
```

tool for creating ad-hoc events datasets.

Parameters:

  - timeRange - a timerange string like "2010-01-01" or
    "2010-01-01/2010-01-10" or "2010-01-01 through 2010-01-09"
  - rgbcolor - and RGB color like 0xFF0000 (red), 0x00FF00 (green), or
    0x0000FF (blue),
  - annotation - label for event, possibly including granny codes.

Returns:

  - a rank 2 n by 4 QDataSet with startTime, duration, rgbColor,
    annotation in each record.

## createEvent

```
public static QDataSet createEvent(QDataSet append,
                                  java.lang.String timeRange,
                                  int rgbcolor,
                                  java.lang.String annotation)
```

tool for creating ad-hoc events datasets.

Parameters:

  - append - null or a dataset to append the result. This events dataset
    must have \[starttime, endtime, RBG color, string\] for each record.
  - timeRange - a timerange like "2010-01-01" or "2010-01-01/2010-01-10"
    or "2010-01-01 through 2010-01-09"
  - rgbcolor - and RGB color like 0xFF0000 (red), 0x00FF00 (green), or
    0x0000FF (blue),
  - annotation - label for event, possibly including granny codes.

Returns:

  - a rank 2 QDataSet n by 4 with startTime, duration, rgbColor,
    annotation in each record.

## dblarr

```
public static QDataSet dblarr(int len0)
```

create a dataset filled with zeros.

Parameters:

  - len0 -

Returns:

## dblarr

```
public static QDataSet dblarr(int len0,
                             int len1)
```

## dblarr

```
public static QDataSet dblarr(int len0,
                             int len1,
                             int len2)
```

## dependsOn

```
public static MutablePropertyDataSet dependsOn(QDataSet ds,
                                              int dim,
                                              QDataSet dep0)
```

declare that the dataset is a dependent parameter of an independent
parameter. This isolates the QDataSet semantics, and verifies
correctness.

Parameters:

  - ds -
  - dim - dimension to declare dependence: 0,1,2.
  - dep0 -

Returns:

## detrend

```
public static QDataSet detrend(QDataSet yy,
              int size)
```

remove D/C and low-frequency components from the data by subtracting out
the smoothed data with a boxcar of the given size. Points on the end are
zero.

Parameters:

  - yy - rank 1 dataset
  - size - size of the boxcar

Returns:

  - dataset

## dindgen

```
public static QDataSet dindgen(int len0)
```

returns rank 1 dataset with values \[0,1,2,...,len0-1\]

Parameters:

  - size - the number of elements

Returns:

  - rank 1 dataset with values \[0,1,2,...,len0-1\]

## dindgen

```
public static QDataSet dindgen(int len0,
                              int len1)
```

returns rank 2 dataset with values increasing \[ \[0,1,2\], \[ 3,4,5\]
\]

Parameters:

  - len0 -
  - len1 -

Returns:

## dindgen

```
public static QDataSet dindgen(int len0,
                              int len1,
                              int len2)
```

returns rank 3 dataset with values increasing ( \[ \[ \[0,1,2\], \[
3,4,5\] \], \[ \[6,7,8\] \], ...\] )

Parameters:

  - len0 -
  - len1 -
  - len2 -

Returns:

  - Rank 3 dataset with elements increasing.

## diff

```
public static QDataSet diff(QDataSet ds)
```

return array that is the differences between each successive pair in the
dataset. Result\[i\]= ds\[i+1\]-ds\[i\], so that for an array with N
elements, an array with N-1 elements is returned. DEPEND\_0 will contain
the average of the two points.

Parameters:

  - ds - a rank 1 dataset with N elements.

Returns:

  - a rank 1 dataset with N-1 elements.

See Also:

  - accum

## dimensionCount

```
public static int dimensionCount(QDataSet dss)
```

returns the number of physical dimensions of a dataset. JOIN, BINS do
not increase dataset dimensionality. DEPEND increases dimensionality by
dimensionality of DEPEND ds. BUNDLE increases dimensionality by N where
N is the number of bundled datasets. Note this includes implicit
dimensions taken by the primary dataset. Z(time,freq)-\>3
rand(20,20)-\>3 B\_gsm(20,\[X,Y,Z\])-\>4

Parameters:

  - ds -

Returns:

  - the number of dimensions occupied by the data.

## div

```
public static QDataSet div(QDataSet ds1,
                          QDataSet ds2)
```

element-wise div of two datasets with compatible geometry.

Parameters:

  - ds -

Returns:

## divide (/)

```
public static QDataSet divide(QDataSet ds1,
                             QDataSet ds2)
```

element-wise divide of two datasets with compatible geometry.

Parameters:

  - ds -

Returns:

## eq

```
public static QDataSet eq(QDataSet ds1,
                         QDataSet ds2)
```

element-wise equality test. 1.0 is returned where the two datasets are
equal. Fill is returned where either measurement is invalid.

Parameters:

  - ds -

Returns:

## equivalent

```
public static boolean equivalent(QDataSet ds1,
                                QDataSet ds2)
```

returns true if and only if the dataset values are equivalent. Note this
may promote rank, etc. A rank 0 dataset is promoted to a rank 1 by
replicating the value, so for example the rank 0 "4" is equivalent to
"4,4,4".

Parameters:

  - ds1 - rank n dataset
  - ds2 - rank m dataset

Returns:

  - true if the two are equivalent.

## exp

```
public static QDataSet exp(QDataSet ds)
```

element-wise exponentiate e\*\*x.

Parameters:

  - ds -

Returns:

## exp10

```
public static QDataSet exp10(QDataSet ds)
```

element-wise exponentiate 10\*\*x.

Parameters:

  - ds -

Returns:

## expm1

```
public static QDataSet expm1(QDataSet ds)
```

returns ex -1. Note that for values of x near 0, the exact sum of
expm1(x) + 1 is much closer to the true result of ex than exp(x). (TODO
lost info in wiki)

Parameters:

  - ds -

Returns:

## extent

```
public static QDataSet extent(QDataSet ds)
```

returns a two element, rank 1 dataset containing the extent of the data.
Note this accounts for DELTA\_PLUS, DELTA\_MINUS properties. The
property QDataSet.SCALE\_TYPE is set to lin or log. The property count
is set to the number of valid measurements. TODO: this could use
MONOTONIC, but it doesn't. DELTA\_PLUS, DELTA\_MINUS make that more
difficult.

Parameters:

  - ds - rank N dataset.

Returns:

  - two element, rank 1 "bins" dataset.

See Also:

  - DataSetUtil.rangeOfMonotonic( QDataSet ds ).

## extent

```
public static QDataSet extent(QDataSet ds,
                             QDataSet range)
```

returns a two element, rank 1 dataset containing the extent of the data.
Note this accounts for DELTA\_PLUS, DELTA\_MINUS properties. The
property QDataSet.SCALE\_TYPE is set to lin or log. The property count
is set to the number of valid measurements. This checks the monotonic
property, and uses it to avoid iterating through the data if available.

Parameters:

  - ds -
  - range, - if non-null, return the union of this range and the extent.
    This must not contain fill\!

Returns:

  - two element, rank 1 "bins" dataset.

## fft

```
public static QDataSet fft(QDataSet ds)
```

Performs an FFT on the provided rank 1 dataset. A rank 2 dataset of
complex numbers is returned.

Parameters:

  - ds - a rank 1 dataset.

Returns:

  - a rank 2 dataset of complex numbers.

```
public static QDataSet fft(QDataSet ds, QDataSet window, int stepFraction, ProgressMonitor mon ) 
```

perform ffts on the waveform as we do with fftPower, but keep real and
imaginary components.

Parameters:

  - ds - the waveform rank 1,2,or 3 dataset.
  - window - the window function, like ones(1024) or windowFunction(
    FFTFilterType.Hanning, 1024 ). This is used to infer window size.
  - stepFraction - step this fraction of the window size. 1 is no
    overlap, 2 is 50% overlap, 4 is 75% overlap, etc.
  - mon - progress monitor.

Returns:

  - result\[ntime,nwindow,2\]

## fftFilter

```
public static QDataSet fftFilter(QDataSet ds,
                                int len,
                                Ops.FFTFilterType filt)
```

## fftPower

```
public static QDataSet fftPower(QDataSet ds,
                               int len,
                               org.das2.util.monitor.ProgressMonitor mon)
```

create a power spectrum on the dataset by breaking it up and doing ffts
on each segment. right now only rank 2 data is supported, but there is
no reason that rank 1 shouldn't be supported. Looks for
DEPEND\_1.USER\_PROPERTIES.FFT\_Translation, which should be a rank 0 or
rank 1 QDataSet. If it is rank 1, then it should correspond to the
DEPEND\_0 dimension.

Parameters:

  - ds - rank 2 dataset ds(N,M) with M\>len
  - len - the number of elements to have in each fft.
  - mon - a ProgressMonitor for the process

Returns:

  - rank 2 fft spectrum

## fftPower

```
public static QDataSet fftPower(QDataSet ds)
```

returns the power spectrum of the waveform. Positive frequencies are
returned for DEPEND\_0, and square of the magnitude is returned for the
values.

Parameters:

  - ds - rank 1 waveform or rank 2 array of waveforms

Returns:

## fftWindow

```
public static QDataSet fftWindow(QDataSet ds,
                                int len)
```

perform ffts on the rank 1 dataset to make a rank2 spectrogram.

Parameters:

  - ds - rank 1 dataset
  - len - the window length

Returns:

  - rank 2 dataset.

## findex

```
public static QDataSet findex(QDataSet uu,
                             QDataSet vv)
```

returns the floating point index of each element of vv within the
monotonically increasing dataset uu. The result dataset will have the
same geometry as vv. The result will be negative when the element of vv
is below the smallest element of uu. The result will be greater than or
equal to the length of uu minus one when it is greater than all
elements.

Parameters:

  - uu - rank 1 monotonically increasing dataset.
  - vv - rank N dataset with values in the same physical dimension as
    uu.

Returns:

  - rank N dataset with the same geometry as vv.

## findgen

```
public static QDataSet findgen(int len0)
```

returns rank 1 dataset with values \[0,1,2,...\]

Parameters:

  - size -

Returns:

## findgen

```
public static QDataSet findgen(int len0,
                              int len1)
```

returns rank 2 dataset with values increasing \[ \[0,1,2\], \[ 3,4,5\]
\]

Parameters:

  - len0 -
  - len1 -

Returns:

## findgen

```
public static QDataSet findgen(int len0,
                              int len1,
                              int len2)
```

returns rank 3 dataset with values increasing

Returns:

## floor

```
public static QDataSet floor(QDataSet ds1)
```

element-wise ceil function.

Parameters:

  - ds1 -

Returns:

## fltarr

```
public static QDataSet fltarr(int len0)
```

create a dataset filled with zeros.

Parameters:

  - len0 -

Returns:

## fltarr

```
public static QDataSet fltarr(int len0,
                             int len1)
```

## fltarr

```
public static QDataSet fltarr(int len0,
                             int len1,
                             int len2)
```

## ge

```
public static QDataSet ge(QDataSet ds1,
                         QDataSet ds2)
```

element-wise function returns 1 where ds1\>=ds2.

Parameters:

  - ds1 -
  - ds2 -

Returns:

## greaterOf

```
public static QDataSet greaterOf(QDataSet ds1,
                                QDataSet ds2)
```

element-wise function returns the greater of ds1 and ds2. If an element
of ds1 or ds2 is fill, then the result is fill.

Parameters:

  - ds1
  - ds2

Returns:

  - the bigger of the two, in the units of ds1. If an element of ds1 or
    ds2 is fill, then the result is fill.

## gt

```
public static QDataSet gt(QDataSet ds1,
                         QDataSet ds2)
```

element-wise function returns 1 where ds1\>ds2.

Parameters:

  - ds1 -
  - ds2 -

Returns:

## hanning

```
public static QDataSet hanning(QDataSet ds,
                              int len)
```

Hanning filter for use with fftPower. ds= fftPower( hanning( randn(
20480 ), 512 ) )

## histogram

```
public static QDataSet histogram(QDataSet ds,
                                double min,
                                double max,
                                double binSize)
```

returns histogram of dataset, the number of points falling in each bin.

Parameters:

  - ds -
  - min -
  - max -
  - binSize -

Returns:

## histogram

```
public static QDataSet histogram(QDataSet ds,
                                int binCount)
```

returns a histogram of the dataset, based on the extent and scaletype of
the data. See also autoHistogram, which automatically identifies bin
width, min and max.

Parameters:

  - ds -
  - binCount - number of bins

Returns:

  - rank 1 QDataSet that is the histogram.

## interpolate

```
public static QDataSet interpolate(QDataSet vv,
                                  QDataSet findex)
```

interpolate values from rank 1 dataset vv using fractional indices in
rank N findex. For example, findex=1.5 means interpolate the 1st and 2nd
indices with equal weight, 1.1 means 90% of the first mixed with 10% of
the second. No extrapolation is done, data with findex\<0 or
findex\>(vv.length()-1) are assigned the first or last value. Note there
is no check on CADENCE. Note nothing is done with DEPEND\_0, presumably
because was already calculated and used for findex.

Parameters:

  - vv - rank 1 dataset that is the data to be interpolated.
  - findex - rank N dataset of fractional indices.

Returns:

  - the result.

## interpolate

```
public static QDataSet interpolate(QDataSet vv,
                                  QDataSet findex0,
                                  QDataSet findex1)
```

interpolate values from rank 2 dataset vv using fractional indices in
rank N findex, using bilinear interpolation.

Parameters:

  - vv - rank 2 dataset.
  - findex0 - rank N dataset of fractional indices for the zeroth index.
  - findex1 - rank N dataset of fractional indices for the first index.

Returns:

  - rank N dataset

## isBundle

```
public static boolean isBundle(QDataSet zds)
```

return true if the dataset is a bundle. It is rank 2 or rank 1, and has
the last dimension a bundle dimension.

Parameters:

  - zds -

Returns:

## isLegacyBundle

```
public static boolean isLegacyBundle(QDataSet zds)
```

return true if DEPEND\_1 is set and its units are EnumerationUnits. This
was the pre-bundle way of representing a bundle of datasets. It might be
supported indefinitely, because it has some nice rules about the data.
For example, data must be of the same units since there is no place to
put the property. Note the "legacy" status has been removed. This is a
fine way to easily create bundle datasets. See BUNDLE\_1 for more
information about bundle datasets.

Parameters:

  - zds -

Returns:

  - true for DEPEND\_1 where units are EnumerationUnits.

## join

```
public static QDataSet join(QDataSet ds1,
                           QDataSet ds2)
```

Join two rank N datasets to make a rank N+1 dataset, with the first
dimension having two elements. This is the anti-slice operator. If the
first dataset is rank N+1 JoinDataset and the other is rank N, then the
rank N dataset is added to the rank N+1 dataset. This is
underimplemented right now, and can only join two rank N datasets or if
the first dataset is the result of a join.

Parameters:

  - ds1 - rank N dataset, or null
  - ds2 - rank N dataset

Returns:

  - rank N+1 dataset

See Also:

  - slice, concatenate

## labels

```
public static QDataSet labels(java.lang.String[] labels,
                             java.lang.String context)
```

create a labels dataset for tagging rows of a dataset. If the context
has been used already, including "default", then the EnumerationUnit for
the data will be preserved. labels(\["red","green","blue"\],"default")
will always return an equivalent (and comparable) result during a
session. Example: dep1= labels( \["X","Y","Z"\], "GSM" )

Parameters:

  - labels -
  - context -

Returns:

  - rank 1 QDataSet

## labels

```
public static QDataSet labels(java.lang.String[] labels)
```

create a labels dataset for tagging rows of a dataset. Example: dep1=
labels( \["red","greed","blue"\] )

Parameters:

  - labels -

Returns:

  - rank 1 QDataSet

## le

```
public static QDataSet le(QDataSet ds1,
                         QDataSet ds2)
```

element-wise function returns 1 where ds1\<=ds2.

Parameters:

  - ds1 -
  - ds2 -

Returns:

## lesserOf

```
public static QDataSet lesserOf(QDataSet ds1,QDataSet ds2)
```

element-wise function returns the lesser of ds1 and ds2. If an element
of ds1 or ds2 is fill, then the result is fill.

Parameters:

  - ds1 -
  - ds2 -

Returns: the lesser of the two, in the units of ds1. If one of the two
elements is fill, then the result is fill.

## link

```
public static QDataSet link(QDataSet x,
                           QDataSet y)
```

This is like bundle, but declare the last dataset is dependent on the
first one. "link" is like a plot command where link(x,y) would behave
like plot(x,y) except you get a dataset back.

Parameters:

  - x - rank 1 dataset
  - y - rank 1 or rank 2 dataset

Returns:

## link

```
public static QDataSet link(QDataSet x,
                           QDataSet y,
                           QDataSet z)
```

like bundle, but declare the last dataset is dependent on the first two.

Parameters:

  - x - rank 1 dataset
  - y - rank 1 dataset
  - z - rank 1 or 2 dataset.

Returns:

## linspace

```
public static QDataSet linspace(double min,
                               double max,
                               int len0)
```

return a rank 1 dataset with len0 linearly-spaced values, the first is
min and the last is max.

Parameters:

  - min - the first value of the series
  - max - the last value of the series.
  - len0 - the number of values

Returns:

## log

```
public static QDataSet log(QDataSet ds)
```

element-wise natural logarithm.

Parameters:

  - ds -

Returns:

## log10

```
public static QDataSet log10(QDataSet ds)
```

element-wise base 10 logarithm.

Parameters:

  - ds -

Returns:

## lt

```
public static QDataSet lt(QDataSet ds1,
                         QDataSet ds2)
```

element-wise function returns 1 where ds1\<ds2.

Parameters:

  - ds1 -
  - ds2 -

Returns:

## magnitude

```
public static QDataSet magnitude(QDataSet ds)
```

return the magnitudes of vectors in a rank 2 or greater dataset. The
last index must be a cartesian dimension, so it must have a depend
dataset either named "cartesian" or having the property
CARTESIAN\_FRAME. TODO: check this in the 2011 branch, I think it's
removed.

Parameters:

  - ds - of Rank N.

Returns:

  - ds of Rank N-1.

## medianFilter

```
public static QDataSet medianFilter(QDataSet ds,
                   int size)
```

1-D median filter with a boxcar of the given size. This is not
particularly efficient and would make a nice project for a student.
Parameters:

  - ds - rank 1 dataset. Future implementations may support higher rank
    data.
  - size - the boxcar size

Returns:

  - rank 1 dataset

## mod

```
public static QDataSet mod(QDataSet ds1,
                          QDataSet ds2)
```

element-wise mod of two datasets with compatible geometry.

Parameters:

  - ds -

Returns:

## multiply (\*)

```
public static QDataSet multiply(QDataSet ds1,
                               QDataSet ds2)
```

element-wise multiply of two datasets with compatible geometry.

Parameters:

  - ds -

Returns:

## ne

```
public static QDataSet ne(QDataSet ds1,
                         QDataSet ds2)
```

element-wise not equal test. 1.0 is returned where elements are not
equal. Fill is returned where either measurement is invalid.

Parameters:

  - ds1 -
  - ds2 -

Returns:

## negate (-)

```
public static QDataSet negate(QDataSet ds1)
```

return a dataset with each element negated.

Parameters:

  - ds1 -

Returns:

## not

```
public static QDataSet not(QDataSet ds1)
```

element-wise logical not function. non-zero is true, zero is false.

```
TODO: This isn't working, use ( ds1.eq(1) ) instead.
```

Parameters:

  - ds1 -
  - ds2 -

Returns:

## ones

```
public static QDataSet ones(int len0)
```

return new dataset filled with ones.

Parameters:

  - len0 -

Returns:

## ones

```
public static QDataSet ones(int len0,
                           int len1)
```

return new dataset filled with ones.

Parameters:

  - len0 -

Returns:

## ones

```
public static QDataSet ones(int len0,
                           int len1,
                           int len2)
```

return new dataset filled with ones.

Parameters:

  - len0 -

Returns:

## or

```
public static QDataSet or(QDataSet ds1,
                         QDataSet ds2)
```

element-wise logical or function. returns 1 where ds1 is non-zero or ds2
is non-zero.

Parameters:

  - ds1 -
  - ds2 -

Returns:

## outerProduct

```
public static QDataSet outerProduct(QDataSet ds1,
                                   QDataSet ds2)
```

returns outerProduct of two rank 1 datasets, a rank 2 dataset with
elements R\[i,j\]= ds1\[i\] \* ds2\[j\].

Parameters:

  - ds1 - Rank 1 dataset having length M
  - ds2 - Rank 1 dataset having length N

Returns:

  - Rank 2 dataset lengths M,N

## pow (\*\*)

```
public static QDataSet pow(QDataSet ds1,
                          QDataSet pow)
```

element-wise pow (\*\* in FORTRAN, ^ in IDL) of two datasets with the
same geometry.

Parameters:

  - ds1 -
  - pow - dataset or scalar

Returns:

## rand

```
public static QDataSet rand(int len0)
```

return returns a rank 1 dataset of random uniform numbers from \[0,1\].

## randn

```
public static QDataSet randn(int len0)
```

return returns a rank 1 dataset of random numbers of a guassian (normal)
distribution.

## randomn

```
public static QDataSet randomn(long seed,
                              int len0)
```

returns a rank 1 dataset of random numbers of a guassian (normal)
distribution. System.currentTimeMillis() may be used for the seed.

Parameters:

  - seed -
  - len0 -

Returns:

## randomu

```
public static QDataSet randomu(long seed,
                              int len0)
```

returns a rank 1 dataset of random numbers of a uniform distribution.
System.currentTimeMillis() may be used for the seed.

Parameters:

  - seed -
  - len0 -

Returns:

## rebin

```
public static DDataSet rebin(QDataSet ds, QDataSet newTags0, QDataSet newTags1) 
```

returns a dataset with tags specified by newTags

  - ds a rank 2 dataset. This can be a bundle dataset of \[i;X,Y,Z\]
  - newTags0 rank 1 monotonic dataset
  - newTags1 rank 1 monotonic dataset

Returns:

  - rank 2 dataset with newTags0 for the DEPEND\_0 tags, newTags1 for
    the DEPEND\_1 tags.

## rebinBundle

```
public static DDataSet rebinBundle(QDataSet ds,
                                  QDataSet dep0,
                                  QDataSet dep1)
```

takes rank 2 bundle (x,y,z) and averages it into table z(x,y). This is
similar to what happens in the spectrogram routine.

Parameters:

  - ds - rank 2 bundle(x,y,z)
  - dep0 - the depend0 for the result
  - dep1 - the depend1 for the result

Returns:

  - rank 2 dataset of z averages with depend\_0 and depend\_1.

## reduceMax

```
public static QDataSet reduceMax(QDataSet ds,
                                int dim)
```

reduce the dataset's rank by reporting the max of all the elements along
a dimension. Only QUBEs are supported presently.

Parameters:

  - ds - rank N qube dataset.
  - dim - zero-based index number.

Returns:

## reduceMean

```
public static QDataSet reduceMean(QDataSet ds,
                                 int dim)
```

reduce the dataset's rank by reporting the mean of all the elements
along a dimension. Only QUBEs are supported presently.

Parameters:

  - ds - rank N qube dataset.
  - dim - zero-based index number.

Returns:

## reduceMin

```
public static QDataSet reduceMin(QDataSet ds,
                                int dim)
```

reduce the dataset's rank by reporting the min of all the elements along
a dimension. Only QUBEs are supported presently.

Parameters:

  - ds - rank N qube dataset.
  - dim - zero-based index number.

Returns:

## reform

```
public static QDataSet reform(QDataSet ds)
```

Reshape the dataset to remove the first dimension with length 1,
reducing its rank by 1. Dependencies are also preserved.

Parameters:

  - ds - a rank r dataset \[1,m\], \[1,n,m\], etc.

Returns:

  - a rank r-1 dataset \[m\], \[n,m\], etc.

## reform

```
public static QDataSet reform(QDataSet ds,
                             int[] qube)
```

change the dimensionality of the elements of the QUBE dataset. For
example, convert \[1,2,3,4,5,6\] to \[\[1,2\],\[3,4\],\[5,6\]\].

params:

  - ds
  - qube the dimensions of the result dataset.

returns:

  - a new dataset with the specified dimensions, and the properties
    (e.g. UNITS) of the input dataset.

## replicate

```
public static WritableDataSet replicate(double val,
                                       int len0)
```

returns rank 1 dataset with value

Parameters:

  - val - fill the dataset with this value.
  - len0 -

Returns:

## replicate

```
public static WritableDataSet replicate(double val,
                                       int len0,
                                       int len1)
```

returns rank 2 dataset filled with value

Parameters:

  - val - fill the dataset with this value.
  - len0 -
  - len1 -

Returns:

## replicate

```
public static WritableDataSet replicate(double val,
                                       int len0,
                                       int len1,
                                       int len2)
```

returns rank 3 dataset with filled with value.

Parameters:

  - val - fill the dataset with this value.
  - len0 -
  - len1 -
  - len2 -

Returns:

## replicate

```
public static WritableDataSet replicate(float val,
                                       int len0)
```

returns rank 1 dataset with value

Parameters:

  - val - fill the dataset with this value.
  - len0 -

Returns:

## replicate

```
public static WritableDataSet replicate(float val,
                                       int len0,
                                       int len1)
```

returns rank 2 dataset filled with value

Parameters:

  - val - fill the dataset with this value.
  - len0 -
  - len1 -

Returns:

## replicate

```
public static WritableDataSet replicate(float val,
                                       int len0,
                                       int len1,
                                       int len2)
```

returns rank 3 dataset with filled with value.

Parameters:

  - val - fill the dataset with this value.
  - len0 -
  - len1 -
  - len2 -

Returns:

## rescaleRange

```
public static QDataSet rescaleRange(QDataSet dr,
                                   double min,
                                   double max)
```

returns rank 1 QDataSet range relative to the range in "dr", where 0. is
the minimum, and 1. is the maximum. For example rescaleRange(ds,1,2) is
scanNext, rescaleRange(ds,-1,0) is scanPrevious,
rescaleRange(ds,-0.5,1.5) is zoomOut.

Parameters:

  - dr - a QDataSet with "min,max" for BINS\_0 and with nonzero width.
  - min - the new min normalized with respect to this range. 0. is this
    range's min, 1 is this range's max, 0 is min-width.
  - max - the new max width normalized with respect to this range. 0. is
    this range's min, 1 is this range's max, 0 is min-width.

Returns:

  - new rank 1 QDataSet range.

## residuals

```
public static QDataSet residuals(QDataSet ds, int boxcarSize) 
```

returns number of stddev from adjacent data.

  - ds, rank 1 dataset.
  - boxcarSize

Returns:

  - QDataSet

## reverse

```
public static QDataSet reverse(QDataSet ds)
```

returns the reverse of the rank 1 dataset.

Parameters:

  - ds -

Returns:

## ripples

```
public static QDataSet ripples( int len0 )
```

rank 1 dataset for demos. It contains fill at index 13.

Parameters:

  - len0 - size of the first dimension

Returns:

```
public static QDataSet ripples( int len0, int len1 )
```

rank 2 dataset for demos.

Parameters:

  - len0 - size of the first dimension
  - len1 - size of the second dimension

Returns:

```
public static QDataSet ripples( int len0, int len1, int len2 )
```

rank 3 dataset for demos.

Parameters:

  - len0 - size of the first dimension
  - len1 - size of the second dimension
  - len2 - size of the third dimension

Returns:

```
public static QDataSet ripples( int len0, int len1, int len2, int len3 )
```

rank 4 dataset for demos.

Parameters:

  - len0 - size of the first dimension
  - len1 - size of the second dimension
  - len2 - size of the third dimension
  - len3 - size of the fourth dimension

Returns:

## ripplesSpectrogramTimeSeries

return fake position data for testing result is rank 2 bundle \[len,27\]

Parameters:

  - len -

Returns:

## ripplesTimeSeries

```
public static QDataSet ripplesTimeSeries(int len)
```

return fake rank 1 data timeseries for testing

Parameters:

  - len - the number of records

Returns:

  - rank 1 time series. (like density(time))

## ripplesWaveformTimeSeries

return fake waveform data for testing result is rank 2 bundle
\[len,512\]

Parameters:

  - len - number of 512-element waveforms.

Returns:

  - rank 2 dataset with record for the zeroth dimension and offset for
    the second.

## safeName

```
public static java.lang.String safeName(java.lang.String suggest)
```

Make a Java-style identifier from the provided string, which will only
include a-z, A-Z, 0-9 (though not the first), and \_. For example,
"a\>b" becomes agtb.

Parameters:

  - suggest - A string suggesting a name. The non-compliant characters
    are replaced. for example

Returns:

  - a string guarenteed to be useful as an identifier.

## sawtooth

```
public static QDataSet sawtooth(QDataSet t)
```

generates a sawtooth from the tags, where a peak occurs with a period
2\*PI. All values of T should be ge zero. TODO: I think there should be
a modp function that is always positive. (-93 % 10 -\>7 though...)

Parameters:

  - t - time

Returns:

  - /|/|/|

## shuffle

```
public static QDataSet shuffle(QDataSet ds)
```

returns a rank 1 dataset of indices that shuffle the rank 1 dataset ds

```
s= shuffle( ds )
dsShuffled= ds[s]
    
```

Parameters:

  - ds - rank 1 dataset

Returns:

  - rank 1 dataset of integer indices.

## signum

```
public static QDataSet signum(QDataSet ds1)
```

returns the signum function of the argument; 0.0 if the argument is
zero, 1.0 if the argument is greater than zero, -1.0 if the argument is
less than zero.

Parameters:

  - ds1 -

Returns:

  - \-1.0, 0.0, or 1.0 to indicate the sign.

See Also:

  - copysign

## sin

```
public static QDataSet sin(QDataSet ds)
```

element-wise sin.

Parameters:

  - ds -

Returns:

## sinh

```
public static QDataSet sinh(QDataSet ds)
```

element-wise sinh.

Parameters:

  - ds -

Returns:

## smooth

```
public static QDataSet smooth(QDataSet ds,
                             int size)
```

run boxcar average over the dataset, returning a dataset of same
geometry. Points near the edge are simply copied from the source
dataset. The result dataset contains a property "weights" that is the
weights for each point.

Parameters:

  - ds - a rank 1 dataset of size N
  - size - the number of adjacent bins to average

Returns:

  - rank 1 dataset of size N

## smoothFit

```
public static QDataSet smoothFit(QDataSet xx,
                QDataSet yy,
                int size)
```

run boxcar average over the dataset, returning a dataset of same
geometry. Points near the edge are fit to a line and replaced. The
result dataset contains a property "weights" that is the weights for
each point.

Parameters:

  - xx - a rank 1 dataset of size N
  - yy - a rank 1 dataset of size N
  - size - the number of adjacent bins to average. If size is greater
    than yy.length, size is reset to yy.length.

Returns:

  - rank 1 dataset of size N

## sort

```
public static QDataSet sort(QDataSet ds)
```

returns a rank 1 dataset of indices that sort the rank 1 dataset ds.
This is not the dataset sorted. For example:

```
ds= randn(2000)
s= sort( ds )
dsSorted= ds[s]
    
```

Parameters:

  - ds - rank 1 dataset

Returns:

  - rank 1 dataset of indices that sort the input dataset.

## sqrt

```
public static QDataSet sqrt(QDataSet ds)
```

element-wise sqrt.

Parameters:

  - ds -

Returns:

## square

```
public static QDataSet square(QDataSet t)
```

generates a square from the tags, where a the signal is 1 from 0-PI, 0
from PI-2\*PI, etc.

Parameters:

  - t - time

Returns:

  - square wave with a period of 2 PI.

## subtract (-)

```
public static QDataSet subtract(QDataSet ds1,
                               QDataSet ds2)
```

subtract one dataset from another.

Parameters:

  - ds1 -
  - ds2 -

Returns:

## taggen

```
public static MutablePropertyDataSet taggen(double base,
                                           double dcadence,
                                           int len0,
                                           org.das2.datum.Units units)
```

creates tags. First tag will be start and they will increase by cadence.
Units specifies the units of each tag.

Parameters:

  - start -
  - cadence -
  - len0 -
  - units -

Returns:

## tan

```
public static QDataSet tan(QDataSet ds)
```

element-wise tan.

Parameters:

  - ds -

Returns:

## tanh

```
public static QDataSet tanh(QDataSet ds)
```

element-wise tanh.

Parameters:

  - ds -

Returns:

## timegen

```
public static QDataSet timegen(java.lang.String baseTime,
                              java.lang.String cadence,
                              int len0)
```

returns rank 1 dataset with values \[0,1,2,...\]

Parameters:

  - baseTime - e.g. "2003-02-04T00:00"
  - cadence - e.g. "4.3 sec" "1 day"
  - len0 - the number of elements.

Returns:

  - rank 1 dataset

## toDegrees

```
public static QDataSet toDegrees(QDataSet ds)
```

## toRadians

```
public static QDataSet toRadians(QDataSet ds)
```

## toTimeDataSet

```
public static QDataSet toTimeDataSet( QDataSet years, QDataSet mons, QDataSet days, QDataSet hour, QDataSet minute, QDataSet second, QDataSet nano )
```

returns a rank 1 dataset of timetags, by adding the components. Any of
the components can be null, except for years and days.

Parameters:

  - years - the years. (2010) Less than 100 is interpreted as 19xx.
  - mons - the months (1..12), or null. If null, then days are day of
    year
  - days - the day of month (1..28) or day of year.
  - hour - null or the hours of the day.
  - minute - null or the minutes of the day
  - second - null or the seconds of the day
  - nano - null or the nanoseconds (1e-9) of the day

Returns:

  - a rank 1 dataset with Units.us2000 (non-leap microseconds since
    2000-01-01T00:00). Be sure to check the units as a future version
    may change.

## total

```
public static double total(QDataSet ds)
```

return the total of all the elements in the dataset, returning a rank 0
dataset. If there are invalid measurements, then fill is returned. Does
not support BINS or BUNDLE dimensions.

Parameters:

  - ds -

Returns:

  - the unweighted total of the dataset, or -1e31 if fill was
    encountered.

## total

```
public static QDataSet total(QDataSet ds,
                            int dim)
```

reduce the dataset's rank by totalling all the elements along a
dimension. Only QUBEs are supported presently.

Parameters:

  - ds - rank N qube dataset. N=1,2,3,4
  - dim - zero-based index number.

Returns:

## transpose

```
public static QDataSet transpose(QDataSet ds)
```

Transpose the rank 2 dataset.

## uniqValues

```
public static QDataSet uniqValues(QDataSet ds,
                                 QDataSet sort)
```

return the unique elements from the dataset. If sort is null (jython
None), then the dataset is assumed to be monotonic, and only repeating
values are coalesced. If sort is non-null, then it is the result of the
function "sort" and should be a rank 1 list of indices that sort the
data. renamed uniqValues from uniq to avoid confusion with the IDL
command.

Parameters:

  - ds -
  - sort -

Returns:

## valid

```
public static QDataSet valid(QDataSet ds)
```

returns a dataset with zero where the data is invalid, and positive
non-zero where the data is valid. (This just returns the weights plane
of the dataset.) r= where( valid( ds ) )

Parameters:

  - ds - a rank N dataset that might have FILL\_VALUE, VALID\_MIN or
    VALID\_MAX set.

Returns:

  - a rank N dataset with the same geometry, with zeros where the data
    is invalid and \>0 where the data is valid.

## where

```
public static QDataSet where(QDataSet ds)
```

returns a dataset containing the indices of where the dataset is
non-zero. For a rank 1 dataset, returns a rank 1 dataset with indices
for the values. For a higher rank dataset, returns a rank 2 qube dataset
with ds.rank() elements in the first dimension. Note when the dataset is
all zeros (false), the result is a zero-length array, as opposed to IDL
which would return a -1 scalar.

Parameters:

  - ds - of any rank M greater than 0.

Returns:

  - when ds is rank 1, a rank 1 list of N indices. When ds is rank M\>1,
    rank 2 dataset with N by M elements, where N is the number of
    non-zero elements found.

## zeros

```
public static WritableDataSet zeros(int len0)
```

return new dataset filled with zeros. Note, unlike Matlab which would
return a rank 2 matrix of data, this returns a rank 1 dataset.

Parameters:

  - len0 - the number of elements

Returns:

  - an Qube dataset with this dimension.

## zeros

```
public static WritableDataSet zeros(int len0,
                                   int len1)
```

return new dataset filled with zeros.

Parameters:

  - len0 -

Returns:

## zeros

```
public static WritableDataSet zeros(int len0,
                                   int len1,
                                   int len2)
```

return new dataset filled with zeros.

Parameters:

  - len0 -

Returns:

## zeros

```
public static WritableDataSet zeros(QDataSet ds)
```

return a new dataset filled with zeroes that has the same geometry as
the given dataset. Only supports QUBE datasets.

Parameters:

  - ds -

Returns:

  - a new dataset with filled with zeroes with the same geometry.

# Misc

## getParam

```
getParam( name, default [, label[, values ]]  )
```

returns the parameter with the name, or the default if not provided.
This is an interesting operator because it is defined in each context,
and parameters are passed in differently in each case.

Params:

  - name - the unique name of the parameter, which must be valid a Java
    identifier.
  - default - a default value for the parameter.
  - label - a short label describing the use. (This should probably be
    renamed "title" since a sentence is okay.)
  - values - is a list of values enumerating the possible values for
    this argument. Note Autoplot doesn't check that these are valid, but
    automatic GUIs limit the option.

How are these typed? "foo" is a string, 4.0 is a double, etc. TODO: need
documentation on interpretation.

For python data sources,
vap+jyds:<script_file>?<paramName>=<paramValue>. Use of this function
will result in an item in the datasource editor.

For --script on the command line, it's a command line argument.

For application context scripts, the default value is always used, but a
future rev may create a GUI. There's an experimental mode for this.
Holding shift and pressing the execute will enter a GUI.

## downloadResourceAsTempFile

```
downloadResourceAsTempFile( url, mon ) -> File
downloadResourceAsTempFile( url, timeoutSeconds, mon ) -> File
```

Download the resource into a file. The URL may be any web address, and
may contain parameters (unlike the FileSystem). Note, the downloaded
resource may be reused by other threads for 10 seconds. This allows
scripts to be simpler and more abstract, written to load one variable
but actually able to load many efficiently.

Params:

  - url - Url to download
  - timeoutSeconds - integer number of seconds to allow use of cached
    file. The default is 10 seconds. 12 hours or 43200 seconds is the
    limit. 0 is allowed.
  - mon - ProgressMonitor to monitor the download.

Returns:

  - File containing the data, which will be deleted when the application
    exits. (TODO: server apps?)

Throws:

  - java.lang.IOException when there is a problem downloading the file

Example:

```
fil= downloadResourceAsTempFile( URL('`<http://autoplot.org/data/autoplot.dat>`'), monitor )
```

## getFile( surl, mon )

```
getFile( surl, mon )
```

Download the file and make it available to the script. The URL may not
contain parameters, but the result is cached.

Params:

  - url - Url to download, without ? and params
  - mon - ProgressMonitor to monitor the download.

Returns:

  - File containing the data, which will persist in the user's cache.

## getDataSet

```
getDataSet( uri )
```

returns a QDataSet for the given URI. Execution will stop at this point
until the dataset is loaded.

```
getDataSet( uri, monitor )
```

can be used to monitor the download. Note "monitor" is the local
variable that contains a ProgressMonitor object.

```
uri= '`<http://www.rbsp-ect.lanl.gov/data_pub/rbspa/hope/level2/rbspa_rel01_ect-hope-sci-L2_$Y$m$d_v$(v,sep>`).cdf?FEDU'
timerange= getParam( 'timerange', '2013-04-25', 'timerange to load' )
ds= getDataSet( uri, timerange )
```

When the uri can load data from any timerange, as with aggregations,
then this will load the data for the given timerange, expressed as
string.

## listDirectory

```
listDirectory( uri )
```

For example:

```
files= listDirectory( '`<http://autoplot.org/data/>`*.cdf' )
```

returns a listing of the directory "uri." If uri ends with a slash, then
the directory is listed without filtering, otherwise the part following
the slash is a glob that is matched. Note, the list does not contain the
folder name, so it is typically added to the result:

```
files= listDirectory( '`<http://autoplot.org/data/>`*.cdf' )
for f in files:
```
`&nbsp;&nbsp;&nbsp;print&nbsp;'`&lt;http://autoplot.org/data/'+f&gt;

## Color

java.awt.Color is imported, so for example Color.RED may be used.

```
dom.plotElements[0].style.color= Color.RED
```

## DataSetBuilder

The DataSetBuilder object is useful for creating datasets.

```
from org.virbo.dsutil import DataSetBuilder
dsb= DataSetBuilder(1,100)  # creates a rank 1 with 100 records pre-allocated. 
for i in xrange(115):
  dsb.putValue(-1,0.0)    # -1 means use the built in position
  dsb.nextRecord()
plot(dsb.getDataSet())
```

```
from org.virbo.dsutil import DataSetBuilder
dsb= DataSetBuilder(2,100,10)  # creates a rank 2 with 100 10-element records pre-allocated. 
for i in range(115):
  for j in range(10):
     dsb.putValue(i,j,0.0)  
plot(dsb.getDataSet())
```

## putProperty

The putProperty method sets the property on a dataset. For datasets that
can be modified (mutable), this sets the property and the dataset is
returned. For datasets that are immutable, a copy is made the property
is set on the copy.

```
ds= ripples(20)
ds= putProperty( ds, QDataSet.UNITS, Units.eV )
```

## dataset

Converts many objects into QDataSet. For example dataset(\[1,2,3\])
converts the Python array into a 3-element QDataSet.

## datum

Converts many objects into Datum. For example datum(1) into the
dimensionless Datum "1", and datum('2014-05-06T07:08'). Note
Units.days.createDatum(20) can be used to create datums as well.

## LinFit

LinFit is a code that does linear fits of Y(X) where there may be errors
in Y. For example:

```
x= linspace( 0,10,200 )
y= x * 6.4 + 0.4 + randn(200) 
from org.virbo.dsutil import LinFit
lf= LinFit(x,y)
setLayoutOverplot(2)
plot( 0, x,y )
plotx( 1, x, lf.getB() * x + lf.getA(), color=Color.RED )
```

# Slice and Trim in Python

The slice and trim operators are available in Python as index operators.
For example:

```
ds= ripples(20,30)
s1= ds[10,:]
```

The trim operator is similar:

```
ds= ripples(20,30)
t1= ds[5:15,:]
```

## Other useful Java stuff

```
java.lang.System.currentTimeMillis()
Runtime.getRuntime().maxMemory()   memory available to the JVM
Runtime.getRuntime().totalMemory() memory allocated by the JVM 
Runtime.getRuntime().freeMemory()  free memory of total memory.
```

# DOM

The DOM represents the state of the application, including the canvas,
the plots, the plot elements on each plot, and all the data sources. For
example,

```
dom.timeRange= DatumRangeUtil.parseTimeRange('2014')
print dom.bindings
```

# Proper, Fully-Capable, Jython Scripts

Ed W at RPWG points out that python provides some of the functionality I
recreate, if scientists were willing to learn a little python. Also Bob
W and I were discussing a method for defining DataSourceEditorPanels for
jyds sources. I've always meant to have an alternate form for specifying
these scripts and this section begins this discussion.

```
def mysource( orbit='A' ):
  """Look up data for an orbit.
     orbit: the orbit number to lookup. A,B,C,0-41"""
```

```
class plugin:
  def dataSourceEditorPanel( uri ): uri
  def getDataSet( params ): QDataSet, or dictionary of calculated parameters
  def formatDataSet( QDataSet, params )
```

# TimeSeriesBrowse

Time Series Browse is the datasource's capability to cover long
timeseries. For example a script shows the outside temperature, and
users can use the script to look at the temperature of any day.

This can be done in two ways. First, you can write a script that takes
one file and produces a dataset. When script uses the variable
"resourceURI" to point to the file, this variable can be an aggregation
and Autoplot's aggregation feature can use the script to read in each
day's data.

Second, the script itself can handle the time range as a parameter. Here
the parameter "timerange" is a string that defines the time range
requested by the user. It is a string that is parsed with the routine
DatumRangeUtil.parseTimeRange which returns a DatumRange representing
the range. Examples show how this is used.

If either resourceURI is an aggregation or the timerange parameter is
used by the script, Autoplot will listen to the axes and re-request data
as we navigate to other time ranges. Note the time series browse
capability also supports a resolution, but this is currently not used in
scripts. They will always load the data at the native resolution. The
script can report a resolution, however, using the CACHE\_TAG property
in the result. For example, a script tries to load low resolution data
if available, and then falls back to high resolution when it is not and
reduces the result. Here the CACHE\_TAG property must be set for the
DEPEND\_0 timetags of the result.
<http://autoplot.org/data/jyds/eg/tsbRes.jyds>

# Listening to Events

GUI events are handled nicely in Jython, often making it so just a
little code is needed to handle events. For example,
org.das2.components.DataPointRecorder will fire off events as new points
are added. In Java, this requires a bit of boilerplate code to listen to
the events, but in Jython the code is simple:

```
dpr= org.das2.components.DataPointRecorder()
def mydataSetUpdated(event):
    print event       
dpr.dataSetUpdated= mydataSetUpdated
```

Here dpr has the Java Bean pattern addDataSetUpdateListener which has
the single method dataSetUpdated.

Here's a Box Selector:

```
from org.das2.event import BoxSelectorMouseModule
mm= BoxSelectorMouseModule.create( dom.plots[0].controller.dasPlot, 'demo box' )
def boxSelected(event):
   print event
mm.boxSelected= boxSelected
dom.plots[0].controller.dasPlot.addMouseModule(mm)
```

Here's a slicer:

```
mm= DataPointSelectorMouseModule( plot, None, 'demo slice', VerticalSliceSelectionRenderer( plot ) )
def mousePointSelected(event):
    print event
mm.dataPointSelected= mousePointSelected
```

## Reading the stack trace on error messages

It's tricky to decipher the stack traces in error messages when there's
a problem in the call back, because Autoplot is not built to receive and
interpret these messages. In the stack trace, look for the name of the
script (demoSlice2.jy in this case):

```
at org.python.core.Py.AttributeError(Py.java:127)
at org.python.core.PyObject.noAttributeError(PyObject.java:991)
at org.python.core.PyObject.__getattr__(PyObject.java:986)
at org.python.pycode._pyx423.mousePointSelected$1(demoSlice2.jy:27)   <---HERE
at org.python.pycode._pyx423.call_function(demoSlice2.jy)
at org.python.core.PyTableCode.call(PyTableCode.java:217)
at org.python.core.PyTableCode.call(PyTableCode.java:437)
at org.python.core.PyFunction.__call__(PyFunction.java:189)
at org.python.core.PyCompoundCallable.__call__(PyCompoundCallable.java:28)
at org.python.core.PyObject.__call__(PyObject.java:460)
at org.python.core.PyObject._jcallexc(PyObject.java:2838)
at org.python.core.PyObject._jcall(PyObject.java:2870)
at org.python.proxies.org.das2.event.DataPointSelectionListener$Adapter.dataPointSelected(Unknown Source)
at org.das2.event.DataPointSelectorMouseModule.fireDataPointSelectionListenerDataPointSelected(DataPointSelectorMouseModule.java:124)
...
```

# DataSets are immutable, sort of

The QDataSet interface is immutable, or read-only, and should be treated
so. Most QDataSet implementations have a mutable version of the
interface, however, which is so implementations can be efficient. The
idea here is that the guy making the dataset knows that it is mutable
and can build it up, then hand it off to the calling code who knows only
that it is a QDataSet and immutable.

Unfortunately, Jython is loosely typed, and a number of scripts use the
fact that the dataset is mutable in their implementation. This can
result in problems, when datasets are cached and mutating the dataset
means mutating it for everybody. The bug motivating this section was
caused when a script was slicing the rank 2 y tags and putting them back
in the data, and then crashing when rerun because the y tags had already
been sliced.

For example in Jython, you can do this:

```
ds= findgen(20)
ds[3]= float('NaN')
plot( ds )
```

But what if the findgen command were optimized so successive calls would
return the same dataset object? Essentially they would be failing their
contract.

Update Jan 2014: Data set implementations that allow for mutability via
putProperty or putValue now have a makeImmutable() method that will
result in runtime errors if these methods are called again. Because if
this, clients should call isImmutable and make a copy if they need to
modify a dataset.

# Other Commands

A few other things are imported into sessions automatically, because
they are useful and we don't want to burden new users with having to
import them.

  - <https://ci-pw.physics.uiowa.edu/job/autoplot-javadoc/lastSuccessfulBuild/artifact/doc/org/das2/qds/ops/Ops.html#method_summary>
  - <https://ci-pw.physics.uiowa.edu/job/autoplot-javadoc/lastSuccessfulBuild/artifact/doc/org/autoplot/jythonsupport/JythonOps.html>
  - <https://ci-pw.physics.uiowa.edu/job/autoplot-javadoc/lastSuccessfulBuild/artifact/doc/org/autoplot/jythonsupport/Util.html>
  - <https://ci-pw.physics.uiowa.edu/job/autoplot-javadoc/lastSuccessfulBuild/artifact/doc/org/das2/qds/QDataSet.html>
    (prefix with class name: QDataSet.DEPEND\_0, etc)
  - <https://ci-pw.physics.uiowa.edu/job/autoplot-javadoc/lastSuccessfulBuild/artifact/doc/org/das2/qds/util/BinAverage.html>
  - <https://ci-pw.physics.uiowa.edu/job/autoplot-javadoc/lastSuccessfulBuild/artifact/doc/org/das2/qds/util/Reduction.html>

These are prefixed with the class name (e.g. Units.cm):

  - <https://ci-pw.physics.uiowa.edu/job/autoplot-javadoc/lastSuccessfulBuild/artifact/doc/org/das2/datum/DatumRange.html>
  - <https://ci-pw.physics.uiowa.edu/job/autoplot-javadoc/lastSuccessfulBuild/artifact/doc/org/das2/datum/Units.html>
  - <https://ci-pw.physics.uiowa.edu/job/autoplot-javadoc/lastSuccessfulBuild/artifact/doc/org/das2/datum/DatumRangeUtil.html>
  - <https://ci-pw.physics.uiowa.edu/job/autoplot-javadoc/lastSuccessfulBuild/artifact/doc/org/das2/datum/TimeUtil.html>
  - <https://ci-pw.physics.uiowa.edu/job/autoplot-javadoc/lastSuccessfulBuild/artifact/doc/org/das2/datum/TimeParser.html>
  - <https://ci-pw.physics.uiowa.edu/job/autoplot-javadoc/lastSuccessfulBuild/artifact/doc/org/das2/util/filesystem/FileSystem.html>
  - <https://ci-pw.physics.uiowa.edu/job/autoplot-javadoc/lastSuccessfulBuild/artifact/doc/org/das2/fsm/FileStorageModel.html>

These are useful but must be imported:

  - from org.das2.qds import DataSetUtil
    <http://apps-pw.physics.uiowa.edu/hudson/job/autoplot-javadoc/ws/doc/org/das2/qds/DataSetUtil.html>
  - from org.das2.qds.dataset import DataSetOps
    <http://apps-pw.physics.uiowa.edu/hudson/job/autoplot-javadoc/ws/doc/org/das2/qds/DataSetOps.html>

TODO:

  - sync up with javadoc
  - remove javadoc, this is the authoritative copy

# Order of Operations

Take care with the order of operations. For example,
magnitude(a)\*magnitude(b).gt(0) should be
(magnitude(a)\*magnitude(b)).gt(0).

# Dealing With Jython

Here we point out some annoyances to be aware of.

  - Constructor calls fail to adapt to PyQDataSet. QDataSets are adapted
    to PyQDataSet, which allows ds\[2\] -\> ds.value(2) and all
    operators.
  - Often you have to explicitly convert a number or list into a
    QDataSet. Use the dataset() command.

# Debugging

  - print statements can be used to indicate variable status: "print ds"
  - When the script context is "application context", when an error is
    hit, the script session is live and variable states can be queried.
    In the script editor, highlight an expression, and mouse over to get
    a tooltip. The tooltip shows the value of the expression.
  - Similarly, you can highlite an variable or expression, and
    \[right-click\]-\>Actions-\>Plot. This will send the data highlited
    over to another Autoplot running in server mode. Start up a second
    Autoplot (jnlp won't let you do this, so use the single jar),
    Options-\>Enable Server, on port 12345. The "plot" command exports
    the data as a .qds file and sends a plot command to the Autoplot in
    server mode.
  - to force execution to stop at a given point, I call the undefined
    function "stop" which causes the script session to crash.
  - the peekAt command can be used with a Java debugger (like Netbeans
    or Eclipse) to jump into the debugger with a Java breakpoint.

# Debugging with pdb

Python has a debugging method built-in "pdb", which probably could be
used in Autoplot's scripting environment. However experiments have shown
that it is very easy to loose control of the debugger, potentially
hanging the application. That said, some notes about this should be
recorded here: [developer.jython.pdb](developer.jython.pdb.md "wikilink")

# Using the console and server mode

The console tab has a command line so that commands can be entered
interactively. For example, start the console tab
(\[menubar\]-\>Options-\>Enable Feature-\>Log Console) and type in at
the AP prompt "plot( '<http://autoplot.org/data/autoplot.dat>' )". This
is the equivalent as typing in the command at the address bar, and also
executing the command in a script. The session persists between
commands, so for example you can type in:

```
AP> ds1= randn(100)
```

then

```
AP> ds2= findgen(100)
```

and

```
AP> plot( ds1 + ds2 )
```

These are the same commands available in scripts (application context),
documented above.

Autoplot also has a server mode to allow for control from other
processes. For example, the applot command for IDL works by formatting
the dataset to a temporary file and then sending a command to the
Autoplot session to plot data in the file. This server mode is a session
just like the command line session. For example try from a unix command
line:

`unix%&nbsp;wget&nbsp;-O&nbsp;autoplot.jar&nbsp;`&lt;http://autoplot.org/jnlp/latest/autoplot.jar&gt;  
```
unix% java -cp autoplot.jar org.autoplot.AutoplotUI --server=12345 &
unix% telnet localhost 12345
autoplot> ds1= randn(100)
autoplot> ds2= findgen(100)
autoplot> plot( ds1 + ds2 )
```

Note this interface introduces a number of security problems, and may
change.

# SciPy vs Autoplot's Jython

People at U. Iowa are starting to compare Autoplot's Jython with SciPy
to see how close they are. This is a brief list of differences found:

  - SciPy allowed sloppiness at array boundaries, like IDL does. If A
    has 20 elements, and B=\[19,20,21\], then A\[B\] is okay. Autoplot
    does not allow this.
  - "where" returns a rank 1 dataset, SciPy returns a strange array of
    arrays. x = np.where(slice == max(slice))\[0\]\[0\]
  - With Autoplot, it's easy to make lists of arrays instead of lists of
    scalars.
  - Autoplot's methods cannot easily be imported as np, but they should
    be.
  - np.float(spectra\_trim\[:,77\].shape\[0\]) is just
    spectra\_trim.length()
  - pycdf/getDataSet CDF reading is different.

There is an effort to make Jython work with native Python code,
[JyNI](http://jyni.org/), and this is expected to be released around the
same time Jython2.7 is released as a production release.

# Including a standard library

Suppose you have functions you use a lot and want to have them all in
one place. You can make a file with these in it, and use "execfile(f)"
to include those functions. This can also be on a website, so that you
can share code with colleagues. For example:

```
f= getFile( '`<http://www-pw.physics.uiowa.edu/~jbf/autoplot/myfunctions.jy>`',monitor)
execfile( f.toString() ) 
```
  
```
print mytotal( dataset([12,14]) ) 
```

Will bring in the mytotal function from
<http://www-pw.physics.uiowa.edu/~jbf/autoplot/myfunctions.jy>.

# Importing Jars

Java .jar files can be imported at runtime, as long as Webstart is
\*not\* used. Webstart's security will not allow this, and the error
feedback is poor.

```
import sys
addToSearchPath( sys.path, jarurl, monitor )
```

where jarurl is a URL like
<http://www-us.apache.org/dist//commons/math/binaries/commons-math3-3.6.1-bin.zip/commons-math3-3.6.1/commons-math3-3.6.1.jar>

# Missing Functions

Functions that should exist but don't appear here and in the sourceforge
bug ticket: <https://sourceforge.net/p/autoplot/bugs/1569/>

