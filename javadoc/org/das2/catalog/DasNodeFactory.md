# org.das2.catalog.DasNodeFactoryPublic static generator functions for das2 federated catalog node objects.
DasNodeFactory( )


***
<a name="defaultDataPath"></a>
# defaultDataPath
defaultDataPath(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=defaultDataPath&unscoped_q=defaultDataPath">[search for examples]</a>

***
<a name="defaultTestPath"></a>
# defaultTestPath
defaultTestPath(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=defaultTestPath&unscoped_q=defaultTestPath">[search for examples]</a>

***
<a name="getNearestNode"></a>
# getNearestNode
getNearestNode( String sUrl, ProgressMonitor mon, boolean bReload ) &rarr; DasNode

Kind of like traceroute, try to resolve successively longer paths until
 you get to one that fails.  For filesystem type URLS (http:, file:, etc.)
 this is the same as getNode().

### Parameters:
sUrl - An autoplot URL
<br>mon - a ProgressMonitor
<br>bReload - a boolean

### Returns:
The nearest loadable DasNode for the path specified.

<a href="https://github.com/autoplot/dev/search?q=getNearestNode&unscoped_q=getNearestNode">[search for examples]</a>

***
<a name="getNode"></a>
# getNode
getNode( String sUrl, ProgressMonitor mon, boolean bReload ) &rarr; DasNode

Get a node from the global node map by URL. 
 
 This function tries to load and return the node for the given URL.  If the file
 portion of the node is a recognized filesystem type then that exact URL is 
 attempted.  For example:

 https://space.physics.uiowa.edu/juno/test/random_source.data
 
 would trigger a filesystem type lookup that expects an exact match.  While a URL
 such as:
 
 tag:das2.org,2012:test:/uiowa/juno/random_collection/das2
 
 For space savings, tag:das2.org,2012: may be left off of the given URLs.
 
 If nothing can be matched, null is return.  The resulting parsed node is saved
 in a cache to avoid repeated network traffic.

### Parameters:
sUrl - a String
<br>mon - a ProgressMonitor
<br>bReload - - Reload the node definition from the original source

### Returns:
The node requested, or throws an error

<a href="https://github.com/autoplot/dev/search?q=getNode&unscoped_q=getNode">[search for examples]</a>

