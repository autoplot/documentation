# org.autoplot.pngwalk.PngWalkTool

GUI for browsing PNGWalks, or sets of PNG images.  These typically contain files named to make a time series, such as
 product_$Y$m$d.png, but this can browse any set of images using wildcards.  This provides a number of views of the
 images, such as a grid of thumbnails and the coverflow view which shows an image and the preceding and succeeding images.
 This also contains a hook to get back into Autoplot, if product.vap (or vap named like the images) is found.

# PngWalkTool( )
Creates new form PngWalkTool

***
<a name="PREF_RECENT"></a>
# PREF_RECENT



***
<a name="PREF_LAST_EXPORT"></a>
# PREF_LAST_EXPORT

last location where image was exported

***
<a name="views"></a>
# views



***
<a name="PROP_THUMBNAILSIZE"></a>
# PROP_THUMBNAILSIZE



***
<a name="PROP_TIMERANGE"></a>
# PROP_TIMERANGE



***
<a name="PROP_MOUSEPRESSLOCATION"></a>
# PROP_MOUSEPRESSLOCATION



***
<a name="PROP_MOUSERELEASELOCATION"></a>
# PROP_MOUSERELEASELOCATION



***
<a name="PROP_IMAGEMOUSEADAPTER"></a>
# PROP_IMAGEMOUSEADAPTER



***
<a name="PROP_STATUS"></a>
# PROP_STATUS



***
<a name="LOCAL_FILE_ENABLER"></a>
# LOCAL_FILE_ENABLER

Enabler that returns true for local files.

***
<a name="PROP_SELECTED_NAME"></a>
# PROP_SELECTED_NAME



***
<a name="addActionComponent"></a>
# addActionComponent
addActionComponent( javax.swing.JComponent c, java.beans.PropertyChangeListener p ) &rarr; void

add a component that will get property change events and should respond
 to property changes.  This allows scientists a way to connect actions to
 the PNGWalk tool.

### Parameters:
c - null or a smallish JComponent that should be about the size of a button.
<br>p - null or the listener for the selected file and timerange.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addActionComponent&unscoped_q=addActionComponent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addFileAction"></a>
# addFileAction
addFileAction( org.autoplot.pngwalk.PngWalkTool.ActionEnabler match, javax.swing.Action abstractAction ) &rarr; void

Add a file action button to the GUI.

### Parameters:
match - returns true when the action can be applied to the current image.
<br>abstractAction - the action.

### Returns:
void (returns nothing)

### See Also:
<a href='#LOCAL_FILE_ENABLER which returns true for local files.'>LOCAL_FILE_ENABLER which returns true for local files.</a> which returns true for local files.<br>

<a href="https://github.com/autoplot/dev/search?q=addFileAction&unscoped_q=addFileAction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addTopDecorator"></a>
# addTopDecorator
addTopDecorator( org.das2.graph.Painter p ) &rarr; void

add a decorator to the PngWalkTool, which is drawn on single-image
 views.  Note this is draw in the coordinate system of the image, pixel
 coordinates with the origin (0,0) at the top left.

### Parameters:
p - a Painter

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addTopDecorator&unscoped_q=addTopDecorator">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="clearBottomLeftPanel"></a>
# clearBottomLeftPanel
clearBottomLeftPanel(  ) &rarr; void

remove all components from the bottom left panel.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=clearBottomLeftPanel&unscoped_q=clearBottomLeftPanel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="firePropertyChange"></a>
# firePropertyChange
firePropertyChange( String propertyName, Object oldValue, Object newValue ) &rarr; void

we need to make this public.

### Parameters:
propertyName - a String
<br>oldValue - an Object
<br>newValue - an Object

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=firePropertyChange&unscoped_q=firePropertyChange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDigitizerDataPointRecorder"></a>
# getDigitizerDataPointRecorder
getDigitizerDataPointRecorder(  ) &rarr; DataPointRecorder

provide access to the digitizer DataPointRecorder, so that points 
 can be deleted programmatically.

### Returns:
the DataPointRecorder.

<a href="https://github.com/autoplot/dev/search?q=getDigitizerDataPointRecorder&unscoped_q=getDigitizerDataPointRecorder">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getImageMouseAdapter"></a>
# getImageMouseAdapter
getImageMouseAdapter(  ) &rarr; MouseAdapter



### Returns:
java.awt.event.MouseAdapter


<a href="https://github.com/autoplot/dev/search?q=getImageMouseAdapter&unscoped_q=getImageMouseAdapter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMousePressLocation"></a>
# getMousePressLocation
getMousePressLocation(  ) &rarr; QDataSet



### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=getMousePressLocation&unscoped_q=getMousePressLocation">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMouseReleaseLocation"></a>
# getMouseReleaseLocation
getMouseReleaseLocation(  ) &rarr; QDataSet



### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=getMouseReleaseLocation&unscoped_q=getMouseReleaseLocation">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNavigationPanel"></a>
# getNavigationPanel
getNavigationPanel(  ) &rarr; JPanel

get a reference to the navigation panel.  To restore the normal layout,
 use setBottomLeftPanel( getNavigationPanel() ).

### Returns:
the navigation panel.

<a href="https://github.com/autoplot/dev/search?q=getNavigationPanel&unscoped_q=getNavigationPanel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSelectedFile"></a>
# getSelectedFile
getSelectedFile(  ) &rarr; String

returns the current selection, which may be a URL on a remote site, or null if no sequence has been selected.

### Returns:
the current selection or null if the sequence is not loaded or empty.

<a href="https://github.com/autoplot/dev/search?q=getSelectedFile&unscoped_q=getSelectedFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSelectedImage"></a>
# getSelectedImage
getSelectedImage(  ) &rarr; BufferedImage

return the currently selected image.

### Returns:
the currently selected image

<a href="https://github.com/autoplot/dev/search?q=getSelectedImage&unscoped_q=getSelectedImage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSelectedName"></a>
# getSelectedName
getSelectedName(  ) &rarr; String

return the name of the current selection, which is just the globbed or aggregated part of the names.
 This is introduced to support tying two pngwalks together.

### Returns:
the name of the currently selected file.

<a href="https://github.com/autoplot/dev/search?q=getSelectedName&unscoped_q=getSelectedName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSequence"></a>
# getSequence
getSequence(  ) &rarr; WalkImageSequence

return the container for the sequence of images, which contains the
 current index and provides a method for jumping to other images.

### Returns:
the sequence.

<a href="https://github.com/autoplot/dev/search?q=getSequence&unscoped_q=getSequence">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getStatus"></a>
# getStatus
getStatus(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getStatus&unscoped_q=getStatus">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTabs"></a>
# getTabs
getTabs(  ) &rarr; TearoffTabbedPane

provide means for scripts to add component to develop new applications.

### Returns:
the TearoffTabbedPane used.

<a href="https://github.com/autoplot/dev/search?q=getTabs&unscoped_q=getTabs">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTemplate"></a>
# getTemplate
getTemplate(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getTemplate&unscoped_q=getTemplate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getThumbnailSize"></a>
# getThumbnailSize
getThumbnailSize(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getThumbnailSize&unscoped_q=getThumbnailSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTimeRange"></a>
# getTimeRange
getTimeRange(  ) &rarr; DatumRange

rfe https://sourceforge.net/p/autoplot/feature-requests/271/

### Returns:
the current timerange

<a href="https://github.com/autoplot/dev/search?q=getTimeRange&unscoped_q=getTimeRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasTopDecorators"></a>
# hasTopDecorators
hasTopDecorators(  ) &rarr; boolean

returns true if there are any top decorators.

### Returns:
true if there are any decorators.

<a href="https://github.com/autoplot/dev/search?q=hasTopDecorators&unscoped_q=hasTopDecorators">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isQualityControlEnabled"></a>
# isQualityControlEnabled
isQualityControlEnabled(  ) &rarr; boolean

return true of the quality control panel is enabled.

### Returns:
return true of the quality control panel is enabled.

<a href="https://github.com/autoplot/dev/search?q=isQualityControlEnabled&unscoped_q=isQualityControlEnabled">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeActionComponent"></a>
# removeActionComponent
removeActionComponent( javax.swing.JComponent c, java.beans.PropertyChangeListener p ) &rarr; void



### Parameters:
c - a JComponent
<br>p - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeActionComponent&unscoped_q=removeActionComponent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeTopDecorator"></a>
# removeTopDecorator
removeTopDecorator( org.das2.graph.Painter p ) &rarr; void

remove a decorator to the PngWalkTool, which is drawn on single-image
 views.  If the decorator is not found, no error is thrown.

### Parameters:
p - a Painter

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeTopDecorator&unscoped_q=removeTopDecorator">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeTopDecorators"></a>
# removeTopDecorators
removeTopDecorators(  ) &rarr; void

remove all decorators from the PngWalkTool.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeTopDecorators&unscoped_q=removeTopDecorators">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setBottomLeftPanel"></a>
# setBottomLeftPanel
setBottomLeftPanel( javax.swing.JComponent c ) &rarr; void

set a new component for the bottom left panel, where by default the 
 navigation panel resides.

### Parameters:
c - a JComponent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setBottomLeftPanel&unscoped_q=setBottomLeftPanel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDigitizerRecording"></a>
# setDigitizerRecording
setDigitizerRecording( boolean enable ) &rarr; void

this can be used to disable recording of the points.

### Parameters:
enable - true means record points, false means don't record.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDigitizerRecording&unscoped_q=setDigitizerRecording">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setImageMouseAdapter"></a>
# setImageMouseAdapter
setImageMouseAdapter( java.awt.event.MouseAdapter imageMouseAdapter ) &rarr; void

add a mouse event handler, which will get events in the coordinate frame
 of the image.  This can be set to null to clear the adapter.

### Parameters:
imageMouseAdapter - a MouseAdapter

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setImageMouseAdapter&unscoped_q=setImageMouseAdapter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setMessage"></a>
# setMessage
setMessage( String message ) &rarr; void



### Parameters:
message - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMessage&unscoped_q=setMessage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

setMessage( javax.swing.Icon icon, String message ) &rarr; void<br>
***
<a name="setMousePressLocation"></a>
# setMousePressLocation
setMousePressLocation( QDataSet mousePressLocation ) &rarr; void



### Parameters:
mousePressLocation - a QDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMousePressLocation&unscoped_q=setMousePressLocation">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setMouseReleaseLocation"></a>
# setMouseReleaseLocation
setMouseReleaseLocation( QDataSet mouseReleaseLocation ) &rarr; void



### Parameters:
mouseReleaseLocation - a QDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMouseReleaseLocation&unscoped_q=setMouseReleaseLocation">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setQCStatus"></a>
# setQCStatus
setQCStatus( String text, org.autoplot.pngwalk.QualityControlRecord.Status status ) &rarr; void

provide a method for setting the QCStatus externally.

### Parameters:
text - message annotating the status change or commenting on status.
<br>status - the status

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setQCStatus&unscoped_q=setQCStatus">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSelectedName"></a>
# setSelectedName
setSelectedName( String name ) &rarr; void

set the name of the file to select, which is just the globber or aggregated part of the name.  For example, 
 if getTemplate is file:/tmp/$Y$m$d.gif, then the setSelectedName might be 20141111.gif.  If the name is not found in the 
 pngwalk, then this has no effect.

### Parameters:
name - the new name

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSelectedName&unscoped_q=setSelectedName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setStatus"></a>
# setStatus
setStatus( String message ) &rarr; void



### Parameters:
message - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setStatus&unscoped_q=setStatus">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTemplate"></a>
# setTemplate
setTemplate( String template ) &rarr; void

set the template which the PNGWalk Tool will display.

### Parameters:
template - file template, like /tmp/$Y$m$d.png

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTemplate&unscoped_q=setTemplate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setThumbnailSize"></a>
# setThumbnailSize
setThumbnailSize( int thumbnailSize ) &rarr; void



### Parameters:
thumbnailSize - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setThumbnailSize&unscoped_q=setThumbnailSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTimeRange"></a>
# setTimeRange
setTimeRange( DatumRange timeRange ) &rarr; void

timerange roughly the focus timerange.  This property is introduced 
 to allow for binding between pngwalks.
 This should not be confused with the &timerange= part of the URI.

### Parameters:
timeRange - a DatumRange

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTimeRange&unscoped_q=setTimeRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="start"></a>
# start
start( String template, java.awt.Window parent ) &rarr; PngWalkTool

initialize a new PNGWalkTool with the given template.

### Parameters:
template - the template, such as http://autoplot.org/data/pngwalk/product_$Y$m$d.vap
<br>parent - null or a parent component to own this application.

### Returns:
a PngWalkTool, which is visible and packed.

<a href="https://github.com/autoplot/dev/search?q=start&unscoped_q=start">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="startDigitizer"></a>
# startDigitizer
startDigitizer(  ) &rarr; void

start the digitizer if it is not started already.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=startDigitizer&unscoped_q=startDigitizer">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="startQC"></a>
# startQC
startQC(  ) &rarr; void

start the quality control if it is not started already.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=startQC&unscoped_q=startQC">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="updateTimeRangeFilter"></a>
# updateTimeRangeFilter
updateTimeRangeFilter(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=updateTimeRangeFilter&unscoped_q=updateTimeRangeFilter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="writeAnimatedGif"></a>
# writeAnimatedGif
writeAnimatedGif(  ) &rarr; void

Write the displayed images to an animated gif.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeAnimatedGif&unscoped_q=writeAnimatedGif">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="writeContactSheet"></a>
# writeContactSheet
writeContactSheet( java.io.File f ) &rarr; void

write the current Grid view to a single PNG file.

### Parameters:
f - a File

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeContactSheet&unscoped_q=writeContactSheet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="writeHtml"></a>
# writeHtml
writeHtml(  ) &rarr; void

write the sequence to a PDF file, so that this can be used to produce
 worksheets.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeHtml&unscoped_q=writeHtml">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="writePdf"></a>
# writePdf
writePdf(  ) &rarr; void

write the sequence to a PDF file, so that this can be used to produce
 worksheets.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writePdf&unscoped_q=writePdf">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

