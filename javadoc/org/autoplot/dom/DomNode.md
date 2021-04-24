# org.autoplot.dom.DomNode

Autoplot's state is stored in a tree of nodes, with Java types constraining to particular abstractions.  Each node
 can have children, and implements:<ul>
  <li> copy -- make a copy of this node and its children.
  <li> syncTo -- make this node look like another node.  (e.g. undo to old state). syncTo can also be told to exclude properties.
  <li> diffs -- show differences between this and another node.
 </ul>
 All nodes have the property "id" which must be unique within the tree.  Each node has properties of the following types:<ul>
  <li> String
  <li>  double
  <li>  boolean
  <li>  Datum
  <li>  DatumRange
  <li>  Color
  <li>  RenderType
  <li>  PlotSymbol
  <li>  PsymConnector
  <li>  Enum
  <li>  Connector
  <li>  LegendPosition
  <li>  AnchorPosition
</ul>
 Any DomNode can be saved and restored using SerializeUtil, which uses Java introspection to look at all the properties.

 Some nodes currently have the method "setXAutomatically" where X is a property.  This is currently used to indicate who is setting
 the property.  For example, PlotElement has setComponentAutomatically for use when a slice is set automatically by the application.
 This is handled specially in SerializeUtil

# DomNode( )


***
<a name="PROP_ID"></a>
# PROP_ID



***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
propertyName - a String
<br>listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addPropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="boundCount"></a>
# boundCount
boundCount(  ) &rarr; int

try and find the leaks caused by binding...

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=boundCount&unscoped_q=boundCount">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="childNodes"></a>
# childNodes
childNodes(  ) &rarr; List

return any child nodes.

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=childNodes&unscoped_q=childNodes">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="copy"></a>
# copy
copy(  ) &rarr; DomNode

returns a deep copy of the node.

### Returns:
an org.autoplot.dom.DomNode


<a href="https://github.com/autoplot/dev/search?q=copy&unscoped_q=copy">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="diffs"></a>
# diffs
diffs( org.autoplot.dom.DomNode that ) &rarr; List

return a list of the differences between this and another node.  The
 differences describe how to mutate that node to make it like this
 node.

### Parameters:
that - a DomNode

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=diffs&unscoped_q=diffs">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getId"></a>
# getId
getId(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getId&unscoped_q=getId">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
propertyName - a String
<br>listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

removePropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="setId"></a>
# setId
setId( String id ) &rarr; void



### Parameters:
id - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setId&unscoped_q=setId">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="syncTo"></a>
# syncTo
syncTo( org.autoplot.dom.DomNode n ) &rarr; void

bulk assignment of properties.  When the node's children differ, then a controller should be used
 to implement the sync.
 Syncing should include the node's ID.

### Parameters:
n - a DomNode

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=syncTo&unscoped_q=syncTo">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

syncTo( org.autoplot.dom.DomNode n, java.util.List exclude ) &rarr; void<br>
***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

