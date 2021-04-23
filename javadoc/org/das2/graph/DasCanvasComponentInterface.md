# org.das2.graph.DasCanvasComponentInterfaceAll entities on the DasCanvas are DasCanvasComponents.
***
<a name="paintComponent"></a>
# paintComponent
paintComponent( java.awt.Graphics g ) &rarr; void

this paints the component, the point 0,0 always refers to the upper-left corner
 of the canvas.

### Parameters:
g - a Graphics

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=paintComponent&unscoped_q=paintComponent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resize"></a>
# resize
resize(  ) &rarr; void

This is called when the canvas is resized or something has happened to make the
 boundries change.  This code should call the setBounds( Rectangle )

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resize&unscoped_q=resize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

