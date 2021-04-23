# org.autoplot.state.VapSchemeinterface allowing for handling forward compatibility.  This is really
 simplified, and really only serves to rename properties.  (By design it should
 handle more complex transformations, but this didn't work, and we use xslt
 instead.)
***
<a name="addUnresolvedProperty"></a>
# addUnresolvedProperty
addUnresolvedProperty( org.w3c.dom.Element element, org.autoplot.dom.DomNode node, java.lang.Exception exception ) &rarr; void



### Parameters:
element - an Element
<br>node - a DomNode
<br>exception - an Exception

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addUnresolvedProperty&unscoped_q=addUnresolvedProperty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="describeUnresolved"></a>
# describeUnresolved
describeUnresolved(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=describeUnresolved&unscoped_q=describeUnresolved">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getClass"></a>
# getClass
getClass( String name ) &rarr; Class



### Parameters:
name - a String

### Returns:
java.lang.Class


<a href="https://github.com/autoplot/dev/search?q=getClass&unscoped_q=getClass">[search for examples]</a>

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
<a name="getName"></a>
# getName
getName( java.lang.Class clas ) &rarr; String



### Parameters:
clas - a java.lang.Class

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getName&unscoped_q=getName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resolveProperty"></a>
# resolveProperty
resolveProperty( org.w3c.dom.Element element, org.autoplot.dom.DomNode node ) &rarr; boolean



### Parameters:
element - an Element
<br>node - a DomNode

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=resolveProperty&unscoped_q=resolveProperty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

