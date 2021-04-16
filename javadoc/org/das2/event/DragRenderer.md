# org.das2.event.DragRendererA DragRenderer provides the feedback to the human operator
 of what their mousing is doing.  It applies constraints to the
 drag as well. It promotes the AWT mouse events into events
 that represent the operation, implementing for example mouse
 gestures.
***
<a name="ghostColor"></a>
# ghostColor

use this color when drawing ghostly backgrounds for contrast.

***
<a name="clear"></a>
# clear
clear( java.awt.Graphics g ) &rarr; void

clears whatever renderDrag rendered.  This is not used by the DasMouseInputAdapter,
 but must still be supported for now.  Originally the drag renderer would have
 to unpaint itself as well, but this is no longer used.

### Parameters:
g - the graphics context

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=clear&unscoped_q=clear">[search for examples]</a>

***
<a name="getMouseDragEvent"></a>
# getMouseDragEvent
getMouseDragEvent( Object source, java.awt.Point p1, java.awt.Point p2, boolean isModified ) &rarr; MouseDragEvent

promotes the drag begin and end into a mouseDragEvent.

### Parameters:
source - an Object
<br>p1 - the click point
<br>p2 - the current mouse position during drag and release.
<br>isModified - a boolean

### Returns:
an org.das2.event.MouseDragEvent


<a href="https://github.com/autoplot/dev/search?q=getMouseDragEvent&unscoped_q=getMouseDragEvent">[search for examples]</a>

***
<a name="isPointSelection"></a>
# isPointSelection
isPointSelection(  ) &rarr; boolean

indicates that the mouse module's mousePointSelected() should be called as new mouse events come in.

### Returns:
true if the mouse module should receive events during the drag.

<a href="https://github.com/autoplot/dev/search?q=isPointSelection&unscoped_q=isPointSelection">[search for examples]</a>

***
<a name="isUpdatingDragSelection"></a>
# isUpdatingDragSelection
isUpdatingDragSelection(  ) &rarr; boolean

range selection events should be fired during drag.

### Returns:
true if selection events should be fired during drag.

<a href="https://github.com/autoplot/dev/search?q=isUpdatingDragSelection&unscoped_q=isUpdatingDragSelection">[search for examples]</a>

***
<a name="renderDrag"></a>
# renderDrag
renderDrag( java.awt.Graphics g, java.awt.Point p1, java.awt.Point p2 ) &rarr; Rectangle

draws the drag for mousing from p1 to p2, and returns an array of
 Rectangles covering the rendering.  If nothing is drawn, then an 
 array of length zero should be returned, and nulls are allowed in the
 array. p1 and p2, and g are in the canvas frame of reference.

### Parameters:
g - the graphics context for rendering
<br>p1 - the click point
<br>p2 - the current mouse position during drag and release.

### Returns:
a java.awt.Rectangle[]


<a href="https://github.com/autoplot/dev/search?q=renderDrag&unscoped_q=renderDrag">[search for examples]</a>

