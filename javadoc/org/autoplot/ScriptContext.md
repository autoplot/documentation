# org.autoplot.ScriptContext

ScriptContext provides the API to perform abstract functions with 
 the application.  For example, 
 
<blockquote><pre><small>{@code
 ScriptContext.load('http://autoplot.org/data/somedata.dat')
 ScriptContext.writeToPdf('/tmp/foo.pdf')
}</small></pre></blockquote>

# ScriptContext( )


***
<a name="_setOutputStream"></a>
# _setOutputStream
_setOutputStream( java.io.OutputStream out ) &rarr; void

resets the output stream.  This method is used internally, do not use
 this routine.

### Parameters:
out - an OutputStream

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=_setOutputStream&unscoped_q=_setOutputStream">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addBottomDecoration"></a>
# addBottomDecoration
addBottomDecoration( org.autoplot.dom.DomNode node, PyFunction painter ) &rarr; void

add code that will paint custom graphics on the canvas or on a plot.
 The command will be invoked after all other painting is done, making
 the decoration to be on top.  Note plots can only have one decoration,
 and the Canvas can have any number.  Calling reset() will remove all
 decorations.
<blockquote><pre><small>
def paint(g):
    g.color= Color.BLUE
    for i in xrange(0,1000,100):
        g.drawOval(500-i/2,500-i/2,i,i)

addBottomDecoration( dom.canvases[0], paint )
</small></pre></blockquote>

### Parameters:
node - the plot or canvas over which to plot
<br>painter - the PyFunction to call when painting

### Returns:
void (returns nothing)

### See Also:
<a href='https://github.com/autoplot/dev/blob/master/demos/2020/20200229/demoAddBottomDecoration.jy'>https://github.com/autoplot/dev/blob/master/demos/2020/20200229/demoAddBottomDecoration.jy</a> <br>

<a href="https://github.com/autoplot/dev/search?q=addBottomDecoration&unscoped_q=addBottomDecoration">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addMouseModule"></a>
# addMouseModule
addMouseModule( org.autoplot.dom.Plot plot, String label, PyFunction listener ) &rarr; MouseModule

add code that will respond to mouse events.  This will receive an 
 event following the mouse release when a box is dragged out.
<blockquote><pre><small>
def boxLookup( evt ):
    showMessageDialog( "<html>start: (%s,%s)<br>finish: (%s,%s)" %
        ( evt.getStartX(), evt.getStartY(), 
        evt.getFinishX(), evt.getFinishY() ) )
  
addMouseModule( dom.plots[0], 'Box Lookup', boxLookup )   
</small></pre></blockquote>

### Parameters:
plot - the plot which will receive the events.
<br>label - a label for the mouse module.
<br>listener - the PyFunction to call with new events.

### Returns:
the mouse module.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/event/MouseModule.md#setDragRenderer'>org.das2.event.MouseModule#setDragRenderer(org.das2.event.DragRenderer)</a> setDragRenderer to see how to set how feedback can be provided.<br>
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/event/BoxSelectionEvent BoxSelectionEvent for the methods of the event/.md'>org.das2.event.BoxSelectionEvent BoxSelectionEvent for the methods of the event.</a> BoxSelectionEvent for the methods of the event.<br>

<a href="https://github.com/autoplot/dev/search?q=addMouseModule&unscoped_q=addMouseModule">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addPlotElement"></a>
# addPlotElement
addPlotElement( int chNum ) &rarr; int

"overplot" by adding another PlotElement to the plot and setting the data to this PlotElement.

### Parameters:
chNum - the focus

### Returns:
the channel number for the new plot element.
### See Also:
<a href='#setLayout'>setLayout(int, int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=addPlotElement&unscoped_q=addPlotElement">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addPlots"></a>
# addPlots
addPlots( int nrows, int ncolumns, String dir ) &rarr; List

adds a block of plots to the canvas below the focus plot. 
 A plotElement is added for each plot as well.

### Parameters:
nrows - number of rows
<br>ncolumns - number of columns
<br>dir - below or above, or null (None in Jython) to replace the current plot.

### Returns:
the new plots.

<a href="https://github.com/autoplot/dev/search?q=addPlots&unscoped_q=addPlots">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addTab"></a>
# addTab
addTab( String label, javax.swing.JComponent c ) &rarr; void

add a tab to the running application.  A new tab will be added with the
 label, with the component added within a scroll pane.

### Parameters:
label - the label for the component.
<br>c - the component to add.

### Returns:
void (returns nothing)

### See Also:
<a href='AutoplotUI.md#setLeftPanel'>AutoplotUI#setLeftPanel(javax.swing.JComponent)</a> setLeftPanel which adds to the GUI<br>

<a href="https://github.com/autoplot/dev/search?q=addTab&unscoped_q=addTab">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addTopDecoration"></a>
# addTopDecoration
addTopDecoration( org.autoplot.dom.DomNode node, PyFunction painter ) &rarr; void

add code that will paint custom graphics on the canvas or on a plot.
 The command will be invoked after all other painting is done, making
 the decoration to be on top.  Note plots can only have one decoration,
 and the Canvas can have any number.  Calling reset() will remove all
 decorations.
<blockquote><pre><small>
def paint(g):
    for i in xrange(0,1000,100):
        g.drawOval(500-i/2,500-i/2,i,i)

addTopDecoration( dom.canvases[0], paint )
</small></pre></blockquote>

### Parameters:
node - the plot or canvas over which to plot
<br>painter - the PyFunction to call when painting

### Returns:
void (returns nothing)

### See Also:
<a href='https://github.com/autoplot/dev/blob/master/demos/2020/20200229/demoAddBottomDecoration.jy'>https://github.com/autoplot/dev/blob/master/demos/2020/20200229/demoAddBottomDecoration.jy</a> <br>

<a href="https://github.com/autoplot/dev/search?q=addTopDecoration&unscoped_q=addTopDecoration">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="alert"></a>
# alert
alert( String message ) &rarr; void

show a popup that you know the user will see.  Note HTML code will work.

### Parameters:
message - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=alert&unscoped_q=alert">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bind"></a>
# bind
bind( Object src, String srcProp, Object dst, String dstProp ) &rarr; void

binds two bean properties together.  Bindings are bidirectional, but
 the initial copy is from src to dst.  In MVC terms, src should be the model
 and dst should be a view.  The properties must fire property
 change events for the binding mechanism to work.
 
 As of v2014a_10, if the src is a DomNode and a child of the application, then use
 dom.getController().bind so that the vap will contain the binding.
 
 Example:
<blockquote><pre><small>
 model= getApplicationModel()
 bind( model.getPlotDefaults(), "title", model.getPlotDefaults().getXAxis(), "label" )
</small></pre></blockquote>

### Parameters:
src - java bean such as model.getPlotDefaults()
<br>srcProp - a property name such as "title"
<br>dst - java bean such as model.getPlotDefaults().getXAxis()
<br>dstProp - a property name such as "label"

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/autoplot/dom/ApplicationController.md#bind'>org.autoplot.dom.ApplicationController#bind(org.autoplot.dom.DomNode, java.lang.String, java.lang.Object, java.lang.String)</a> which will save the binding to a vap.<br>

<a href="https://github.com/autoplot/dev/search?q=bind&unscoped_q=bind">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

bind( Object src, String srcProp, Object dst, String dstProp, Converter c ) &rarr; void<br>
***
<a name="bindGuiSafe"></a>
# bindGuiSafe
bindGuiSafe( Object src, String srcProp, Object dst, String dstProp, Converter c ) &rarr; void

binds two bean properties together.  Bindings are bidirectional, but
 the initial copy is from src to dst.  In MVC terms, src should be the model
 and dst should be a view.  The properties must fire property
 change events for the binding mechanism to work.
 
 As of v2014a_10, if the src is a DomNode and a child of the application, then use
 dom.getController().bind so that the vap will contain the binding.
 
 Example:
<blockquote><pre><small>
 model= getApplicationModel()
 bind( model.getPlotDefaults(), "title", model.getPlotDefaults().getXAxis(), "label" )
</small></pre></blockquote>

### Parameters:
src - java bean such as model.getPlotDefaults()
<br>srcProp - a property name such as "title"
<br>dst - java bean such as model.getPlotDefaults().getXAxis()
<br>dstProp - a property name such as "label"
<br>c - converter for the binding, or null.

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/autoplot/dom/ApplicationController.md#bind'>org.autoplot.dom.ApplicationController#bind(org.autoplot.dom.DomNode, java.lang.String, java.lang.Object, java.lang.String, org.jdesktop.beansbinding.Converter)</a> which will save the binding to a vap.<br>

<a href="https://github.com/autoplot/dev/search?q=bindGuiSafe&unscoped_q=bindGuiSafe">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createGui"></a>
# createGui
createGui(  ) &rarr; void

create a model with a GUI presentation layer.  If the GUI is already 
 created, then this does nothing.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=createGui&unscoped_q=createGui">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="dumpToDas2Stream"></a>
# dumpToDas2Stream
dumpToDas2Stream( QDataSet ds, boolean ascii ) &rarr; void

serializes the dataset to a das2stream, a well-documented, open, streaming
 data format. (that's a joke.)  Das2Streams are the legacy stream format used
 by the Plasma Wave Groups's server, and can serialize a limited set of
 QDataSets.  QStreams were introduced to allow streaming of any QDataSet, see
 dumpToQStream.
 Currently, to keep the channel open, the stream is created in a buffer and 
 then the buffer is sent.
 TODO: write a stream-producing code that doesn't close the output stream.  (TODO: does it still do this?)

### Parameters:
ds - a QDataSet
<br>ascii - use ascii transfer types, otherwise binary are used.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dumpToDas2Stream&unscoped_q=dumpToDas2Stream">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

dumpToDas2Stream( QDataSet ds, String file, boolean ascii ) &rarr; void<br>
***
<a name="dumpToQStream"></a>
# dumpToQStream
dumpToQStream( QDataSet ds, java.io.OutputStream out, boolean ascii ) &rarr; void

serializes the dataset to a QStream, a self-documenting, streaming format
 useful for moving datasets.

 <p><blockquote><pre>
ds= getDataSet('http://autoplot.org/data/somedata.cdf?BGSEc')
from java.lang import System
dumpToQStream( ds, System.out, True )
 </pre></blockquote></p>

### Parameters:
ds - The dataset to stream.  Note all schemes should be streamable, but
   some bugs exist that may prevent this.
<br>out - stream, such as "System.out"
<br>ascii - use ascii transfer types, otherwise binary are used.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dumpToQStream&unscoped_q=dumpToQStream">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="fixLayout"></a>
# fixLayout
fixLayout(  ) &rarr; void

make the layout more efficient by removing empty spaces and overlapping 
 plots.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=fixLayout&unscoped_q=fixLayout">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="formatDataSet"></a>
# formatDataSet
formatDataSet( QDataSet ds, String file ) &rarr; void

Export the data into a format implied by the filename extension.  
 See the export data dialog for additional parameters available for formatting.

 For example:
<blockquote><pre><small>
 ds= getDataSet('http://autoplot.org/data/somedata.cdf?BGSEc')
 formatDataSet( ds, 'vap+dat:file:/home/jbf/temp/foo.dat?tformat=minutes&format=6.2f')
</small></pre></blockquote>

### Parameters:
ds - a QDataSet
<br>file - local file name that is the target

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=formatDataSet&unscoped_q=formatDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

formatDataSet( QDataSet ds, String file, ProgressMonitor monitor ) &rarr; void<br>
***
<a name="generateTimeRanges"></a>
# generateTimeRanges
generateTimeRanges( String spec, String srange ) &rarr; String

Given a spec to format timeranges and a range to contain each timerange,
 produce a list of all timeranges covering the range formatted with the
 spec.  For example, <code>generateTimeRanges( "%Y-%m-%d", "Jun 2009" )</code> would result in
 2009-06-01, 2009-06-02, ..., 2009-06-30.

### Parameters:
spec - such as "%Y-%m".  Note specs like "%Y%m" will not be parsable.
<br>srange - range limiting the list, such as "2009"

### Returns:
a string array of formatted time ranges, such as [ "2009-01", "2009-02", ..., "2009-12" ]

<a href="https://github.com/autoplot/dev/search?q=generateTimeRanges&unscoped_q=generateTimeRanges">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getApplication"></a>
# getApplication
getApplication(  ) &rarr; AutoplotUI

return the focus application.

### Returns:
the focus application.

<a href="https://github.com/autoplot/dev/search?q=getApplication&unscoped_q=getApplication">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getApplicationModel"></a>
# getApplicationModel
getApplicationModel(  ) &rarr; ApplicationModel

returns the internal application model (the object that does all the 
 business).  This provides access to the internal model for power users.
 Note the applicationModel provides limited access, and the DOM now
 provides full access to the application.

### Returns:
ApplicationModel object

<a href="https://github.com/autoplot/dev/search?q=getApplicationModel&unscoped_q=getApplicationModel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCompletions"></a>
# getCompletions
getCompletions( String file ) &rarr; String

return a list of completions.  This is useful in the IDL context
 as well as Jython scripts.  This will perform the completion for where the carot is
 at the end of the string.  Only completions where maybePlot indicates the URI is now 
 valid are returned, so for example http://autoplot.org/data/somedata.cdf?noDep is not
 returned and http://autoplot.org/data/somedata.cdf?Magnitude is.
 Note this is included to continue support as this is described in http://autoplot.org/developer.idlMatlab.

### Parameters:
file - a String

### Returns:
list of completions, containing the entire URI.

<a href="https://github.com/autoplot/dev/search?q=getCompletions&unscoped_q=getCompletions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDocumentModel"></a>
# getDocumentModel
getDocumentModel(  ) &rarr; Application

get the document model (DOM).  This may initialize the model, in which
 case defaults like the cache directory are set.

### Returns:
an org.autoplot.dom.Application


<a href="https://github.com/autoplot/dev/search?q=getDocumentModel&unscoped_q=getDocumentModel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTimeRangesFor"></a>
# getTimeRangesFor
getTimeRangesFor( String surl, String timeRange, String format ) &rarr; String

return an array of URLs that match the spec for the time range provided.
 For example,
 <p><blockquote><pre>
  uri= 'http://cdaweb.gsfc.nasa.gov/istp_public/data/polar/hyd_h0/$Y/po_h0_hyd_$Y$m$d_v01.cdf?ELECTRON_DIFFERENTIAL_ENERGY_FLUX'
  xx= getTimeRangesFor( uri, '2000-jan', '$Y-$d-$m' )
  for x in xx:
    print x
 </pre></blockquote><p>

### Parameters:
surl - an Autoplot uri with an aggregation specifier.
<br>timeRange - a string that is parsed to a time range, such as "2001"
<br>format - format for the result, such as "%Y-%m-%d"

### Returns:
a list of URLs without the aggregation specifier.

<a href="https://github.com/autoplot/dev/search?q=getTimeRangesFor&unscoped_q=getTimeRangesFor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getViewWindow"></a>
# getViewWindow
getViewWindow(  ) &rarr; Window

return the Window for the application, to be used for dialogs.
 See createGui(), which creates the view.

### Returns:
a java.awt.Window


<a href="https://github.com/autoplot/dev/search?q=getViewWindow&unscoped_q=getViewWindow">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getWindow"></a>
# getWindow
getWindow(  ) &rarr; ApplicationModel

return the internal handle for the window and dom within.

### Returns:
the internal handle for the application.

<a href="https://github.com/autoplot/dev/search?q=getWindow&unscoped_q=getWindow">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isModelInitialized"></a>
# isModelInitialized
isModelInitialized(  ) &rarr; boolean

provide way to see if the model is already initialized (e.g. for clone application)

### Returns:
true is the model is already initialized.

<a href="https://github.com/autoplot/dev/search?q=isModelInitialized&unscoped_q=isModelInitialized">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="load"></a>
# load
load( String filename ) &rarr; void

load the .vap file.  This is implemented by calling plot on the URI.

### Parameters:
filename - local or remote filename like http://autoplot.org/data/autoplot.vap

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=load&unscoped_q=load">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="loadVap"></a>
# loadVap
loadVap( String filename ) &rarr; Application

load a vap from a file and return the dom.

### Parameters:
filename - .vap file

### Returns:
Application
### See Also:
<a href='#saveVap'>saveVap(org.autoplot.dom.Application, java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=loadVap&unscoped_q=loadVap">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="makeColorTable"></a>
# makeColorTable
makeColorTable( String name, QDataSet index, QDataSet rgb ) &rarr; Type

returns a color table 
 using QDataSets as inputs to make it easier to use in scripts.

### Parameters:
name - the name for the colortable
<br>index - control points for the colors, or None
<br>rgb - dataset of ds[N,3] where N is the number of colors

### Returns:
object representing the color table.
### See Also:
<a href='rgbColorDataset.md'>rgbColorDataset</a> <br>

<a href="https://github.com/autoplot/dev/search?q=makeColorTable&unscoped_q=makeColorTable">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mkdir"></a>
# mkdir
mkdir( String dir ) &rarr; void

make the directory.  This must be a local file right now, but may start with "file://"

### Parameters:
dir - the directory

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mkdir&unscoped_q=mkdir">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="newApplication"></a>
# newApplication
newApplication( String id ) &rarr; AutoplotUI

get or create the application identified by the name.  For example:
<blockquote><pre>
ds= ripples(20,20)
plot( 0, ds )
sliceWindow= newApplication('slice')
setApplication(sliceWindow)
plot( slice0(ds,0) ) 
 </pre></blockquote>
 Windows with this name will be reused.

### Parameters:
id - an identifier

### Returns:
the AutoplotUI.

<a href="https://github.com/autoplot/dev/search?q=newApplication&unscoped_q=newApplication">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="newDialogWindow"></a>
# newDialogWindow
newDialogWindow( java.awt.Window parent, String title ) &rarr; ApplicationModel

return a new Autoplot.

### Parameters:
parent - a Window
<br>title - a String

### Returns:
an org.autoplot.ApplicationModel


<a href="https://github.com/autoplot/dev/search?q=newDialogWindow&unscoped_q=newDialogWindow">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="newWindow"></a>
# newWindow
newWindow( String id, int width, int height, int x, int y ) &rarr; ApplicationModel

create a new window with the given location and size.

### Parameters:
id - identifier for the window
<br>width - the canvas width
<br>height - the canvas height
<br>x - the window upper-left location, if possible
<br>y - the window upper-left location, if possible

### Returns:
a handle (do not use this object, code will break) for the window.
### See Also:
<a href='#setWindow'>setWindow(org.autoplot.ApplicationModel)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=newWindow&unscoped_q=newWindow">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

newWindow( String id ) &rarr; ApplicationModel<br>
***
<a name="peekAt"></a>
# peekAt
peekAt( Object o ) &rarr; void

This is intended to be used with a debugger.  The developer should put
 a breakpoint at the out.write statement, and then call peekAt from
 the script.

### Parameters:
o - any object we want to look at.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=peekAt&unscoped_q=peekAt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="plot"></a>
# plot
plot( String suri ) &rarr; void

bring up the autoplot with the specified URL.  Note the URI is resolved
 asynchronously, so errors thrown during the load cannot be caught here.
 See getDataSet to load data synchronously.

### Parameters:
suri - a URI or vap file

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=plot&unscoped_q=plot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

plot( String surl1, String surl2 ) &rarr; void<br>
plot( int chNum, String surl ) &rarr; void<br>
plot( int chNum, String label, String surl ) &rarr; void<br>
plot( QDataSet ds ) &rarr; void<br>
plot( QDataSet x, QDataSet y ) &rarr; void<br>
plot( QDataSet x, QDataSet y, QDataSet z ) &rarr; void<br>
plot( int chNum, QDataSet ds ) &rarr; void<br>
plot( int chNum, QDataSet x, QDataSet y ) &rarr; void<br>
plot( int chNum, QDataSet x, QDataSet y, QDataSet z ) &rarr; void<br>
plot( int chNum, String label, QDataSet ds ) &rarr; void<br>
plot( int chNum, String label, QDataSet x, QDataSet y ) &rarr; void<br>
plot( int chNum, String label, QDataSet x, QDataSet y, String renderType ) &rarr; void<br>
plot( int chNum, String label, QDataSet x, QDataSet y, String renderType, boolean reset ) &rarr; void<br>
plot( int chNum, String label, QDataSet x, QDataSet y, QDataSet z ) &rarr; void<br>
plot( int chNum, String label, QDataSet x, QDataSet y, QDataSet z, String renderType ) &rarr; void<br>
plot( int chNum, String label, QDataSet x, QDataSet y, QDataSet z, String renderType, boolean reset ) &rarr; void<br>
***
<a name="reset"></a>
# reset
reset(  ) &rarr; void

reset the application to its initial state.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reset&unscoped_q=reset">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="save"></a>
# save
save( String filename ) &rarr; void

save the current state as a vap file

### Parameters:
filename - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=save&unscoped_q=save">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="saveVap"></a>
# saveVap
saveVap( org.autoplot.dom.Application dom, String filename ) &rarr; void

save the application dom to a file.

### Parameters:
dom - the application state
<br>filename - the file.

### Returns:
void (returns nothing)

### See Also:
<a href='#loadVap'>loadVap(java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=saveVap&unscoped_q=saveVap">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setApplication"></a>
# setApplication
setApplication( org.autoplot.AutoplotUI app ) &rarr; void

set the current application for commands.  For example, to
 have two windows plotting data, you would:
 <pre>
 plot([1,2,3])
 popup=newWindow('popup')
 setWindow(popup)
 plot([3,2,1])
 </pre>

### Parameters:
app - the application

### Returns:
void (returns nothing)

### See Also:
<a href='#setWindow'>setWindow(org.autoplot.ApplicationModel)</a> <br>
<a href='#newApplication'>newApplication(java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setApplication&unscoped_q=setApplication">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setApplicationModel"></a>
# setApplicationModel
setApplicationModel( org.autoplot.ApplicationModel m ) &rarr; void

set the focus for scripts.

### Parameters:
m - the application model.

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/setWindow, which should be used instead/.md'>setWindow, which should be used instead.</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setApplicationModel&unscoped_q=setApplicationModel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setCanvasSize"></a>
# setCanvasSize
setCanvasSize( int width, int height ) &rarr; void

set the size of the canvas.  This is only used when the GUI is not used, and in
 headless mode, otherwise the GUI controls the size of the canvas.

### Parameters:
width - the width of the canvas
<br>height - the height of the canvas

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCanvasSize&unscoped_q=setCanvasSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataSourceURL"></a>
# setDataSourceURL
setDataSourceURL( String surl ) &rarr; void

set the internal model's url to surl.  The data set will be loaded,
 and writeToPng and writeToSvg can be used in headless mode.

### Parameters:
surl - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSourceURL&unscoped_q=setDataSourceURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDefaultApplication"></a>
# setDefaultApplication
setDefaultApplication(  ) &rarr; void

reset the script focus to the default application.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDefaultApplication&unscoped_q=setDefaultApplication">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLayout"></a>
# setLayout
setLayout( int nrows ) &rarr; void

make a stack plot.

### Parameters:
nrows - number of rows (plots)

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLayout&unscoped_q=setLayout">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

setLayout( int nrows, int ncolumns ) &rarr; void<br>
***
<a name="setLayoutOverplot"></a>
# setLayoutOverplot
setLayoutOverplot( int nplotElement ) &rarr; void

make a single plot with so many plot elements.

### Parameters:
nplotElement - the number of plotElements on the one plot.

### Returns:
void (returns nothing)

### See Also:
<a href='#setLayout'>setLayout(int, int)</a> setLayout(int, int) which will create a grid of plots.<br>
<a href='#addPlotElement'>addPlotElement(int)</a> addPlotElement(int) which will an another plotElement (an overplot) to the ith position.<br>

<a href="https://github.com/autoplot/dev/search?q=setLayoutOverplot&unscoped_q=setLayoutOverplot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRenderStyle"></a>
# setRenderStyle
setRenderStyle( String name ) &rarr; void

Set the style used to render the data using a string identifier:
   spectrogram, series, scatter, histogram, fill_to_zero, digital

### Parameters:
name - string name of the plot style.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRenderStyle&unscoped_q=setRenderStyle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setStatus"></a>
# setStatus
setStatus( String message ) &rarr; void

set the Autoplot status bar string.  Use the prefixes "busy:", "warning:"
 and "error:" to set icons.

### Parameters:
message - a String

### Returns:
void (returns nothing)

### See Also:
<a href='#showMessageDialog'>showMessageDialog(java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setStatus&unscoped_q=setStatus">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTitle"></a>
# setTitle
setTitle( String title ) &rarr; void

set the title of the plot.

### Parameters:
title - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTitle&unscoped_q=setTitle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setWindow"></a>
# setWindow
setWindow( org.autoplot.ApplicationModel appm ) &rarr; void

Set the application model.  This is the simplest Autoplot implementation
 existing, where there are no buttons, etc.

### Parameters:
appm - an ApplicationModel

### Returns:
void (returns nothing)

### See Also:
<a href='#newWindow'>newWindow(java.lang.String)</a> <br>
<a href='#getWindow'>getWindow()</a> which returns the current window.<br>
<a href='#setApplication'>setApplication(org.autoplot.AutoplotUI)</a> which creates another application.<br>

<a href="https://github.com/autoplot/dev/search?q=setWindow&unscoped_q=setWindow">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setWindowLocation"></a>
# setWindowLocation
setWindowLocation( int x, int y ) &rarr; void

set the window location

### Parameters:
x - the window upper-left location, if possible
<br>y - the window upper-left location, if possible

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setWindowLocation&unscoped_q=setWindowLocation">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showMessageDialog"></a>
# showMessageDialog
showMessageDialog( String message ) &rarr; void

show a popup to the scientist, which they must acknowledge before this
 returns.

### Parameters:
message - a String

### Returns:
void (returns nothing)

### See Also:
<a href='#setStatus'>setStatus(java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=showMessageDialog&unscoped_q=showMessageDialog">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="sleep"></a>
# sleep
sleep( int millis ) &rarr; void

sleep for so many milliseconds.  This is introduced to avoid the import,
 which makes running scripts securely non-trivial.

### Parameters:
millis - number of milliseconds to pause execution

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=sleep&unscoped_q=sleep">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="unbind"></a>
# unbind
unbind( org.autoplot.dom.DomNode src ) &rarr; void

unbind the property

### Parameters:
src - a DomNode

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=unbind&unscoped_q=unbind">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

unbind( org.autoplot.dom.DomNode src, String srcProp, org.autoplot.dom.DomNode dst, String dstProp ) &rarr; void<br>
***
<a name="waitUntilIdle"></a>
# waitUntilIdle
waitUntilIdle(  ) &rarr; void

wait until the application is idle.  This does a model.waitUntilIdle,
 but also checks for the DataSetSelector for pending operations.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=waitUntilIdle&unscoped_q=waitUntilIdle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

waitUntilIdle( String id ) &rarr; void<br>
***
<a name="writeToBufferedImage"></a>
# writeToBufferedImage
writeToBufferedImage( org.autoplot.dom.Application applicationIn ) &rarr; BufferedImage

creates a BufferedImage from the provided DOM.  This blocks until the
 image is ready.

### Parameters:
applicationIn - an Application

### Returns:
the image

<a href="https://github.com/autoplot/dev/search?q=writeToBufferedImage&unscoped_q=writeToBufferedImage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

writeToBufferedImage(  ) &rarr; BufferedImage<br>
***
<a name="writeToPdf"></a>
# writeToPdf
writeToPdf( String filename ) &rarr; void

write out the current canvas to a pdf file.
 TODO: this has issues with the size.  See writeToPng(filename).  It looks
   like this might be handled here
 Note for relative references, this will use the Java process present working directory (PWD) instead
 of the PWD variable found in scripts

### Parameters:
filename - the local file to write the file.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeToPdf&unscoped_q=writeToPdf">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

writeToPdf( java.io.OutputStream out ) &rarr; void<br>
***
<a name="writeToPng"></a>
# writeToPng
writeToPng( String filename ) &rarr; void

write out the current canvas to a png file.
 TODO: bug 557: this has issues with the size.  It's coded to get the size from
  the DOM, but if it is fitted and has a container it must get size from
  the container.  Use writeToPng( filename, width, height ) instead for now.
  See writeToPdf(String filename), which appears to have a fix for this that
  would affect how this is resolved.
 Note for relative references, this will use the Java process present working directory (PWD) instead
 of the PWD variable found in scripts

### Parameters:
filename - The name of a local file

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeToPng&unscoped_q=writeToPng">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

writeToPng( String filename, int width, int height ) &rarr; void<br>
writeToPng( java.awt.image.BufferedImage image, String filename, java.util.Map metadata ) &rarr; void<br>
writeToPng( java.io.OutputStream out ) &rarr; void<br>
***
<a name="writeToSvg"></a>
# writeToSvg
writeToSvg( String filename ) &rarr; void

write out the current canvas to a svg file.
 Note for relative references, this will use the Java process present working directory (PWD) instead
 of the PWD variable found in scripts

### Parameters:
filename - the local file to write the file.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeToSvg&unscoped_q=writeToSvg">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

writeToSvg( java.io.OutputStream out ) &rarr; void<br>
