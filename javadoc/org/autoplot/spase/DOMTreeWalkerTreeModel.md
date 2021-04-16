# org.autoplot.spase.DOMTreeWalkerTreeModelThis class implements the Swing TreeModel interface so that the DOM tree
 returned by a TreeWalker can be displayed in a JTree component.
DOMTreeWalkerTreeModel( org.w3c.dom.traversal.TreeWalker walker )
Create a TreeModel for the specified TreeWalker

DOMTreeWalkerTreeModel( org.w3c.dom.Document document )
Create a TreeModel for a TreeWalker that returns all nodes
 in the specified document

DOMTreeWalkerTreeModel( org.w3c.dom.Element element )
Create a TreeModel for a TreeWalker that returns the specified 
 element and all of its descendant nodes.

***
<a name="addTreeModelListener"></a>
# addTreeModelListener
addTreeModelListener( javax.swing.event.TreeModelListener l ) &rarr; void



### Parameters:
l - a TreeModelListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addTreeModelListener&unscoped_q=addTreeModelListener">[search for examples]</a>

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

***
<a name="getChildCount"></a>
# getChildCount
getChildCount( Object node ) &rarr; int



### Parameters:
node - an Object

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getChildCount&unscoped_q=getChildCount">[search for examples]</a>

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

***
<a name="getRoot"></a>
# getRoot
getRoot(  ) &rarr; Object



### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=getRoot&unscoped_q=getRoot">[search for examples]</a>

***
<a name="isLeaf"></a>
# isLeaf
isLeaf( Object node ) &rarr; boolean



### Parameters:
node - an Object

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isLeaf&unscoped_q=isLeaf">[search for examples]</a>

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

***
<a name="removeTreeModelListener"></a>
# removeTreeModelListener
removeTreeModelListener( javax.swing.event.TreeModelListener l ) &rarr; void



### Parameters:
l - a TreeModelListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeTreeModelListener&unscoped_q=removeTreeModelListener">[search for examples]</a>

***
<a name="valueForPathChanged"></a>
# valueForPathChanged
valueForPathChanged( javax.swing.tree.TreePath path, Object newvalue ) &rarr; void



### Parameters:
path - a TreePath
<br>newvalue - an Object

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=valueForPathChanged&unscoped_q=valueForPathChanged">[search for examples]</a>

