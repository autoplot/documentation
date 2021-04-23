# org.das2.event.DataPointSelectorMouseModule

General purpose mouse module for getting data point selections.  The client
 provides the DragRenderer, generally a vertical line, horizontal line or a
 crosshair.

 Three properties control when DataPointSelectionEvents are to be fired:
   dragEvents     as the mouse is dragged,
   keyEvents      when a key is pressed.  (The key is the "keyChar" plane of the event)
   releaseEvents  when the mouse is released.  (false by default)

# DataPointSelectorMouseModule( org.das2.graph.DasPlot parent, org.das2.dataset.DataSetConsumer consumer, org.das2.event.DragRenderer dragRenderer, String label )


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
<a name="isDragEvents"></a>
# isDragEvents
isDragEvents(  ) &rarr; boolean

Getter for property dragEvents.

### Returns:
Value of property dragEvents.

<a href="https://github.com/autoplot/dev/search?q=isDragEvents&unscoped_q=isDragEvents">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isKeyEvents"></a>
# isKeyEvents
isKeyEvents(  ) &rarr; boolean

Getter for property keyEvents.

### Returns:
Value of property keyEvents.

<a href="https://github.com/autoplot/dev/search?q=isKeyEvents&unscoped_q=isKeyEvents">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isReleaseEvents"></a>
# isReleaseEvents
isReleaseEvents(  ) &rarr; boolean

Getter for property releaseEvents.

### Returns:
Value of property releaseEvents.

<a href="https://github.com/autoplot/dev/search?q=isReleaseEvents&unscoped_q=isReleaseEvents">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="keyPressed"></a>
# keyPressed
keyPressed( java.awt.event.KeyEvent e ) &rarr; void



### Parameters:
e - a KeyEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=keyPressed&unscoped_q=keyPressed">[search for examples]</a>

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
<a name="mouseReleased"></a>
# mouseReleased
mouseReleased( java.awt.event.MouseEvent e ) &rarr; void



### Parameters:
e - a MouseEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mouseReleased&unscoped_q=mouseReleased">[search for examples]</a>

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

***
<a name="setDragEvents"></a>
# setDragEvents
setDragEvents( boolean dragEvents ) &rarr; void

Setter for property dragEvents.

### Parameters:
dragEvents - New value of property dragEvents.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDragEvents&unscoped_q=setDragEvents">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setKeyEvents"></a>
# setKeyEvents
setKeyEvents( boolean keyEvents ) &rarr; void

Setter for property keyEvents.

### Parameters:
keyEvents - New value of property keyEvents.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setKeyEvents&unscoped_q=setKeyEvents">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setReleaseEvents"></a>
# setReleaseEvents
setReleaseEvents( boolean releaseEvents ) &rarr; void

Setter for property releaseEvents.

### Parameters:
releaseEvents - New value of property releaseEvents.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setReleaseEvents&unscoped_q=setReleaseEvents">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

