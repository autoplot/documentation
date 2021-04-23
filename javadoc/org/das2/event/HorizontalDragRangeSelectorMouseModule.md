# org.das2.event.HorizontalDragRangeSelectorMouseModuleWith the HorizontalDragRangeRenderer and VerticalSpectrogramAverager,
 this shows the average over an interval.
HorizontalDragRangeSelectorMouseModule( org.das2.graph.DasPlot parent, org.das2.dataset.DataSetConsumer dataSetConsumer, org.das2.graph.DasAxis axis )


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
create( org.das2.graph.DasPlot parent ) &rarr; HorizontalDragRangeSelectorMouseModule



### Parameters:
parent - a DasPlot

### Returns:
org.das2.event.HorizontalDragRangeSelectorMouseModule


<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataRangeSelectionListener"></a>
# getDataRangeSelectionListener
getDataRangeSelectionListener( int index ) &rarr; DataRangeSelectionListener

allow a peek at the listener.

### Parameters:
index - an int

### Returns:
the listener at the index.

<a href="https://github.com/autoplot/dev/search?q=getDataRangeSelectionListener&unscoped_q=getDataRangeSelectionListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataRangeSelectionListenerCount"></a>
# getDataRangeSelectionListenerCount
getDataRangeSelectionListenerCount(  ) &rarr; int

allow a peek at the listeners.

### Returns:
the number of listeners.

<a href="https://github.com/autoplot/dev/search?q=getDataRangeSelectionListenerCount&unscoped_q=getDataRangeSelectionListenerCount">[search for examples]</a>

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

