# org.das2.catalog.DasDirNode

All directory node objects can have children

***
<a name="childPath"></a>
# childPath
childPath( org.das2.catalog.DasNode child ) &rarr; String

Given a child object get the complete path to it

### Parameters:
child - The child object for which the path is desired.

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=childPath&unscoped_q=childPath">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="get"></a>
# get
get( String sChildId ) &rarr; DasNode

Get a child node by it's ID.

### Parameters:
sChildId - a String

### Returns:
The child node, or null if no child node has the id sChildId

<a href="https://github.com/autoplot/dev/search?q=get&unscoped_q=get">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="list"></a>
# list
list(  ) &rarr; String

List child nodes of this directory type item

### Returns:
A list of child node string ids.  Return values may be used in the get node
         function below.

<a href="https://github.com/autoplot/dev/search?q=list&unscoped_q=list">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="nearest"></a>
# nearest
nearest( String sSubPath, ProgressMonitor mon ) &rarr; DasNode

Walk down a given sub-path as far as possible and retrieve the closest descendant
 FIXME: Find a better name for this function, maybe resolveDeepest

### Parameters:
sSubPath - A sub-path to resolve into a fully loaded node.  If this node is a
        root catalog, then the sub-path is the complete path.
<br>mon - A progress monitor since sub-node lookup can involve network operations

### Returns:
The deepest resolvable node which may just be "this", or even the "parent"
         in cases where this node is a stub that can't even resolve itself.

<a href="https://github.com/autoplot/dev/search?q=nearest&unscoped_q=nearest">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="pathSeparator"></a>
# pathSeparator
pathSeparator( ProgressMonitor mon ) &rarr; String

Get the separator string to place after my path but before then names of any 
 child items when generating a child path string.

### Parameters:
mon - The separator may be defined in the object data which may trigger
            Phase-2 construction.  Since this is a network operation a progress
            monitor may be supplied.

### Returns:
The path separator string, which may be zero length (and that's okay).

<a href="https://github.com/autoplot/dev/search?q=pathSeparator&unscoped_q=pathSeparator">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resolve"></a>
# resolve
resolve( String sSubPath, ProgressMonitor mon ) &rarr; DasNode

Walk down a given sub-path and retrieve a fully constructed descendant node.

### Parameters:
sSubPath - A sub-path to resolve into a fully loaded node.  If this node is a 
        root catalog, then the sub-path is the complete path.
<br>mon - A progress monitor since sub-node lookup can involve network operations

### Returns:
The full constructed child node object.

<a href="https://github.com/autoplot/dev/search?q=resolve&unscoped_q=resolve">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

