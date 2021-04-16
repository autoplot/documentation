# org.autoplot.dom.AxisController
AxisController( org.autoplot.dom.Application dom, org.autoplot.dom.Plot plot, org.autoplot.dom.Axis axis, org.das2.graph.DasAxis dasAxis )


***
<a name="bindTo"></a>
# bindTo
bindTo(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=bindTo&unscoped_q=bindTo">[search for examples]</a>

***
<a name="getDasAxis"></a>
# getDasAxis
getDasAxis(  ) &rarr; DasAxis



### Returns:
org.das2.graph.DasAxis


<a href="https://github.com/autoplot/dev/search?q=getDasAxis&unscoped_q=getDasAxis">[search for examples]</a>

***
<a name="removeBindings"></a>
# removeBindings
removeBindings(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeBindings&unscoped_q=removeBindings">[search for examples]</a>

***
<a name="removeReferences"></a>
# removeReferences
removeReferences(  ) &rarr; void

remove any references this object has before as it is deleted.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeReferences&unscoped_q=removeReferences">[search for examples]</a>

***
<a name="resetAxisRange"></a>
# resetAxisRange
resetAxisRange( DatumRange newRange ) &rarr; void

reset the axis range, without the units check.

### Parameters:
newRange - a DatumRange

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resetAxisRange&unscoped_q=resetAxisRange">[search for examples]</a>

***
<a name="resetAxisUnits"></a>
# resetAxisUnits
resetAxisUnits( Units nu ) &rarr; void

reset the axis units to a new unit which is convertible.

### Parameters:
nu - an Units

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resetAxisUnits&unscoped_q=resetAxisUnits">[search for examples]</a>

***
<a name="setLabelAutomatically"></a>
# setLabelAutomatically
setLabelAutomatically( String label ) &rarr; void

set the label, leaving its autoLabel property true.

### Parameters:
label - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLabelAutomatically&unscoped_q=setLabelAutomatically">[search for examples]</a>

***
<a name="setRangeAutomatically"></a>
# setRangeAutomatically
setRangeAutomatically( DatumRange range, boolean log ) &rarr; void

set the range without affecting the auto state.

### Parameters:
range - the new range
<br>log - true if the axis should be log.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRangeAutomatically&unscoped_q=setRangeAutomatically">[search for examples]</a>

***
<a name="valueIsAdjusting"></a>
# valueIsAdjusting
valueIsAdjusting(  ) &rarr; boolean

true if the Axis is adjusting, or the DasAxis which implements.

### Returns:
true if the Axis is adjusting, or the DasAxis which implements.

<a href="https://github.com/autoplot/dev/search?q=valueIsAdjusting&unscoped_q=valueIsAdjusting">[search for examples]</a>

