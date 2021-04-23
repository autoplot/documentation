# org.das2.graph.DasAxisOne dimensional axis component that transforms data to device space and back, 
 and provides controls for navigating the 1-D data space.
DasAxis( Datum min, Datum max, int orientation )
Create an axis object, relating data and canvas pixel coordinates.

DasAxis( DatumRange range, int orientation )
Create an axis object, relating data and canvas pixel coordinates.

DasAxis( Datum min, Datum max, int orientation, boolean log )
Create an axis object, relating data and canvas pixel coordinates.

***
<a name="PROP_LABEL"></a>
# PROP_LABEL



***
<a name="PROP_LOG"></a>
# PROP_LOG



***
<a name="PROP_OPPOSITE_AXIS_VISIBLE"></a>
# PROP_OPPOSITE_AXIS_VISIBLE



***
<a name="PROP_BOUNDS"></a>
# PROP_BOUNDS



***
<a name="PROP_SCAN_RANGE"></a>
# PROP_SCAN_RANGE



***
<a name="PROP_UNITS"></a>
# PROP_UNITS



***
<a name="PROPERTY_TICKS"></a>
# PROPERTY_TICKS



***
<a name="TOP"></a>
# TOP

This value indicates that the axis should be located at the top of its cell

***
<a name="BOTTOM"></a>
# BOTTOM

This value indicates that the axis should be located at the bottom of its cell

***
<a name="LEFT"></a>
# LEFT

This value indicates that the axis should be located to the left of its cell

***
<a name="RIGHT"></a>
# RIGHT

This value indicates that the axis should be located to the right of its cell

***
<a name="HORIZONTAL"></a>
# HORIZONTAL

This value indicates that the axis should be oriented horizontally

***
<a name="VERTICAL"></a>
# VERTICAL

This value indicates that the axis should be oriented vertically

***
<a name="PROPERTY_DATUMRANGE"></a>
# PROPERTY_DATUMRANGE



***
<a name="PROP_ENABLEHISTORY"></a>
# PROP_ENABLEHISTORY

true if the axis built-in history is enabled.

***
<a name="PROP_REFERENCE"></a>
# PROP_REFERENCE



***
<a name="PROP_TICKVALUES"></a>
# PROP_TICKVALUES



***
<a name="PROP_FONTSIZE"></a>
# PROP_FONTSIZE



***
<a name="PROP_LINETHICKNESS"></a>
# PROP_LINETHICKNESS



***
<a name="PROP_FLIPPED"></a>
# PROP_FLIPPED



***
<a name="PROP_FORMATSTRING"></a>
# PROP_FORMATSTRING



***
<a name="PROP_FLIPLABEL"></a>
# PROP_FLIPLABEL



***
<a name="PROP_DIVIDERDATUMFORMATTER"></a>
# PROP_DIVIDERDATUMFORMATTER



***
<a name="PROP_MINORTICKSDOMAINDIVIDER"></a>
# PROP_MINORTICKSDOMAINDIVIDER



***
<a name="PROP_MAJORTICKSDOMAINDIVIDER"></a>
# PROP_MAJORTICKSDOMAINDIVIDER



***
<a name="PROP_USEDOMAINDIVIDER"></a>
# PROP_USEDOMAINDIVIDER



***
<a name="PROP_LOCKDOMAINDIVIDER"></a>
# PROP_LOCKDOMAINDIVIDER



***
<a name="addMouseListener"></a>
# addMouseListener
addMouseListener( java.awt.event.MouseListener l ) &rarr; void

add mouse wheel listener.

### Parameters:
l - the listener

### Returns:
void (returns nothing)

### See Also:
<a href='#maybeInitializeInputPanels'>maybeInitializeInputPanels()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=addMouseListener&unscoped_q=addMouseListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addMouseMotionListener"></a>
# addMouseMotionListener
addMouseMotionListener( java.awt.event.MouseMotionListener l ) &rarr; void

add mouse motion listener.

### Parameters:
l - the listener

### Returns:
void (returns nothing)

### See Also:
<a href='#maybeInitializeInputPanels'>maybeInitializeInputPanels()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=addMouseMotionListener&unscoped_q=addMouseMotionListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addMouseWheelListener"></a>
# addMouseWheelListener
addMouseWheelListener( java.awt.event.MouseWheelListener l ) &rarr; void

Adds a MouseWheelListener to the DasAxis.  Special care must be taken
 with the DasAxis, because it is composed of two sub panels, and their
 parent panel (this), must not recieve the events.  (This is because
 the DasPlot between them should get the events, and the DasPlot does
 not have a simple rectangular boundary.

### Parameters:
l - the listener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addMouseWheelListener&unscoped_q=addMouseWheelListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addTickV"></a>
# addTickV
addTickV( Datum majorTick ) &rarr; void

add the tick to the current set of major ticks.  If the ticks were
 automatic, they will now be manual.  Note this copies the ticks into
 a new array, presuming this is done at most a few tens of times.

### Parameters:
majorTick - tick in the same units as the axis.

### Returns:
void (returns nothing)

### See Also:
<a href='#setTickV'>setTickV(double[], double[])</a> <br>

<a href="https://github.com/autoplot/dev/search?q=addTickV&unscoped_q=addTickV">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addTimeRangeSelectionListener"></a>
# addTimeRangeSelectionListener
addTimeRangeSelectionListener( org.das2.event.TimeRangeSelectionListener listener ) &rarr; void

Registers TimeRangeSelectionListener to receive events.

### Parameters:
listener - The listener to register.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addTimeRangeSelectionListener&unscoped_q=addTimeRangeSelectionListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addToFavorites"></a>
# addToFavorites
addToFavorites( DatumRange range ) &rarr; void

add the range to the favorites list, which is accessible from the popup-menu.

### Parameters:
range - the range to add.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addToFavorites&unscoped_q=addToFavorites">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="attachTo"></a>
# attachTo
attachTo( org.das2.graph.DasAxis axis ) &rarr; void

attach the axis to another axis, so they will both show the same range,
 as with a stack of time axes or with a slice.

### Parameters:
axis - the axis.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=attachTo&unscoped_q=attachTo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="clearHistory"></a>
# clearHistory
clearHistory(  ) &rarr; void

clear the internal history.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=clearHistory&unscoped_q=clearHistory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="clone"></a>
# clone
clone(  ) &rarr; Object



### Returns:
a copy of the axis, also cloning the dataRange that backs the axis.

<a href="https://github.com/autoplot/dev/search?q=clone&unscoped_q=clone">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createAttachedAxis"></a>
# createAttachedAxis
createAttachedAxis(  ) &rarr; DasAxis

create another axis that follows this axis.  It will have the same
 range and orientation.

### Returns:
attached axis.

<a href="https://github.com/autoplot/dev/search?q=createAttachedAxis&unscoped_q=createAttachedAxis">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

createAttachedAxis( int orientation ) &rarr; DasAxis<br>
***
<a name="dataRangeSelected"></a>
# dataRangeSelected
dataRangeSelected( org.das2.event.DataRangeSelectionEvent e ) &rarr; void

target event handlers to reset the axis bounds.

### Parameters:
e - the event

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dataRangeSelected&unscoped_q=dataRangeSelected">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="detach"></a>
# detach
detach(  ) &rarr; void

disconnect this from the common DataRange object that ties this to other
 axes, and create a new DataRange.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=detach&unscoped_q=detach">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="findTick"></a>
# <del>findTick</del>
Deprecated: Use getTickVDescriptor.findTick
***
<a name="getActiveRegion"></a>
# getActiveRegion
getActiveRegion(  ) &rarr; Shape

get the region containing the axis.

### Returns:
the region containing the axis.

<a href="https://github.com/autoplot/dev/search?q=getActiveRegion&unscoped_q=getActiveRegion">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getAffineTransform"></a>
# getAffineTransform
getAffineTransform( org.das2.graph.DasAxis.Memento memento, java.awt.geom.AffineTransform at ) &rarr; AffineTransform

return the AffineTransform, or null.  The transform will be applied after the input
 transform is applied.  So to just get the transform, pass in identity.

### Parameters:
memento - memento from another axis state.
<br>at - initial transform

### Returns:
the transform from that state to this state, or null if no transform can be created.

<a href="https://github.com/autoplot/dev/search?q=getAffineTransform&unscoped_q=getAffineTransform">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDLength"></a>
# getDLength
getDLength(  ) &rarr; int

return the length of the axis in pixels.

### Returns:
returns the length of the axis in pixels.

<a href="https://github.com/autoplot/dev/search?q=getDLength&unscoped_q=getDLength">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataMaximum"></a>
# getDataMaximum
getDataMaximum(  ) &rarr; Datum

return the maximum value

### Returns:
the maximum value

<a href="https://github.com/autoplot/dev/search?q=getDataMaximum&unscoped_q=getDataMaximum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getDataMaximum( Units units ) &rarr; double<br>
***
<a name="getDataMinimum"></a>
# getDataMinimum
getDataMinimum(  ) &rarr; Datum

return the minimum value

### Returns:
the minimum value

<a href="https://github.com/autoplot/dev/search?q=getDataMinimum&unscoped_q=getDataMinimum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getDataMinimum( Units units ) &rarr; double<br>
***
<a name="getDataPath"></a>
# getDataPath
getDataPath(  ) &rarr; String

return the path for the TCA dataset.  This will be a das2server data set
 address, such as http://www-pw.physics.uiowa.edu/das/das2Server?voyager/tca/earth

### Returns:
the path of the TCA dataset, or "".

<a href="https://github.com/autoplot/dev/search?q=getDataPath&unscoped_q=getDataPath">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataRange"></a>
# getDataRange
getDataRange(  ) &rarr; DataRange

return the mutable DataRange object.  This is used 
 to bind axes together by sharing an internal model.

### Returns:
the DataRange.

<a href="https://github.com/autoplot/dev/search?q=getDataRange&unscoped_q=getDataRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDatumFormatter"></a>
# getDatumFormatter
getDatumFormatter(  ) &rarr; DatumFormatter

return the formatter which converts Datum tick positions to a string.

### Returns:
the formatter which converts Datum tick positions to a string.

<a href="https://github.com/autoplot/dev/search?q=getDatumFormatter&unscoped_q=getDatumFormatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDatumRange"></a>
# getDatumRange
getDatumRange(  ) &rarr; DatumRange

return the current range

### Returns:
the current range

<a href="https://github.com/autoplot/dev/search?q=getDatumRange&unscoped_q=getDatumRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDevicePosition"></a>
# <del>getDevicePosition</del>
Deprecated: this should not be used.
***
<a name="getDividerDatumFormatter"></a>
# getDividerDatumFormatter
getDividerDatumFormatter(  ) &rarr; DatumFormatter



### Returns:
org.das2.datum.format.DatumFormatter


<a href="https://github.com/autoplot/dev/search?q=getDividerDatumFormatter&unscoped_q=getDividerDatumFormatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDrawTca"></a>
# <del>getDrawTca</del>
Deprecated: use isDrawTca()
***
<a name="getFontSize"></a>
# getFontSize
getFontSize(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getFontSize&unscoped_q=getFontSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFormat"></a>
# getFormat
getFormat(  ) &rarr; String

return the format string for each tick.

### Returns:
the format string for each tick.

<a href="https://github.com/autoplot/dev/search?q=getFormat&unscoped_q=getFormat">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLabel"></a>
# getLabel
getLabel(  ) &rarr; String

get the label for the axis.

### Returns:
A String instance that contains the title displayed
    for this axis, or "" if the axis has no title.

<a href="https://github.com/autoplot/dev/search?q=getLabel&unscoped_q=getLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLabelFont"></a>
# getLabelFont
getLabelFont(  ) &rarr; Font

get the font for labels.  If the component currently has null for the
 font, then Font.decode("sans-12") is used.

### Returns:
the font to use for labels.

<a href="https://github.com/autoplot/dev/search?q=getLabelFont&unscoped_q=getLabelFont">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLabelOffset"></a>
# getLabelOffset
getLabelOffset(  ) &rarr; String



### Returns:
the label offset.

<a href="https://github.com/autoplot/dev/search?q=getLabelOffset&unscoped_q=getLabelOffset">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLineSpacing"></a>
# getLineSpacing
getLineSpacing(  ) &rarr; int

calculate the spacing (whitespace) between the TCA items.

### Returns:
the spacing between lines.

<a href="https://github.com/autoplot/dev/search?q=getLineSpacing&unscoped_q=getLineSpacing">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLineThickness"></a>
# getLineThickness
getLineThickness(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getLineThickness&unscoped_q=getLineThickness">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMajorTicksDomainDivider"></a>
# getMajorTicksDomainDivider
getMajorTicksDomainDivider(  ) &rarr; DomainDivider

return the domain divider for major ticks, or null.

### Returns:
the domain divider for major ticks, or null.

<a href="https://github.com/autoplot/dev/search?q=getMajorTicksDomainDivider&unscoped_q=getMajorTicksDomainDivider">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMasterAxis"></a>
# getMasterAxis
getMasterAxis(  ) &rarr; DasAxis

return the axis this is attached to.

### Returns:
the axis this is attached to.

<a href="https://github.com/autoplot/dev/search?q=getMasterAxis&unscoped_q=getMasterAxis">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMemento"></a>
# getMemento
getMemento(  ) &rarr; Memento

get the memento object which identifies the state of the axis transformation.

### Returns:
the momento.

<a href="https://github.com/autoplot/dev/search?q=getMemento&unscoped_q=getMemento">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMinorTicksDomainDivider"></a>
# getMinorTicksDomainDivider
getMinorTicksDomainDivider(  ) &rarr; DomainDivider

return the domain divider for minor ticks, or null.

### Returns:
the domain divider for minor ticks, or null.

<a href="https://github.com/autoplot/dev/search?q=getMinorTicksDomainDivider&unscoped_q=getMinorTicksDomainDivider">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getOrientation"></a>
# getOrientation
getOrientation(  ) &rarr; int

returns the orientation of the axis, which is one of BOTTOM,TOP,LEFT or RIGHT.

### Returns:
BOTTOM,TOP,LEFT or RIGHT.

<a href="https://github.com/autoplot/dev/search?q=getOrientation&unscoped_q=getOrientation">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRange"></a>
# <del>getRange</del>
Deprecated: use getDatumRange instead.
***
<a name="getReference"></a>
# getReference
getReference(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getReference&unscoped_q=getReference">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getScanRange"></a>
# getScanRange
getScanRange(  ) &rarr; DatumRange

get the limit the scan buttons, which may be null.

### Returns:
the limit the scan buttons, which may be null.

<a href="https://github.com/autoplot/dev/search?q=getScanRange&unscoped_q=getScanRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTickDirection"></a>
# getTickDirection
getTickDirection(  ) &rarr; int

return the tick direction, 1=down or left, -1=up or right

### Returns:
1=down or left, -1=up or right

<a href="https://github.com/autoplot/dev/search?q=getTickDirection&unscoped_q=getTickDirection">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTickLabelFont"></a>
# getTickLabelFont
getTickLabelFont(  ) &rarr; Font

get the font for tick labels.  If the component currently has null for the
 font, then Font.decode("sans-12") is used and a warning logged.

### Returns:
the font to use for ticks.

<a href="https://github.com/autoplot/dev/search?q=getTickLabelFont&unscoped_q=getTickLabelFont">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTickLength"></a>
# getTickLength
getTickLength(  ) &rarr; String

get the tick length string, for example "0.66em"

### Returns:
the tick length string

<a href="https://github.com/autoplot/dev/search?q=getTickLength&unscoped_q=getTickLength">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTickLines"></a>
# getTickLines
getTickLines(  ) &rarr; int

return the number of lines that the ticks use.

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=getTickLines&unscoped_q=getTickLines">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTickV"></a>
# getTickV
getTickV(  ) &rarr; TickVDescriptor

return the current set of ticks.

### Returns:
the current set of ticks.

<a href="https://github.com/autoplot/dev/search?q=getTickV&unscoped_q=getTickV">[search for examples]</a>

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
<a name="getUnits"></a>
# getUnits
getUnits(  ) &rarr; Units

return the units of the axis.

### Returns:
the units of the axis.

<a href="https://github.com/autoplot/dev/search?q=getUnits&unscoped_q=getUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getUserDatumFormatter"></a>
# getUserDatumFormatter
getUserDatumFormatter(  ) &rarr; DatumFormatter

get the userDatumFormatter, which converts Datums into Strings.  This
 can be null if none should be used.

### Returns:
the userDatumFormatter.

<a href="https://github.com/autoplot/dev/search?q=getUserDatumFormatter&unscoped_q=getUserDatumFormatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="invTransform"></a>
# invTransform
invTransform( double idata1, double idata2 ) &rarr; DatumRange

get the range covered by the two points.  This allows clients to
 get a range without having to worry about the flipped property.

### Parameters:
idata1 - pixel position on the axis, in the canvas frame.
<br>idata2 - pixel position on the axis, in the canvas frame.

### Returns:
DatumRange implied by the two pixel positions.

<a href="https://github.com/autoplot/dev/search?q=invTransform&unscoped_q=invTransform">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

invTransform( double idata ) &rarr; Datum<br>
***
<a name="isAnimated"></a>
# isAnimated
isAnimated(  ) &rarr; boolean

true if the axis is animated.  Transitions in axis position are drawn 
 rapidly to animate the transition.

### Returns:
true if the axis is animated.

<a href="https://github.com/autoplot/dev/search?q=isAnimated&unscoped_q=isAnimated">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isAttached"></a>
# isAttached
isAttached(  ) &rarr; boolean

return true if this is attached to another axis.

### Returns:
true if this is attached to another axis.

<a href="https://github.com/autoplot/dev/search?q=isAttached&unscoped_q=isAttached">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDrawTca"></a>
# isDrawTca
isDrawTca(  ) &rarr; boolean

true if additional tick labels are drawn using the TCA function.

### Returns:
true if additional ticks will be drawn.
### See Also:
<a href='#setTcaFunction'>setTcaFunction(org.das2.qds.QFunction)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isDrawTca&unscoped_q=isDrawTca">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isEnableHistory"></a>
# isEnableHistory
isEnableHistory(  ) &rarr; boolean

true if the axis built-in history is enabled.

### Returns:
true if the axis built-in history is enabled.

<a href="https://github.com/autoplot/dev/search?q=isEnableHistory&unscoped_q=isEnableHistory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isFlipLabel"></a>
# isFlipLabel
isFlipLabel(  ) &rarr; boolean

true if the right vertical label should be flipped.

### Returns:
true if the right vertical label should be flipped.

<a href="https://github.com/autoplot/dev/search?q=isFlipLabel&unscoped_q=isFlipLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isFlipped"></a>
# isFlipped
isFlipped(  ) &rarr; boolean

return true if the axis is flipped.

### Returns:
true if the axis is flipped.

<a href="https://github.com/autoplot/dev/search?q=isFlipped&unscoped_q=isFlipped">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isHorizontal"></a>
# isHorizontal
isHorizontal(  ) &rarr; boolean

test if the axis is horizontal.

### Returns:
true if the orientation is BOTTOM or TOP.

<a href="https://github.com/autoplot/dev/search?q=isHorizontal&unscoped_q=isHorizontal">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isLockDomainDivider"></a>
# isLockDomainDivider
isLockDomainDivider(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isLockDomainDivider&unscoped_q=isLockDomainDivider">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isLog"></a>
# isLog
isLog(  ) &rarr; boolean

return true if the axis is log.

### Returns:
true if the axis is log.

<a href="https://github.com/autoplot/dev/search?q=isLog&unscoped_q=isLog">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isOppositeAxisVisible"></a>
# isOppositeAxisVisible
isOppositeAxisVisible(  ) &rarr; boolean

return true if the opposite side is also drawn.

### Returns:
true if the opposite side is also drawn.

<a href="https://github.com/autoplot/dev/search?q=isOppositeAxisVisible&unscoped_q=isOppositeAxisVisible">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isTcaLoaded"></a>
# isTcaLoaded
isTcaLoaded(  ) &rarr; boolean

true if the TCA data has been loaded and the axis bounds reflect TCA data present.

### Returns:
true if the TCA data has been loaded and the axis bounds reflect TCA data present.

<a href="https://github.com/autoplot/dev/search?q=isTcaLoaded&unscoped_q=isTcaLoaded">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isTickLabelsVisible"></a>
# isTickLabelsVisible
isTickLabelsVisible(  ) &rarr; boolean

true if the tick labels should be drawn.

### Returns:
true if the tick labels should be drawn.

<a href="https://github.com/autoplot/dev/search?q=isTickLabelsVisible&unscoped_q=isTickLabelsVisible">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isUseDomainDivider"></a>
# isUseDomainDivider
isUseDomainDivider(  ) &rarr; boolean

true if the domain divider should be used.  This is a new object that
 locates ticks.

### Returns:
true if the domain divider should be used.

<a href="https://github.com/autoplot/dev/search?q=isUseDomainDivider&unscoped_q=isUseDomainDivider">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mutatorLock"></a>
# mutatorLock
mutatorLock(  ) &rarr; Lock

get an object to lock the axis for multiple operations.

### Returns:
an org.das2.graph.DasAxis.Lock


<a href="https://github.com/autoplot/dev/search?q=mutatorLock&unscoped_q=mutatorLock">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeFromFavorites"></a>
# removeFromFavorites
removeFromFavorites( DatumRange range ) &rarr; void

remove the range from the favorites list, which is accessible from the popup-menu.

### Parameters:
range - the range to add.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeFromFavorites&unscoped_q=removeFromFavorites">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeMouseListener"></a>
# removeMouseListener
removeMouseListener( java.awt.event.MouseListener l ) &rarr; void

remove mouse motion listener.

### Parameters:
l - the listener

### Returns:
void (returns nothing)

### See Also:
<a href='#maybeInitializeInputPanels'>maybeInitializeInputPanels()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=removeMouseListener&unscoped_q=removeMouseListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeMouseMotionListener"></a>
# removeMouseMotionListener
removeMouseMotionListener( java.awt.event.MouseMotionListener l ) &rarr; void

remove mouse motion listener.

### Parameters:
l - the listener

### Returns:
void (returns nothing)

### See Also:
<a href='#maybeInitializeInputPanels'>maybeInitializeInputPanels()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=removeMouseMotionListener&unscoped_q=removeMouseMotionListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeMouseWheelListener"></a>
# removeMouseWheelListener
removeMouseWheelListener( java.awt.event.MouseWheelListener l ) &rarr; void

remove mouse wheel listener.

### Parameters:
l - the listener

### Returns:
void (returns nothing)

### See Also:
<a href='#maybeInitializeInputPanels'>maybeInitializeInputPanels()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=removeMouseWheelListener&unscoped_q=removeMouseWheelListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeTimeRangeSelectionListener"></a>
# removeTimeRangeSelectionListener
removeTimeRangeSelectionListener( org.das2.event.TimeRangeSelectionListener listener ) &rarr; void

Removes TimeRangeSelectionListener from the list of listeners.

### Parameters:
listener - The listener to remove.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeTimeRangeSelectionListener&unscoped_q=removeTimeRangeSelectionListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resetRange"></a>
# resetRange
resetRange( DatumRange range ) &rarr; void

set the axis to the new range, allowing the units to change.

### Parameters:
range - the new range

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resetRange&unscoped_q=resetRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resize"></a>
# resize
resize(  ) &rarr; void

reset bounds (and unused transform), invalidate the tickV, etc.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resize&unscoped_q=resize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="scanNext"></a>
# scanNext
scanNext(  ) &rarr; void

scan to the next interval.  If we were looking at a day with fuzz, then
 scan to the next day.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=scanNext&unscoped_q=scanNext">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="scanPrevious"></a>
# scanPrevious
scanPrevious(  ) &rarr; void

scan to the previous interval.  If we were looking at a day with fuzz, then
 scan to the previous day.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=scanPrevious&unscoped_q=scanPrevious">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAnimated"></a>
# setAnimated
setAnimated( boolean animated ) &rarr; void

if true then the axis will be animated.

### Parameters:
animated - if true then the axis will be animated.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAnimated&unscoped_q=setAnimated">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataMaximum"></a>
# setDataMaximum
setDataMaximum( Datum max ) &rarr; void

set the bigger extent of the range of this axis.

### Parameters:
max - the new value

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataMaximum&unscoped_q=setDataMaximum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataMinimum"></a>
# setDataMinimum
setDataMinimum( Datum min ) &rarr; void

set the smaller extent of the range of this axis.

### Parameters:
min - the new value

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataMinimum&unscoped_q=setDataMinimum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataPath"></a>
# setDataPath
setDataPath( String dataset ) &rarr; void



### Parameters:
dataset - The URL identifier string of a TCA data set, or "" for no TCAs.

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/setDrawTca which turns on additional ticks/.md'>setDrawTca which turns on additional ticks.</a> which turns on additional ticks.<br>

<a href="https://github.com/autoplot/dev/search?q=setDataPath&unscoped_q=setDataPath">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataRange"></a>
# setDataRange
setDataRange( Datum minimum, Datum maximum ) &rarr; void

Set the data range.  minimum must be less than maximum, but for nominal
 data they can be equal.

### Parameters:
minimum - the minimum value
<br>maximum - the maximum value

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataRange&unscoped_q=setDataRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataRangeForward"></a>
# setDataRangeForward
setDataRangeForward(  ) &rarr; void

set the range to the next interval.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataRangeForward&unscoped_q=setDataRangeForward">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataRangePrev"></a>
# setDataRangePrev
setDataRangePrev(  ) &rarr; void

set the range to the previous interval.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataRangePrev&unscoped_q=setDataRangePrev">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataRangeZoomOut"></a>
# setDataRangeZoomOut
setDataRangeZoomOut(  ) &rarr; void

set the range to min-width to max+width.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataRangeZoomOut&unscoped_q=setDataRangeZoomOut">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDatumRange"></a>
# setDatumRange
setDatumRange( DatumRange dr ) &rarr; void

Set the range for the axis.  Note this is allowed to change the units as well.

### Parameters:
dr - the new range.  The range must be interval or ratio measurements.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDatumRange&unscoped_q=setDatumRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDividerDatumFormatter"></a>
# setDividerDatumFormatter
setDividerDatumFormatter( org.das2.datum.format.DatumFormatter dividerDatumFormatter ) &rarr; void



### Parameters:
dividerDatumFormatter - a DatumFormatter

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDividerDatumFormatter&unscoped_q=setDividerDatumFormatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDrawTca"></a>
# setDrawTca
setDrawTca( boolean b ) &rarr; void

if true then turn on additional tick labels using the TCA function.

### Parameters:
b - if true then additional ticks will be drawn.

### Returns:
void (returns nothing)

### See Also:
<a href='#setTcaFunction'>setTcaFunction(org.das2.qds.QFunction)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setDrawTca&unscoped_q=setDrawTca">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setEnableHistory"></a>
# setEnableHistory
setEnableHistory( boolean enableHistory ) &rarr; void

true if the axis built-in history is enabled.

### Parameters:
enableHistory - true if the axis built-in history is enabled.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setEnableHistory&unscoped_q=setEnableHistory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFlipLabel"></a>
# setFlipLabel
setFlipLabel( boolean flipLabel ) &rarr; void

true if the right vertical label should be flipped.

### Parameters:
flipLabel - true if the right vertical label should be flipped.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFlipLabel&unscoped_q=setFlipLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFlipped"></a>
# setFlipped
setFlipped( boolean b ) &rarr; void

flip over the axis.

### Parameters:
b - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFlipped&unscoped_q=setFlipped">[search for examples]</a>

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
<a name="setFormat"></a>
# setFormat
setFormat( String formatString ) &rarr; void

set a hint at the format string.  Examples include:<ul>
  <li> 0.000
  <li> %H:%M!c%Y-%j
  <li> 0
 </ul>

### Parameters:
formatString - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFormat&unscoped_q=setFormat">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLabel"></a>
# setLabel
setLabel( String t ) &rarr; void

set the label for the axis.
 
 The label for this axis is displayed below the ticks for horizontal axes
 or to left of the ticks for vertical axes.

### Parameters:
t - The new label for this axis

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLabel&unscoped_q=setLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLabelOffset"></a>
# setLabelOffset
setLabelOffset( String spec ) &rarr; void

explicitly set the position of the label from the axis.
 For example, "4em" will position the y-axis label 4ems away from the
 axis.  Empty string is default automatic behavior.

### Parameters:
spec - offset string like "5em+5px"

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLabelOffset&unscoped_q=setLabelOffset">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLeftXLabelOverride"></a>
# <del>setLeftXLabelOverride</del>
Deprecated: use setLabelOffset instead.
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

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLockDomainDivider"></a>
# setLockDomainDivider
setLockDomainDivider( boolean lockDomainDivider ) &rarr; void

don't allow the domain divider to adjust.

### Parameters:
lockDomainDivider - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLockDomainDivider&unscoped_q=setLockDomainDivider">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLog"></a>
# setLog
setLog( boolean log ) &rarr; void

Set the axis to be log or linear.  If necessary, axis range will be 
 adjusted to make the range valid.

### Parameters:
log - true if the axis should be log.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLog&unscoped_q=setLog">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setMajorTicksDomainDivider"></a>
# setMajorTicksDomainDivider
setMajorTicksDomainDivider( org.das2.datum.DomainDivider majorTicksDomainDivider ) &rarr; void



### Parameters:
majorTicksDomainDivider - a DomainDivider

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMajorTicksDomainDivider&unscoped_q=setMajorTicksDomainDivider">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setMinorTicksDomainDivider"></a>
# setMinorTicksDomainDivider
setMinorTicksDomainDivider( org.das2.datum.DomainDivider minorTicksDomainDivider ) &rarr; void



### Parameters:
minorTicksDomainDivider - a DomainDivider

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMinorTicksDomainDivider&unscoped_q=setMinorTicksDomainDivider">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setNextAction"></a>
# setNextAction
setNextAction( String label, javax.swing.AbstractAction abstractAction ) &rarr; void

set the action for the next button

### Parameters:
label - the label (step or scan)
<br>abstractAction - the action to invoke.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setNextAction&unscoped_q=setNextAction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setNextActionLabel"></a>
# setNextActionLabel
setNextActionLabel( String label, String tooltip ) &rarr; void

set the label for the popup button

### Parameters:
label - concise label
<br>tooltip - text for popup tooltip

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setNextActionLabel&unscoped_q=setNextActionLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setOppositeAxisVisible"></a>
# setOppositeAxisVisible
setOppositeAxisVisible( boolean visible ) &rarr; void

if true, then the axis and its ticks on the opposite side will also be drawn.

### Parameters:
visible - if true, then the axis and its ticks on the opposite side will also be drawn.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setOppositeAxisVisible&unscoped_q=setOppositeAxisVisible">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setOrientation"></a>
# setOrientation
setOrientation( int orientation ) &rarr; void

Set the axis orientation.  One of: DasAxis.TOP, DasAxis.BOTTOM,
  DasAxis.LEFT, DasAxis.RIGHT

### Parameters:
orientation - the orientation, one of TOP,BOTTOM,LEFT,RIGHT.

### Returns:
void (returns nothing)

### See Also:
<a href='#TOP'>TOP</a> <br>
<a href='#BOTTOM'>BOTTOM</a> <br>
<a href='#LEFT'>LEFT</a> <br>
<a href='#RIGHT'>RIGHT</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setOrientation&unscoped_q=setOrientation">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPlot"></a>
# setPlot
setPlot( org.das2.graph.DasPlot p ) &rarr; void

set the plot that will get updates

### Parameters:
p - plot object.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPlot&unscoped_q=setPlot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPreviousAction"></a>
# setPreviousAction
setPreviousAction( String label, javax.swing.AbstractAction abstractAction ) &rarr; void

set the action for the prev button

### Parameters:
label - the label (step or scan)
<br>abstractAction - the action to invoke.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPreviousAction&unscoped_q=setPreviousAction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPreviousActionLabel"></a>
# setPreviousActionLabel
setPreviousActionLabel( String label, String tooltip ) &rarr; void

set the label for the popup button

### Parameters:
label - concise label
<br>tooltip - text for popup tooltip

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPreviousActionLabel&unscoped_q=setPreviousActionLabel">[search for examples]</a>

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
<a name="setScanRange"></a>
# setScanRange
setScanRange( DatumRange range ) &rarr; void

limit the scan buttons to operate within this range.
 http://sourceforge.net/p/autoplot/bugs/473/

### Parameters:
range - the range to limit the scanning

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setScanRange&unscoped_q=setScanRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTcaFunction"></a>
# setTcaFunction
setTcaFunction( org.das2.qds.QFunction f ) &rarr; void

Add auxiliary data to an axis (usually OrbitAttitude data for a time axis).
 This function does the same thing as setDataPath, but with a different interface.
 The QFunction must have one input parameter which will be positions on this axis 
 (e.g. times from a time axis).

### Parameters:
f - will be called upon to generate auxiliary data sets, or null to disable.

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/setDrawTca which turns on additional ticks/.md'>setDrawTca which turns on additional ticks.</a> which turns on additional ticks.<br>

<a href="https://github.com/autoplot/dev/search?q=setTcaFunction&unscoped_q=setTcaFunction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTickLabelsVisible"></a>
# setTickLabelsVisible
setTickLabelsVisible( boolean b ) &rarr; void

set true if the tick labels should be drawn.

### Parameters:
b - true if the tick labels should be drawn.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTickLabelsVisible&unscoped_q=setTickLabelsVisible">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTickLength"></a>
# setTickLength
setTickLength( String tickLengthStr ) &rarr; void

set the tick length string, for example
 "0.33em" "5px" "-0.33em"

### Parameters:
tickLengthStr - the tick length string.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTickLength&unscoped_q=setTickLength">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTickV"></a>
# setTickV
setTickV( double[] minorTicks, double[] majorTicks ) &rarr; void

convenience method for manually setting the ticks so the user
 needn't understand TickVDescriptor.  setTickV(null) can be 
 used to reset the ticks as well as setTickV(null,null).

### Parameters:
minorTicks - the minor ticks, or null (None) for the current minor ticks
<br>majorTicks - the major ticks, or null (None) to automatic.

### Returns:
void (returns nothing)

### See Also:
<a href='#setTickV'>setTickV(org.das2.graph.TickVDescriptor)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setTickV&unscoped_q=setTickV">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

setTickV( org.das2.graph.TickVDescriptor tickV ) &rarr; void<br>
***
<a name="setTickValues"></a>
# setTickValues
setTickValues( String ticks ) &rarr; void

manually set the tick positions or spacing.  The following are 
 examples of accepted settings:<table>
 <tr><td></td><td>empty string is automatic behavior</td></tr>
 <tr><td>0,45,90,135,180</td><td>explicit tick positions, in axis units</td></tr>
 <tr><td>+45</td><td>spacing between ticks, parsed with the axis offset units.</td></tr>
 <tr><td>+20s/4</td><td>every 20 seconds, with four minor divisions.</td></tr>
 <tr><td>+30s</td><td>30 seconds spacing between ticks</td></tr>
 <tr><td>*10/2,3,4,5,6,7,8,9</td><td>normal log axis.</td></tr>
 <tr><td>*1e2/5,10,50</td><td>log major ticks should be every two cycles</td></tr>
 <tr><td>*5/2,3,4</td><td>log major ticks at 1,5,25/</td></tr>
 </table>

### Parameters:
ticks - a String

### Returns:
void (returns nothing)

### See Also:
<a href='https://cdn.graphpad.com/faq/1910/file/1487logaxes.pdf about log axes.'>https://cdn.graphpad.com/faq/1910/file/1487logaxes.pdf about log axes.</a> about log axes.<br>
<a href='GraphUtil.md#calculateManualTicks'>GraphUtil#calculateManualTicks(java.lang.String, org.das2.datum.DatumRange, boolean)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setTickValues&unscoped_q=setTickValues">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setUnits"></a>
# setUnits
setUnits( Units newUnits ) &rarr; void

set the units of the axis, which must be convertible from the old units.

### Parameters:
newUnits - the units of the axis.

### Returns:
void (returns nothing)

### See Also:
<a href='#resetRange'>resetRange(org.das2.datum.DatumRange)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setUnits&unscoped_q=setUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setUseDomainDivider"></a>
# setUseDomainDivider
setUseDomainDivider( boolean useDomainDivider ) &rarr; void

true if the domain divider should be used.  This is a new object that
 locates ticks.

### Parameters:
useDomainDivider - true if the domain divider should be used.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUseDomainDivider&unscoped_q=setUseDomainDivider">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setUserDatumFormatter"></a>
# setUserDatumFormatter
setUserDatumFormatter( org.das2.datum.format.DatumFormatter userDatumFormatter ) &rarr; void

set the userDatumFormatter, which converts Datums into Strings.  This
 can be null if none should be used.

### Parameters:
userDatumFormatter - the userDatumFormatter.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUserDatumFormatter&unscoped_q=setUserDatumFormatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setVisible"></a>
# setVisible
setVisible( boolean aFlag ) &rarr; void

set the component visible or invisible. The axis bounds are updated.  So in addition to the JComponent visibility, this
 also makes a useful property to completely hide the axis.  drawTickLabels hides the labels but still draws the ticks, this
 completely hides the axis.  Note too that even though it is not visible, tick positions are still updated to support
 drawing a grid on the plot.

### Parameters:
aFlag - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setVisible&unscoped_q=setVisible">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="timeRangeSelected"></a>
# timeRangeSelected
timeRangeSelected( org.das2.event.TimeRangeSelectionEvent e ) &rarr; void

call back for time range selection event.

### Parameters:
e - the event

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=timeRangeSelected&unscoped_q=timeRangeSelected">[search for examples]</a>

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
<a name="transform"></a>
# transform
transform( Datum datum ) &rarr; double

Transforms a Datum in data coordinates to a horizontal or vertical
 position on the parent canvas.

### Parameters:
datum - a data value

### Returns:
Horizontal or vertical position on the canvas.

<a href="https://github.com/autoplot/dev/search?q=transform&unscoped_q=transform">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

transform( double data, Units units ) &rarr; double<br>
transform( QDataSet data, Units units ) &rarr; double<br>
transform( QDataSet data ) &rarr; double<br>
***
<a name="valueIsAdjusting"></a>
# valueIsAdjusting
valueIsAdjusting(  ) &rarr; boolean

true if a lock is out and an object is rapidly mutating the object.
 clients listening for property changes can safely ignore property
 changes while valueIsAdjusting is true, as they should receive a
 final propertyChangeEvent after the lock is released.  (note it's not
 clear who is responsible for this.
 See http://das2.org/wiki/index.php/Das2.valueIsAdjusting)

### Returns:
true if valueIsAdjusting

<a href="https://github.com/autoplot/dev/search?q=valueIsAdjusting&unscoped_q=valueIsAdjusting">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

