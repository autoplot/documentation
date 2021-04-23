# org.autoplot.datasource.MetadataModelMaps various metadata models to set of canonical name/value pairs
 See QDataSet properties for list of properties.
MetadataModel( )


***
<a name="copyTree"></a>
# copyTree
copyTree( javax.swing.tree.TreeModel src ) &rarr; TreeModel

method for copying tree when the tree does not provide random access.

### Parameters:
src - a TreeModel

### Returns:
a javax.swing.tree.TreeModel


<a href="https://github.com/autoplot/dev/search?q=copyTree&unscoped_q=copyTree">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createNullModel"></a>
# createNullModel
createNullModel(  ) &rarr; MetadataModel



### Returns:
org.autoplot.datasource.MetadataModel


<a href="https://github.com/autoplot/dev/search?q=createNullModel&unscoped_q=createNullModel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLabel"></a>
# getLabel
getLabel(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getLabel&unscoped_q=getLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNode"></a>
# getNode
getNode( java.util.Map tree, java.lang.String[] path ) &rarr; Object

drills down through the Maps.  This returns value.

### Parameters:
tree - a java.util.Map
<br>path - a java.lang.String[]

### Returns:
an Object


<a href="https://github.com/autoplot/dev/search?q=getNode&unscoped_q=getNode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNodeValue"></a>
# getNodeValue
getNodeValue( java.util.Map tree, java.lang.String[] path ) &rarr; String

drills down through the Maps.  This returns value.

### Parameters:
tree - a java.util.Map
<br>path - a java.lang.String[]

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getNodeValue&unscoped_q=getNodeValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getNodeValue( javax.swing.tree.TreeModel tree, java.lang.String[] path ) &rarr; String<br>
***
<a name="properties"></a>
# properties
properties( java.util.Map meta ) &rarr; Map

Derive QDataSet properties from inspection of the metadata tree.
 DEPEND_0, etc are Map&lt;String,Object&gt;.

### Parameters:
meta - model provided by DataSource

### Returns:
Map with properties such as QDataSet.TITLE

<a href="https://github.com/autoplot/dev/search?q=properties&unscoped_q=properties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

