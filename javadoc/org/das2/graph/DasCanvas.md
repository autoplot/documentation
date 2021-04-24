# org.das2.graph.DasCanvas

Canvas for das2 graphics.  The DasCanvas contains any number of DasCanvasComponents such as axes, plots, colorbars, etc.

# DasCanvas( )
Creates a new instance of DasCanvas.

# DasCanvas( int width, int height )
Creates a new instance of DasCanvas with the specified width and height

***
<a name="DEFAULT_LAYER"></a>
# DEFAULT_LAYER

Default drawing layer of the JLayeredPane

***
<a name="PLOT_LAYER"></a>
# PLOT_LAYER

Z-Layer for drawing the plot.

***
<a name="VERTICAL_AXIS_LAYER"></a>
# VERTICAL_AXIS_LAYER

Z-Layer for vertical axis.  Presently lower than the horizontal axis, presumably to remove ambiguity

***
<a name="HORIZONTAL_AXIS_LAYER"></a>
# HORIZONTAL_AXIS_LAYER

Z-Layer

***
<a name="AXIS_LAYER"></a>
# AXIS_LAYER

Z-Layer

***
<a name="ANNOTATION_LAYER"></a>
# ANNOTATION_LAYER

Z-Layer

***
<a name="GLASS_PANE_LAYER"></a>
# GLASS_PANE_LAYER

Z-Layer

***
<a name="SAVE_AS_PNG_ACTION"></a>
# SAVE_AS_PNG_ACTION



***
<a name="SAVE_AS_SVG_ACTION"></a>
# SAVE_AS_SVG_ACTION



***
<a name="SAVE_AS_PDF_ACTION"></a>
# SAVE_AS_PDF_ACTION



***
<a name="EDIT_DAS_PROPERTIES_ACTION"></a>
# EDIT_DAS_PROPERTIES_ACTION



***
<a name="PRINT_ACTION"></a>
# PRINT_ACTION



***
<a name="REFRESH_ACTION"></a>
# REFRESH_ACTION



***
<a name="ABOUT_ACTION"></a>
# ABOUT_ACTION

Override Component.setBounds for debugging.

***
<a name="PROPERTIES_ACTION"></a>
# PROPERTIES_ACTION



***
<a name="broken"></a>
# broken



***
<a name="PROP_SCALEFONTS"></a>
# PROP_SCALEFONTS

The font used should be the base font scaled based on the canvas size.
 If this is false, then the canvas font is simply the base font.

***
<a name="PROP_BASEFONT"></a>
# PROP_BASEFONT

Property name for the base font.

***
<a name="PROP_PAINTCOUNT"></a>
# PROP_PAINTCOUNT



***
<a name="add"></a>
# add
add( org.das2.graph.DasCanvasComponent c, org.das2.graph.DasRow row, org.das2.graph.DasColumn column ) &rarr; void

This methods adds the specified <code>DasCanvasComponent</code> to this canvas.

### Parameters:
c - the component to be added to this canvas
 Note that the canvas will need to be revalidated after the component
 is added.
<br>row - DasRow specifying the layout of the component.
<br>column - DasColumn specifying the layout of the component.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=add&unscoped_q=add">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addBottomDecorator"></a>
# addBottomDecorator
addBottomDecorator( org.das2.graph.Painter painter ) &rarr; void

add a decorator that will be painted on below all other objects.  
 Each decorator object should complete painting within 100 milliseconds, and the
 total for all decorators should not exceed 300 milliseconds.
 This should be done on the event thread.

### Parameters:
painter - a Painter

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addBottomDecorator&unscoped_q=addBottomDecorator">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addTopDecorator"></a>
# addTopDecorator
addTopDecorator( org.das2.graph.Painter painter ) &rarr; void

add a decorator that will be painted on top of all other objects.  
 Each decorator object should complete painting within 100 milliseconds, and the
 total for all decorators should not exceed 300 milliseconds.
 This should be done on the event thread.

### Parameters:
painter - a Painter

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addTopDecorator&unscoped_q=addTopDecorator">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="changePerformed"></a>
# changePerformed
changePerformed( Object client, Object lockObject ) &rarr; void

indicate to the canvas that a change is now complete.

### Parameters:
client - the client registering the change
<br>lockObject - an object identifying the change

### Returns:
void (returns nothing)

### See Also:
<a href='ChangesSupport.md'>ChangesSupport</a> <br>

<a href="https://github.com/autoplot/dev/search?q=changePerformed&unscoped_q=changePerformed">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createFormCanvas"></a>
# createFormCanvas
createFormCanvas( String name, int width, int height ) &rarr; DasCanvas



### Parameters:
name - a String
<br>width - an int
<br>height - an int

### Returns:
DasCanvas with a name.

<a href="https://github.com/autoplot/dev/search?q=createFormCanvas&unscoped_q=createFormCanvas">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="devicePositionList"></a>
# devicePositionList
devicePositionList(  ) &rarr; List

returns a list of all the rows and columns on the canvas.

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=devicePositionList&unscoped_q=devicePositionList">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getActions"></a>
# getActions
getActions(  ) &rarr; Action



### Returns:
javax.swing.Action[]


<a href="https://github.com/autoplot/dev/search?q=getActions&unscoped_q=getActions">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getApplication"></a>
# getApplication
getApplication(  ) &rarr; DasApplication



### Returns:
org.das2.DasApplication


<a href="https://github.com/autoplot/dev/search?q=getApplication&unscoped_q=getApplication">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBaseFont"></a>
# getBaseFont
getBaseFont(  ) &rarr; Font

the base font, which is the font or the font which is scaled when scaleFont is true.

### Returns:
the base font, which is the font or the font which is scaled when scaleFont is true.

<a href="https://github.com/autoplot/dev/search?q=getBaseFont&unscoped_q=getBaseFont">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCanvasComponentAt"></a>
# getCanvasComponentAt
getCanvasComponentAt( int x, int y ) &rarr; DasCanvasComponent

Returns the DasCanvasComponent that contains the (x, y) location.
 If there is no component at that location, this method
 returns <CODE>null</CODE>

### Parameters:
x - the x coordinate
<br>y - the y coordinate

### Returns:
the component at the specified point, or null

<a href="https://github.com/autoplot/dev/search?q=getCanvasComponentAt&unscoped_q=getCanvasComponentAt">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCanvasComponents"></a>
# getCanvasComponents
getCanvasComponents( int index ) &rarr; DasCanvasComponent

return the component at the index.

### Parameters:
index - the index

### Returns:
the component at the index.

<a href="https://github.com/autoplot/dev/search?q=getCanvasComponents&unscoped_q=getCanvasComponents">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getCanvasComponents(  ) &rarr; DasCanvasComponent<br>
***
<a name="getCellAt"></a>
# getCellAt
getCellAt( int x, int y ) &rarr; Cell

TODO

### Parameters:
x - an int
<br>y - an int

### Returns:
an org.das2.graph.DasCanvas.Cell


<a href="https://github.com/autoplot/dev/search?q=getCellAt&unscoped_q=getCellAt">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDasApplication"></a>
# getDasApplication
getDasApplication(  ) &rarr; DasApplication

return the application object for this canvas.

### Returns:
the application object for this canvas.

<a href="https://github.com/autoplot/dev/search?q=getDasApplication&unscoped_q=getDasApplication">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDasName"></a>
# getDasName
getDasName(  ) &rarr; String

return the name identifying the component.

### Returns:
the name identifying the component.

<a href="https://github.com/autoplot/dev/search?q=getDasName&unscoped_q=getDasName">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDevicePositionList"></a>
# getDevicePositionList
getDevicePositionList(  ) &rarr; List

return a list of all the rows and columns.

### Returns:
a list of all the rows and columns.

<a href="https://github.com/autoplot/dev/search?q=getDevicePositionList&unscoped_q=getDevicePositionList">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDnDSupport"></a>
# getDnDSupport
getDnDSupport(  ) &rarr; DnDSupport

TODO

### Returns:
an org.das2.util.DnDSupport


<a href="https://github.com/autoplot/dev/search?q=getDnDSupport&unscoped_q=getDnDSupport">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getEditingMode"></a>
# getEditingMode
getEditingMode(  ) &rarr; boolean

TODO

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=getEditingMode&unscoped_q=getEditingMode">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFocusCanvas"></a>
# getFocusCanvas
getFocusCanvas(  ) &rarr; DasCanvas

return the canvas that has the focus.

### Returns:
an org.das2.graph.DasCanvas


<a href="https://github.com/autoplot/dev/search?q=getFocusCanvas&unscoped_q=getFocusCanvas">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getGlassPane"></a>
# getGlassPane
getGlassPane(  ) &rarr; Component

returns the GlassPane above all other components. This is used for drawing dragRenderers, etc.

### Returns:
a java.awt.Component


<a href="https://github.com/autoplot/dev/search?q=getGlassPane&unscoped_q=getGlassPane">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getImage"></a>
# getImage
getImage( int width, int height ) &rarr; BufferedImage

Creates a BufferedImage by blocking until the image is ready.  This
 includes waiting for datasets to load, etc.  Works by submitting
 an invokeAfter request to the RequestProcessor that calls
 {@link #writeToImageImmediately(Image)}.

### Parameters:
width - an int
<br>height - an int

### Returns:
a BufferedImage

<a href="https://github.com/autoplot/dev/search?q=getImage&unscoped_q=getImage">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getImageMetadata"></a>
# getImageMetadata
getImageMetadata(  ) &rarr; String

returns JSON code that can be used to get plot positions and axes.

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getImageMetadata&unscoped_q=getImageMetadata">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getImageNonPrint"></a>
# getImageNonPrint
getImageNonPrint( int width, int height ) &rarr; Image

Creates a BufferedImage by blocking until the image is ready.  This
 includes waiting for datasets to load, etc.  Works by submitting
 an invokeAfter request to the RequestProcessor that calls
 {@link #writeToImageImmediately(Image)}.

 Note, this calls writeToImageImmediatelyNonPrint, which avoids the usual overhead of
 revalidating the DasPlot elements we normally do when printing to a new device.

### Parameters:
width - an int
<br>height - an int

### Returns:
an Image

<a href="https://github.com/autoplot/dev/search?q=getImageNonPrint&unscoped_q=getImageNonPrint">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLineAt"></a>
# getLineAt
getLineAt( int x, int y ) &rarr; HotLine

TODO

### Parameters:
x - an int
<br>y - an int

### Returns:
an org.das2.graph.DasCanvas.HotLine


<a href="https://github.com/autoplot/dev/search?q=getLineAt&unscoped_q=getLineAt">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMaximumSize"></a>
# getMaximumSize
getMaximumSize(  ) &rarr; Dimension

simply returns getPreferredSize()

### Returns:
getPreferredSize()

<a href="https://github.com/autoplot/dev/search?q=getMaximumSize&unscoped_q=getMaximumSize">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPaintCount"></a>
# getPaintCount
getPaintCount(  ) &rarr; int

provide a property which can be used to monitor updates.

### Returns:
arbitrary int which will change as the canvas is painted.

<a href="https://github.com/autoplot/dev/search?q=getPaintCount&unscoped_q=getPaintCount">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPreferredScrollableViewportSize"></a>
# getPreferredScrollableViewportSize
getPreferredScrollableViewportSize(  ) &rarr; Dimension



### Returns:
java.awt.Dimension


<a href="https://github.com/autoplot/dev/search?q=getPreferredScrollableViewportSize&unscoped_q=getPreferredScrollableViewportSize">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPrintable"></a>
# getPrintable
getPrintable(  ) &rarr; Printable

Returns an instance of <code>java.awt.print.Printable</code> that can
 be used to render this canvas to a printer.  The current implementation
 returns a reference to this canvas.  This method is provided so that in
 the future, the canvas can delegate it's printing to another object.

### Returns:
a <code>Printable</code> instance for rendering this component.

<a href="https://github.com/autoplot/dev/search?q=getPrintable&unscoped_q=getPrintable">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPrintingTag"></a>
# getPrintingTag
getPrintingTag(  ) &rarr; String

printingTag is the DateFormat string to use to tag printed images.

### Returns:
Value of property printingTag.

<a href="https://github.com/autoplot/dev/search?q=getPrintingTag&unscoped_q=getPrintingTag">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getScrollableBlockIncrement"></a>
# getScrollableBlockIncrement
getScrollableBlockIncrement( java.awt.Rectangle visibleRect, int orientation, int direction ) &rarr; int



### Parameters:
visibleRect - a Rectangle
<br>orientation - an int
<br>direction - an int

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getScrollableBlockIncrement&unscoped_q=getScrollableBlockIncrement">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getScrollableTracksViewportHeight"></a>
# getScrollableTracksViewportHeight
getScrollableTracksViewportHeight(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=getScrollableTracksViewportHeight&unscoped_q=getScrollableTracksViewportHeight">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getScrollableTracksViewportWidth"></a>
# getScrollableTracksViewportWidth
getScrollableTracksViewportWidth(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=getScrollableTracksViewportWidth&unscoped_q=getScrollableTracksViewportWidth">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getScrollableUnitIncrement"></a>
# getScrollableUnitIncrement
getScrollableUnitIncrement( java.awt.Rectangle visibleRect, int orientation, int direction ) &rarr; int



### Parameters:
visibleRect - a Rectangle
<br>orientation - an int
<br>direction - an int

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getScrollableUnitIncrement&unscoped_q=getScrollableUnitIncrement">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasBottomDecorators"></a>
# hasBottomDecorators
hasBottomDecorators(  ) &rarr; boolean

returns true if there are any bottom decorators.

### Returns:
true if there are any decorators.

<a href="https://github.com/autoplot/dev/search?q=hasBottomDecorators&unscoped_q=hasBottomDecorators">[search for examples]</a>
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
<a name="isAntiAlias"></a>
# isAntiAlias
isAntiAlias(  ) &rarr; boolean

true if data will be fully rendered with anti-aliasing.

### Returns:
true if data will be fully rendered with anti-aliasing.

<a href="https://github.com/autoplot/dev/search?q=isAntiAlias&unscoped_q=isAntiAlias">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDirty"></a>
# isDirty
isDirty(  ) &rarr; boolean

returns true if work needs to be done to make the canvas clean.  
 This checks each component's isDirty.

### Returns:
true if work needs to be done to make the canvas clean

<a href="https://github.com/autoplot/dev/search?q=isDirty&unscoped_q=isDirty">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isFitted"></a>
# isFitted
isFitted(  ) &rarr; boolean

If true, and the canvas was added to a scrollpane, the canvas
 will size itself to fit within the scrollpane.

### Returns:
value of fitted property

<a href="https://github.com/autoplot/dev/search?q=isFitted&unscoped_q=isFitted">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isPendingChanges"></a>
# isPendingChanges
isPendingChanges( Object lockObject ) &rarr; boolean

ask the canvas if the particular change is already pending.

### Parameters:
lockObject - an object identifying the change

### Returns:
true if that particular change is pending.
### See Also:
<a href='ChangesSupport.md'>ChangesSupport</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isPendingChanges&unscoped_q=isPendingChanges">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

isPendingChanges(  ) &rarr; boolean<br>
***
<a name="isScaleFonts"></a>
# isScaleFonts
isScaleFonts(  ) &rarr; boolean

true if the fonts should be rescaled as the window size is changed.

### Returns:
true if the fonts should be rescaled as the window size is changed.

<a href="https://github.com/autoplot/dev/search?q=isScaleFonts&unscoped_q=isScaleFonts">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isTextAntiAlias"></a>
# isTextAntiAlias
isTextAntiAlias(  ) &rarr; boolean

return true if fonts will be fully rendered.

### Returns:
true if fonts will be fully rendered.

<a href="https://github.com/autoplot/dev/search?q=isTextAntiAlias&unscoped_q=isTextAntiAlias">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isValueAdjusting"></a>
# isValueAdjusting
isValueAdjusting(  ) &rarr; boolean

returns true if an operation is being performed that should be treated as atomic.

### Returns:
true if an operation is being performed that should be treated as atomic.
### See Also:
<a href='ChangesSupport.md'>ChangesSupport</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isValueAdjusting&unscoped_q=isValueAdjusting">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="lisPaintingForPrint"></a>
# lisPaintingForPrint
lisPaintingForPrint(  ) &rarr; boolean

Java1.6 has this function native

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=lisPaintingForPrint&unscoped_q=lisPaintingForPrint">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="makeCurrent"></a>
# makeCurrent
makeCurrent(  ) &rarr; void

make this the current canvas

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=makeCurrent&unscoped_q=makeCurrent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mutatorLock"></a>
# mutatorLock
mutatorLock(  ) &rarr; Lock

access the lock for an atomic operation.

### Returns:
the lock.
### See Also:
<a href='ChangesSupport.md'>ChangesSupport</a> <br>

<a href="https://github.com/autoplot/dev/search?q=mutatorLock&unscoped_q=mutatorLock">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="pendingChanges"></a>
# pendingChanges
pendingChanges( java.util.Map result ) &rarr; void

return a list of pending changes.

### Parameters:
result - a java.util.Map

### Returns:
void (returns nothing)

### See Also:
<a href='waitUntilIdle.md'>waitUntilIdle</a> <br>

<a href="https://github.com/autoplot/dev/search?q=pendingChanges&unscoped_q=pendingChanges">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="performingChange"></a>
# performingChange
performingChange( Object client, Object lockObject ) &rarr; void

indicate to the canvas that a change is being performed.

### Parameters:
client - the client registering the change
<br>lockObject - an object identifying the change

### Returns:
void (returns nothing)

### See Also:
<a href='ChangesSupport.md'>ChangesSupport</a> <br>

<a href="https://github.com/autoplot/dev/search?q=performingChange&unscoped_q=performingChange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="prepareForOutput"></a>
# prepareForOutput
prepareForOutput( int width, int height ) &rarr; void

resets the width and height, then waits for all update
 messages to be processed.  In headless mode,
 the GUI components are validated.
 This must not be called from the event queue, because
 it uses eventQueueBlocker!

### Parameters:
width - the width of the output in pixels.
<br>height - the width of the output in pixels.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=prepareForOutput&unscoped_q=prepareForOutput">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="print"></a>
# print
print( java.awt.Graphics printGraphics, java.awt.print.PageFormat format, int pageIndex ) &rarr; int

Prints the canvas, scaling and possibly rotating it to improve fit.

### Parameters:
printGraphics - the Graphics object.
<br>format - the PageFormat object.
<br>pageIndex - should be 0, since the image will be on one page.

### Returns:
Printable.PAGE_EXISTS or Printable.NO_SUCH_PAGE

<a href="https://github.com/autoplot/dev/search?q=print&unscoped_q=print">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

print( java.awt.Graphics g1 ) &rarr; void<br>
***
<a name="registerPendingChange"></a>
# registerPendingChange
registerPendingChange( Object client, Object lockObject ) &rarr; void

indicate to the canvas that a change will be made soon. 
 For example, the canvas should wait for the change to be performed before creating an image.

### Parameters:
client - the client registering the change
<br>lockObject - an object identifying the change

### Returns:
void (returns nothing)

### See Also:
<a href='ChangesSupport.md'>ChangesSupport</a> <br>

<a href="https://github.com/autoplot/dev/search?q=registerPendingChange&unscoped_q=registerPendingChange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="remove"></a>
# remove
remove( int index ) &rarr; void

Removes the component, specified by <code>index</code>,
 from this container, calling its uninstallComponent 
 method if it's a DasCanvasComponent.

### Parameters:
index - the index of the component to be removed.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=remove&unscoped_q=remove">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

remove( java.awt.Component comp ) &rarr; void<br>
***
<a name="removeBottomDecorator"></a>
# removeBottomDecorator
removeBottomDecorator( org.das2.graph.Painter painter ) &rarr; void

remove the decorator.  This should be done on the event thread.

### Parameters:
painter - a Painter

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeBottomDecorator&unscoped_q=removeBottomDecorator">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeBottomDecorators"></a>
# removeBottomDecorators
removeBottomDecorators(  ) &rarr; void

remove all bottom decorators.  This should be done on the event thread.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeBottomDecorators&unscoped_q=removeBottomDecorators">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeDasDevicePosition"></a>
# removeDasDevicePosition
removeDasDevicePosition( org.das2.graph.DasDevicePosition position ) &rarr; void

remove the device position from the list we keep track of.  Note those
 with parent rows and columns should not be registered (or at least existing
 code doesn't add it).

### Parameters:
position - a DasDevicePosition

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeDasDevicePosition&unscoped_q=removeDasDevicePosition">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeTopDecorator"></a>
# removeTopDecorator
removeTopDecorator( org.das2.graph.Painter painter ) &rarr; void

remove the decorator.  This should be done on the event thread.

### Parameters:
painter - a Painter

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeTopDecorator&unscoped_q=removeTopDecorator">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeTopDecorators"></a>
# removeTopDecorators
removeTopDecorators(  ) &rarr; void

remove all top decorators.  This should be done on the event thread.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeTopDecorators&unscoped_q=removeTopDecorators">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removepwDevicePosition"></a>
# <del>removepwDevicePosition</del>
Deprecated: use removeDasDevicePosition instead.
***
<a name="resizeAllComponents"></a>
# resizeAllComponents
resizeAllComponents(  ) &rarr; void

introduced as a kludgy way for clients to force the canvas to resize all of its components.
 validate or revalidate should probably do this.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resizeAllComponents&unscoped_q=resizeAllComponents">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAntiAlias"></a>
# setAntiAlias
setAntiAlias( boolean antiAlias ) &rarr; void

true if data will be fully rendered with anti-aliasing.

### Parameters:
antiAlias - if data will be fully rendered with anti-aliasing.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAntiAlias&unscoped_q=setAntiAlias">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setApplication"></a>
# setApplication
setApplication( org.das2.DasApplication application ) &rarr; void



### Parameters:
application - a DasApplication

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setApplication&unscoped_q=setApplication">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setBaseFont"></a>
# setBaseFont
setBaseFont( java.awt.Font font ) &rarr; void

the base font, which is the font or the font which is scaled with canvas size when scaleFont is true.

### Parameters:
font - the font used to derive all other fonts.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setBaseFont&unscoped_q=setBaseFont">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDasName"></a>
# setDasName
setDasName( String name ) &rarr; void

set the name identifying the component.

### Parameters:
name - the name identifying the component.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDasName&unscoped_q=setDasName">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDisableActions"></a>
# setDisableActions
setDisableActions( boolean val ) &rarr; void



### Parameters:
val - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDisableActions&unscoped_q=setDisableActions">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setEditingMode"></a>
# setEditingMode
setEditingMode( boolean b ) &rarr; void

TODO

### Parameters:
b - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setEditingMode&unscoped_q=setEditingMode">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFitted"></a>
# setFitted
setFitted( boolean fitted ) &rarr; void

If true, and the canvas was added to a scrollpane, the canvas
 will size itself to fit within the scrollpane.

### Parameters:
fitted - value of fitted property

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFitted&unscoped_q=setFitted">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFont"></a>
# setFont
setFont( java.awt.Font font ) &rarr; void



### Parameters:
font - a Font

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFont&unscoped_q=setFont">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPreferredHeight"></a>
# setPreferredHeight
setPreferredHeight( int height ) &rarr; void

Sets the preferred height of the canvas to the specified height.

### Parameters:
height - the specified height

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPreferredHeight&unscoped_q=setPreferredHeight">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPreferredWidth"></a>
# setPreferredWidth
setPreferredWidth( int width ) &rarr; void

Sets the preferred width of the canvas to the specified width.

### Parameters:
width - the specified width.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPreferredWidth&unscoped_q=setPreferredWidth">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPrintingTag"></a>
# setPrintingTag
setPrintingTag( String printingTag ) &rarr; void

printingTag is the string to use to tag printed images.
 This can be 'yyyymmdd (SimpleDateFormat) or $Y$m$d, or just a string.

### Parameters:
printingTag - New value of property printingTag.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPrintingTag&unscoped_q=setPrintingTag">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setScaleFonts"></a>
# setScaleFonts
setScaleFonts( boolean scaleFonts ) &rarr; void

true if the fonts should be rescaled as the window size is changed.

### Parameters:
scaleFonts - true if the fonts should be rescaled as the window size is changed.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setScaleFonts&unscoped_q=setScaleFonts">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTextAntiAlias"></a>
# setTextAntiAlias
setTextAntiAlias( boolean textAntiAlias ) &rarr; void

true if fonts will be fully rendered.

### Parameters:
textAntiAlias - true if fonts will be fully rendered.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTextAntiAlias&unscoped_q=setTextAntiAlias">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="startDrag"></a>
# startDrag
startDrag( int x, int y, int action, java.awt.event.MouseEvent evt ) &rarr; boolean

TODO

### Parameters:
x - an int
<br>y - an int
<br>action - an int
<br>evt - a MouseEvent

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=startDrag&unscoped_q=startDrag">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="waitUntilIdle"></a>
# waitUntilIdle
waitUntilIdle( boolean monitors ) &rarr; void

blocks until everything is idle, including no active monitors.
 PRESENTLY THIS DOES NOT CHECK MONITORS!

### Parameters:
monitors - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=waitUntilIdle&unscoped_q=waitUntilIdle">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

waitUntilIdle(  ) &rarr; void<br>
***
<a name="waitUntilValid"></a>
# waitUntilValid
waitUntilValid(  ) &rarr; void

process all pending operations and make sure we're repainted.  See PlotCommand in Autoplot.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=waitUntilValid&unscoped_q=waitUntilValid">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="writeToGraphicsOutput"></a>
# writeToGraphicsOutput
writeToGraphicsOutput( java.io.OutputStream out, org.das2.util.awt.GraphicsOutput go ) &rarr; void

write to various graphics devices such as png, pdf and svg.  This handles the synchronization and
 parameter settings.

### Parameters:
out - OutputStream to receive the data
<br>go - GraphicsOutput object.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeToGraphicsOutput&unscoped_q=writeToGraphicsOutput">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

writeToGraphicsOutput( String filename, String graphicsOutput ) &rarr; void<br>
***
<a name="writeToImageImmediately"></a>
# writeToImageImmediately
writeToImageImmediately( java.awt.Image image ) &rarr; void

Writes on to the image without waiting, using the print method.
 The graphics context is accessed with image.getGraphics.

### Parameters:
image - the image

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeToImageImmediately&unscoped_q=writeToImageImmediately">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="writeToImageImmediatelyNoCount"></a>
# writeToImageImmediatelyNoCount
writeToImageImmediatelyNoCount( java.awt.Image image ) &rarr; void

silly code so that Autoplot can get an image without incrementing paintCount.

### Parameters:
image - an Image

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeToImageImmediatelyNoCount&unscoped_q=writeToImageImmediatelyNoCount">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="writeToImageImmediatelyNonPrint"></a>
# writeToImageImmediatelyNonPrint
writeToImageImmediatelyNonPrint( java.awt.Image image ) &rarr; void

This by passes the normal print method used in writeToImageImmedately, which sets the printing flags which
 tell the components, like DasPlot, to fully reset.  This was introduced so that Autoplot could get thumbnails
 and an image of the canvas for its layout tab without having to reset.

### Parameters:
image - the image

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeToImageImmediatelyNonPrint&unscoped_q=writeToImageImmediatelyNonPrint">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="writeToPDF"></a>
# writeToPDF
writeToPDF( String filename ) &rarr; void

write the canvas to a PDF file.

### Parameters:
filename - the PDF file name.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeToPDF&unscoped_q=writeToPDF">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="writeToPng"></a>
# writeToPng
writeToPng( java.io.OutputStream out, int w, int h ) &rarr; void

uses getImage to get an image of the canvas and encodes it
 as a png.

 Note this now puts in a JSON representation of plot locations in the "plotInfo" tag.  The plotInfo
 tag will contain:
<blockquote><pre>
   "size:[640,480]"
   "numberOfPlots:0"   
   "plots: { ... "  where each plot contains:
   "title" "xaxis" "yaxis"
}</pre></blockquote>
 See http://autoplot.org/richPng.

### Parameters:
out - the outputStream. This is left open, so the opener code must close it!
<br>w - width in pixels
<br>h - height in pixels

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeToPng&unscoped_q=writeToPng">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

writeToPng( String filename ) &rarr; void<br>
***
<a name="writeToSVG"></a>
# writeToSVG
writeToSVG( String filename ) &rarr; void



### Parameters:
filename - the specified filename

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeToSVG&unscoped_q=writeToSVG">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

