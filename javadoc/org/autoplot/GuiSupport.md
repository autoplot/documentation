# org.autoplot.GuiSupport

Extra methods to support AutoplotUI.

# GuiSupport( org.autoplot.AutoplotUI parent )


***
<a name="createCloneApplicationAction"></a>
# createCloneApplicationAction
createCloneApplicationAction(  ) &rarr; Action



### Returns:
javax.swing.Action


<a href="https://github.com/autoplot/dev/search?q=createCloneApplicationAction&unscoped_q=createCloneApplicationAction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createEZAccessMenu"></a>
# createEZAccessMenu
createEZAccessMenu( org.autoplot.dom.Plot plot ) &rarr; JMenu



### Parameters:
plot - a Plot

### Returns:
javax.swing.JMenu


<a href="https://github.com/autoplot/dev/search?q=createEZAccessMenu&unscoped_q=createEZAccessMenu">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createExamplesPopup"></a>
# createExamplesPopup
createExamplesPopup( javax.swing.JTextField tf, java.lang.String[] labels, java.lang.String[] tooltips ) &rarr; MouseAdapter

legacy code for adding examples to a text field.

### Parameters:
tf - a JTextField
<br>labels - a java.lang.String[]
<br>tooltips - a java.lang.String[]

### Returns:
a java.awt.event.MouseAdapter


<a href="https://github.com/autoplot/dev/search?q=createExamplesPopup&unscoped_q=createExamplesPopup">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createNewApplicationAction"></a>
# createNewApplicationAction
createNewApplicationAction(  ) &rarr; Action



### Returns:
javax.swing.Action


<a href="https://github.com/autoplot/dev/search?q=createNewApplicationAction&unscoped_q=createNewApplicationAction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createNewDOMAction"></a>
# createNewDOMAction
createNewDOMAction(  ) &rarr; Action



### Returns:
javax.swing.Action


<a href="https://github.com/autoplot/dev/search?q=createNewDOMAction&unscoped_q=createNewDOMAction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="doCopyDataSetImage"></a>
# doCopyDataSetImage
doCopyDataSetImage(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=doCopyDataSetImage&unscoped_q=doCopyDataSetImage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="doCopyDataSetURL"></a>
# doCopyDataSetURL
doCopyDataSetURL(  ) &rarr; void

copy the current URI to the system clipboard.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=doCopyDataSetURL&unscoped_q=doCopyDataSetURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="doPasteClipboardPlotElementsIntoPlot"></a>
# doPasteClipboardPlotElementsIntoPlot
doPasteClipboardPlotElementsIntoPlot( Object client, org.autoplot.dom.ApplicationController controller, org.autoplot.dom.Application state, org.autoplot.dom.PlotElement[] pes, boolean[] selected, org.autoplot.dom.Plot targetPlot ) &rarr; void

do not use, this is introduced for testing.

### Parameters:
client - just used as lock object
<br>controller - the drop target's controller.
<br>state - the DOM we are merging in.
<br>pes - the plotElements from state.
<br>selected - a boolean[]
<br>targetPlot - a Plot

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=doPasteClipboardPlotElementsIntoPlot&unscoped_q=doPasteClipboardPlotElementsIntoPlot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="doPasteDataSetURL"></a>
# doPasteDataSetURL
doPasteDataSetURL(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=doPasteDataSetURL&unscoped_q=doPasteDataSetURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="editPlotElement"></a>
# editPlotElement
editPlotElement( org.autoplot.ApplicationModel applicationModel, java.awt.Component parent ) &rarr; void



### Parameters:
applicationModel - an ApplicationModel
<br>parent - a Component

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=editPlotElement&unscoped_q=editPlotElement">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFileNameExtensionFilter"></a>
# getFileNameExtensionFilter
getFileNameExtensionFilter( String description, String ext ) &rarr; FileFilter

get simple filter based on extension for use with JFileChooser.

### Parameters:
description - descriptions, like "png image file"
<br>ext - file extension, like ".png"

### Returns:
the FileFilter

<a href="https://github.com/autoplot/dev/search?q=getFileNameExtensionFilter&unscoped_q=getFileNameExtensionFilter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFrameForComponent"></a>
# getFrameForComponent
getFrameForComponent( java.awt.Component parent ) &rarr; Frame

attempt to get the Frame for the component, which may already be a Frame.

### Parameters:
parent - a Component

### Returns:
a java.awt.Frame


<a href="https://github.com/autoplot/dev/search?q=getFrameForComponent&unscoped_q=getFrameForComponent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPrintAction"></a>
# getPrintAction
getPrintAction( org.autoplot.dom.Application app, java.awt.Component parent, String ext ) &rarr; Action

return an action which will send the canvas to the printer.

### Parameters:
app - app containing the canvas
<br>parent - the focus dialog
<br>ext - extention like "svg" or "pdf" or "png"

### Returns:
a javax.swing.Action


<a href="https://github.com/autoplot/dev/search?q=getPrintAction&unscoped_q=getPrintAction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getStylePanel"></a>
# getStylePanel
getStylePanel( org.autoplot.RenderType renderType ) &rarr; StylePanel

return a GUI controller for the RenderType.

### Parameters:
renderType - the render type, such as RenderType.colorScatter

### Returns:
the GUI controller.

<a href="https://github.com/autoplot/dev/search?q=getStylePanel&unscoped_q=getStylePanel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="importBookmarks"></a>
# importBookmarks
importBookmarks( String bookmarksFile ) &rarr; void

Maybe import the bookmarks in response to the "bookmarks:..." URI.

### Parameters:
bookmarksFile - URL which refers to a local, HTTP, HTTPS, or FTP resource.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=importBookmarks&unscoped_q=importBookmarks">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="pasteClipboardIntoPlot"></a>
# pasteClipboardIntoPlot
pasteClipboardIntoPlot( java.awt.Component app, org.autoplot.dom.ApplicationController controller, org.autoplot.dom.Plot newP ) &rarr; void

replace the plot with the plot stored in the clipboard.  This plot
 in the clipboard is simply a one-plot .vap file.

### Parameters:
app - component parent for dialogs.
<br>controller - the application controller where we
<br>newP - the plotElements are added to this plot

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=pasteClipboardIntoPlot&unscoped_q=pasteClipboardIntoPlot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="pasteClipboardPlotElementsIntoPlot"></a>
# pasteClipboardPlotElementsIntoPlot
pasteClipboardPlotElementsIntoPlot( java.awt.Component app, org.autoplot.dom.ApplicationController controller, org.autoplot.dom.Plot targetPlot ) &rarr; void

allow plot elements from the clipboard single-plot .vap into the target plot.
 This will just insert new plot elements which point at the same data source.
 This was added to make it easier to add reference lines (Fce, Fuh) to
 spectrograms of each B-field component.

### Parameters:
app - component parent for dialogs.
<br>controller - the application controller where we
<br>targetPlot - the plotElements are added to this plot

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=pasteClipboardPlotElementsIntoPlot&unscoped_q=pasteClipboardPlotElementsIntoPlot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="pickFont"></a>
# pickFont
pickFont( java.awt.Frame parent, org.autoplot.ApplicationModel app ) &rarr; Font

show the pick font dialog.  The font chosen, is applied and returned, or null if cancel was pressed.

### Parameters:
parent - dialog parent.
<br>app - the applicationModel with canvas.

### Returns:
a java.awt.Font


<a href="https://github.com/autoplot/dev/search?q=pickFont&unscoped_q=pickFont">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="raiseApplicationWindow"></a>
# raiseApplicationWindow
raiseApplicationWindow( java.awt.Frame frame ) &rarr; void

raise the application window
 http://stackoverflow.com/questions/309023/howto-bring-a-java-window-to-the-front
 This is not working for me on Ubuntu 10.04.

### Parameters:
frame - a Frame

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=raiseApplicationWindow&unscoped_q=raiseApplicationWindow">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setClipboard"></a>
# setClipboard
setClipboard( String s ) &rarr; void

set the system clipboard (cut-n-paste mouse buffer).

### Parameters:
s - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setClipboard&unscoped_q=setClipboard">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFont"></a>
# setFont
setFont( org.autoplot.ApplicationModel app, java.awt.Font nf ) &rarr; Font

encapsulates the goofy logic about setting the font.

### Parameters:
app - an ApplicationModel
<br>nf - a Font

### Returns:
the Font actually used.

<a href="https://github.com/autoplot/dev/search?q=setFont&unscoped_q=setFont">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

