# org.das2.event.LabelDragRenderer

LabelDragRenderer draws a label at the current mouse location.  Typically
 this one overrides this class and calls the setLabel and super.renderDrag
 classes.

# LabelDragRenderer( org.das2.graph.DasCanvasComponent parent )
create an instance.

# LabelDragRenderer( )
create an instance, and presumably the mouse module will set the parent.

***
<a name="clear"></a>
# clear
clear( java.awt.Graphics g ) &rarr; void



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

This method is called by the DMIA on mouse release.  We use this to infer the mouse release
 and hide the Window.  Note this assumes isUpdatingDragSelection is false!
 TODO: DMIA should call clear so this is more explicit.

### Parameters:
source - an Object
<br>p1 - a Point
<br>p2 - a Point
<br>isModified - a boolean

### Returns:
the DragEvent

<a href="https://github.com/autoplot/dev/search?q=getMouseDragEvent&unscoped_q=getMouseDragEvent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isPointSelection"></a>
# isPointSelection
isPointSelection(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isPointSelection&unscoped_q=isPointSelection">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isTooltip"></a>
# isTooltip
isTooltip(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isTooltip&unscoped_q=isTooltip">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isUpdatingDragSelection"></a>
# isUpdatingDragSelection
isUpdatingDragSelection(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isUpdatingDragSelection&unscoped_q=isUpdatingDragSelection">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="renderDrag"></a>
# renderDrag
renderDrag( java.awt.Graphics g, java.awt.Point p1, java.awt.Point p2 ) &rarr; Rectangle



### Parameters:
g - a Graphics
<br>p1 - a Point
<br>p2 - a Point

### Returns:
java.awt.Rectangle[]


<a href="https://github.com/autoplot/dev/search?q=renderDrag&unscoped_q=renderDrag">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLabel"></a>
# setLabel
setLabel( String s ) &rarr; void

set the label to be drawn.  This should be done before this object's renderDrag is called.

### Parameters:
s - the label, which can contain Granny control sequences like !A and !n.

### Returns:
void (returns nothing)

### See Also:
<a href='http://autoplot.org/help#Granny_Strings'>http://autoplot.org/help#Granny_Strings</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setLabel&unscoped_q=setLabel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTooltip"></a>
# setTooltip
setTooltip( boolean tooltip ) &rarr; void



### Parameters:
tooltip - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTooltip&unscoped_q=setTooltip">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

