# org.das2.graph.DasAnnotation

This makes a DasCanvasComponent for GrannyTextRenderer, and 
 optionally adds an arrow to point at things.
 
 TODO: See http://autoplot.org//developer.annotations

# DasAnnotation( String string )
Create the annotation

***
<a name="PROP_TEXT"></a>
# PROP_TEXT



***
<a name="PROP_URL"></a>
# PROP_URL



***
<a name="PROP_SCALE"></a>
# PROP_SCALE



***
<a name="PROP_FONT_SIZE"></a>
# PROP_FONT_SIZE

the font size in pixels.

***
<a name="PROP_BORDERTYPE"></a>
# PROP_BORDERTYPE



***
<a name="PROP_ANCHORPOSITION"></a>
# PROP_ANCHORPOSITION



***
<a name="PROP_XRANGE"></a>
# PROP_XRANGE



***
<a name="PROP_YRANGE"></a>
# PROP_YRANGE



***
<a name="PROP_POINTATX"></a>
# PROP_POINTATX



***
<a name="PROP_POINTATY"></a>
# PROP_POINTATY



***
<a name="PROP_REFERENCEX"></a>
# PROP_REFERENCEX



***
<a name="PROP_REFERENCEY"></a>
# PROP_REFERENCEY



***
<a name="PROP_SYMBOL"></a>
# PROP_SYMBOL



***
<a name="PROP_POINTATOFFSET"></a>
# PROP_POINTATOFFSET



***
<a name="PROP_SHOWARROW"></a>
# PROP_SHOWARROW



***
<a name="PROP_ANCHORBORDERTYPE"></a>
# PROP_ANCHORBORDERTYPE



***
<a name="PROP_ANCHORBACKGROUND"></a>
# PROP_ANCHORBACKGROUND



***
<a name="PROP_ANCHORTYPE"></a>
# PROP_ANCHORTYPE



***
<a name="PROP_SPLITANCHORTYPE"></a>
# PROP_SPLITANCHORTYPE



***
<a name="PROP_VERTICALANCHORTYPE"></a>
# PROP_VERTICALANCHORTYPE



***
<a name="PROP_ARROWSTYLE"></a>
# PROP_ARROWSTYLE



***
<a name="PROP_OVERRIDECOLORS"></a>
# PROP_OVERRIDECOLORS



***
<a name="PROP_TEXTCOLOR"></a>
# PROP_TEXTCOLOR



***
<a name="PROP_ANCHOROFFSET"></a>
# PROP_ANCHOROFFSET



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
<a name="addPainter"></a>
# addPainter
addPainter( String id, org.das2.util.GrannyTextRenderer.Painter p ) &rarr; void

add a painter for the grannyTextRenderer.  This is done by associating
 a Painter code with an id, and the id is used within the annotation string.

### Parameters:
id - id for the painter, where the id is found in the granny text string
<br>p - the painter code which draws on a graphics context.

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/util/GrannyTextRenderer.md#addPainter'>org.das2.util.GrannyTextRenderer#addPainter(java.lang.String, org.das2.util.GrannyTextRenderer.Painter)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=addPainter&unscoped_q=addPainter">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="clearPainters"></a>
# clearPainters
clearPainters(  ) &rarr; void

remove all the painters

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=clearPainters&unscoped_q=clearPainters">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="contains"></a>
# contains
contains( int x, int y ) &rarr; boolean

This item should only accept mouse events on the bubble

### Parameters:
x - an int
<br>y - an int

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=contains&unscoped_q=contains">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getActiveRegion"></a>
# getActiveRegion
getActiveRegion(  ) &rarr; Shape



### Returns:
java.awt.Shape


<a href="https://github.com/autoplot/dev/search?q=getActiveRegion&unscoped_q=getActiveRegion">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getAnchorBackground"></a>
# getAnchorBackground
getAnchorBackground(  ) &rarr; Color



### Returns:
java.awt.Color


<a href="https://github.com/autoplot/dev/search?q=getAnchorBackground&unscoped_q=getAnchorBackground">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getAnchorBorderType"></a>
# getAnchorBorderType
getAnchorBorderType(  ) &rarr; BorderType



### Returns:
org.das2.graph.BorderType


<a href="https://github.com/autoplot/dev/search?q=getAnchorBorderType&unscoped_q=getAnchorBorderType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getAnchorOffset"></a>
# getAnchorOffset
getAnchorOffset(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getAnchorOffset&unscoped_q=getAnchorOffset">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getAnchorPosition"></a>
# getAnchorPosition
getAnchorPosition(  ) &rarr; AnchorPosition

get the location within the box where the annotation will be drawn.

### Returns:
anchorPosition

<a href="https://github.com/autoplot/dev/search?q=getAnchorPosition&unscoped_q=getAnchorPosition">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getAnchorType"></a>
# getAnchorType
getAnchorType(  ) &rarr; AnchorType



### Returns:
org.das2.graph.AnchorType


<a href="https://github.com/autoplot/dev/search?q=getAnchorType&unscoped_q=getAnchorType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getArrowStyle"></a>
# getArrowStyle
getArrowStyle(  ) &rarr; HeadStyle

get the arrow style

### Returns:
the arrow style

<a href="https://github.com/autoplot/dev/search?q=getArrowStyle&unscoped_q=getArrowStyle">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBorderType"></a>
# getBorderType
getBorderType(  ) &rarr; BorderType

the border type

### Returns:
the border type

<a href="https://github.com/autoplot/dev/search?q=getBorderType&unscoped_q=getBorderType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFontSize"></a>
# getFontSize
getFontSize(  ) &rarr; float

the font size in points.  If zero, then use the canvas size.

### Returns:
the font size in points.

<a href="https://github.com/autoplot/dev/search?q=getFontSize&unscoped_q=getFontSize">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPointAt"></a>
# getPointAt
getPointAt(  ) &rarr; PointDescriptor

return the thing we are pointing at.

### Returns:
the thing we are pointing at.

<a href="https://github.com/autoplot/dev/search?q=getPointAt&unscoped_q=getPointAt">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPointAtOffset"></a>
# getPointAtOffset
getPointAtOffset(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getPointAtOffset&unscoped_q=getPointAtOffset">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPointAtX"></a>
# getPointAtX
getPointAtX(  ) &rarr; Datum



### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getPointAtX&unscoped_q=getPointAtX">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPointAtY"></a>
# getPointAtY
getPointAtY(  ) &rarr; Datum



### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getPointAtY&unscoped_q=getPointAtY">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getReferenceX"></a>
# getReferenceX
getReferenceX(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getReferenceX&unscoped_q=getReferenceX">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getReferenceY"></a>
# getReferenceY
getReferenceY(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getReferenceY&unscoped_q=getReferenceY">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getScale"></a>
# getScale
getScale(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=getScale&unscoped_q=getScale">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSymbol"></a>
# getSymbol
getSymbol(  ) &rarr; PlotSymbol



### Returns:
org.das2.graph.PlotSymbol


<a href="https://github.com/autoplot/dev/search?q=getSymbol&unscoped_q=getSymbol">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getText"></a>
# getText
getText(  ) &rarr; String

get the text, which can be Granny Text.

### Returns:
the text.
### See Also:
<a href='GrannyTextRenderer.md'>GrannyTextRenderer</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getText&unscoped_q=getText">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTextColor"></a>
# getTextColor
getTextColor(  ) &rarr; Color



### Returns:
java.awt.Color


<a href="https://github.com/autoplot/dev/search?q=getTextColor&unscoped_q=getTextColor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getUrl"></a>
# getUrl
getUrl(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getUrl&unscoped_q=getUrl">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getVerticalAnchorType"></a>
# getVerticalAnchorType
getVerticalAnchorType(  ) &rarr; AnchorType



### Returns:
org.das2.graph.AnchorType


<a href="https://github.com/autoplot/dev/search?q=getVerticalAnchorType&unscoped_q=getVerticalAnchorType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getXrange"></a>
# getXrange
getXrange(  ) &rarr; DatumRange



### Returns:
org.das2.datum.DatumRange


<a href="https://github.com/autoplot/dev/search?q=getXrange&unscoped_q=getXrange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getYrange"></a>
# getYrange
getYrange(  ) &rarr; DatumRange



### Returns:
org.das2.datum.DatumRange


<a href="https://github.com/autoplot/dev/search?q=getYrange&unscoped_q=getYrange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isOverrideColors"></a>
# isOverrideColors
isOverrideColors(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isOverrideColors&unscoped_q=isOverrideColors">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isShowArrow"></a>
# isShowArrow
isShowArrow(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isShowArrow&unscoped_q=isShowArrow">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isSplitAnchorType"></a>
# isSplitAnchorType
isSplitAnchorType(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isSplitAnchorType&unscoped_q=isSplitAnchorType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="paintComponent"></a>
# paintComponent
paintComponent( java.awt.Graphics g1 ) &rarr; void



### Parameters:
g1 - a Graphics

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=paintComponent&unscoped_q=paintComponent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePainter"></a>
# removePainter
removePainter( String id ) &rarr; void

remove the painter with the given id.

### Parameters:
id - id for the painter, where the id is found in the granny text string

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePainter&unscoped_q=removePainter">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resize"></a>
# resize
resize(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resize&unscoped_q=resize">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAnchorBackground"></a>
# setAnchorBackground
setAnchorBackground( java.awt.Color anchorBackground ) &rarr; void



### Parameters:
anchorBackground - a Color

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAnchorBackground&unscoped_q=setAnchorBackground">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAnchorBorderType"></a>
# setAnchorBorderType
setAnchorBorderType( org.das2.graph.BorderType anchorBorderType ) &rarr; void



### Parameters:
anchorBorderType - a BorderType

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAnchorBorderType&unscoped_q=setAnchorBorderType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAnchorOffset"></a>
# setAnchorOffset
setAnchorOffset( String anchorOffset ) &rarr; void

the offset in x and y for the text bubble from the anchor.  For
 example, "4em,4em" will place a OutsideNE label 4ems up and 4ems over 
 from the default.

### Parameters:
anchorOffset - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAnchorOffset&unscoped_q=setAnchorOffset">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAnchorPosition"></a>
# setAnchorPosition
setAnchorPosition( org.das2.graph.AnchorPosition anchorPosition ) &rarr; void

set the location within the box where the annotation will be drawn.

### Parameters:
anchorPosition - an AnchorPosition

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAnchorPosition&unscoped_q=setAnchorPosition">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAnchorType"></a>
# setAnchorType
setAnchorType( org.das2.graph.AnchorType anchorType ) &rarr; void



### Parameters:
anchorType - an AnchorType

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAnchorType&unscoped_q=setAnchorType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setArrowStyle"></a>
# setArrowStyle
setArrowStyle( org.das2.graph.Arrow.HeadStyle newarrowStyle ) &rarr; void

set the arrow style to BIG,SMALL,DRAFTING.

### Parameters:
newarrowStyle - the arrow style

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setArrowStyle&unscoped_q=setArrowStyle">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setBorderType"></a>
# setBorderType
setBorderType( org.das2.graph.BorderType newborderType ) &rarr; void

set the border type to NONE, rounded rectangle, etc.

### Parameters:
newborderType - the border type

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setBorderType&unscoped_q=setBorderType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFontSize"></a>
# setFontSize
setFontSize( float fontSize ) &rarr; void

override the canvas font size.  If zero, then use the canvas size, 
 otherwise, use this size.

### Parameters:
fontSize - New value of property fontSize.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFontSize&unscoped_q=setFontSize">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setOverrideColors"></a>
# setOverrideColors
setOverrideColors( boolean overrideColors ) &rarr; void

true will use the colors specified, otherwise the canvas colors are used.

### Parameters:
overrideColors - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setOverrideColors&unscoped_q=setOverrideColors">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPlot"></a>
# setPlot
setPlot( org.das2.graph.DasPlot p ) &rarr; void



### Parameters:
p - a DasPlot

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPlot&unscoped_q=setPlot">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPointAt"></a>
# setPointAt
setPointAt( org.das2.graph.DasAnnotation.PointDescriptor p ) &rarr; void

set the thing to point at.  If %p will be replaced by p.getLabel()

### Parameters:
p - the thing.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPointAt&unscoped_q=setPointAt">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPointAtOffset"></a>
# setPointAtOffset
setPointAtOffset( String pointAtOffset ) &rarr; void



### Parameters:
pointAtOffset - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPointAtOffset&unscoped_q=setPointAtOffset">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPointAtX"></a>
# setPointAtX
setPointAtX( Datum pointAtX ) &rarr; void



### Parameters:
pointAtX - a Datum

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPointAtX&unscoped_q=setPointAtX">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPointAtY"></a>
# setPointAtY
setPointAtY( Datum pointAtY ) &rarr; void



### Parameters:
pointAtY - a Datum

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPointAtY&unscoped_q=setPointAtY">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setReferenceX"></a>
# setReferenceX
setReferenceX( String referenceX ) &rarr; void

single or semicolon-separated list of values.

### Parameters:
referenceX - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setReferenceX&unscoped_q=setReferenceX">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setReferenceY"></a>
# setReferenceY
setReferenceY( String referenceY ) &rarr; void

single or semicolon-separated list of values.

### Parameters:
referenceY - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setReferenceY&unscoped_q=setReferenceY">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setScale"></a>
# setScale
setScale( double scale ) &rarr; void

set the amount to scale the image by, if using URL to point at an image, where 0.5 is half of the
 original image size.

### Parameters:
scale - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setScale&unscoped_q=setScale">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setShowArrow"></a>
# setShowArrow
setShowArrow( boolean showArrow ) &rarr; void



### Parameters:
showArrow - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setShowArrow&unscoped_q=setShowArrow">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSplitAnchorType"></a>
# setSplitAnchorType
setSplitAnchorType( boolean splitAnchorType ) &rarr; void



### Parameters:
splitAnchorType - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSplitAnchorType&unscoped_q=setSplitAnchorType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSymbol"></a>
# setSymbol
setSymbol( org.das2.graph.PlotSymbol symbol ) &rarr; void

set the symbol used to mark the reference locations

### Parameters:
symbol - a PlotSymbol

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSymbol&unscoped_q=setSymbol">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setText"></a>
# setText
setText( String string ) &rarr; void

Set the text, which can be Granny Text, or image URL. (Image URL is 
 deprecated, use url property instead.)  If the url property has length>0,
 then this is ignored.
 URLs must start with http:, https:, or file:.

### Parameters:
string - the text

### Returns:
void (returns nothing)

### See Also:
<a href='GrannyTextRenderer.md'>GrannyTextRenderer</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setText&unscoped_q=setText">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTextColor"></a>
# setTextColor
setTextColor( java.awt.Color textColor ) &rarr; void

the color of the text, or if transparent then the border
 color should be used.

### Parameters:
textColor - a Color

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTextColor&unscoped_q=setTextColor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setUrl"></a>
# setUrl
setUrl( String url ) &rarr; void

set the URL to the location of a png or jpg file.  If this is set,
 then the text property is ignored.

### Parameters:
url - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUrl&unscoped_q=setUrl">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setVerticalAnchorType"></a>
# setVerticalAnchorType
setVerticalAnchorType( org.das2.graph.AnchorType verticalAnchorType ) &rarr; void

when splitAnchorType==True, use this for the vertical position instead
 of the anchorType property.

### Parameters:
verticalAnchorType - an AnchorType

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setVerticalAnchorType&unscoped_q=setVerticalAnchorType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setXrange"></a>
# setXrange
setXrange( DatumRange xrange ) &rarr; void



### Parameters:
xrange - a DatumRange

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setXrange&unscoped_q=setXrange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setYrange"></a>
# setYrange
setYrange( DatumRange yrange ) &rarr; void



### Parameters:
yrange - a DatumRange

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setYrange&unscoped_q=setYrange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

