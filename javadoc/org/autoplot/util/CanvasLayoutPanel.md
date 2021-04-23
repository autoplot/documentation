# org.autoplot.util.CanvasLayoutPanel

This is the small GUI in the upper left corner of the layout tab, which
 shows abstractly where plots sit in relation to one another, for
 reference.

# CanvasLayoutPanel( )


***
<a name="PROP_COMPONENT"></a>
# PROP_COMPONENT



***
<a name="PROP_SELECTEDCOMPONENTS"></a>
# PROP_SELECTEDCOMPONENTS



***
<a name="addComponentType"></a>
# addComponentType
addComponentType( java.lang.Class c, java.awt.Color color ) &rarr; void

mark this type of component with the given color.

### Parameters:
c - the class of the component, like org.das2.graph.DasPlot.class
<br>color - the color, like Color.BLUE

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addComponentType&unscoped_q=addComponentType">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCanvasComponentAt"></a>
# getCanvasComponentAt
getCanvasComponentAt( int x, int y ) &rarr; Object

return the plot component at the position on this GUI.

### Parameters:
x - the x position, 0 is left side of this component.
<br>y - the x position, 0 is top of this component.

### Returns:
DasPlot, DasAxis, etc.

<a href="https://github.com/autoplot/dev/search?q=getCanvasComponentAt&unscoped_q=getCanvasComponentAt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCanvasComponentsWithin"></a>
# getCanvasComponentsWithin
getCanvasComponentsWithin( java.awt.Rectangle r ) &rarr; List

get the canvas components within the rectangle.

### Parameters:
r - rectangle within the GUI.

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=getCanvasComponentsWithin&unscoped_q=getCanvasComponentsWithin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getComponent"></a>
# getComponent
getComponent(  ) &rarr; Object

get the primary selected component.

### Returns:
an Object


<a href="https://github.com/autoplot/dev/search?q=getComponent&unscoped_q=getComponent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSelectedComponents"></a>
# getSelectedComponents
getSelectedComponents(  ) &rarr; List

get the user-selected components.

### Returns:
a list containing the components.

<a href="https://github.com/autoplot/dev/search?q=getSelectedComponents&unscoped_q=getSelectedComponents">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setComponent"></a>
# setComponent
setComponent( Object component ) &rarr; void

set the primary selected component.

### Parameters:
component - null or the selected component.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setComponent&unscoped_q=setComponent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setContainer"></a>
# setContainer
setContainer( org.das2.graph.DasCanvas c ) &rarr; void

this is the JComponent we are monitoring.  If this is a
 DasCanvas, then a special listener is added for repaints.

### Parameters:
c - a DasCanvas

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setContainer&unscoped_q=setContainer">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRectangleSelect"></a>
# setRectangleSelect
setRectangleSelect( java.awt.Rectangle r ) &rarr; void

set the bounds of the selecting rectangle, to provide feedback.

### Parameters:
r - a Rectangle

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRectangleSelect&unscoped_q=setRectangleSelect">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSelectedComponents"></a>
# setSelectedComponents
setSelectedComponents( java.util.List selectedComponents ) &rarr; void

set the selected components.

### Parameters:
selectedComponents - a java.util.List

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSelectedComponents&unscoped_q=setSelectedComponents">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

setSelectedComponents( java.awt.Rectangle r ) &rarr; void<br>
