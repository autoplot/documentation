# org.autoplot.dom.Template

Template for making new nodes.  There's a lot to get right when 
 changing the dom, and this should help.  
 Make sure the node is mutable.  I added properties to the Connector
 and this was tricky because before it was not mutable.

# Template( )


***
<a name="PROP_CONTROLLER"></a>
# PROP_CONTROLLER



***
<a name="copy"></a>
# copy
copy(  ) &rarr; DomNode



### Returns:
org.autoplot.dom.DomNode


<a href="https://github.com/autoplot/dev/search?q=copy&unscoped_q=copy">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="diffs"></a>
# diffs
diffs( org.autoplot.dom.DomNode node ) &rarr; List



### Parameters:
node - a DomNode

### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=diffs&unscoped_q=diffs">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getController"></a>
# getController
getController(  ) &rarr; CanvasController



### Returns:
org.autoplot.dom.CanvasController


<a href="https://github.com/autoplot/dev/search?q=getController&unscoped_q=getController">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="syncTo"></a>
# syncTo
syncTo( org.autoplot.dom.DomNode n ) &rarr; void



### Parameters:
n - a DomNode

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=syncTo&unscoped_q=syncTo">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

syncTo( org.autoplot.dom.DomNode n, java.util.List exclude ) &rarr; void<br>
