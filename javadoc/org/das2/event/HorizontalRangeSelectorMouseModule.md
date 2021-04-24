# org.das2.event.HorizontalRangeSelectorMouseModule



# HorizontalRangeSelectorMouseModule( org.das2.graph.DasCanvasComponent parent, org.das2.graph.DasAxis axis )


***
<a name="addDataRangeSelectionListener"></a>
# addDataRangeSelectionListener
addDataRangeSelectionListener( org.das2.event.DataRangeSelectionListener listener ) &rarr; void

Registers DataRangeSelectionListener to receive events.

### Parameters:
listener - The listener to register.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addDataRangeSelectionListener&unscoped_q=addDataRangeSelectionListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="create"></a>
# create
create( org.das2.graph.DasPlot parent ) &rarr; HorizontalRangeSelectorMouseModule



### Parameters:
parent - a DasPlot

### Returns:
org.das2.event.HorizontalRangeSelectorMouseModule


<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mouseRangeSelected"></a>
# mouseRangeSelected
mouseRangeSelected( org.das2.event.MouseDragEvent e0 ) &rarr; void



### Parameters:
e0 - a MouseDragEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mouseRangeSelected&unscoped_q=mouseRangeSelected">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mouseWheelMoved"></a>
# mouseWheelMoved
mouseWheelMoved( java.awt.event.MouseWheelEvent e ) &rarr; void

mouse wheel events zoom or pan rapidly.  With a physical wheel, I (jbf) found
 that I get 17ms per click, and this is manageable.  With a touchpad on a mac,
 these events come much faster, like 10ms per click, which can disorient the
 operator.  So we limit the speed to 20ms per click, for now by dropping
 rapid clicks.

### Parameters:
e - a MouseWheelEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mouseWheelMoved&unscoped_q=mouseWheelMoved">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeDataRangeSelectionListener"></a>
# removeDataRangeSelectionListener
removeDataRangeSelectionListener( org.das2.event.DataRangeSelectionListener listener ) &rarr; void

Removes DataRangeSelectionListener from the list of listeners.

### Parameters:
listener - The listener to remove.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeDataRangeSelectionListener&unscoped_q=removeDataRangeSelectionListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

