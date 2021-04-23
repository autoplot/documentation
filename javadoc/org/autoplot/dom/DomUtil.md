# org.autoplot.dom.DomUtil

operations for the DOM, such as search-for-node and child properties

# DomUtil( )


***
<a name="STRING_TO_FONT"></a>
# STRING_TO_FONT



***
<a name="STRING_TO_COLOR"></a>
# STRING_TO_COLOR



***
<a name="AUTO_TO_COLOR"></a>
# AUTO_TO_COLOR



***
<a name="abbreviateRight"></a>
# abbreviateRight
abbreviateRight( String s, int len ) &rarr; String

trim the string on the left, leaving the right visible.

### Parameters:
s - the string
<br>len - the number of characters

### Returns:
"..."+s.substring(s.length() - len)

<a href="https://github.com/autoplot/dev/search?q=abbreviateRight&unscoped_q=abbreviateRight">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="applyMacro"></a>
# applyMacro
applyMacro( org.autoplot.dom.DomNode state, String node, String sval ) &rarr; void

Look through the state property values for references to ${PWD}
 and replace them with sval.

### Parameters:
state - the domNode, typically starting from the Application root.
<br>node - %{PWD}
<br>sval - /tmp

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=applyMacro&unscoped_q=applyMacro">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="asArrayList"></a>
# asArrayList
asArrayList( java.lang.Object[] a ) &rarr; ArrayList

Just like Arrays.toList, but copies into ArrayList so elements may be inserted.

### Parameters:
a - a java.lang.Object[]

### Returns:
ArrayList that can have elements inserted

<a href="https://github.com/autoplot/dev/search?q=asArrayList&unscoped_q=asArrayList">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="checkUniqueIdsAndReferences"></a>
# checkUniqueIdsAndReferences
checkUniqueIdsAndReferences( org.autoplot.dom.Application dom, java.util.List problems ) &rarr; List



### Parameters:
dom - an Application
<br>problems - a java.util.List

### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=checkUniqueIdsAndReferences&unscoped_q=checkUniqueIdsAndReferences">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="childDiff"></a>
# childDiff
childDiff( String childName, org.autoplot.dom.Diff diff ) &rarr; Diff

return the child diff in the context of the parent node.  May return
 null if the diff cannot be described.

### Parameters:
childName - a String
<br>diff - a Diff

### Returns:
an org.autoplot.dom.Diff


<a href="https://github.com/autoplot/dev/search?q=childDiff&unscoped_q=childDiff">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="childDiffs"></a>
# childDiffs
childDiffs( String childName, java.util.List diffs ) &rarr; List

return the child diff in the context of the parent node.  May return
 null if the diff cannot be described.

### Parameters:
childName - a String
<br>diffs - a java.util.List

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=childDiffs&unscoped_q=childDiffs">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="copyOverInternalData"></a>
# copyOverInternalData
copyOverInternalData( org.autoplot.dom.Application srcdom, org.autoplot.dom.Application dstdom ) &rarr; void

copy over "vap+internal:" data, where data is found in the controller but no URI represents it.
 This is to support https://sourceforge.net/p/autoplot/bugs/2332/, where we now copy over any data
 we find as well.

### Parameters:
srcdom - the src dom with controllers and possibly internal data.
<br>dstdom - the dst dom with controllers.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=copyOverInternalData&unscoped_q=copyOverInternalData">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="deleteDataSourceFilter"></a>
# deleteDataSourceFilter
deleteDataSourceFilter( org.autoplot.dom.Application application, org.autoplot.dom.DataSourceFilter dsf ) &rarr; void

delete the data source filter.

### Parameters:
application - an Application
<br>dsf - the data source filter to remove.

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/autoplot/dom/ApplicationController.md#deleteDataSourceFilter'>org.autoplot.dom.ApplicationController#deleteDataSourceFilter(org.autoplot.dom.DataSourceFilter)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=deleteDataSourceFilter&unscoped_q=deleteDataSourceFilter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="describe"></a>
# describe
describe( DatumRange init, DatumRange fin ) &rarr; String

describe the change in axis range.  These include:<ul>
 <li>zoom in, zoom out - one range completely contains the other.
 <li>pan - the range is adjusted but partially overlaps
 <li>scan - the range is adjusted so that the two do not intersect.
 </ul>

### Parameters:
init - the initial range
<br>fin - the final range

### Returns:
the human consumable string, e.g. "zoom out"

<a href="https://github.com/autoplot/dev/search?q=describe&unscoped_q=describe">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="encodeColor"></a>
# encodeColor
encodeColor( java.awt.Color c ) &rarr; String



### Parameters:
c - a Color

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=encodeColor&unscoped_q=encodeColor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="encodeFont"></a>
# encodeFont
encodeFont( java.awt.Font f ) &rarr; String



### Parameters:
f - a Font

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=encodeFont&unscoped_q=encodeFont">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="findBinding"></a>
# findBinding
findBinding( org.autoplot.dom.Application dom, org.autoplot.dom.DomNode src, String srcProp, org.autoplot.dom.DomNode dst, String dstProp ) &rarr; BindingModel

Find the binding, if it exists.  All bindingImpls are symmetric, so the src and dst order is ignored in this
 search.

### Parameters:
dom - the dom tree
<br>src - a DomNode
<br>srcProp - a String
<br>dst - a DomNode
<br>dstProp - a String

### Returns:
the BindingModel or null if it doesn't exist.

<a href="https://github.com/autoplot/dev/search?q=findBinding&unscoped_q=findBinding">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="findBindings"></a>
# findBindings
findBindings( org.autoplot.dom.Application dom, org.autoplot.dom.DomNode src, String srcProp ) &rarr; List

returns a list of bindings of the node for the property

### Parameters:
dom - the dom tree
<br>src - the node to which or from which a binding exists
<br>srcProp - the property name of the binding.

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=findBindings&unscoped_q=findBindings">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

findBindings( org.autoplot.dom.Application dom, org.autoplot.dom.DomNode src, String srcProp, org.autoplot.dom.DomNode dst, String dstProp ) &rarr; List<br>
***
<a name="findElementsById"></a>
# findElementsById
findElementsById( org.autoplot.dom.DomNode root, String regex ) &rarr; List

find the nodes matching this regex.

### Parameters:
root - the node to start at.
<br>regex - the regular expression.

### Returns:
the nodes.

<a href="https://github.com/autoplot/dev/search?q=findElementsById&unscoped_q=findElementsById">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="formatObject"></a>
# formatObject
formatObject( Object obj ) &rarr; String



### Parameters:
obj - an Object

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=formatObject&unscoped_q=formatObject">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getArrayDiffs"></a>
# getArrayDiffs
getArrayDiffs( String property, java.lang.Object[] nodes1, java.lang.Object[] nodes2 ) &rarr; List

list the differences in two arrays of the same type of object.
 This is the diffs that will make nodes2 look like nodes1.
 Presently this just identifies inserts and deletes.  If the objects
 are DomNodes, then ids are used to match nodes.

### Parameters:
property - name used to identify the difference in the result.
<br>nodes1 - list of nodes
<br>nodes2 - list of nodex

### Returns:
list of Diffs between the lists.

<a href="https://github.com/autoplot/dev/search?q=getArrayDiffs&unscoped_q=getArrayDiffs">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSourceFiltersFor"></a>
# getDataSourceFiltersFor
getDataSourceFiltersFor( org.autoplot.dom.Application dom, org.autoplot.dom.Plot p ) &rarr; List

return the list of DataSourceFilters for a plot.

### Parameters:
dom - the application
<br>p - the plot

### Returns:
new list of dataSourceFilters

<a href="https://github.com/autoplot/dev/search?q=getDataSourceFiltersFor&unscoped_q=getDataSourceFiltersFor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDiffs"></a>
# getDiffs
getDiffs( org.autoplot.dom.DomNode node1, org.autoplot.dom.DomNode node2 ) &rarr; List

automatically detect the diffs between two DomNodes of the same type.
 return the list of diffs that will make node2 look like node1.
 The property "controller" is ignored.

### Parameters:
node1 - a DomNode
<br>node2 - a DomNode

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=getDiffs&unscoped_q=getDiffs">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getDiffs( org.autoplot.dom.DomNode node1, org.autoplot.dom.DomNode node2, java.util.List exclude ) &rarr; List<br>
***
<a name="getElementByAddress"></a>
# getElementByAddress
getElementByAddress( org.autoplot.dom.DomNode domNode, String address ) &rarr; DomNode

return the node at the address, for example "plots[2].xaxis" of an application.

### Parameters:
domNode - the initial dom node, like dom.
<br>address - the address, like plots[2].xaxis

### Returns:
the domNode at the address.
### See Also:
<a href='#getElementById'>getElementById(org.autoplot.dom.DomNode, java.lang.String)</a> y<br>

<a href="https://github.com/autoplot/dev/search?q=getElementByAddress&unscoped_q=getElementByAddress">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getElementById"></a>
# getElementById
getElementById( org.autoplot.dom.DomNode root, String id ) &rarr; DomNode

return the node with this id, or null if the id is not found.

### Parameters:
root - the root, such as the dom or the canvas.
<br>id - the id of the node.

### Returns:
the node with this id, or null if the id is not found.
### See Also:
<a href='#getElementByAddress'>getElementByAddress(org.autoplot.dom.DomNode, java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getElementById&unscoped_q=getElementById">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getParentsFor"></a>
# getParentsFor
getParentsFor( org.autoplot.dom.Application dom, String uri ) &rarr; List

return the parent DataSourceFilters for uris like vap+internal:data_1,data_2
 Note this was the only way to combine 
 data before the "Data Mashup Tool" was introduced, and the Mashup tool
 is probably a better way to do this.

### Parameters:
dom - the dom
<br>uri - the uri, like vap+internal:data_1,data_2

### Returns:
the DataSourceFilters

<a href="https://github.com/autoplot/dev/search?q=getParentsFor&unscoped_q=getParentsFor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlotAsString"></a>
# getPlotAsString
getPlotAsString( org.autoplot.dom.Application application, org.autoplot.dom.Plot domPlot ) &rarr; String

this was made public for bug 1520.  This returns a 1-plot dom, but 
 this may change.

### Parameters:
application - an Application
<br>domPlot - a Plot

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getPlotAsString&unscoped_q=getPlotAsString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlotElementsFor"></a>
# getPlotElementsFor
getPlotElementsFor( org.autoplot.dom.Application application, org.autoplot.dom.Plot plot ) &rarr; List

Return the plot elements that contained within a plot.

### Parameters:
application - the dom for a plot.
<br>plot - the plot containing plot elements.

### Returns:
the plot elements contained by the plot.

<a href="https://github.com/autoplot/dev/search?q=getPlotElementsFor&unscoped_q=getPlotElementsFor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getPlotElementsFor( org.autoplot.dom.Application application, org.autoplot.dom.DataSourceFilter dsf ) &rarr; List<br>
***
<a name="getPlotForAxis"></a>
# getPlotForAxis
getPlotForAxis( org.autoplot.dom.Application app, org.autoplot.dom.Axis oa ) &rarr; Plot

return null or the plot using the axis.

### Parameters:
app - the application
<br>oa - the axis

### Returns:
null or the plot using the axis

<a href="https://github.com/autoplot/dev/search?q=getPlotForAxis&unscoped_q=getPlotForAxis">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPropertyType"></a>
# getPropertyType
getPropertyType( org.autoplot.dom.DomNode node, String propertyName ) &rarr; Class

get the property type, e.g. Datum.class or [Lorg.virbo.autoplot.dom.Canvas (array of Canvases.)

### Parameters:
node - the dom node
<br>propertyName - the property name

### Returns:
the property type

<a href="https://github.com/autoplot/dev/search?q=getPropertyType&unscoped_q=getPropertyType">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPropertyValue"></a>
# getPropertyValue
getPropertyValue( org.autoplot.dom.DomNode node, String propertyName ) &rarr; Object

get the node property value

### Parameters:
node - the dom node
<br>propertyName - the property name

### Returns:
the node property value

<a href="https://github.com/autoplot/dev/search?q=getPropertyValue&unscoped_q=getPropertyValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="indexOf"></a>
# indexOf
indexOf( java.util.List nodes, Object node ) &rarr; int

returns the index by ID, not by equals.  Equals cannot be 
 overriden, because property change diffs, etc.

### Parameters:
nodes - list of nodes
<br>node - the node to search for

### Returns:
the index or -1.

<a href="https://github.com/autoplot/dev/search?q=indexOf&unscoped_q=indexOf">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="layoutToString"></a>
# layoutToString
layoutToString( org.autoplot.dom.Canvas c ) &rarr; String

print a one-line representation of the layout, showing canvas dimensions,
 font size, margin row and column, and the first row.

### Parameters:
c - a Canvas

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=layoutToString&unscoped_q=layoutToString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="nodeHasProperty"></a>
# nodeHasProperty
nodeHasProperty( org.autoplot.dom.DomNode node1, String property ) &rarr; boolean

allow verification that the node has a property.  I killed an hour with a 
 bug where I was using "timerange" instead of "timeRange"...
 Always use the constants: Application.PROP_TIMERANGE

### Parameters:
node1 - a DomNode
<br>property - a String

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=nodeHasProperty&unscoped_q=nodeHasProperty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="oneFamily"></a>
# oneFamily
oneFamily( java.util.List elementsIn ) &rarr; boolean

returns true if all the plotElements are a parent and its children.

### Parameters:
elementsIn - a java.util.List

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=oneFamily&unscoped_q=oneFamily">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parseObject"></a>
# parseObject
parseObject( Object context, String s ) &rarr; Object



### Parameters:
context - an Object
<br>s - a String

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=parseObject&unscoped_q=parseObject">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resolveProperties"></a>
# resolveProperties
resolveProperties( String template, String root, java.util.Map props ) &rarr; String

plugs values from USER_PROPERTIES or METADATA into template string.

### Parameters:
template - template, for example the title or label.
<br>root - USER_PROPERTIES, METADATA, etc.
<br>props - properties tree.

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=resolveProperties&unscoped_q=resolveProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPropertyValue"></a>
# setPropertyValue
setPropertyValue( org.autoplot.dom.DomNode node, String propertyName, Object val ) &rarr; void

set the property value

### Parameters:
node - the dom node
<br>propertyName - the property name
<br>val - the new value

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPropertyValue&unscoped_q=setPropertyValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="structureChanges"></a>
# structureChanges
structureChanges( org.autoplot.dom.Application dom, org.autoplot.dom.Application state ) &rarr; boolean

returns true if the dom structure changes.  For example the number of
 plotElements changes, then this returns true.  If only the range of
 an axis changes, then return false;
 2012-01-11: check axis units after failure in test002_003 showed that old dataset was used for autoranging.

### Parameters:
dom - an Application
<br>state - an Application

### Returns:
true if the dom structure changes.

<a href="https://github.com/autoplot/dev/search?q=structureChanges&unscoped_q=structureChanges">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="syncTo"></a>
# syncTo
syncTo( org.autoplot.dom.DomNode node1, org.autoplot.dom.DomNode node2 ) &rarr; void

sync node1 to node2 through introspection.  This only works for nodes
 without controllers, etc.  It would be really nice to figure out how
 to generalize this to include inserted nodes,etc.

### Parameters:
node1 - a DomNode
<br>node2 - a DomNode

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=syncTo&unscoped_q=syncTo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

syncTo( org.autoplot.dom.DomNode node1, org.autoplot.dom.DomNode node2, java.util.List exclude ) &rarr; void<br>
***
<a name="validateDom"></a>
# validateDom
validateDom( org.autoplot.dom.Application application, java.util.List problems ) &rarr; boolean

returns true if the dom is valid, throws a runtime exception otherwise

### Parameters:
application - the dom
<br>problems - descriptions of the problems will be inserted here

### Returns:
true if the dom is valid, throws a runtime exception otherwise

<a href="https://github.com/autoplot/dev/search?q=validateDom&unscoped_q=validateDom">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="vapToJython"></a>
# vapToJython
vapToJython( org.autoplot.dom.Application app0, org.autoplot.dom.Application app ) &rarr; String

Ivar requested a vap-to-Jython converter.

### Parameters:
app0 - an Application
<br>app - an Application

### Returns:
a java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=vapToJython&unscoped_q=vapToJython">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

