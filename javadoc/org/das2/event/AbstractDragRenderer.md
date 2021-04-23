# org.das2.event.AbstractDragRendererDo-nothing drag renderer and extension point for other DragRenderers.
AbstractDragRenderer( )


AbstractDragRenderer( org.das2.graph.DasCanvasComponent parent )


***
<a name="clear"></a>
# clear
clear( java.awt.Graphics g ) &rarr; void

this is not used, and is left over from an old version of the library.

### Parameters:
g - a Graphics

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=clear&unscoped_q=clear">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMouseDragEvent"></a>
# getMouseDragEvent
getMouseDragEvent( Object source, java.awt.Point p1, java.awt.Point p2, boolean isModified ) &rarr; MouseDragEvent

return the event for the gesture.  A mouse box event is returned.

### Parameters:
source - an Object
<br>p1 - a Point
<br>p2 - a Point
<br>isModified - a boolean

### Returns:
an org.das2.event.MouseDragEvent


<a href="https://github.com/autoplot/dev/search?q=getMouseDragEvent&unscoped_q=getMouseDragEvent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getParent"></a>
# getParent
getParent(  ) &rarr; DasCanvasComponent



### Returns:
org.das2.graph.DasCanvasComponent


<a href="https://github.com/autoplot/dev/search?q=getParent&unscoped_q=getParent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isPointSelection"></a>
# isPointSelection
isPointSelection(  ) &rarr; boolean

indicates that MM.mousePointSelected() should called as new mouse events 
 come in.

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isPointSelection&unscoped_q=isPointSelection">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isUpdatingDragSelection"></a>
# isUpdatingDragSelection
isUpdatingDragSelection(  ) &rarr; boolean

range selection events should be fired during drag.

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isUpdatingDragSelection&unscoped_q=isUpdatingDragSelection">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setParent"></a>
# setParent
setParent( org.das2.graph.DasCanvasComponent parent ) &rarr; void



### Parameters:
parent - a DasCanvasComponent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setParent&unscoped_q=setParent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

