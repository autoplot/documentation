# org.das2.graph.EventsRenderer

Draw colored horizontal bars for the dataset, marking events datasets or modes of the data.  This expects
 a QDataSet with the canonical scheme:
<blockquote><pre><small>{@code
    Events[:,BUNDLE_1=4] where the columns are:
      BUNDLE_1=startTime,stopTime,Color,Message
    startTime,stopTime are in some time location unit.  stopTime may also be an offset from startTime (e.g. seconds)
    Color is an int, that is either 0xRRGGBB or 0xAARRGGBB.
    Message is any datum, so typically an enumeration unit is used.
}</small></pre></blockquote>
 Note this also contains systems for coloring data in old schemes, such as the colorSpecifier interface and textSpecifier.
 These should not be used when a dataset will be sufficient.

# EventsRenderer( )


***
<a name="PROP_COLOR"></a>
# PROP_COLOR



***
<a name="DEFAULT_TEXT_SPECIFIER"></a>
# DEFAULT_TEXT_SPECIFIER



***
<a name="PROP_LINESTYLE"></a>
# PROP_LINESTYLE



***
<a name="PROP_LINETHICK"></a>
# PROP_LINETHICK



***
<a name="PROP_OPAQUE"></a>
# PROP_OPAQUE



***
<a name="PROP_SHOWLABELS"></a>
# PROP_SHOWLABELS



***
<a name="PROP_ORBITMODE"></a>
# PROP_ORBITMODE



***
<a name="PROP_GANTTMODE"></a>
# PROP_GANTTMODE



***
<a name="PROP_FONTSIZE"></a>
# PROP_FONTSIZE



***
<a name="PROP_COLOR_SPECIFIER"></a>
# PROP_COLOR_SPECIFIER



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
<a name="doAutorange"></a>
# doAutorange
doAutorange( QDataSet ds ) &rarr; QDataSet

return bounding cube

### Parameters:
ds - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=doAutorange&unscoped_q=doAutorange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getColor"></a>
# getColor
getColor(  ) &rarr; Color



### Returns:
java.awt.Color


<a href="https://github.com/autoplot/dev/search?q=getColor&unscoped_q=getColor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getColorSpecifier"></a>
# getColorSpecifier
getColorSpecifier(  ) &rarr; ColorSpecifier



### Returns:
org.das2.graph.EventsRenderer.ColorSpecifier


<a href="https://github.com/autoplot/dev/search?q=getColorSpecifier&unscoped_q=getColorSpecifier">[search for examples]</a>

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
<a name="getLineStyle"></a>
# getLineStyle
getLineStyle(  ) &rarr; PsymConnector



### Returns:
org.das2.graph.PsymConnector


<a href="https://github.com/autoplot/dev/search?q=getLineStyle&unscoped_q=getLineStyle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLineThick"></a>
# getLineThick
getLineThick(  ) &rarr; String

the line thickness, examples include "5pt" and "0.1em"

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getLineThick&unscoped_q=getLineThick">[search for examples]</a>

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
<a name="getRenderTimeLimitMs"></a>
# getRenderTimeLimitMs
getRenderTimeLimitMs(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getRenderTimeLimitMs&unscoped_q=getRenderTimeLimitMs">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTextSpecifier"></a>
# getTextSpecifier
getTextSpecifier(  ) &rarr; TextSpecifier

Getter for property textSpecifier.

### Returns:
Value of property textSpecifier.

<a href="https://github.com/autoplot/dev/search?q=getTextSpecifier&unscoped_q=getTextSpecifier">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isGanttMode"></a>
# isGanttMode
isGanttMode(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isGanttMode&unscoped_q=isGanttMode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isOpaque"></a>
# isOpaque
isOpaque(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isOpaque&unscoped_q=isOpaque">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isOrbitMode"></a>
# isOrbitMode
isOrbitMode(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isOrbitMode&unscoped_q=isOrbitMode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isShowLabels"></a>
# isShowLabels
isShowLabels(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isShowLabels&unscoped_q=isShowLabels">[search for examples]</a>

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
<a name="setColor"></a>
# setColor
setColor( java.awt.Color color ) &rarr; void

set the color to use when the data doesn't specify a color.  If an alpha channel is specified, then
 this alpha value is used, otherwise 80% is used.

### Parameters:
color - a Color

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setColor&unscoped_q=setColor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setColorSpecifier"></a>
# setColorSpecifier
setColorSpecifier( org.das2.graph.EventsRenderer.ColorSpecifier spec ) &rarr; void

set this to be an object implementing ColorSpecifier interface, if more than
 one color is to be used when drawing the bars.  Setting this to null will
 restore the initial behavior of drawing all bars in one color (or with rank 2 bundle containing color).

### Parameters:
spec - the color specifier.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setColorSpecifier&unscoped_q=setColorSpecifier">[search for examples]</a>

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



### Parameters:
fontSize - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFontSize&unscoped_q=setFontSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setGanttMode"></a>
# setGanttMode
setGanttMode( boolean ganttMode ) &rarr; void



### Parameters:
ganttMode - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setGanttMode&unscoped_q=setGanttMode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLineStyle"></a>
# setLineStyle
setLineStyle( org.das2.graph.PsymConnector lineStyle ) &rarr; void



### Parameters:
lineStyle - a PsymConnector

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLineStyle&unscoped_q=setLineStyle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLineThick"></a>
# setLineThick
setLineThick( String lineThick ) &rarr; void



### Parameters:
lineThick - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLineThick&unscoped_q=setLineThick">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setOpaque"></a>
# setOpaque
setOpaque( boolean opaque ) &rarr; void



### Parameters:
opaque - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setOpaque&unscoped_q=setOpaque">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setOrbitMode"></a>
# setOrbitMode
setOrbitMode( boolean orbitMode ) &rarr; void



### Parameters:
orbitMode - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setOrbitMode&unscoped_q=setOrbitMode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRenderTimeLimitMs"></a>
# setRenderTimeLimitMs
setRenderTimeLimitMs( int renderTimeLimitMs ) &rarr; void



### Parameters:
renderTimeLimitMs - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRenderTimeLimitMs&unscoped_q=setRenderTimeLimitMs">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setShowLabels"></a>
# setShowLabels
setShowLabels( boolean showLabels ) &rarr; void



### Parameters:
showLabels - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setShowLabels&unscoped_q=setShowLabels">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTextSpecifier"></a>
# setTextSpecifier
setTextSpecifier( org.das2.graph.EventsRenderer.TextSpecifier textSpecifier ) &rarr; void

Setter for property textSpecifier.

### Parameters:
textSpecifier - New value of property textSpecifier.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTextSpecifier&unscoped_q=setTextSpecifier">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

