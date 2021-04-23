# org.autoplot.spase.DOMWalker



# DOMWalker( org.w3c.dom.traversal.TreeWalker walker )
Create a TreeModel for the specified TreeWalker

# DOMWalker( org.w3c.dom.Document document )
Create a TreeModel for a TreeWalker that returns all nodes
 in the specified document

# DOMWalker( org.w3c.dom.Element element )
Create a TreeModel for a TreeWalker that returns the specified 
 element and all of its descendant nodes.

***
<a name="getAttributes"></a>
# getAttributes
getAttributes( org.w3c.dom.Node node ) &rarr; Map



### Parameters:
node - a Node

### Returns:
java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getAttributes&unscoped_q=getAttributes">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getChild"></a>
# getChild
getChild( Object parent, int index ) &rarr; Object



### Parameters:
parent - an Object
<br>index - an int

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=getChild&unscoped_q=getChild">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getChildCount"></a>
# getChildCount
getChildCount( Object node ) &rarr; int



### Parameters:
node - an Object

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getChildCount&unscoped_q=getChildCount">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getIndexOfChild"></a>
# getIndexOfChild
getIndexOfChild( Object parent, Object child ) &rarr; int



### Parameters:
parent - an Object
<br>child - an Object

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getIndexOfChild&unscoped_q=getIndexOfChild">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRoot"></a>
# getRoot
getRoot(  ) &rarr; Node



### Returns:
org.w3c.dom.Node


<a href="https://github.com/autoplot/dev/search?q=getRoot&unscoped_q=getRoot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void

This main() method demonstrates the use of this class, the use of the
 Xerces DOM parser, and the creation of a DOM Level 2 TreeWalker object.

### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

