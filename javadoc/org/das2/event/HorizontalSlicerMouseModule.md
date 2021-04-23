# org.das2.event.HorizontalSlicerMouseModule

Slices spectrogram horizontally, e.g. showing one channel vs time.

# HorizontalSlicerMouseModule( org.das2.graph.DasPlot parent, org.das2.dataset.TableDataSetConsumer dataSetConsumer, org.das2.graph.DasAxis xaxis, org.das2.graph.DasAxis yaxis )


***
<a name="addDataPointSelectionListener"></a>
# addDataPointSelectionListener
addDataPointSelectionListener( org.das2.event.DataPointSelectionListener listener ) &rarr; void

Registers DataPointSelectionListener to receive events.

### Parameters:
listener - The listener to register.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addDataPointSelectionListener&unscoped_q=addDataPointSelectionListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="create"></a>
# create
create( org.das2.graph.DasPlot parent ) &rarr; HorizontalSlicerMouseModule



### Parameters:
parent - a DasPlot

### Returns:
org.das2.event.HorizontalSlicerMouseModule


<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

create( org.das2.graph.Renderer renderer ) &rarr; HorizontalSlicerMouseModule<br>
***
<a name="getSlicer"></a>
# getSlicer
getSlicer(  ) &rarr; HorizontalSpectrogramSlicer

return the slicer listening to the slices.  This returns the 
 first one found.

### Returns:
the slicer

<a href="https://github.com/autoplot/dev/search?q=getSlicer&unscoped_q=getSlicer">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mousePointSelected"></a>
# mousePointSelected
mousePointSelected( org.das2.event.MousePointSelectionEvent e ) &rarr; void



### Parameters:
e - a MousePointSelectionEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mousePointSelected&unscoped_q=mousePointSelected">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeDataPointSelectionListener"></a>
# removeDataPointSelectionListener
removeDataPointSelectionListener( org.das2.event.DataPointSelectionListener listener ) &rarr; void

Removes DataPointSelectionListener from the list of listeners.

### Parameters:
listener - The listener to remove.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeDataPointSelectionListener&unscoped_q=removeDataPointSelectionListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

