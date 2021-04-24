# org.das2.event.ZoomPanMouseModule

Provide navigation similar to Google Maps, where drag events result a pan on the axes, and mouse wheel events
 are zoom in and zoom out.  This is typically attached to the middle mouse button.

# ZoomPanMouseModule( org.das2.graph.DasCanvasComponent parent, org.das2.graph.DasAxis horizontalAxis, org.das2.graph.DasAxis verticalAxis )
Creates a new instance of ZoomPanMouseModule

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

mouse wheel events zoom or pan rapidly.  With a physical wheel, I (jbf) found
 that I get 17ms per click, and this is managable.  With a touchpad on a mac,
 these events come much faster, like 10ms per click, which can disorient the
 operator.  So we limit the speed to 20ms per click, for now by dropping
 rapid clicks.

### Parameters:
e - a MouseWheelEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mouseWheelMoved&unscoped_q=mouseWheelMoved">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

