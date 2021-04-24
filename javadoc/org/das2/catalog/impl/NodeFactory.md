# org.das2.catalog.impl.NodeFactory

Static generator functions for das2 federated catalog node objects. 
 
 One of the main purposes of this class is to maintain the root node registry.  Since
 many formally constant responses (such as completions) are now dynamic, something has
 to keep track of the catalog nodes or they would be re-loaded all the time.
 Furthermore some of the catalog nodes (namely SPASE) can be loaded from locations that
 require query parameters in the URLs, so we don't want to use the http filesystem
 objects because they (AFAIK) would not map URLs like this:
 
    http://spase-group.org/registry/resolver?t=yes&i=spase://ASWS
 
 to a file object on disk due to the '?' character in the URL.  The das2 catalog is
 supposed to paper over all kinds of weird URLs, so directly downloading and caching
 items seems like the best bet.

# NodeFactory( )


***
<a name="DAS_ROOT_PATH"></a>
# DAS_ROOT_PATH



***
<a name="DEFAULT_DATA_PATH"></a>
# DEFAULT_DATA_PATH



***
<a name="DEFAULT_TEST_PATH"></a>
# DEFAULT_TEST_PATH



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
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getUtf8NodeDef"></a>
# getUtf8NodeDef
getUtf8NodeDef( String sUrl, ProgressMonitor mon ) &rarr; String



### Parameters:
sUrl - a String
<br>mon - a ProgressMonitor

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getUtf8NodeDef&unscoped_q=getUtf8NodeDef">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

