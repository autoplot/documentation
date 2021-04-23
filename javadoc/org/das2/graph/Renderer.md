# org.das2.graph.Renderer



***
<a name="PROP_BOTTOMDECORATOR"></a>
# PROP_BOTTOMDECORATOR



***
<a name="PROP_TOPDECORATOR"></a>
# PROP_TOPDECORATOR



***
<a name="CONTROL_KEY_COLOR"></a>
# CONTROL_KEY_COLOR

allocate a bunch of canonical properties.  See http://autoplot.org/developer.guessRenderType#Proposed_extensions

***
<a name="CONTROL_KEY_FILL_COLOR"></a>
# CONTROL_KEY_FILL_COLOR



***
<a name="CONTROL_KEY_FILL_DIRECTION"></a>
# CONTROL_KEY_FILL_DIRECTION



***
<a name="CONTROL_KEY_COLOR_TABLE"></a>
# CONTROL_KEY_COLOR_TABLE



***
<a name="CONTROL_KEY_LINE_THICK"></a>
# CONTROL_KEY_LINE_THICK



***
<a name="CONTROL_KEY_LINE_STYLE"></a>
# CONTROL_KEY_LINE_STYLE



***
<a name="CONTROL_KEY_SYMBOL"></a>
# CONTROL_KEY_SYMBOL



***
<a name="CONTROL_KEY_SYMBOL_SIZE"></a>
# CONTROL_KEY_SYMBOL_SIZE



***
<a name="CONTROL_KEY_FONT_SIZE"></a>
# CONTROL_KEY_FONT_SIZE

font size relative to the parent, so "" or "1em" is the same size.

***
<a name="CONTROL_KEY_REFERENCE"></a>
# CONTROL_KEY_REFERENCE



***
<a name="CONTROL_KEY_DRAW_ERROR"></a>
# CONTROL_KEY_DRAW_ERROR



***
<a name="PROP_CONTROL"></a>
# PROP_CONTROL



***
<a name="PROP_ACTIVE"></a>
# PROP_ACTIVE

display the renderer.  This is allows a renderer to be disabled without removing it from the application.

***
<a name="PROP_LEGENDLABEL"></a>
# PROP_LEGENDLABEL

If non-null and non-zero-length, use this label to describe the renderer
 in the plot's legend.

***
<a name="PROP_DRAWLEGENDLABEL"></a>
# PROP_DRAWLEGENDLABEL

true if the legend label should be drawn.

***
<a name="PROP_ID"></a>
# PROP_ID



***
<a name="PROP_COLORBAR"></a>
# PROP_COLORBAR



***
<a name="PROP_RECORDFILE"></a>
# PROP_RECORDFILE



***
<a name="acceptContext"></a>
# acceptContext
acceptContext( int x, int y ) &rarr; boolean

Returns true if the render will accept the context for a point.  
 That is, the renderer affected that point, or nearby points.  This is 
 used currently to provide a way for the operator to click on a plot and 
 directly edit the renderer which drew the pixel.

### Parameters:
x - the x coordinate in the canvas coordinate system.
<br>y - the y coordinate in the canvas coordinate system.

### Returns:
true if the renderer will accept the context.

<a href="https://github.com/autoplot/dev/search?q=acceptContext&unscoped_q=acceptContext">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="acceptsDataSet"></a>
# acceptsDataSet
acceptsDataSet( QDataSet ds ) &rarr; boolean

return true if the dataset appears to be in a scheme accepted by this renderer.  This should assume that axis
 units can be reset, etc.

### Parameters:
ds - a QDataSet

### Returns:
true if the dataset appears to be acceptable.

<a href="https://github.com/autoplot/dev/search?q=acceptsDataSet&unscoped_q=acceptsDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void

Adds a PropertyChangeListener to the listener list.

### Parameters:
l - The listener to add.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addPropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="decodePlotSymbolConnectorControl"></a>
# decodePlotSymbolConnectorControl
decodePlotSymbolConnectorControl( String s, org.das2.graph.PsymConnector deflt ) &rarr; PsymConnector

decode the string into a plot symbol.

### Parameters:
s - the symbol name, such as none, dashes, dashFine
<br>deflt - the symbol to use when the value is not parsed.

### Returns:
the parsed value.

<a href="https://github.com/autoplot/dev/search?q=decodePlotSymbolConnectorControl&unscoped_q=decodePlotSymbolConnectorControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="decodePlotSymbolControl"></a>
# decodePlotSymbolControl
decodePlotSymbolControl( String s, org.das2.graph.PlotSymbol deflt ) &rarr; PlotSymbol

decode the string into a plot symbol.

### Parameters:
s - the symbol name, such as none, circles, triangles, cross, ex, star, diamond, box
<br>deflt - the symbol to use when the value is not parsed.

### Returns:
the parsed value.

<a href="https://github.com/autoplot/dev/search?q=decodePlotSymbolControl&unscoped_q=decodePlotSymbolControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="drawListIcon"></a>
# drawListIcon
drawListIcon( java.awt.Graphics2D g, int x, int y ) &rarr; void



### Parameters:
g - a Graphics2D
<br>x - an int
<br>y - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=drawListIcon&unscoped_q=drawListIcon">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="encodeBooleanControl"></a>
# encodeBooleanControl
encodeBooleanControl( boolean v ) &rarr; String

return the encoding for the boolean value.

### Parameters:
v - the boolean value.

### Returns:
"T" or "F"

<a href="https://github.com/autoplot/dev/search?q=encodeBooleanControl&unscoped_q=encodeBooleanControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="encodeColorControl"></a>
# encodeColorControl
encodeColorControl( java.awt.Color color ) &rarr; String

encode the Color control.

### Parameters:
color - a Color

### Returns:
the color encoded as a string.
### See Also:
<a href='ColorUtil.md#encodeColor'>ColorUtil#encodeColor(java.awt.Color)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=encodeColorControl&unscoped_q=encodeColorControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="encodePlotSymbolConnectorControl"></a>
# encodePlotSymbolConnectorControl
encodePlotSymbolConnectorControl( org.das2.graph.PsymConnector psymConnector ) &rarr; String

encode the plot symbol connector as a string, such as:
 solid, dotted

### Parameters:
psymConnector - a PsymConnector

### Returns:
the string encoding.

<a href="https://github.com/autoplot/dev/search?q=encodePlotSymbolConnectorControl&unscoped_q=encodePlotSymbolConnectorControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="encodePlotSymbolControl"></a>
# encodePlotSymbolControl
encodePlotSymbolControl( org.das2.graph.PlotSymbol psym ) &rarr; String

encode the plot symbol as a string, such as:
 none, circles, triangles, cross, ex, star, diamond, box

### Parameters:
psym - the plot symbol.

### Returns:
the string encoding.

<a href="https://github.com/autoplot/dev/search?q=encodePlotSymbolControl&unscoped_q=encodePlotSymbolControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="formatControl"></a>
# formatControl
formatControl( java.util.Map c ) &rarr; String

convenient and official location for method that formats control string.

### Parameters:
c - a java.util.Map

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=formatControl&unscoped_q=formatControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBooleanControl"></a>
# getBooleanControl
getBooleanControl( String key, boolean deft ) &rarr; boolean

get the boolean control.

### Parameters:
key - the key name.
<br>deft - the default value.

### Returns:
the boolean value, where "T" is true, false otherwise; or the default when the value is not found.

<a href="https://github.com/autoplot/dev/search?q=getBooleanControl&unscoped_q=getBooleanControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBottomDecorator"></a>
# getBottomDecorator
getBottomDecorator(  ) &rarr; Painter



### Returns:
org.das2.graph.Painter


<a href="https://github.com/autoplot/dev/search?q=getBottomDecorator&unscoped_q=getBottomDecorator">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getColorBar"></a>
# getColorBar
getColorBar(  ) &rarr; DasColorBar

get the colorbar for the renderer.

### Returns:
the colorbar for the renderer.

<a href="https://github.com/autoplot/dev/search?q=getColorBar&unscoped_q=getColorBar">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getColorControl"></a>
# getColorControl
getColorControl( String key, java.awt.Color deft ) &rarr; Color

get the Color control.

### Parameters:
key - the key name.
<br>deft - the default value

### Returns:
the Color or the default when the value is not found.
### See Also:
<a href='ColorUtil.md#decodeColor'>ColorUtil#decodeColor(java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getColorControl&unscoped_q=getColorControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getConsumedDataSet"></a>
# getConsumedDataSet
getConsumedDataSet(  ) &rarr; QDataSet

return the data for DataSetConsumer, which might be rebinned.

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=getConsumedDataSet&unscoped_q=getConsumedDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getControl"></a>
# getControl
getControl(  ) &rarr; String

get the string which summarizes the state of the renderer.  These allow a compact string to contain the renderer settings.
 This should be an ampersand-delimited list of name=value pairs.

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getControl&unscoped_q=getControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getControl( String key, String deft ) &rarr; String<br>
***
<a name="getDataLoader"></a>
# getDataLoader
getDataLoader(  ) &rarr; DataLoader



### Returns:
org.das2.graph.DataLoader


<a href="https://github.com/autoplot/dev/search?q=getDataLoader&unscoped_q=getDataLoader">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSet"></a>
# getDataSet
getDataSet(  ) &rarr; QDataSet

returns the current dataset being displayed.

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSetDescriptor"></a>
# getDataSetDescriptor
getDataSetDescriptor(  ) &rarr; DataSetDescriptor



### Returns:
org.das2.dataset.DataSetDescriptor


<a href="https://github.com/autoplot/dev/search?q=getDataSetDescriptor&unscoped_q=getDataSetDescriptor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSetID"></a>
# getDataSetID
getDataSetID(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getDataSetID&unscoped_q=getDataSetID">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDatumControl"></a>
# getDatumControl
getDatumControl( String key, Datum deft ) &rarr; Datum

get the Datum control.

### Parameters:
key - the key name.
<br>deft - the default value, which also provides the units.

### Returns:
the Datum or the default when the value is not found.

<a href="https://github.com/autoplot/dev/search?q=getDatumControl&unscoped_q=getDatumControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDoubleArrayControl"></a>
# getDoubleArrayControl
getDoubleArrayControl( String key, double[] deft ) &rarr; double

get the double array control.  These should be encoded on a string
 with commas delimiting values.

### Parameters:
key - the key name.
<br>deft - the default value.

### Returns:
the double array, each element parsed with Double.parseDouble or the default when the value is not found.

<a href="https://github.com/autoplot/dev/search?q=getDoubleArrayControl&unscoped_q=getDoubleArrayControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDoubleControl"></a>
# getDoubleControl
getDoubleControl( String key, double deft ) &rarr; double

get the double control.

### Parameters:
key - the key name.
<br>deft - the default value.

### Returns:
the double, parsed with Double.parseDouble; or the default when the value is not found.

<a href="https://github.com/autoplot/dev/search?q=getDoubleControl&unscoped_q=getDoubleControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getId"></a>
# getId
getId(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getId&unscoped_q=getId">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getIntegerControl"></a>
# getIntegerControl
getIntegerControl( String key, int deft ) &rarr; int

get the integer control.

### Parameters:
key - the key name.
<br>deft - the default value.

### Returns:
the int, parsed with Integer.parseInt; or the default when the value is not found.

<a href="https://github.com/autoplot/dev/search?q=getIntegerControl&unscoped_q=getIntegerControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLastException"></a>
# getLastException
getLastException(  ) &rarr; Exception



### Returns:
java.lang.Exception


<a href="https://github.com/autoplot/dev/search?q=getLastException&unscoped_q=getLastException">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLegendLabel"></a>
# getLegendLabel
getLegendLabel(  ) &rarr; String

get the label to describe the renderer in the plot's legend.   
 If zero-length, then the legend label should be hidden.

### Returns:
the label to describe the renderer

<a href="https://github.com/autoplot/dev/search?q=getLegendLabel&unscoped_q=getLegendLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getListIcon"></a>
# getListIcon
getListIcon(  ) &rarr; Icon



### Returns:
javax.swing.Icon


<a href="https://github.com/autoplot/dev/search?q=getListIcon&unscoped_q=getListIcon">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getListLabel"></a>
# getListLabel
getListLabel(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getListLabel&unscoped_q=getListLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getParent"></a>
# getParent
getParent(  ) &rarr; DasPlot



### Returns:
org.das2.graph.DasPlot


<a href="https://github.com/autoplot/dev/search?q=getParent&unscoped_q=getParent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRenderCount"></a>
# getRenderCount
getRenderCount(  ) &rarr; int

return the number of times render has been called since the last reset.

### Returns:
number of times render has been called since the last reset.

<a href="https://github.com/autoplot/dev/search?q=getRenderCount&unscoped_q=getRenderCount">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getStatsFile"></a>
# getStatsFile
getStatsFile(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getStatsFile&unscoped_q=getStatsFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTopDecorator"></a>
# getTopDecorator
getTopDecorator(  ) &rarr; Painter



### Returns:
org.das2.graph.Painter


<a href="https://github.com/autoplot/dev/search?q=getTopDecorator&unscoped_q=getTopDecorator">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getUpdateCount"></a>
# getUpdateCount
getUpdateCount(  ) &rarr; int

return the number of times updatePlotImage has been called since the last reset.

### Returns:
the number of times updatePlotImage has been called since the last reset.

<a href="https://github.com/autoplot/dev/search?q=getUpdateCount&unscoped_q=getUpdateCount">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getXmemento"></a>
# getXmemento
getXmemento(  ) &rarr; Memento



### Returns:
org.das2.graph.DasAxis.Memento


<a href="https://github.com/autoplot/dev/search?q=getXmemento&unscoped_q=getXmemento">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getYmemento"></a>
# getYmemento
getYmemento(  ) &rarr; Memento



### Returns:
org.das2.graph.DasAxis.Memento


<a href="https://github.com/autoplot/dev/search?q=getYmemento&unscoped_q=getYmemento">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasControl"></a>
# hasControl
hasControl( String key ) &rarr; boolean

return true if the control is specified.

### Parameters:
key - the key name

### Returns:
true if the control is specified.

<a href="https://github.com/autoplot/dev/search?q=hasControl&unscoped_q=hasControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isActive"></a>
# isActive
isActive(  ) &rarr; boolean

true when the renderer should be drawn.

### Returns:
true when the renderer should be drawn.

<a href="https://github.com/autoplot/dev/search?q=isActive&unscoped_q=isActive">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDrawLegendLabel"></a>
# isDrawLegendLabel
isDrawLegendLabel(  ) &rarr; boolean

get the switch used to turn off legend label.  This allows the label
 to be hidden without loosing the information it provides.

### Returns:
true if the legend label should be drawn

<a href="https://github.com/autoplot/dev/search?q=isDrawLegendLabel&unscoped_q=isDrawLegendLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDumpDataSet"></a>
# isDumpDataSet
isDumpDataSet(  ) &rarr; boolean

Getter for property dumpDataSet.

### Returns:
Value of property dumpDataSet.

<a href="https://github.com/autoplot/dev/search?q=isDumpDataSet&unscoped_q=isDumpDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isTableDataSet"></a>
# isTableDataSet
isTableDataSet( QDataSet ds ) &rarr; boolean



### Parameters:
ds - a QDataSet

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isTableDataSet&unscoped_q=isTableDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parseControl"></a>
# parseControl
parseControl( String c ) &rarr; Map

convenient and official location for method that parses control string.
 This will split on ampersand, and when no ampersands are found then it will
 try semicolons.  This is to support embedding the control string in 
 other control strings (like Autoplot URIs) which use ampersands.

### Parameters:
c - the control string or null.

### Returns:
the control string, parsed.

<a href="https://github.com/autoplot/dev/search?q=parseControl&unscoped_q=parseControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parseLayoutString"></a>
# parseLayoutString
parseLayoutString( String sizeStr, int nsize, double emSize, double fail ) &rarr; double

return the size encoded as normalized by the container size and em size.

### Parameters:
sizeStr - spec like "5em" or "50%"
<br>nsize - the dimension for percents, for example the size of the canvas or column.
<br>emSize - the size of the current font, for ems.
<br>fail - value to return if the spec cannot be parsed.

### Returns:
the size in pixels
### See Also:
<a href='DasDevicePosition.md#parseLayoutStr'>DasDevicePosition#parseLayoutStr(java.lang.String, double, int, double)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=parseLayoutString&unscoped_q=parseLayoutString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void

Removes a PropertyChangeListener from the listener list.

### Parameters:
l - The listener to remove.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

removePropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="render"></a>
# render
render( java.awt.Graphics2D g, org.das2.graph.DasAxis xAxis, org.das2.graph.DasAxis yAxis ) &rarr; void

Render is called whenever the image needs to be refreshed or the content
 has changed.  This operation should occur with an animation-interactive
 time scale, and an image should be cached when this is not possible.  The graphics
 object will have its origin at the upper-left corner of the screen.

### Parameters:
g - the graphics context in the canvas reference frame.
<br>xAxis - the axis relating x data coordinates to horizontal pixel coordinates
<br>yAxis - the axis relating y data coordinates to horizontal pixel coordinates

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=render&unscoped_q=render">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resetCounters"></a>
# resetCounters
resetCounters(  ) &rarr; void

reset the counters.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resetCounters&unscoped_q=resetCounters">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setActive"></a>
# setActive
setActive( boolean active ) &rarr; void

set the active property, when false the renderer will not be drawn.
 This is allows a renderer to be 
 disabled without removing it from the application.

### Parameters:
active - false if the renderer should not be drawn.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setActive&unscoped_q=setActive">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setBottomDecorator"></a>
# setBottomDecorator
setBottomDecorator( org.das2.graph.Painter bottomDecorator ) &rarr; void

add additional painting code to the renderer, which is called before
 the renderer is called.

### Parameters:
bottomDecorator - the Painter to call, or null to clear.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setBottomDecorator&unscoped_q=setBottomDecorator">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setColorBar"></a>
# setColorBar
setColorBar( org.das2.graph.DasColorBar cb ) &rarr; void

set a colorbar for the renderer.  By default, the renderer simply ignores 
 the colorbar, but instances may introduce special handling.
 WARNING: some subclasses override this, but do not call super.setColorBar.

### Parameters:
cb - a colorbar

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setColorBar&unscoped_q=setColorBar">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setControl"></a>
# setControl
setControl( String s ) &rarr; void

set the control string which contains a number of properties.  These are defined for
 each renderer, but they should try to be consistent.  See http://autoplot.org/developer.guessRenderType#Proposed_extensions
 When overriding this, be sure to call super.

### Parameters:
s - the control

### Returns:
void (returns nothing)

### See Also:
<a href='#CONTROL_KEY_COLOR etc'>CONTROL_KEY_COLOR etc</a> etc<br>

<a href="https://github.com/autoplot/dev/search?q=setControl&unscoped_q=setControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataSet"></a>
# setDataSet
setDataSet( QDataSet ds ) &rarr; void

Set the dataset to be plotted.  Different renderers accept QDataSets with
 different schemes.  For example SeriesRenderer takes:
   ds[t]   rank 1 dataset with rank 1 DEPEND_0  or
   ds[t,n] rank 2 bundle dataset with X in ds[t,0] and Y in ds[t,n-1]
 and SpectrogramRenderer takes:
   ds[t,y] rank 2 table dataset
   ds[n,t,y]  rank 3 dataset with the first dimension join
 See each renderer's documentation for the schemes it takes.
 Note the lastException property is cleared, even when the dataset is null.

### Parameters:
ds - a QDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSet&unscoped_q=setDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataSetDescriptor"></a>
# setDataSetDescriptor
setDataSetDescriptor( org.das2.dataset.DataSetDescriptor dsd ) &rarr; void



### Parameters:
dsd - a DataSetDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSetDescriptor&unscoped_q=setDataSetDescriptor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataSetID"></a>
# setDataSetID
setDataSetID( String id ) &rarr; void



### Parameters:
id - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSetID&unscoped_q=setDataSetID">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataSetLoader"></a>
# setDataSetLoader
setDataSetLoader( org.das2.graph.DataLoader loader ) &rarr; void



### Parameters:
loader - a DataLoader

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSetLoader&unscoped_q=setDataSetLoader">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDrawLegendLabel"></a>
# setDrawLegendLabel
setDrawLegendLabel( boolean drawLegendLabel ) &rarr; void

set the switch used to turn off legend label.  This allows the label
 to be hidden without loosing the information it provides.

### Parameters:
drawLegendLabel - true if the legend label should be drawn

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDrawLegendLabel&unscoped_q=setDrawLegendLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDumpDataSet"></a>
# setDumpDataSet
setDumpDataSet( boolean dumpDataSet ) &rarr; void

Setter for property dumpDataSet setting this to
 true causes the dataSet to be dumped.

### Parameters:
dumpDataSet - New value of property dumpDataSet.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDumpDataSet&unscoped_q=setDumpDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setException"></a>
# setException
setException( java.lang.Exception e ) &rarr; void

set the exception to be rendered instead of the dataset.

### Parameters:
e - an Exception

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setException&unscoped_q=setException">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setId"></a>
# setId
setId( String id ) &rarr; void



### Parameters:
id - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setId&unscoped_q=setId">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLastException"></a>
# setLastException
setLastException( java.lang.Exception e ) &rarr; void

TODO: what is the difference between lastException and exception?

### Parameters:
e - an Exception

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLastException&unscoped_q=setLastException">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLegendLabel"></a>
# setLegendLabel
setLegendLabel( String legendLabel ) &rarr; void

set the label to describe the renderer in the plot's legend.  
 If zero-length, then the legend label should be hidden.

### Parameters:
legendLabel - the label to describe the renderer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLegendLabel&unscoped_q=setLegendLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setParent"></a>
# setParent
setParent( org.das2.graph.DasPlot parent ) &rarr; void



### Parameters:
parent - a DasPlot

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setParent&unscoped_q=setParent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setStatsFile"></a>
# setStatsFile
setStatsFile( String recordFile ) &rarr; void

name of the file where rendering speed is recorded.

### Parameters:
recordFile - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setStatsFile&unscoped_q=setStatsFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setUpFont"></a>
# setUpFont
setUpFont( java.awt.Font f, String fontSize ) &rarr; Font

handle the fontSize property, which has values like "1em" and "7px"

### Parameters:
f - the parent font.
<br>fontSize - fontSize property, for example "1em" and "7px"

### Returns:
the relative font.

<a href="https://github.com/autoplot/dev/search?q=setUpFont&unscoped_q=setUpFont">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="update"></a>
# update
update(  ) &rarr; void

Something has changed with the Render, and the plot should come back
 to allow this render to repaint.  Its cacheImage is invalidated and a
 repaint is posted on the event thread.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=update&unscoped_q=update">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="updateCacheImage"></a>
# updateCacheImage
updateCacheImage(  ) &rarr; void

The cacheImage is invalidated and updateEvent posted on the event thread
 by calling update.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=updateCacheImage&unscoped_q=updateCacheImage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="updatePlotImage"></a>
# updatePlotImage
updatePlotImage( org.das2.graph.DasAxis xAxis, org.das2.graph.DasAxis yAxis, ProgressMonitor monitor ) &rarr; void

updatePlotImage is called once the expensive operation of loading
 the data is completed.  This operation should occur on an interactive
 time scale.  This is an opportunity to create a cache
 image of the data with the current axis state, when the render
 operation cannot operate on an animation interactive time scale.
 Also, several Renders can be updating at once on separate threads, while
 the render methods must be called sequentially.
 
 Only Renderer should call this method!  (This should be protected then, but
 this is not possible because of exiting use.  TODO: introduce "revalidate"
 to replace this operation.)

### Parameters:
xAxis - the axis relating x data coordinates to horizontal pixel coordinates
<br>yAxis - the axis relating y data coordinates to horizontal pixel coordinates
<br>monitor - a monitor for the operation.  Note the updatePlotImage operation should be fast (&lt;1000ms).

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=updatePlotImage&unscoped_q=updatePlotImage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

