# org.das2.catalog.impl.AbstractDirNodeAll nodes which have child catalog nodes should inherit from this package
 private class.
 
 In addition to the 3-phase construction interface, this abstract class adds the
 ability to have sub-nodes, which is provided via the resolve() and nearest() 
 functions.
 
 The two main data members intended for inheritance are dSubNodes and sSep.
 If derived classes use this sub-node list and fill in their separator string
 the sub-node resolution can be handled by this class with out overriding 
 resolve() and nearest().
***
<a name="childPath"></a>
# childPath
childPath( org.das2.catalog.DasNode child ) &rarr; String



### Parameters:
child - a DasNode

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=childPath&unscoped_q=childPath">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="get"></a>
# get
get( String sChildId ) &rarr; DasNode



### Parameters:
sChildId - a String

### Returns:
org.das2.catalog.DasNode


<a href="https://github.com/autoplot/dev/search?q=get&unscoped_q=get">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="list"></a>
# list
list(  ) &rarr; String



### Returns:
java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=list&unscoped_q=list">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="nearest"></a>
# nearest
nearest( String sSubPath, ProgressMonitor mon ) &rarr; DasNode



### Parameters:
sSubPath - a String
<br>mon - a ProgressMonitor

### Returns:
org.das2.catalog.DasNode


<a href="https://github.com/autoplot/dev/search?q=nearest&unscoped_q=nearest">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="pathSeparator"></a>
# pathSeparator
pathSeparator( ProgressMonitor mon ) &rarr; String



### Parameters:
mon - a ProgressMonitor

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=pathSeparator&unscoped_q=pathSeparator">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resolve"></a>
# resolve
resolve( String sSubPath, ProgressMonitor mon ) &rarr; DasNode



### Parameters:
sSubPath - a String
<br>mon - a ProgressMonitor

### Returns:
org.das2.catalog.DasNode


<a href="https://github.com/autoplot/dev/search?q=resolve&unscoped_q=resolve">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

