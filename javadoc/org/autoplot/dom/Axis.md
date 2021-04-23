# org.autoplot.dom.Axis

The state of an axis, X, Y, or a Z axis colorbar, such as range and the
 scale type.

# Axis( )


***
<a name="DEFAULT_RANGE"></a>
# DEFAULT_RANGE



***
<a name="PROP_RANGE"></a>
# PROP_RANGE



***
<a name="PROP_SCALE"></a>
# PROP_SCALE



***
<a name="PROP_LOG"></a>
# PROP_LOG



***
<a name="PROP_REFERENCE"></a>
# PROP_REFERENCE



***
<a name="PROP_LABEL"></a>
# PROP_LABEL

concise label for the axis.

***
<a name="PROP_FONTSIZE"></a>
# PROP_FONTSIZE



***
<a name="PROP_DRAWTICKLABELS"></a>
# PROP_DRAWTICKLABELS



***
<a name="PROP_OPPOSITE"></a>
# PROP_OPPOSITE



***
<a name="PROP_VISIBLE"></a>
# PROP_VISIBLE

false indicates the component will not be drawn.  Note the x and y axes
 are only drawn if the plot is drawn, and the colorbar may be drawn
 if the plot is not drawn.

***
<a name="PROP_AUTORANGE"></a>
# PROP_AUTORANGE

true indicates the axis hasn't been changed and may/should be autoranged.

***
<a name="PROP_AUTORANGEHINTS"></a>
# PROP_AUTORANGEHINTS



***
<a name="PROP_AUTOLABEL"></a>
# PROP_AUTOLABEL

true indicates the axis label hasn't been changed by a human and may/should be autoranged.

***
<a name="PROP_FLIPPED"></a>
# PROP_FLIPPED



***
<a name="PROP_TICKVALUES"></a>
# PROP_TICKVALUES



***
<a name="copy"></a>
# copy
copy(  ) &rarr; DomNode



### Returns:
org.autoplot.dom.DomNode


<a href="https://github.com/autoplot/dev/search?q=copy&unscoped_q=copy">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="diffs"></a>
# diffs
diffs( org.autoplot.dom.DomNode node ) &rarr; List



### Parameters:
node - a DomNode

### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=diffs&unscoped_q=diffs">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getAutoRangeHints"></a>
# getAutoRangeHints
getAutoRangeHints(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getAutoRangeHints&unscoped_q=getAutoRangeHints">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getController"></a>
# getController
getController(  ) &rarr; AxisController



### Returns:
org.autoplot.dom.AxisController


<a href="https://github.com/autoplot/dev/search?q=getController&unscoped_q=getController">[search for examples]</a>

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
<a name="getLabel"></a>
# getLabel
getLabel(  ) &rarr; String

concise label for the axis.

### Returns:
the label

<a href="https://github.com/autoplot/dev/search?q=getLabel&unscoped_q=getLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRange"></a>
# getRange
getRange(  ) &rarr; DatumRange



### Returns:
org.das2.datum.DatumRange


<a href="https://github.com/autoplot/dev/search?q=getRange&unscoped_q=getRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getReference"></a>
# getReference
getReference(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getReference&unscoped_q=getReference">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getScale"></a>
# getScale
getScale(  ) &rarr; Datum



### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getScale&unscoped_q=getScale">[search for examples]</a>

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
<a name="isAutoLabel"></a>
# isAutoLabel
isAutoLabel(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isAutoLabel&unscoped_q=isAutoLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isAutoRange"></a>
# isAutoRange
isAutoRange(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isAutoRange&unscoped_q=isAutoRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDrawTickLabels"></a>
# isDrawTickLabels
isDrawTickLabels(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isDrawTickLabels&unscoped_q=isDrawTickLabels">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isFlipped"></a>
# isFlipped
isFlipped(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isFlipped&unscoped_q=isFlipped">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isLog"></a>
# isLog
isLog(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isLog&unscoped_q=isLog">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isOpposite"></a>
# isOpposite
isOpposite(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isOpposite&unscoped_q=isOpposite">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isVisible"></a>
# isVisible
isVisible(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isVisible&unscoped_q=isVisible">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAutoLabel"></a>
# setAutoLabel
setAutoLabel( boolean autolabel ) &rarr; void



### Parameters:
autolabel - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAutoLabel&unscoped_q=setAutoLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAutoRange"></a>
# setAutoRange
setAutoRange( boolean autorange ) &rarr; void



### Parameters:
autorange - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAutoRange&unscoped_q=setAutoRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAutoRangeHints"></a>
# setAutoRangeHints
setAutoRangeHints( String autoRangeHints ) &rarr; void



### Parameters:
autoRangeHints - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAutoRangeHints&unscoped_q=setAutoRangeHints">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDrawTickLabels"></a>
# setDrawTickLabels
setDrawTickLabels( boolean drawTickLabels ) &rarr; void



### Parameters:
drawTickLabels - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDrawTickLabels&unscoped_q=setDrawTickLabels">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFlipped"></a>
# setFlipped
setFlipped( boolean flipped ) &rarr; void



### Parameters:
flipped - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFlipped&unscoped_q=setFlipped">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFontSize"></a>
# setFontSize
setFontSize( String fontSize ) &rarr; void

set the font size relative to the canvas font size.  For example 
 "2em" will be twice the size.  "" is an alias for 1em.

### Parameters:
fontSize - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFontSize&unscoped_q=setFontSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLabel"></a>
# setLabel
setLabel( String label ) &rarr; void

concise label for the axis.

### Parameters:
label - the label

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLabel&unscoped_q=setLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLog"></a>
# setLog
setLog( boolean log ) &rarr; void

set the log property.  If the value makes the range invalid (log and zero),
 then the range is adjusted to make it valid.  This works because the order
 of property setters doesn't matter.

### Parameters:
log - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLog&unscoped_q=setLog">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setOpposite"></a>
# setOpposite
setOpposite( boolean opposite ) &rarr; void



### Parameters:
opposite - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setOpposite&unscoped_q=setOpposite">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRange"></a>
# setRange
setRange( DatumRange range ) &rarr; void

set the range property.  Right now, if the axis is log, and the range
 contains negative values, then the axis will be in an invalid state.
 We cannot change the range setting automatically because the next setting
 may be the log property, then the order of property setter calls would
 matter.  TODO: consider mutatorLock...  TODO: consider making the axis
 linear...

### Parameters:
range - a DatumRange

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRange&unscoped_q=setRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setReference"></a>
# setReference
setReference( String reference ) &rarr; void

draw an optional reference line at the location.  Valid entries
 can be parsed into a Datum, using the units of the axis.

### Parameters:
reference - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setReference&unscoped_q=setReference">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setScale"></a>
# setScale
setScale( Datum scale ) &rarr; void



### Parameters:
scale - a Datum

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setScale&unscoped_q=setScale">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTickValues"></a>
# setTickValues
setTickValues( String ticks ) &rarr; void

manually set the tick positions or spacing.  The following are 
 examples of accepted settings:<table>
 <tr><td></td><td>empty string is legacy behavior</td></tr>
 <tr><td>0,45,90,135,180</td><td>explicit tick positions, in axis units</td></tr>
 <tr><td>+45</td><td>spacing between tickValues, parsed with the axis offset units.</td></tr>
 <tr><td>+30s</td><td>30 seconds spacing between tickValues</td></tr>
 </table>

### Parameters:
ticks - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTickValues&unscoped_q=setTickValues">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setVisible"></a>
# setVisible
setVisible( boolean visible ) &rarr; void



### Parameters:
visible - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setVisible&unscoped_q=setVisible">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="syncTo"></a>
# syncTo
syncTo( org.autoplot.dom.DomNode n ) &rarr; void



### Parameters:
n - a DomNode

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=syncTo&unscoped_q=syncTo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

syncTo( org.autoplot.dom.DomNode n, java.util.List exclude ) &rarr; void<br>
