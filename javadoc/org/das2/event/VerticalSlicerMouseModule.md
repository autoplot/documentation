# org.das2.event.VerticalSlicerMouseModule
VerticalSlicerMouseModule( org.das2.graph.DasCanvasComponent parent, org.das2.dataset.DataSetConsumer dataSetConsumer, org.das2.graph.DasAxis xaxis, org.das2.graph.DasAxis yaxis )


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
create( org.das2.graph.DasPlot parent ) &rarr; VerticalSlicerMouseModule



### Parameters:
parent - a DasPlot

### Returns:
org.das2.event.VerticalSlicerMouseModule


<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

create( org.das2.graph.Renderer renderer ) &rarr; VerticalSlicerMouseModule<br>
***
<a name="getDirections"></a>
# getDirections
getDirections(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getDirections&unscoped_q=getDirections">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSlicer"></a>
# getSlicer
getSlicer(  ) &rarr; VerticalSpectrogramSlicer

return the slicer listening to the slices.  This returns the 
 first one found.

### Returns:
the slicer

<a href="https://github.com/autoplot/dev/search?q=getSlicer&unscoped_q=getSlicer">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="keyTyped"></a>
# keyTyped
keyTyped( java.awt.event.KeyEvent keyEvent ) &rarr; void



### Parameters:
keyEvent - a KeyEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=keyTyped&unscoped_q=keyTyped">[search for examples]</a>

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

