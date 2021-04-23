# org.das2.graph.TickCurveRendererRenderer showing ticks along a curve, useful for orbits.  Note this renderer
 assumes that someone else is showing the context, so just HH:MM is shown, 
 assuming YYYY-MM-DD is shown elsewhere.
TickCurveRenderer( QDataSet ds, String xplane, String yplane, org.das2.graph.TickVDescriptor tickv )
Create a new renderer with the x and y planes of the bundle ds identified.  If the xplane or yplane is 
 not identified, then use unbundle(1) for the xplane and unbundle(y) for the yplane.

TickCurveRenderer( )


***
<a name="PROP_TICK_STYLE"></a>
# PROP_TICK_STYLE



***
<a name="CONTROL_TICK_LENGTH"></a>
# CONTROL_TICK_LENGTH



***
<a name="PROP_FONTSIZE"></a>
# PROP_FONTSIZE



***
<a name="PROP_TICKDIRECTION"></a>
# PROP_TICKDIRECTION



***
<a name="PROP_TICKSPACING"></a>
# PROP_TICKSPACING



***
<a name="PROP_TICKVALUES"></a>
# PROP_TICKVALUES



***
<a name="acceptContext"></a>
# acceptContext
acceptContext( int x, int y ) &rarr; boolean



### Parameters:
x - an int
<br>y - an int

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=acceptContext&unscoped_q=acceptContext">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="acceptsData"></a>
# acceptsData
acceptsData( QDataSet ds ) &rarr; boolean

return true if the data is ds[:,3] (T,X,Y) or ds[x[t]]  t&rarr;x&rarr;y

### Parameters:
ds - the dataset

### Returns:
true if the data is ds[:,3] or ds[x[t]]

<a href="https://github.com/autoplot/dev/search?q=acceptsData&unscoped_q=acceptsData">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="checkTickV"></a>
# checkTickV
checkTickV( QDataSet tds ) &rarr; double

returns the minimal distance between consecutive ticks, or Double.MAX_VALUE if fewer than two ticks are found.

### Parameters:
tds - a QDataSet

### Returns:
a double


<a href="https://github.com/autoplot/dev/search?q=checkTickV&unscoped_q=checkTickV">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="doAutorange"></a>
# doAutorange
doAutorange( QDataSet ds1 ) &rarr; QDataSet

autorange on the data, returning a rank 2 bounds for the dataset.

### Parameters:
ds1 - the dataset

### Returns:
rank 2 bounding box.  r[0,0] is x min, r[0,1] is x max.

<a href="https://github.com/autoplot/dev/search?q=doAutorange&unscoped_q=doAutorange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getColor"></a>
# getColor
getColor(  ) &rarr; Color

get the color of the orbit

### Returns:
the color

<a href="https://github.com/autoplot/dev/search?q=getColor&unscoped_q=getColor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getControl"></a>
# getControl
getControl(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getControl&unscoped_q=getControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFontSize"></a>
# getFontSize
getFontSize(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getFontSize&unscoped_q=getFontSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLineWidth"></a>
# getLineWidth
getLineWidth(  ) &rarr; double

Getter for property lineWidth.

### Returns:
Value of property lineWidth.

<a href="https://github.com/autoplot/dev/search?q=getLineWidth&unscoped_q=getLineWidth">[search for examples]</a>

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
<a name="getTickDirection"></a>
# getTickDirection
getTickDirection(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getTickDirection&unscoped_q=getTickDirection">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTickLabeller"></a>
# getTickLabeller
getTickLabeller(  ) &rarr; TickLabeller

provide access to the tick labelling code

### Returns:
an org.das2.graph.TickLabeller


<a href="https://github.com/autoplot/dev/search?q=getTickLabeller&unscoped_q=getTickLabeller">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTickLength"></a>
# getTickLength
getTickLength(  ) &rarr; String

Getter for property tickLength.

### Returns:
Value of property tickLength.

<a href="https://github.com/autoplot/dev/search?q=getTickLength&unscoped_q=getTickLength">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTickSpacing"></a>
# getTickSpacing
getTickSpacing(  ) &rarr; String

get the spacing between ticks, which might be "" meaning automatic.

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getTickSpacing&unscoped_q=getTickSpacing">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTickStyle"></a>
# getTickStyle
getTickStyle(  ) &rarr; TickStyle

Getter for property tickStyle.

### Returns:
Value of property tickStyle.

<a href="https://github.com/autoplot/dev/search?q=getTickStyle&unscoped_q=getTickStyle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTickValues"></a>
# getTickValues
getTickValues(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getTickValues&unscoped_q=getTickValues">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="render"></a>
# render
render( java.awt.Graphics2D g1, org.das2.graph.DasAxis xAxis, org.das2.graph.DasAxis yAxis ) &rarr; void



### Parameters:
g1 - a Graphics2D
<br>xAxis - a DasAxis
<br>yAxis - a DasAxis

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=render&unscoped_q=render">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="selectionArea"></a>
# selectionArea
selectionArea(  ) &rarr; Shape



### Returns:
java.awt.Shape


<a href="https://github.com/autoplot/dev/search?q=selectionArea&unscoped_q=selectionArea">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setColor"></a>
# setColor
setColor( java.awt.Color color ) &rarr; void

set the color of the orbit

### Parameters:
color - a Color

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setColor&unscoped_q=setColor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setControl"></a>
# setControl
setControl( String s ) &rarr; void



### Parameters:
s - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setControl&unscoped_q=setControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataSet"></a>
# setDataSet
setDataSet( QDataSet ds ) &rarr; void



### Parameters:
ds - a QDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSet&unscoped_q=setDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFontSize"></a>
# setFontSize
setFontSize( String fontSize ) &rarr; void

relative font size.

### Parameters:
fontSize - a String

### Returns:
void (returns nothing)

### See Also:
<a href='Renderer.md#CONTROL_KEY_FONT_SIZE'>Renderer#CONTROL_KEY_FONT_SIZE</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setFontSize&unscoped_q=setFontSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLineWidth"></a>
# setLineWidth
setLineWidth( double lineWidth ) &rarr; void

Setter for property lineWidth.

### Parameters:
lineWidth - New value of property lineWidth.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLineWidth&unscoped_q=setLineWidth">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTickDirection"></a>
# setTickDirection
setTickDirection( String tickDirection ) &rarr; void



### Parameters:
tickDirection - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTickDirection&unscoped_q=setTickDirection">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTickLabeller"></a>
# setTickLabeller
setTickLabeller( org.das2.graph.TickLabeller tickLabeller ) &rarr; void

set the tick labelling code.  If this is an instance of GrannyTickLabeller,
 then a property change listener will be added.

### Parameters:
tickLabeller - a TickLabeller

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTickLabeller&unscoped_q=setTickLabeller">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTickLength"></a>
# setTickLength
setTickLength( String tickLength ) &rarr; void

Setter for property tickLength.

### Parameters:
tickLength - New value of property tickLength.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTickLength&unscoped_q=setTickLength">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTickSpacing"></a>
# setTickSpacing
setTickSpacing( String tickSpacing ) &rarr; void

set the spacing between ticks, for example "2hr" is every two hours, and an
 empty string is the default automatic behavior.

### Parameters:
tickSpacing - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTickSpacing&unscoped_q=setTickSpacing">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTickStyle"></a>
# setTickStyle
setTickStyle( org.das2.graph.TickCurveRenderer.TickStyle tickStyle ) &rarr; void

Setter for property tickStyle.

### Parameters:
tickStyle - New value of property tickStyle.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTickStyle&unscoped_q=setTickStyle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTickVDescriptor"></a>
# setTickVDescriptor
setTickVDescriptor( org.das2.graph.TickVDescriptor ticks ) &rarr; void

manually set the ticks for the renderer, or null means use automatic.

### Parameters:
ticks - a TickVDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTickVDescriptor&unscoped_q=setTickVDescriptor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTickValues"></a>
# setTickValues
setTickValues( String tickValues ) &rarr; void

set like the axis control, with values like:<ul>
 <li>+2hr for every two hours
 <li>2019-11-26T00:02,2019-11-26T00:07 for explicit positions
 </ul>

### Parameters:
tickValues - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTickValues&unscoped_q=setTickValues">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

