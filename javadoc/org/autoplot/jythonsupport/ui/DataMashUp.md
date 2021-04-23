# org.autoplot.jythonsupport.ui.DataMashUpGUI for specifying mashups, where a number of 
 data sets are loaded and combined.  These are implemented as small
 jython scripts, consisting only of declarations and an expression.
DataMashUp( )
Creates new form DataMashUp

***
<a name="enableTimeRange"></a>
# enableTimeRange
enableTimeRange(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=enableTimeRange&unscoped_q=enableTimeRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getAsJythonInline"></a>
# getAsJythonInline
getAsJythonInline(  ) &rarr; String

return the mashup as a jython inline script.

### Returns:
the mashup as a jython inline script.

<a href="https://github.com/autoplot/dev/search?q=getAsJythonInline&unscoped_q=getAsJythonInline">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getAsJythonInline( javax.swing.tree.TreeNode tn ) &rarr; String<br>
***
<a name="insertElement"></a>
# insertElement
insertElement( java.lang.Object[] array, int index, Object node ) &rarr; Object

insert element into array at index, as long as index is within the array
 or at the length of the array.

### Parameters:
array - array of elements
<br>index - index for insertion, which may be out of bounds for the array.
<br>node - the object to insert.

### Returns:
a java.lang.Object[]

### See Also:
<a href='.md'></a> <br>

<a href="https://github.com/autoplot/dev/search?q=insertElement&unscoped_q=insertElement">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDataMashupJythonInline"></a>
# isDataMashupJythonInline
isDataMashupJythonInline( String jython ) &rarr; boolean

return true if the script conforms to the jython dashup requirements.

### Parameters:
jython - script.

### Returns:
true if the script conforms to the jython dashup requirements.

<a href="https://github.com/autoplot/dev/search?q=isDataMashupJythonInline&unscoped_q=isDataMashupJythonInline">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="printPath"></a>
# printPath
printPath( java.lang.Object[] newPath ) &rarr; String

print the path to a string, comma delimited.

### Parameters:
newPath - a java.lang.Object[]

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=printPath&unscoped_q=printPath">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rename"></a>
# rename
rename( String oldName, String newName ) &rarr; void

rename the parameter and all usages within the tree.

### Parameters:
oldName - a String
<br>newName - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=rename&unscoped_q=rename">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAsJythonInline"></a>
# setAsJythonInline
setAsJythonInline( String script ) &rarr; void

configure the mashup tool using the "vap+inline" URI.

### Parameters:
script - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAsJythonInline&unscoped_q=setAsJythonInline">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setIds"></a>
# setIds
setIds( java.util.List ids ) &rarr; void

set the ids for each of the URIs.

### Parameters:
ids - list of Java identifiers.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setIds&unscoped_q=setIds">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setResolver"></a>
# setResolver
setResolver( org.autoplot.jythonsupport.ui.DataMashUp.Resolver r ) &rarr; void



### Parameters:
r - a DataMashUp.Resolver

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setResolver&unscoped_q=setResolver">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setUris"></a>
# setUris
setUris( java.util.List uris ) &rarr; void

set the list of URIs.

### Parameters:
uris - a list of URIs.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUris&unscoped_q=setUris">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

