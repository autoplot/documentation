# org.das2.event.MouseModuleA MouseModule is a pluggable unit that promotes simple
 mouse events into human events or actions that are useful
 for science analysis.  Each component has a mouseInputAdapter
 that manages a set of mouseModules, one is active at any
 given time.

 The DasMouseInputAdapter will delegate mouse events, key events, and 
 mouse wheel events to the active mouse module.
 
 This base class will be extended by instances of MouseModule, overriding
 methods they wish to handle.
MouseModule( org.das2.graph.DasCanvasComponent parent )
create the mouse module for the parent component.  This is 
 without a drag renderer, and the class name is used
 for the label.
 paint graphic feedback to the human operator.

MouseModule( org.das2.graph.DasCanvasComponent parent, org.das2.event.DragRenderer dragRenderer, String label )
create the mouse module for the parent component using the dragRenderer to
 paint graphic feedback to the human operator.  For example, the 
 dragRenderer might draw a box during the click-drag-release mouse action,
 and then on release this mouse module creates the event used elsewhere.

***
<a name="drawListIcon"></a>
# drawListIcon
drawListIcon( java.awt.Graphics2D g, int x, int y ) &rarr; void



### Parameters:
g - a Graphics2D
<br>x - an int
<br>y - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=drawListIcon&unscoped_q=drawListIcon">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCursor"></a>
# getCursor
getCursor(  ) &rarr; Cursor

return a cursor that indicates the selected module.  Note this is currently
 not used.

### Returns:
a cursor that indicates the selected module.

<a href="https://github.com/autoplot/dev/search?q=getCursor&unscoped_q=getCursor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDirections"></a>
# getDirections
getDirections(  ) &rarr; String

allow one-line directions to be added to the mouse module.
 This is used in Autoplot for the status bar.

### Returns:
the directions, or null.

<a href="https://github.com/autoplot/dev/search?q=getDirections&unscoped_q=getDirections">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDragRenderer"></a>
# getDragRenderer
getDragRenderer(  ) &rarr; DragRenderer

return the current drag renderer.

### Returns:
the current drag renderer.

<a href="https://github.com/autoplot/dev/search?q=getDragRenderer&unscoped_q=getDragRenderer">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLabel"></a>
# getLabel
getLabel(  ) &rarr; String

returns a human-readable string that identifies the module

### Returns:
a human-readable string that identifies the module

<a href="https://github.com/autoplot/dev/search?q=getLabel&unscoped_q=getLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getListIcon"></a>
# getListIcon
getListIcon(  ) &rarr; Icon

return the list icon.  This will be be overridden by MouseModules to
 give a visual reference.

### Returns:
the list icon.

<a href="https://github.com/autoplot/dev/search?q=getListIcon&unscoped_q=getListIcon">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getListLabel"></a>
# getListLabel
getListLabel(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getListLabel&unscoped_q=getListLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getParent"></a>
# getParent
getParent(  ) &rarr; DasCanvasComponent

return the canvas component (for example, a DasPlot) where this
 MouseModule is listening.

### Returns:
the canvas component.

<a href="https://github.com/autoplot/dev/search?q=getParent&unscoped_q=getParent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="keyPressed"></a>
# keyPressed
keyPressed( java.awt.event.KeyEvent keyEvent ) &rarr; void



### Parameters:
keyEvent - a KeyEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=keyPressed&unscoped_q=keyPressed">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="keyReleased"></a>
# keyReleased
keyReleased( java.awt.event.KeyEvent keyEvent ) &rarr; void



### Parameters:
keyEvent - a KeyEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=keyReleased&unscoped_q=keyReleased">[search for examples]</a>

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
<a name="mouseClicked"></a>
# mouseClicked
mouseClicked( java.awt.event.MouseEvent e ) &rarr; void



### Parameters:
e - a MouseEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mouseClicked&unscoped_q=mouseClicked">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mouseDragged"></a>
# mouseDragged
mouseDragged( java.awt.event.MouseEvent e ) &rarr; void



### Parameters:
e - a MouseEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mouseDragged&unscoped_q=mouseDragged">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mouseEntered"></a>
# mouseEntered
mouseEntered( java.awt.event.MouseEvent e ) &rarr; void



### Parameters:
e - a MouseEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mouseEntered&unscoped_q=mouseEntered">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mouseExited"></a>
# mouseExited
mouseExited( java.awt.event.MouseEvent e ) &rarr; void



### Parameters:
e - a MouseEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mouseExited&unscoped_q=mouseExited">[search for examples]</a>

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
<a name="mousePointSelected"></a>
# mousePointSelected
mousePointSelected( org.das2.event.MousePointSelectionEvent e ) &rarr; void

Action to take when a point (click or drag) is selected.  This is intended
 to be overridden.

### Parameters:
e - the event.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mousePointSelected&unscoped_q=mousePointSelected">[search for examples]</a>

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

Action to take when a mouse range (click, drag, release) has been 
 selected.  This is intended to be overridden.

### Parameters:
e - the drag event.

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
<a name="mouseWheelMoved"></a>
# mouseWheelMoved
mouseWheelMoved( java.awt.event.MouseWheelEvent e ) &rarr; void



### Parameters:
e - a MouseWheelEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mouseWheelMoved&unscoped_q=mouseWheelMoved">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="position"></a>
# position
position( org.das2.graph.DasDevicePosition ddp, int pos, int threshold ) &rarr; Pos

indicate if the position (pixels) is near the ends of the DasRow or
 DasColumn.  Note that the max of a row is its bottom.

### Parameters:
ddp - the row or column
<br>pos - the position to describe.
<br>threshold - pixel distance to the boundary, 20 is often used.

### Returns:
enumeration of the position, for example Pos.beyondMin.

<a href="https://github.com/autoplot/dev/search?q=position&unscoped_q=position">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDirections"></a>
# setDirections
setDirections( String directions ) &rarr; void

set the human-readable directions string, so clients like Autoplot can display
 them.

### Parameters:
directions - human-readable directions.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDirections&unscoped_q=setDirections">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDragRenderer"></a>
# setDragRenderer
setDragRenderer( org.das2.event.DragRenderer d ) &rarr; void

set the drag renderer. (Made public when the digitizer had different modes.)

### Parameters:
d - set the drag renderer.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDragRenderer&unscoped_q=setDragRenderer">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLabel"></a>
# setLabel
setLabel( String label ) &rarr; void

set the human-readable label.

### Parameters:
label - the human-readable label.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLabel&unscoped_q=setLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

