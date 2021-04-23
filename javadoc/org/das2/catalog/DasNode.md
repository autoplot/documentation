# org.das2.catalog.DasNodeA single node from the das2 federated catalog, which may, or may not, be fully
  realized from source data.
***
<a name="getRoot"></a>
# getRoot
getRoot(  ) &rarr; DasNode

Return the highest node reachable by this catalog node.

### Returns:
the highest node reachable by this catalog node, which may just be itself.

<a href="https://github.com/autoplot/dev/search?q=getRoot&unscoped_q=getRoot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDir"></a>
# isDir
isDir(  ) &rarr; boolean

Can this catalog node have the sub-nodes?

### Returns:
true if this node can have child nodes, not that it necessarily
          contains any.

<a href="https://github.com/autoplot/dev/search?q=isDir&unscoped_q=isDir">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isInfo"></a>
# isInfo
isInfo(  ) &rarr; boolean

Is this object an information node.

### Returns:
true if this node in the catalog provides a description of a mission, 
         spacecraft, instrument, person or any other item category

<a href="https://github.com/autoplot/dev/search?q=isInfo&unscoped_q=isInfo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isLoaded"></a>
# isLoaded
isLoaded(  ) &rarr; boolean

Does this node have a full definition

### Returns:
True if this node successfully passed the second construction stage.

<a href="https://github.com/autoplot/dev/search?q=isLoaded&unscoped_q=isLoaded">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isRoot"></a>
# isRoot
isRoot(  ) &rarr; boolean

Is this object a detached root of a catalog tree.
 Note that the build in root URLs are always detached roots because there is no
 higher node to find.  A detached source or info node can still be a root node 
 <b>without</b> also being a directory.

### Returns:
true if no higher node is reachable from this one.

<a href="https://github.com/autoplot/dev/search?q=isRoot&unscoped_q=isRoot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isSrc"></a>
# isSrc
isSrc(  ) &rarr; boolean

Can this catalog node provide data

### Returns:
true if this node describes one or more data sources

<a href="https://github.com/autoplot/dev/search?q=isSrc&unscoped_q=isSrc">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="load"></a>
# load
load( ProgressMonitor mon ) &rarr; void

Phase 2 construction for the node.
 
 DasNode objects exist to represent remote catalog data.  Since one catalog
 node can point to others, it is possible to create a stub node that knows 
 how to load itself, but is not actually loaded yet.  This function can be
 used to trigger full catalog node resolution.
 
 
 This will trigger a re-load if the node is already loaded.

### Parameters:
mon - A human amusement device incase network operations are taking a while.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=load&unscoped_q=load">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="name"></a>
# name
name(  ) &rarr; String

get the node name

### Returns:
The human readable name of the node, not it's path ID

<a href="https://github.com/autoplot/dev/search?q=name&unscoped_q=name">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="path"></a>
# path
path(  ) &rarr; String

get the node path

### Returns:
The catalog path to this node.  For root nodes this is null

<a href="https://github.com/autoplot/dev/search?q=path&unscoped_q=path">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="prop"></a>
# prop
prop( String sFragment, Object oDefault ) &rarr; DasProp

Get a property of the node, or the default
 
 Similar to sub-page references for web-pages, property values are retrieved
 by providing a fragment path.  Fragment paths are standardized using the '/'
 as the sub-item separator.  By combining node paths with fragment paths every
 single property value within the global catalog system has a unique URI.  For
 example:
 
 :tag:das2.org,2012:site:/uiowa/voyager/1/pws#interface/coords/time/max/value
 ^    ^        ^    ^                         ^
 |    |        |    |                         |
 |    |        |    +- path                   +- fragment
 |    |        +- date
 |    +- authority  
 +-- scheme
 
 The purpose of this function is to retrieve properties from within a node 
 given a fragment string.

### Parameters:
sFragment - The fragment path, for example "tech_contact/0/email"
<br>oDefault - The default object to return if nothing exists at the
                   fragment location.  The object will be wrapped as a 
                   DasProp, so it must be null or one of the accepted 
                   object types defined for constructing DasProp objects.

### Returns:
A DasProp. If load has not been called for this node, the return will
         always be the default.

<a href="https://github.com/autoplot/dev/search?q=prop&unscoped_q=prop">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

prop( String sFragment ) &rarr; DasProp<br>
***
<a name="toString"></a>
# toString
toString(  ) &rarr; String

A summary of the node

### Returns:
A short string describing the node, not an info dump of the contents

<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="type"></a>
# type
type(  ) &rarr; String

Get the node type.

### Returns:
A string representing the node type

<a href="https://github.com/autoplot/dev/search?q=type&unscoped_q=type">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

