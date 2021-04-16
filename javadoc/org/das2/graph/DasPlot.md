# org.das2.graph.DasPlotDasPlot is the 2D plot containing a horizontal X axis and vertical Y
 axis, and a stack of Renderers that paint data onto the plot.  It coordinates
 calls to each Renderer's updatePlotImage and render methods, and manages
 the rendered stack image to provide previews of new axis settings.
DasPlot( org.das2.graph.DasAxis xAxis, org.das2.graph.DasAxis yAxis )
create a new plot with the x and y axes.

***
<a name="PROP_TITLE"></a>
# PROP_TITLE

title for the plot

***
<a name="PROP_FOCUSRENDERER"></a>
# PROP_FOCUSRENDERER

property name for the current renderer that the operator has selected.

***
<a name="PROP_MULTILINETEXTALIGNMENT"></a>
# PROP_MULTILINETEXTALIGNMENT

property name for multiline labels, the horizontal alignment, where 0 is left, 0.5 is center, and 1.0 is right.

***
<a name="DUMP_TO_FILE_ACTION"></a>
# DUMP_TO_FILE_ACTION

Action to dump the first (0th) renderer's data to a file.

***
<a name="INFO"></a>
# INFO

These levels are now taken from java.util.logging.Level.  Generally
 INFO messages are displayed.

***
<a name="WARNING"></a>
# WARNING

mark the log message as a warning where the operator should be aware.

***
<a name="SEVERE"></a>
# SEVERE

mark the log message as severe, where an error condition has occurred.

***
<a name="PROP_DISPLAYTITLE"></a>
# PROP_DISPLAYTITLE

turns the plot title off or on.

***
<a name="PROP_BOTTOMDECORATOR"></a>
# PROP_BOTTOMDECORATOR



***
<a name="PROP_TOPDECORATOR"></a>
# PROP_TOPDECORATOR



***
<a name="PROP_CONTEXT"></a>
# PROP_CONTEXT

property where the plot context can be stored.

***
<a name="PROP_DISPLAY_CONTEXT"></a>
# PROP_DISPLAY_CONTEXT

necessary place to put the range of the data actually displayed.  The context is the controller,
 and the displayContext closes the loop.  This is mostly here to provide legacy support to Autoplot which
 abused the context property as both a write and read, and note there's a small problem that displayed
 items may have different display contexts.  So this property should be used carefully, and generally
 when just one thing is visible.

***
<a name="PROP_LEGENDPOSITION"></a>
# PROP_LEGENDPOSITION

the location of the legend position, which can be one of the four corners, 
 or outside and to the right of the plot.

***
<a name="PROP_LEGENDRELATIVESIZESIZE"></a>
# PROP_LEGENDRELATIVESIZESIZE

relative font size for the legend.  For example, -2 will use sans-8 when the
 plot font is sans-10.

***
<a name="PROP_FONTSIZE"></a>
# PROP_FONTSIZE



***
<a name="PROP_DISPLAYLEGEND"></a>
# PROP_DISPLAYLEGEND

true if the legend should be displayed

***
<a name="PROP_DRAWBACKGROUND"></a>
# PROP_DRAWBACKGROUND

the background should be drawn, if alpha is &gt;0.

***
<a name="PROP_DRAWGRIDCOLOR"></a>
# PROP_DRAWGRIDCOLOR

if not transparent, draw the grid in this color.  Otherwise
 the grid is drawn with the tick color.

***
<a name="PROP_DRAWGRID"></a>
# PROP_DRAWGRID

If true, faint grey lines continue the axis major
 ticks across the plot.

***
<a name="PROP_DRAWMINORGRID"></a>
# PROP_DRAWMINORGRID

If true, faint grey lines continue the axis minor
 ticks across the plot.

***
<a name="PROP_DRAWGRIDOVER"></a>
# PROP_DRAWGRIDOVER

if true, then the grid is on top of the data.

***
<a name="PROP_LINETHICKNESS"></a>
# PROP_LINETHICKNESS



***
<a name="PROP_PLOTVISIBLE"></a>
# PROP_PLOTVISIBLE



***
<a name="PROP_OVERSIZE"></a>
# PROP_OVERSIZE

boolean property indicating that the data outside the axis
 bounds is rendered, to smooth animation when the axis is panned.

***
<a name="PROP_LOG_LEVEL"></a>
# PROP_LOG_LEVEL

the log level for the messages on the screen.

***
<a name="PROP_PRINTINGLOGLEVEL"></a>
# PROP_PRINTINGLOGLEVEL

the log level to indicate the log level when printing.

***
<a name="PROP_LOG_TIMEOUT_SEC"></a>
# PROP_LOG_TIMEOUT_SEC

number of seconds to show the log messages.  If Integer.MAX_VALUE/100 or 
 greater then there is no timeout.

***
<a name="PROP_ISOTROPIC"></a>
# PROP_ISOTROPIC

true if the x and y scaling (pixel:data) ratio is locked together.

***
<a name="PROP_DRAWDEBUGMESSAGES"></a>
# PROP_DRAWDEBUGMESSAGES

draw a purple box in the lower right corner indicating the number
 of times each renderer has updated, rendered, and the plot itself
 has painted.

***
<a name="addCustomizer"></a>
# addCustomizer
addCustomizer( org.das2.graph.CustomizerKey key, org.das2.graph.Customizer customizer ) &rarr; void

Add a new customizer to the collection of customizers being used when creating
 new plots. The new customizer will be invoked last.

### Parameters:
key - the new customizer's lookup key
<br>customizer - the new customizer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addCustomizer&unscoped_q=addCustomizer">[search for examples]</a>

***
<a name="addRenderer"></a>
# addRenderer
addRenderer( org.das2.graph.Renderer rend ) &rarr; void

add the renderer to the stack of renderers.  It will be the 
 last element drawn.

### Parameters:
rend - the renderer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addRenderer&unscoped_q=addRenderer">[search for examples]</a>

addRenderer( int index, org.das2.graph.Renderer rend ) &rarr; void<br>
***
<a name="addToLegend"></a>
# addToLegend
addToLegend( org.das2.graph.Renderer renderer, javax.swing.ImageIcon icon, int pos, String message ) &rarr; void

Add the message to the messages in the legend.

### Parameters:
renderer - identifies the renderer adding to the legend
<br>icon - if non-null, an icon to use.  If null, the renderer's icon is used.
<br>pos - integer order parameter, and also identifies item.
<br>message - String message to display.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addToLegend&unscoped_q=addToLegend">[search for examples]</a>

***
<a name="contains"></a>
# contains
contains( int x, int y ) &rarr; boolean

since the plotVisible property can be false and the plot having 
 no renderers, we want the mouse events to pass on to elements below them.

### Parameters:
x - the mouse x
<br>y - the mouse y

### Returns:
true if the plot "contains" this point.

<a href="https://github.com/autoplot/dev/search?q=contains&unscoped_q=contains">[search for examples]</a>

***
<a name="containsRenderer"></a>
# containsRenderer
containsRenderer( org.das2.graph.Renderer rend ) &rarr; boolean

return true if the plot contains the renderer.

### Parameters:
rend - the renderer

### Returns:
true if the plot contains the renderer.

<a href="https://github.com/autoplot/dev/search?q=containsRenderer&unscoped_q=containsRenderer">[search for examples]</a>

***
<a name="createDummyPlot"></a>
# createDummyPlot
createDummyPlot(  ) &rarr; DasPlot

provide convenient method for creating a plot.  For example:
<blockquote><pre>
DasCanvas c= new DasCanvas(400,400);
DasPlot p= DasPlot.createDummyPlot( );
c.add(p,DasRow.create(c,0,1),DasColumn.create(c,0,1));
JOptionPane.showConfirmDialog(None,c)
</pre></blockquote>

### Returns:
a DasPlot, reader to be added to a canvas.

<a href="https://github.com/autoplot/dev/search?q=createDummyPlot&unscoped_q=createDummyPlot">[search for examples]</a>

***
<a name="createPlot"></a>
# createPlot
createPlot( DatumRange xrange, DatumRange yrange ) &rarr; DasPlot

provide convenient method for creating a plot.  For example:
<blockquote><pre> 
DasCanvas c= new DasCanvas(400,400);
DasPlot p= DasPlot.createPlot( DatumRangeUtil.parseTimeRange('2001'),DatumRange.newDatumRange(0,10,Units.dimensionless) );
c.add(p,DasRow.create(c,0,1),DasColumn.create(c,0,1));
JOptionPane.showConfirmDialog(None,c)
</pre></blockquote>

### Parameters:
xrange - the range for the x axis.
<br>yrange - the range for the y axis

### Returns:
a DasPlot, reader to be added to a canvas.

<a href="https://github.com/autoplot/dev/search?q=createPlot&unscoped_q=createPlot">[search for examples]</a>

***
<a name="findRendererAt"></a>
# findRendererAt
findRendererAt( int x, int y ) &rarr; int

return the index of the renderer at canvas location (x,y), or -1 if
 no renderer is found at the position.

### Parameters:
x - the x position on the canvas.
<br>y - the y position on the canvas.  Note 0,0 is the upper left corner.

### Returns:
the index of the renderer at the position, or -1 if no renderer is at the position.

<a href="https://github.com/autoplot/dev/search?q=findRendererAt&unscoped_q=findRendererAt">[search for examples]</a>

***
<a name="getActiveRegion"></a>
# getActiveRegion
getActiveRegion(  ) &rarr; Shape

return a Shape containing the plot.

### Returns:
a shape containing the active plot.

<a href="https://github.com/autoplot/dev/search?q=getActiveRegion&unscoped_q=getActiveRegion">[search for examples]</a>

***
<a name="getAxisClip"></a>
# getAxisClip
getAxisClip(  ) &rarr; Rectangle

return the Rectangle where data is drawn, useful for clipping.

### Returns:
Rectangle in canvas coordinates.
### See Also:
<a href='DasDevicePosition.md#toRectangle'>DasDevicePosition#toRectangle(org.das2.graph.DasRow, org.das2.graph.DasColumn)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getAxisClip&unscoped_q=getAxisClip">[search for examples]</a>

***
<a name="getBottomDecorator"></a>
# getBottomDecorator
getBottomDecorator(  ) &rarr; Painter



### Returns:
org.das2.graph.Painter


<a href="https://github.com/autoplot/dev/search?q=getBottomDecorator&unscoped_q=getBottomDecorator">[search for examples]</a>

***
<a name="getContext"></a>
# getContext
getContext(  ) &rarr; DatumRange

convenient place to put the plot context.  The context is used to
 store the timerange when there is no axis for it, for example, to
 show the state of data during a range.  This may change to a QDataSet
 to provide several context dimensions.

### Returns:
the context
### See Also:
<a href='#setContext'>setContext(org.das2.datum.DatumRange)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getContext&unscoped_q=getContext">[search for examples]</a>

***
<a name="getCustomizer"></a>
# getCustomizer
getCustomizer( org.das2.graph.CustomizerKey key ) &rarr; Customizer



### Parameters:
key - a CustomizerKey

### Returns:
org.das2.graph.Customizer


<a href="https://github.com/autoplot/dev/search?q=getCustomizer&unscoped_q=getCustomizer">[search for examples]</a>

***
<a name="getCustomizerKeys"></a>
# getCustomizerKeys
getCustomizerKeys(  ) &rarr; List

Return a list of keys of all current customizing objects in the order they would be invoked.

### Returns:
the keys

<a href="https://github.com/autoplot/dev/search?q=getCustomizerKeys&unscoped_q=getCustomizerKeys">[search for examples]</a>

***
<a name="getDasColorBar"></a>
# getDasColorBar
getDasColorBar(  ) &rarr; DasColorBar

return the colorbar associated with this DasPlot.  This loops
 through the renderers, from the top most to the bottom most,
 looking for the first with a non-null colorBar property.

### Returns:
null if not found or the dasColorBar most visible.

<a href="https://github.com/autoplot/dev/search?q=getDasColorBar&unscoped_q=getDasColorBar">[search for examples]</a>

***
<a name="getDisplayContext"></a>
# getDisplayContext
getDisplayContext(  ) &rarr; DatumRange



### Returns:
the property value
### See Also:
<a href='#PROP_DISPLAY_CONTEXT'>PROP_DISPLAY_CONTEXT</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getDisplayContext&unscoped_q=getDisplayContext">[search for examples]</a>

***
<a name="getDrawBackground"></a>
# getDrawBackground
getDrawBackground(  ) &rarr; Color

return the background color, where alpha=0 (transparent) means don't draw the background.

### Returns:
the background color.

<a href="https://github.com/autoplot/dev/search?q=getDrawBackground&unscoped_q=getDrawBackground">[search for examples]</a>

***
<a name="getDrawGridColor"></a>
# getDrawGridColor
getDrawGridColor(  ) &rarr; Color



### Returns:
the grid color
### See Also:
<a href='#PROP_DRAWGRIDCOLOR'>PROP_DRAWGRIDCOLOR</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getDrawGridColor&unscoped_q=getDrawGridColor">[search for examples]</a>

***
<a name="getFocusRenderer"></a>
# getFocusRenderer
getFocusRenderer(  ) &rarr; Renderer

get the current renderer that the operator has selected.

### Returns:
the current renderer that the operator has selected.

<a href="https://github.com/autoplot/dev/search?q=getFocusRenderer&unscoped_q=getFocusRenderer">[search for examples]</a>

***
<a name="getFontSize"></a>
# getFontSize
getFontSize(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getFontSize&unscoped_q=getFontSize">[search for examples]</a>

***
<a name="getLegendPosition"></a>
# getLegendPosition
getLegendPosition(  ) &rarr; LegendPosition



### Returns:
the current legend position
### See Also:
<a href='#PROP_LEGENDPOSITION'>PROP_LEGENDPOSITION</a> <br>
<a href='LegendPosition.md'>LegendPosition</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getLegendPosition&unscoped_q=getLegendPosition">[search for examples]</a>

***
<a name="getLegendRelativeFontSize"></a>
# getLegendRelativeFontSize
getLegendRelativeFontSize(  ) &rarr; int



### Returns:
the current relative size of the legend in points.
### See Also:
<a href='#PROP_LEGENDRELATIVESIZESIZE'>PROP_LEGENDRELATIVESIZESIZE</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getLegendRelativeFontSize&unscoped_q=getLegendRelativeFontSize">[search for examples]</a>

***
<a name="getLineThickness"></a>
# getLineThickness
getLineThickness(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getLineThickness&unscoped_q=getLineThickness">[search for examples]</a>

***
<a name="getLogLevel"></a>
# getLogLevel
getLogLevel(  ) &rarr; Level



### Returns:
level
### See Also:
<a href='#PROP_LOG_LEVEL'>PROP_LOG_LEVEL</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getLogLevel&unscoped_q=getLogLevel">[search for examples]</a>

***
<a name="getLogTimeoutSec"></a>
# getLogTimeoutSec
getLogTimeoutSec(  ) &rarr; int



### Returns:
property value
### See Also:
<a href='#PROP_LOG_TIMEOUT_SEC'>PROP_LOG_TIMEOUT_SEC</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getLogTimeoutSec&unscoped_q=getLogTimeoutSec">[search for examples]</a>

***
<a name="getMultiLineTextAlignment"></a>
# getMultiLineTextAlignment
getMultiLineTextAlignment(  ) &rarr; float

get the horizontal alignment for multiline labels, where 0 is left, 0.5 is center, and 1.0 is right.

### Returns:
the alignment

<a href="https://github.com/autoplot/dev/search?q=getMultiLineTextAlignment&unscoped_q=getMultiLineTextAlignment">[search for examples]</a>

***
<a name="getPaintCount"></a>
# getPaintCount
getPaintCount(  ) &rarr; int

get the diagnostic for the number of times the component was asked to paint
 itself since the last reset.

### Returns:
the number of times the component has painted itself.

<a href="https://github.com/autoplot/dev/search?q=getPaintCount&unscoped_q=getPaintCount">[search for examples]</a>

***
<a name="getPrintingLogLevel"></a>
# getPrintingLogLevel
getPrintingLogLevel(  ) &rarr; Level



### Returns:
the level
### See Also:
<a href='#PROP_PRINTINGLOGLEVEL'>PROP_PRINTINGLOGLEVEL</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getPrintingLogLevel&unscoped_q=getPrintingLogLevel">[search for examples]</a>

***
<a name="getRenderer"></a>
# getRenderer
getRenderer( int index ) &rarr; Renderer

return one of the renderers, which paint the data on to the plot.

### Parameters:
index - the index of the renderer

### Returns:
the renderer

<a href="https://github.com/autoplot/dev/search?q=getRenderer&unscoped_q=getRenderer">[search for examples]</a>

***
<a name="getRenderers"></a>
# getRenderers
getRenderers(  ) &rarr; Renderer

return a list of the renderers, which paint the data on to the plot.
 This makes a copy of the renderer array.

### Returns:
the Renderer

<a href="https://github.com/autoplot/dev/search?q=getRenderers&unscoped_q=getRenderers">[search for examples]</a>

***
<a name="getTitle"></a>
# getTitle
getTitle(  ) &rarr; String

Returns the title of this plot.

### Returns:
The plot title
### See Also:
<a href='#setTitle'>setTitle(String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getTitle&unscoped_q=getTitle">[search for examples]</a>

***
<a name="getTopDecorator"></a>
# getTopDecorator
getTopDecorator(  ) &rarr; Painter



### Returns:
org.das2.graph.Painter


<a href="https://github.com/autoplot/dev/search?q=getTopDecorator&unscoped_q=getTopDecorator">[search for examples]</a>

***
<a name="getXAxis"></a>
# getXAxis
getXAxis(  ) &rarr; DasAxis

return the x (horizontal) axis.

### Returns:
the x axis

<a href="https://github.com/autoplot/dev/search?q=getXAxis&unscoped_q=getXAxis">[search for examples]</a>

***
<a name="getYAxis"></a>
# getYAxis
getYAxis(  ) &rarr; DasAxis

return the y (vertical) axis

### Returns:
the y axis

<a href="https://github.com/autoplot/dev/search?q=getYAxis&unscoped_q=getYAxis">[search for examples]</a>

***
<a name="invalidateCacheImage"></a>
# invalidateCacheImage
invalidateCacheImage(  ) &rarr; void

mark the dasPlot's cache image as invalid, forcing it to repaint.
 TODO: when should a user use invalidateCacheImage vs markDirty?

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=invalidateCacheImage&unscoped_q=invalidateCacheImage">[search for examples]</a>

***
<a name="invalidateCacheImageNoUpdate"></a>
# invalidateCacheImageNoUpdate
invalidateCacheImageNoUpdate(  ) &rarr; void

mark the dasPlot's cache image as invalid, but from the update method, so
 we don't need to update. (Updating results in a loop.)

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=invalidateCacheImageNoUpdate&unscoped_q=invalidateCacheImageNoUpdate">[search for examples]</a>

***
<a name="isCacheImageValid"></a>
# isCacheImageValid
isCacheImageValid(  ) &rarr; boolean

introduced to debug Autoplot test018.  This should not be used otherwise.

### Returns:
true if the cache image is marked as valid.

<a href="https://github.com/autoplot/dev/search?q=isCacheImageValid&unscoped_q=isCacheImageValid">[search for examples]</a>

***
<a name="isDisplayLegend"></a>
# isDisplayLegend
isDisplayLegend(  ) &rarr; boolean

true if the legend should be displayed

### Returns:
true if the legend should be displayed

<a href="https://github.com/autoplot/dev/search?q=isDisplayLegend&unscoped_q=isDisplayLegend">[search for examples]</a>

***
<a name="isDisplayTitle"></a>
# isDisplayTitle
isDisplayTitle(  ) &rarr; boolean

return the state of enable/disable display of the title.

### Returns:
the current state.
### See Also:
<a href='#setDisplayTitle'>setDisplayTitle(boolean)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isDisplayTitle&unscoped_q=isDisplayTitle">[search for examples]</a>

***
<a name="isDrawDebugMessages"></a>
# isDrawDebugMessages
isDrawDebugMessages(  ) &rarr; boolean



### Returns:
true if the messages should be shown.
### See Also:
<a href='#PROP_DRAWDEBUGMESSAGES'>PROP_DRAWDEBUGMESSAGES</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isDrawDebugMessages&unscoped_q=isDrawDebugMessages">[search for examples]</a>

***
<a name="isDrawGrid"></a>
# isDrawGrid
isDrawGrid(  ) &rarr; boolean

Getter for property drawGrid.  If true, faint grey lines continue the axis major
 ticks across the plot.

### Returns:
Value of property drawGrid.

<a href="https://github.com/autoplot/dev/search?q=isDrawGrid&unscoped_q=isDrawGrid">[search for examples]</a>

***
<a name="isDrawGridOver"></a>
# isDrawGridOver
isDrawGridOver(  ) &rarr; boolean



### Returns:
true if the grid is on top of the data.
### See Also:
<a href='#PROP_DRAWGRIDOVER'>PROP_DRAWGRIDOVER</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isDrawGridOver&unscoped_q=isDrawGridOver">[search for examples]</a>

***
<a name="isDrawMinorGrid"></a>
# isDrawMinorGrid
isDrawMinorGrid(  ) &rarr; boolean

Get the value of drawMinorGrid

### Returns:
the value of drawMinorGrid
### See Also:
<a href='#PROP_DRAWMINORGRID'>PROP_DRAWMINORGRID</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isDrawMinorGrid&unscoped_q=isDrawMinorGrid">[search for examples]</a>

***
<a name="isIsotropic"></a>
# isIsotropic
isIsotropic(  ) &rarr; boolean



### Returns:
property value
### See Also:
<a href='#PROP_ISOTROPIC'>PROP_ISOTROPIC</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isIsotropic&unscoped_q=isIsotropic">[search for examples]</a>

***
<a name="isOverSize"></a>
# isOverSize
isOverSize(  ) &rarr; boolean



### Returns:
oversize property
### See Also:
<a href='#PROP_OVERSIZE'>PROP_OVERSIZE</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isOverSize&unscoped_q=isOverSize">[search for examples]</a>

***
<a name="isPlotVisible"></a>
# isPlotVisible
isPlotVisible(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isPlotVisible&unscoped_q=isPlotVisible">[search for examples]</a>

***
<a name="isPreviewEnabled"></a>
# isPreviewEnabled
isPreviewEnabled(  ) &rarr; boolean

true if the data rendering will be scaled immediately to indicate 
 axis state changes.

### Returns:
true if preview is enabled.

<a href="https://github.com/autoplot/dev/search?q=isPreviewEnabled&unscoped_q=isPreviewEnabled">[search for examples]</a>

***
<a name="postException"></a>
# postException
postException( org.das2.graph.Renderer renderer, java.lang.Exception exception ) &rarr; void

notify user of an exception, in the context of the plot.  This is similar
 to postMessage(renderer, exception.getMessage(), DasPlot.SEVERE, null, null )
 except that it does catch CancelledOperationExceptions and reduced the
 severity since the user probably initiated the condition.

### Parameters:
renderer - the renderer posting the exception.
<br>exception - the exception to post.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=postException&unscoped_q=postException">[search for examples]</a>

***
<a name="postMessage"></a>
# postMessage
postMessage( org.das2.graph.Renderer renderer, String message, int messageType, Datum x, Datum y ) &rarr; void

Notify user of an exception, in the context of the plot.  A position in
 the data space may be specified to locate the text within the data context.
 Note either or both x or y may be null.  Messages must only be posted while the
 Renderer's render method is called, not during updatePlotImage.  All messages are
 cleared before the render step. (TODO:check on this)

### Parameters:
renderer - identifies the renderer posting the exception
<br>message - the text to be displayed, may contain granny text.
<br>messageType - DasPlot.INFO, DasPlot.WARNING, or DasPlot.SEVERE.  (SEVERE was ERROR before)
<br>x - if non-null, the location on the x axis giving context for the text.
<br>y - if non-null, the location on the y axis giving context for the text.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=postMessage&unscoped_q=postMessage">[search for examples]</a>

postMessage( org.das2.graph.Renderer renderer, String message, java.util.logging.Level messageLevel, Datum x, Datum y ) &rarr; void<br>
***
<a name="releaseAll"></a>
# releaseAll
releaseAll(  ) &rarr; void

In Autoplot, we need a way to get help releasing all resources.  This
 clears out all the mouse modules, axis references, etc.  Basically anything
 that could have a reference to other parts of the system that we know we
 don't need here, explicitly remove the reference.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=releaseAll&unscoped_q=releaseAll">[search for examples]</a>

***
<a name="removeCustomizer"></a>
# removeCustomizer
removeCustomizer( org.das2.graph.CustomizerKey key ) &rarr; void

Remove the customizer that is associated with the given key.

### Parameters:
key - the key to the customizer to be removed.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeCustomizer&unscoped_q=removeCustomizer">[search for examples]</a>

***
<a name="removeRenderer"></a>
# removeRenderer
removeRenderer( org.das2.graph.Renderer rend ) &rarr; void

remove the renderer from the stack of renderers.  A warning 
 is logged if the renderer is not present.

### Parameters:
rend - the renderer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeRenderer&unscoped_q=removeRenderer">[search for examples]</a>

***
<a name="removeRenderers"></a>
# removeRenderers
removeRenderers(  ) &rarr; void

remove all the renderers from the dasPlot.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeRenderers&unscoped_q=removeRenderers">[search for examples]</a>

***
<a name="repaint"></a>
# repaint
repaint(  ) &rarr; void

request that the plot be repainted.  This contains commented code that
 counts the number of repaints.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=repaint&unscoped_q=repaint">[search for examples]</a>

***
<a name="resetPaintCount"></a>
# resetPaintCount
resetPaintCount(  ) &rarr; void

reset the paint counter.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resetPaintCount&unscoped_q=resetPaintCount">[search for examples]</a>

***
<a name="resize"></a>
# resize
resize(  ) &rarr; void

recalculate the bounds of the component.  TODO: this is used a lot and needs to be explained in more detail.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resize&unscoped_q=resize">[search for examples]</a>

***
<a name="setAxisPlotVisible"></a>
# setAxisPlotVisible
setAxisPlotVisible( boolean visible ) &rarr; void

set the visibility of both the plot and its x and y axes.  Recently,
 setVisible(v) would do this, but it incorrectly couples the visible properties
 of the separate components.

### Parameters:
visible - false if the x and y axes, and the plot is visisble.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAxisPlotVisible&unscoped_q=setAxisPlotVisible">[search for examples]</a>

***
<a name="setBottomDecorator"></a>
# setBottomDecorator
setBottomDecorator( org.das2.graph.Painter bottomDecorator ) &rarr; void

add additional painting code to the renderer, which is called after 
 the renderer is called.

### Parameters:
bottomDecorator - the Painter to call, or null to clear.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setBottomDecorator&unscoped_q=setBottomDecorator">[search for examples]</a>

***
<a name="setContext"></a>
# setContext
setContext( DatumRange context ) &rarr; void

convenient place to put the plot context.  The context is used to
 store the timerange when there is no axis for it, for example, to
 show the state of data during a range.  This may change to a QDataSet
 to provide several context dimensions.  Note this may be null to support
 no context.

### Parameters:
context - the context

### Returns:
void (returns nothing)

### See Also:
<a href='#getContext'>getContext()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setContext&unscoped_q=setContext">[search for examples]</a>

***
<a name="setDisplayContext"></a>
# setDisplayContext
setDisplayContext( DatumRange displayContext ) &rarr; void

set the property

### Parameters:
displayContext - null or the display context.

### Returns:
void (returns nothing)

### See Also:
<a href='#PROP_DISPLAY_CONTEXT'>PROP_DISPLAY_CONTEXT</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setDisplayContext&unscoped_q=setDisplayContext">[search for examples]</a>

***
<a name="setDisplayLegend"></a>
# setDisplayLegend
setDisplayLegend( boolean displayLegend ) &rarr; void

true if the legend should be displayed

### Parameters:
displayLegend - true if the legend should be displayed

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDisplayLegend&unscoped_q=setDisplayLegend">[search for examples]</a>

***
<a name="setDisplayTitle"></a>
# setDisplayTitle
setDisplayTitle( boolean v ) &rarr; void

enable/disable display of the title.  Often the title contains
 useful information describing the plot content that we want to know during
 interactive use but not when the plot is printed.

### Parameters:
v - true if the title should be displayed.

### Returns:
void (returns nothing)

### See Also:
<a href='#isDisplayTitle'>isDisplayTitle()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setDisplayTitle&unscoped_q=setDisplayTitle">[search for examples]</a>

***
<a name="setDrawBackground"></a>
# setDrawBackground
setDrawBackground( java.awt.Color drawBackground ) &rarr; void

if not transparent, draw this background first.

### Parameters:
drawBackground - the background, or a color with no opacity (new Color(0,0,0,0)) to turn off.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDrawBackground&unscoped_q=setDrawBackground">[search for examples]</a>

***
<a name="setDrawDebugMessages"></a>
# setDrawDebugMessages
setDrawDebugMessages( boolean v ) &rarr; void



### Parameters:
v - true if the messages should be shown.

### Returns:
void (returns nothing)

### See Also:
<a href='#PROP_DRAWDEBUGMESSAGES'>PROP_DRAWDEBUGMESSAGES</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setDrawDebugMessages&unscoped_q=setDrawDebugMessages">[search for examples]</a>

***
<a name="setDrawGrid"></a>
# setDrawGrid
setDrawGrid( boolean drawGrid ) &rarr; void

Setter for property drawGrid.  If true, faint grey lines continue the axis major
 ticks across the plot.

### Parameters:
drawGrid - New value of property drawGrid.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDrawGrid&unscoped_q=setDrawGrid">[search for examples]</a>

***
<a name="setDrawGridColor"></a>
# setDrawGridColor
setDrawGridColor( java.awt.Color drawGridColor ) &rarr; void

if not transparent, draw the grid in this color.  Otherwise
 the grid is drawn with the tick color.

### Parameters:
drawGridColor - the color

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDrawGridColor&unscoped_q=setDrawGridColor">[search for examples]</a>

***
<a name="setDrawGridOver"></a>
# setDrawGridOver
setDrawGridOver( boolean gridOver ) &rarr; void



### Parameters:
gridOver - if the grid is on top of the data.

### Returns:
void (returns nothing)

### See Also:
<a href='#PROP_DRAWGRIDOVER'>PROP_DRAWGRIDOVER</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setDrawGridOver&unscoped_q=setDrawGridOver">[search for examples]</a>

***
<a name="setDrawMinorGrid"></a>
# setDrawMinorGrid
setDrawMinorGrid( boolean newdrawMinorGrid ) &rarr; void

Set the value of drawMinorGrid

### Parameters:
newdrawMinorGrid - new value of drawMinorGrid

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDrawMinorGrid&unscoped_q=setDrawMinorGrid">[search for examples]</a>

***
<a name="setEnableRenderPropertiesAction"></a>
# setEnableRenderPropertiesAction
setEnableRenderPropertiesAction( boolean b ) &rarr; void

add or remove the menu item to get at the renderer properties.
 Das2 applications generally allow this so that applications don't have
 to bother handling this.  Others like Autoplot have their own systems 
 and uses for the click.

### Parameters:
b - false to remove the menu item if it has been added.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setEnableRenderPropertiesAction&unscoped_q=setEnableRenderPropertiesAction">[search for examples]</a>

***
<a name="setFocusRenderer"></a>
# setFocusRenderer
setFocusRenderer( org.das2.graph.Renderer focusRenderer ) &rarr; void

set the current renderer that the operator has selected.

### Parameters:
focusRenderer - the current renderer that the operator has selected.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFocusRenderer&unscoped_q=setFocusRenderer">[search for examples]</a>

***
<a name="setFontSize"></a>
# setFontSize
setFontSize( String fontSize ) &rarr; void



### Parameters:
fontSize - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFontSize&unscoped_q=setFontSize">[search for examples]</a>

***
<a name="setIsotropic"></a>
# setIsotropic
setIsotropic( boolean isotropic ) &rarr; void

set the property value

### Parameters:
isotropic - property value

### Returns:
void (returns nothing)

### See Also:
<a href='#PROP_ISOTROPIC'>PROP_ISOTROPIC</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setIsotropic&unscoped_q=setIsotropic">[search for examples]</a>

***
<a name="setLegendPosition"></a>
# setLegendPosition
setLegendPosition( org.das2.graph.LegendPosition newlegendPosition ) &rarr; void



### Parameters:
newlegendPosition - the legend position

### Returns:
void (returns nothing)

### See Also:
<a href='#PROP_LEGENDPOSITION'>PROP_LEGENDPOSITION</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setLegendPosition&unscoped_q=setLegendPosition">[search for examples]</a>

***
<a name="setLegendRelativeFontSize"></a>
# setLegendRelativeFontSize
setLegendRelativeFontSize( int size ) &rarr; void

set the relative size of the legend element text.

### Parameters:
size - relative size in points.

### Returns:
void (returns nothing)

### See Also:
<a href='#PROP_LEGENDRELATIVESIZESIZE'>PROP_LEGENDRELATIVESIZESIZE</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setLegendRelativeFontSize&unscoped_q=setLegendRelativeFontSize">[search for examples]</a>

***
<a name="setLineThickness"></a>
# setLineThickness
setLineThickness( String lineThickness ) &rarr; void

set the thickness of the lines drawn.

### Parameters:
lineThickness - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLineThickness&unscoped_q=setLineThickness">[search for examples]</a>

***
<a name="setLogLevel"></a>
# setLogLevel
setLogLevel( java.util.logging.Level level ) &rarr; void



### Parameters:
level - where Level.INFO is the default.

### Returns:
void (returns nothing)

### See Also:
<a href='#PROP_LOG_LEVEL'>PROP_LOG_LEVEL</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setLogLevel&unscoped_q=setLogLevel">[search for examples]</a>

***
<a name="setLogTimeoutSec"></a>
# setLogTimeoutSec
setLogTimeoutSec( int logTimeoutSec ) &rarr; void



### Parameters:
logTimeoutSec - the property value

### Returns:
void (returns nothing)

### See Also:
<a href='#PROP_LOG_TIMEOUT_SEC'>PROP_LOG_TIMEOUT_SEC</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setLogTimeoutSec&unscoped_q=setLogTimeoutSec">[search for examples]</a>

***
<a name="setMultiLineTextAlignment"></a>
# setMultiLineTextAlignment
setMultiLineTextAlignment( float multiLineTextAlignment ) &rarr; void

set the horizontal alignment for multiline labels, where 0 is left, 0.5 is center, and 1.0 is right.

### Parameters:
multiLineTextAlignment - the alignment

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMultiLineTextAlignment&unscoped_q=setMultiLineTextAlignment">[search for examples]</a>

***
<a name="setOverSize"></a>
# setOverSize
setOverSize( boolean overSize ) &rarr; void



### Parameters:
overSize - true means draw outside the axis bounds.

### Returns:
void (returns nothing)

### See Also:
<a href='#PROP_OVERSIZE'>PROP_OVERSIZE</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setOverSize&unscoped_q=setOverSize">[search for examples]</a>

***
<a name="setPlotVisible"></a>
# setPlotVisible
setPlotVisible( boolean plotVisible ) &rarr; void



### Parameters:
plotVisible - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPlotVisible&unscoped_q=setPlotVisible">[search for examples]</a>

***
<a name="setPreviewEnabled"></a>
# setPreviewEnabled
setPreviewEnabled( boolean preview ) &rarr; void

if true then the data rendering will be scaled immediately to indicate 
 axis state changes.

### Parameters:
preview - true if preview should be enabled.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPreviewEnabled&unscoped_q=setPreviewEnabled">[search for examples]</a>

***
<a name="setPrintingLogLevel"></a>
# setPrintingLogLevel
setPrintingLogLevel( java.util.logging.Level printingLogLevel ) &rarr; void



### Parameters:
printingLogLevel - where Level.ALL is the default.

### Returns:
void (returns nothing)

### See Also:
<a href='#PROP_PRINTINGLOGLEVEL'>PROP_PRINTINGLOGLEVEL</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setPrintingLogLevel&unscoped_q=setPrintingLogLevel">[search for examples]</a>

***
<a name="setReduceOutsideLegendTopMargin"></a>
# setReduceOutsideLegendTopMargin
setReduceOutsideLegendTopMargin( boolean reduceOutsideLegendTopMargin ) &rarr; void

Used at APL for layout.  This is off by default.  This appears to shift the Y position.

### Parameters:
reduceOutsideLegendTopMargin - shift the Y position.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setReduceOutsideLegendTopMargin&unscoped_q=setReduceOutsideLegendTopMargin">[search for examples]</a>

***
<a name="setTitle"></a>
# setTitle
setTitle( String t ) &rarr; void

Sets the title which will be displayed above this plot.  
 null or empty string may be used to turn off the title.

### Parameters:
t - The new title for this plot.

### Returns:
void (returns nothing)

### See Also:
<a href='#setDisplayTitle'>setDisplayTitle(boolean)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setTitle&unscoped_q=setTitle">[search for examples]</a>

***
<a name="setTopDecorator"></a>
# setTopDecorator
setTopDecorator( org.das2.graph.Painter topDecorator ) &rarr; void

add additional painting code to the renderer, which is called after 
 the renderer is called.

### Parameters:
topDecorator - the Painter to call, or null to clear.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTopDecorator&unscoped_q=setTopDecorator">[search for examples]</a>

***
<a name="setXAxis"></a>
# setXAxis
setXAxis( org.das2.graph.DasAxis xAxis ) &rarr; void

set the x axis.  This removes property change listeners to the old
 axis and adds PCLs to the new axis.

### Parameters:
xAxis - a horizontal axis.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setXAxis&unscoped_q=setXAxis">[search for examples]</a>

***
<a name="setYAxis"></a>
# setYAxis
setYAxis( org.das2.graph.DasAxis yAxis ) &rarr; void

Attaches a new axis to the plot.  The old axis is disconnected, and
 the plot will listen to the new axis.  Also, the row and column for the
 axis is set, but this might change in the future.  null appears to be
 a valid input as well.

 TODO: plot does not seem to be responding to changes in the axis.
 (goes grey because updatePlotImage is never done.

### Parameters:
yAxis - a vertical axis.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setYAxis&unscoped_q=setYAxis">[search for examples]</a>

