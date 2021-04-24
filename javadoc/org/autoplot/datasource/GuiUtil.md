# org.autoplot.datasource.GuiUtil

Utility class for working with GUIs, first introduced to listen for
 who is setting the minimum size.

# GuiUtil( )


***
<a name="addResizeListenerToAll"></a>
# addResizeListenerToAll
addResizeListenerToAll( javax.swing.JComponent c ) &rarr; void

utility for figuring out who is setting the minimum size of a
 component.

### Parameters:
c - the parent component.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addResizeListenerToAll&unscoped_q=addResizeListenerToAll">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasScrollPane"></a>
# hasScrollPane
hasScrollPane( javax.swing.JComponent c ) &rarr; boolean

scan through all the child components looking to see if there is a 
 JScrollPane.  This was introduced when a JSplitPane with two JScrollPanes
 was used with addTab, and an extra JScrollPane was added.

### Parameters:
c - the component

### Returns:
true if a child has a scroll

<a href="https://github.com/autoplot/dev/search?q=hasScrollPane&unscoped_q=hasScrollPane">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

