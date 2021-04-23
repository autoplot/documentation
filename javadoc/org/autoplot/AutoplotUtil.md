# org.autoplot.AutoplotUtilUtility functions for Autoplot and other related applications. Note this
 has no reference to the specific app AutoplotUI, because this is also used
 in the applet which doesn't use AutoplotUI.
AutoplotUtil( )


***
<a name="SERIES_SIZE_LIMIT"></a>
# SERIES_SIZE_LIMIT



***
<a name="DS_LENGTH_LIMIT"></a>
# DS_LENGTH_LIMIT

absolute length limit for plots.  This is used to limit the elements used in autoranging, etc.

***
<a name="is32bit"></a>
# is32bit



***
<a name="javaVersionWarning"></a>
# javaVersionWarning



***
<a name="autoRange"></a>
# autoRange
autoRange( QDataSet hist, QDataSet ds, java.util.Map properties ) &rarr; AutoRangeDescriptor

this is a copy of the other autorange, lacking some of its hacks.  TODO: why?
 This is not used.

### Parameters:
hist - a QDataSet
<br>ds - a QDataSet
<br>properties - a java.util.Map

### Returns:
an org.autoplot.AutoRangeUtil.AutoRangeDescriptor

### See Also:
<a href='#autoRange'>autoRange(QDataSet, java.util.Map, boolean)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=autoRange&unscoped_q=autoRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

autoRange( QDataSet ds, java.util.Map properties ) &rarr; AutoRangeDescriptor<br>
autoRange( QDataSet ds, java.util.Map properties, boolean ignoreDsProps ) &rarr; AutoRangeDescriptor<br>
***
<a name="bounds"></a>
# bounds
bounds( QDataSet dataSet, org.autoplot.RenderType renderType ) &rarr; QDataSet

return the bounding qube for the given render type.  This was stolen from Test022.

### Parameters:
dataSet - a QDataSet
<br>renderType - a RenderType

### Returns:
bounding cube[3,2]

<a href="https://github.com/autoplot/dev/search?q=bounds&unscoped_q=bounds">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="cancelIcon"></a>
# cancelIcon
cancelIcon(  ) &rarr; Icon



### Returns:
javax.swing.Icon


<a href="https://github.com/autoplot/dev/search?q=cancelIcon&unscoped_q=cancelIcon">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createImage"></a>
# createImage
createImage( QDataSet ds, int width, int height ) &rarr; BufferedImage

experiment to see if we can get an image of a dataset.  
 This must be called from off of the event thread.

### Parameters:
ds - a QDataSet
<br>width - an int
<br>height - an int

### Returns:
the image
 TODO: test me!

<a href="https://github.com/autoplot/dev/search?q=createImage&unscoped_q=createImage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createPlot"></a>
# createPlot
createPlot( org.das2.graph.DasCanvas c, QDataSet ds, org.das2.graph.DasPlot recyclable, org.das2.graph.DasColorBar cb ) &rarr; DasPlot

Create a dasPlot that can be useful to scripts.

### Parameters:
c - the canvas for the plot, or null.
<br>ds - the dataset
<br>recyclable - the recyclable dasPlot, or null.
<br>cb - the colorbar, or null.

### Returns:
the DasPlot.

<a href="https://github.com/autoplot/dev/search?q=createPlot&unscoped_q=createPlot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="disableCertificates"></a>
# disableCertificates
disableCertificates(  ) &rarr; void

disable certificate checking.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=disableCertificates&unscoped_q=disableCertificates">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="extractProperties"></a>
# extractProperties
extractProperties( QDataSet ds ) &rarr; Map

extract the properties from the dataset into the same format as metadata model returns.

### Parameters:
ds - a QDataSet

### Returns:
a java.util.Map


<a href="https://github.com/autoplot/dev/search?q=extractProperties&unscoped_q=extractProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="formatDevicePosition"></a>
# formatDevicePosition
formatDevicePosition( org.das2.graph.DasDevicePosition pos ) &rarr; String



### Parameters:
pos - a DasDevicePosition

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=formatDevicePosition&unscoped_q=formatDevicePosition">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getAboutAutoplotHtml"></a>
# getAboutAutoplotHtml
getAboutAutoplotHtml( org.autoplot.ApplicationModel model ) &rarr; String

return an HTML page showing the current system environment.

### Parameters:
model - an ApplicationModel

### Returns:
string containing HTML

<a href="https://github.com/autoplot/dev/search?q=getAboutAutoplotHtml&unscoped_q=getAboutAutoplotHtml">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getAutoplotIcon"></a>
# getAutoplotIcon
getAutoplotIcon(  ) &rarr; Image

return 64x64 pixel Autoplot Icon.

### Returns:
a java.awt.Image


<a href="https://github.com/autoplot/dev/search?q=getAutoplotIcon&unscoped_q=getAutoplotIcon">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNoIcon"></a>
# getNoIcon
getNoIcon(  ) &rarr; Image



### Returns:
java.awt.Image


<a href="https://github.com/autoplot/dev/search?q=getNoIcon&unscoped_q=getNoIcon">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getProcessId"></a>
# getProcessId
getProcessId( String fallback ) &rarr; String

return the processID (pid), or the fallback if the pid cannot be found.

### Parameters:
fallback - the string (null is okay) to return when the pid cannot be found.

### Returns:
the process id or the fallback provided by the caller.
 //TODO: Java9 has method for accessing process ID.

<a href="https://github.com/autoplot/dev/search?q=getProcessId&unscoped_q=getProcessId">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getProperty"></a>
# getProperty
getProperty( String name, String deft ) &rarr; String

support restricted security environment by checking permissions before 
 checking property.

### Parameters:
name - a String
<br>deft - a String

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getProperty&unscoped_q=getProperty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getUrls"></a>
# getUrls
getUrls( java.util.List recent ) &rarr; List



### Parameters:
recent - a java.util.List

### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=getUrls&unscoped_q=getUrls">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="guessRenderType"></a>
# guessRenderType
guessRenderType( QDataSet fillds ) &rarr; RenderType



### Parameters:
fillds - a QDataSet

### Returns:
an org.autoplot.RenderType

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/autoplot/datasource/DataSourceUtil.md#guessRenderType'>org.autoplot.datasource.DataSourceUtil#guessRenderType(QDataSet)</a> <br>
<a href='http://autoplot.org/developer.guessRenderType'>http://autoplot.org/developer.guessRenderType</a> <br>

<a href="https://github.com/autoplot/dev/search?q=guessRenderType&unscoped_q=guessRenderType">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isParsableDouble"></a>
# isParsableDouble
isParsableDouble( String myString ) &rarr; boolean

The Double.parseDouble contains this javadoc describing how to test for a valid double.

### Parameters:
myString - a String

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isParsableDouble&unscoped_q=isParsableDouble">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="maybeCreateRenderer"></a>
# maybeCreateRenderer
maybeCreateRenderer( org.autoplot.RenderType renderType, org.das2.graph.Renderer recyclable, org.das2.graph.DasColorBar colorbar, boolean justRenderType ) &rarr; Renderer

return a renderer that is configured for this renderType.

### Parameters:
renderType - a RenderType
<br>recyclable - a Renderer
<br>colorbar - a DasColorBar
<br>justRenderType - if true, then just set the render type, other code will configure it.
    If true, presumably bindings will set the state.

### Returns:
an org.das2.graph.Renderer


<a href="https://github.com/autoplot/dev/search?q=maybeCreateRenderer&unscoped_q=maybeCreateRenderer">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="maybeInitializeEditorColors"></a>
# maybeInitializeEditorColors
maybeInitializeEditorColors(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=maybeInitializeEditorColors&unscoped_q=maybeInitializeEditorColors">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="maybeLoadSystemProperties"></a>
# maybeLoadSystemProperties
maybeLoadSystemProperties(  ) &rarr; void

check to see if the user has the file HOME/autoplot_data/system.properties, which
 if found will cause System.setProperty for each one.  This was introduced
 to facilitate Craig with his testing of enableReferenceCache=true, and should
 make it easier to provide generic extensions.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=maybeLoadSystemProperties&unscoped_q=maybeLoadSystemProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mergeProperties"></a>
# mergeProperties
mergeProperties( java.util.Map properties, java.util.Map deflt ) &rarr; Map

combine the two properties trees, using values from the first when both contain the same property.

### Parameters:
properties - a java.util.Map
<br>deflt - a java.util.Map

### Returns:
a java.util.Map


<a href="https://github.com/autoplot/dev/search?q=mergeProperties&unscoped_q=mergeProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="openBrowser"></a>
# openBrowser
openBrowser( String url ) &rarr; void

open the URL in a browser.   Borrowed from http://www.centerkey.com/java/browser/.

### Parameters:
url - the URL.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=openBrowser&unscoped_q=openBrowser">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readDoc"></a>
# readDoc
readDoc( java.io.InputStream is ) &rarr; Document



### Parameters:
is - an InputStream

### Returns:
org.w3c.dom.Document


<a href="https://github.com/autoplot/dev/search?q=readDoc&unscoped_q=readDoc">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reloadAll"></a>
# reloadAll
reloadAll( org.autoplot.dom.Application dom ) &rarr; void

reload all the data.  This should not be called on the event thread.

### Parameters:
dom - an Application

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reloadAll&unscoped_q=reloadAll">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="replaceFile"></a>
# replaceFile
replaceFile( java.awt.Component parent, org.autoplot.dom.Application dom ) &rarr; void

Replace filename references within the DOM, and reset xrange.  This was 
 the often-used ReplaceFile script.  This now follows focus.

### Parameters:
parent - focus for response dialogs.
<br>dom - the application

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=replaceFile&unscoped_q=replaceFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resetZoomX"></a>
# resetZoomX
resetZoomX( org.autoplot.dom.Application dom ) &rarr; boolean



### Parameters:
dom - an Application

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=resetZoomX&unscoped_q=resetZoomX">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

resetZoomX( org.autoplot.dom.Application dom, org.autoplot.dom.Plot plot ) &rarr; boolean<br>
***
<a name="resetZoomY"></a>
# resetZoomY
resetZoomY( org.autoplot.dom.Application dom ) &rarr; boolean



### Parameters:
dom - an Application

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=resetZoomY&unscoped_q=resetZoomY">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

resetZoomY( org.autoplot.dom.Application dom, org.autoplot.dom.Plot plot ) &rarr; boolean<br>
***
<a name="resetZoomZ"></a>
# resetZoomZ
resetZoomZ( org.autoplot.dom.Application dom ) &rarr; boolean



### Parameters:
dom - an Application

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=resetZoomZ&unscoped_q=resetZoomZ">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

resetZoomZ( org.autoplot.dom.Application dom, org.autoplot.dom.Plot plot ) &rarr; boolean<br>
***
<a name="scaleIcon"></a>
# scaleIcon
scaleIcon( javax.swing.ImageIcon icon, int w, int h ) &rarr; ImageIcon

create a new Icon that is a scaled instance of the first.  The image
 should be a BufferedImage.

### Parameters:
icon - an ImageIcon
<br>w - an int
<br>h - an int

### Returns:
a javax.swing.ImageIcon


<a href="https://github.com/autoplot/dev/search?q=scaleIcon&unscoped_q=scaleIcon">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="scaleImage"></a>
# scaleImage
scaleImage( java.awt.image.BufferedImage image, int w, int h ) &rarr; BufferedImage



### Parameters:
image - a BufferedImage
<br>w - an int
<br>h - an int

### Returns:
java.awt.image.BufferedImage


<a href="https://github.com/autoplot/dev/search?q=scaleImage&unscoped_q=scaleImage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDevicePosition"></a>
# setDevicePosition
setDevicePosition( org.das2.graph.DasDevicePosition row, String spec ) &rarr; void

set the device position, using spec string like "+5em,80%-5em"

### Parameters:
row - the row/column to modify
<br>spec - the spec

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDevicePosition&unscoped_q=setDevicePosition">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showConfirmDialog"></a>
# showConfirmDialog
showConfirmDialog( java.awt.Component parentComponent, Object message, String title, int optionType ) &rarr; int

Wrapper for displaying ok,cancel dialogs.  
 If the message is a component, then the dialog will be resizeable.

### Parameters:
parentComponent - determines the Frame in which the dialog is displayed; if null, or if the parentComponent has no Frame, a default Frame is used
<br>message - the String or GUI component to display
<br>title - the title string for the dialog
<br>optionType - an int designating the options available on the dialog: YES_NO_OPTION, YES_NO_CANCEL_OPTION, or OK_CANCEL_OPTION

### Returns:
JOptionPane.OK_OPTION, JOptionPane.CANCEL_OPTION, etc.

<a href="https://github.com/autoplot/dev/search?q=showConfirmDialog&unscoped_q=showConfirmDialog">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showConfirmDialog2"></a>
# showConfirmDialog2
showConfirmDialog2( java.awt.Component parent, Object omessage, String title, int optionType ) &rarr; int

new okay/cancel dialog that is resizable and is made with a simple dialog.

### Parameters:
parent - a Component
<br>omessage - String or Component.
<br>title - a String
<br>optionType - an int

### Returns:
JOptionPane.OK_OPTION, JOptionPane.CANCEL_OPTION.

<a href="https://github.com/autoplot/dev/search?q=showConfirmDialog2&unscoped_q=showConfirmDialog2">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showMessageDialog"></a>
# showMessageDialog
showMessageDialog( java.awt.Component parentComponent, Object message, String title, int messageType ) &rarr; void

wrapper for displaying messages.  This will eventually use the Autoplot icon, etc.
 This should be called, not JOptionPane.showMessageDialog(...)

### Parameters:
parentComponent - a Component
<br>message - an Object
<br>title - a String
<br>messageType - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showMessageDialog&unscoped_q=showMessageDialog">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showUserExceptionDialog"></a>
# showUserExceptionDialog
showUserExceptionDialog( java.awt.Component parent, String string, java.lang.Exception ex, org.das2.util.ExceptionHandler exh ) &rarr; void

put in a place to call where the message is shown assuming the 
 problem is on the user's end, but provide a button to inspect
 the exception.

### Parameters:
parent - parent component to center the dialog.
<br>string - the message, a string or html code.
<br>ex - the wrapped exception
<br>exh - an exception handler to show the exception.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showUserExceptionDialog&unscoped_q=showUserExceptionDialog">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toDataSet"></a>
# toDataSet
toDataSet( org.autoplot.AutoRangeUtil.AutoRangeDescriptor ard ) &rarr; QDataSet

convert the legacy AutoRangeDescriptor to a QDataSet bounding cube.
 The bounding cube is a rank 1, 2-element dataset with min and max as the
 elements, and SCALE_TYPE="log" if the AutoRangeDescriptor log property was
 true.

### Parameters:
ard - AutoRangeDescriptor.

### Returns:
a rank 1 bounding cube.

<a href="https://github.com/autoplot/dev/search?q=toDataSet&unscoped_q=toDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

