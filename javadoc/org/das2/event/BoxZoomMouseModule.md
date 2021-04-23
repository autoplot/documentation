# org.das2.event.BoxZoomMouseModuleProvide a box zoom where drag to draw a box that will be the new range, and mouse wheel events
 are zoom in and zoom out.  This is typically attached to the left mouse button.
BoxZoomMouseModule( org.das2.graph.DasCanvasComponent parent, org.das2.dataset.DataSetConsumer consumer, org.das2.graph.DasAxis xAxis, org.das2.graph.DasAxis yAxis )
Creates a new instance of BoxZoomMouseModule

***
<a name="isAutoUpdate"></a>
# isAutoUpdate
isAutoUpdate(  ) &rarr; boolean

Getter for property autoUpdate.

### Returns:
Value of property autoUpdate.

<a href="https://github.com/autoplot/dev/search?q=isAutoUpdate&unscoped_q=isAutoUpdate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isConstrainProportions"></a>
# isConstrainProportions
isConstrainProportions(  ) &rarr; boolean

Getter for property constrainProportions.

### Returns:
Value of property constrainProportions.

<a href="https://github.com/autoplot/dev/search?q=isConstrainProportions&unscoped_q=isConstrainProportions">[search for examples]</a>

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

***
<a name="setAutoUpdate"></a>
# setAutoUpdate
setAutoUpdate( boolean autoUpdate ) &rarr; void

Setter for property autoUpdate.

### Parameters:
autoUpdate - New value of property autoUpdate.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAutoUpdate&unscoped_q=setAutoUpdate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setConstrainProportions"></a>
# setConstrainProportions
setConstrainProportions( boolean constrainProportions ) &rarr; void

Setter for property constrainProportions.

### Parameters:
constrainProportions - New value of property constrainProportions.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setConstrainProportions&unscoped_q=setConstrainProportions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

