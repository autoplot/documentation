# org.das2.graph.SelectionUtilutilities for managing selection feedback, where we have a glow to indicate 
 focus.
SelectionUtil( )


***
<a name="NULL"></a>
# NULL



***
<a name="getSelectionArea"></a>
# getSelectionArea
getSelectionArea( org.das2.graph.Renderer r ) &rarr; Shape

returns the selection area, or SelectionUtil.NULL.

### Parameters:
r - the renderer, one of a list of coded renderers

### Returns:
the renderer-specific selection area, or the current bounds of the renderer parent.
 TODO: this should be part of the Renderer interface.

<a href="https://github.com/autoplot/dev/search?q=getSelectionArea&unscoped_q=getSelectionArea">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getSelectionArea( org.das2.graph.DasCanvasComponent cc ) &rarr; Shape<br>
