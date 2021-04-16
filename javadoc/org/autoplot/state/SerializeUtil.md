# org.autoplot.state.SerializeUtilUtility class for creating a Document from a DomNode.  Note that there is special
 handling for:<ul>
 <li>controller -- these nodes are dropped.
 <li>class -- this is noise from java.
 <li>*Automatically -- properties ending in "Automatically" are used to set another property.
 </ul>
 There may be other exceptional properties that are not documented here.
SerializeUtil( )


***
<a name="getDomElement"></a>
# getDomElement
getDomElement( org.w3c.dom.Document document, org.autoplot.dom.DomNode node, org.autoplot.state.VapScheme scheme ) &rarr; Element

Return the XML for the node.

### Parameters:
document - the document to which the node is added.
<br>node - the dom node (Application, Plot, PlotElement, etc.)
<br>scheme - the version of the vap that we are writing.  This identifies the scheme, but also provides names for nodes.

### Returns:
the Document (XML) element for the node.

<a href="https://github.com/autoplot/dev/search?q=getDomElement&unscoped_q=getDomElement">[search for examples]</a>

getDomElement( org.w3c.dom.Document document, org.autoplot.dom.DomNode node, org.autoplot.state.VapScheme scheme, boolean includeDefaults ) &rarr; Element<br>
***
<a name="getDomNode"></a>
# getDomNode
getDomNode( org.w3c.dom.Element element, org.autoplot.state.VapScheme scheme ) &rarr; DomNode

decode the DomNode from the document element.

### Parameters:
element - the DOM element
<br>scheme - the current version

### Returns:
an org.autoplot.dom.DomNode


<a href="https://github.com/autoplot/dev/search?q=getDomNode&unscoped_q=getDomNode">[search for examples]</a>

***
<a name="getElementForLeafNode"></a>
# getElementForLeafNode
getElementForLeafNode( org.w3c.dom.Document document, java.lang.Class propClass, Object value, Object defltValue ) &rarr; Element

return the Element, or null if we can't handle it

### Parameters:
document - a Document
<br>propClass - a java.lang.Class
<br>value - an Object
<br>defltValue - an Object

### Returns:
an org.w3c.dom.Element


<a href="https://github.com/autoplot/dev/search?q=getElementForLeafNode&unscoped_q=getElementForLeafNode">[search for examples]</a>

***
<a name="getLeafNode"></a>
# getLeafNode
getLeafNode( org.w3c.dom.Element element ) &rarr; Object



### Parameters:
element - an Element

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=getLeafNode&unscoped_q=getLeafNode">[search for examples]</a>

