# org.das2.graph.Painter

interface for objects that can paint on a graphics context from the canvas.
 We introduce the interface so that objects can be painted without having
 the overhead of full Swing components.

***
<a name="paint"></a>
# paint
paint( java.awt.Graphics2D g ) &rarr; void

the graphics context, in the canvas coordinates, is provided for additional
 painting.

### Parameters:
g - the graphics context.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=paint&unscoped_q=paint">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

