# org.das2.event.BoxSelectorMouseModuleGeneral purpose mouse module for getting data point selections.  The client
 provides the DragRenderer, generally a vertical line, horizontal line or a
 crosshair.

 Three properties control when BoxSelectionEvents are to be fired:
 <ul>
 <li> dragEvents,     as the mouse is dragged,
 <li> keyEvents,      when a key is pressed.  (The key is the "keyChar" plane of the event)
 <li> releaseEvents,  when the mouse is released.  (false by default)
 </ul>
 This is intended to be used as a base class for other slicers which need a
 range to be selected in X, Y, or both.
BoxSelectorMouseModule( org.das2.graph.DasCanvasComponent parent, org.das2.graph.DasAxis xAxis, org.das2.graph.DasAxis yAxis, org.das2.dataset.DataSetConsumer consumer, org.das2.event.DragRenderer dragRenderer, String label )
create a new BoxSelectorMouseModule

***
<a name="addBoxSelectionListener"></a>
# addBoxSelectionListener
addBoxSelectionListener( org.das2.event.BoxSelectionListener listener ) &rarr; void

Registers BoxSelectionListener to receive events.

### Parameters:
listener - The listener to register.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addBoxSelectionListener&unscoped_q=addBoxSelectionListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="create"></a>
# create
create( org.das2.graph.DasPlot parent, String label ) &rarr; BoxSelectorMouseModule

create a BoxSelectorMouseModule

### Parameters:
parent - the plot component
<br>label - the label for this mouseModule.

### Returns:
new  BoxSelectorMouseModule

<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

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
<a name="mouseMoved"></a>
# mouseMoved
mouseMoved( java.awt.event.MouseEvent e ) &rarr; void



### Parameters:
e - a MouseEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mouseMoved&unscoped_q=mouseMoved">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mousePressed"></a>
# mousePressed
mousePressed( java.awt.event.MouseEvent e ) &rarr; void



### Parameters:
e - a MouseEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mousePressed&unscoped_q=mousePressed">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mouseRangeSelected"></a>
# mouseRangeSelected
mouseRangeSelected( org.das2.event.MouseDragEvent e ) &rarr; void



### Parameters:
e - a MouseDragEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mouseRangeSelected&unscoped_q=mouseRangeSelected">[search for examples]</a>

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
<a name="removeBoxSelectionListener"></a>
# removeBoxSelectionListener
removeBoxSelectionListener( org.das2.event.BoxSelectionListener listener ) &rarr; void

Removes BoxSelectionListener from the list of listeners.

### Parameters:
listener - The listener to remove.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeBoxSelectionListener&unscoped_q=removeBoxSelectionListener">[search for examples]</a>

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

***
<a name="setTweakable"></a>
# setTweakable
setTweakable( boolean b ) &rarr; void

allow the last selection to be tweaked.  It's the client's responsibility
 to draw the current selection.

### Parameters:
b - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTweakable&unscoped_q=setTweakable">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

