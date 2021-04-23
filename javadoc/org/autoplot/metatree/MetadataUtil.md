# org.autoplot.metatree.MetadataUtil



# MetadataUtil( )


***
<a name="getMetadataModel"></a>
# getMetadataModel
getMetadataModel( String t ) &rarr; MetadataModel

return the MetadataModel object for this identifier, or null.

### Parameters:
t - the id of the model, such as "ISTP-CDF", or null.

### Returns:
an org.autoplot.datasource.MetadataModel


<a href="https://github.com/autoplot/dev/search?q=getMetadataModel&unscoped_q=getMetadataModel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNode"></a>
# getNode
getNode( org.w3c.dom.Node node, java.lang.String[] path ) &rarr; Node



### Parameters:
node - a Node
<br>path - a java.lang.String[]

### Returns:
org.w3c.dom.Node


<a href="https://github.com/autoplot/dev/search?q=getNode&unscoped_q=getNode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getNode( java.util.Map tree, java.lang.String[] path ) &rarr; Object<br>
***
<a name="normalizeFormatSpecifier"></a>
# normalizeFormatSpecifier
normalizeFormatSpecifier( String spec ) &rarr; String

converts IDL and Fortran-style specs (F7.2) to Java/C style (%7.2f), or
 returns null when this cannot be done.

### Parameters:
spec - Java or Fortran style format

### Returns:
null if no conversion can be made, or Java style
### See Also:
<a href='String.md#format'>String#format(java.lang.String, java.lang.Object...)</a> <br>
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/util/AsciiParser.md#getRegexForFormat'>org.das2.qds.util.AsciiParser#getRegexForFormat(java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=normalizeFormatSpecifier&unscoped_q=normalizeFormatSpecifier">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="sliceProperties"></a>
# sliceProperties
sliceProperties( java.util.Map properties, int sliceDimension ) &rarr; Map

slice the properties to reduce rank.  TODO: This all needs review, since the QDataSet model is mature.

### Parameters:
properties - a java.util.Map
<br>sliceDimension - an int

### Returns:
a java.util.Map

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/DataSetOps/sliceProperties.md'>DataSetOps.sliceProperties</a> <br>

<a href="https://github.com/autoplot/dev/search?q=sliceProperties&unscoped_q=sliceProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="sprocess"></a>
# sprocess
sprocess( String c, java.util.Map properties ) &rarr; Map

run the DataSource-provided properties through sprocess.
 TODO: this has not been implemented for most operations, and this all needs to be reconsidered

### Parameters:
c - a String
<br>properties - a java.util.Map

### Returns:
a java.util.Map


<a href="https://github.com/autoplot/dev/search?q=sprocess&unscoped_q=sprocess">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toMetaTree"></a>
# toMetaTree
toMetaTree( org.w3c.dom.Node node ) &rarr; Map

converts tree model node into canonical Map<String,Object>.  Branch nodes
 are HashMap<String,Object> as well.

### Parameters:
node - a Node

### Returns:
a java.util.Map


<a href="https://github.com/autoplot/dev/search?q=toMetaTree&unscoped_q=toMetaTree">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="transposeProperties"></a>
# transposeProperties
transposeProperties( java.util.Map properties ) &rarr; Map



### Parameters:
properties - a java.util.Map

### Returns:
a java.util.Map


<a href="https://github.com/autoplot/dev/search?q=transposeProperties&unscoped_q=transposeProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

