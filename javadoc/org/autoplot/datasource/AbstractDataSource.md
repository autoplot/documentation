# org.autoplot.datasource.AbstractDataSource

Base class for file-based DataSources that keeps track of the uri, makes
 the parameters available, manages capabilities and has do-nothing
 implementations for rarely-used methods of DataSource.

 Also this provides the filePollUpdating parameter and Updating capability.

# AbstractDataSource( java.net.URI uri )


***
<a name="addCability"></a>
# <del>addCability</del>
Deprecated: use addCapability
***
<a name="addCapability"></a>
# addCapability
addCapability( java.lang.Class clazz, Object o ) &rarr; void

attach a capability

### Parameters:
clazz - the capability class.
<br>o - an implementation.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addCapability&unscoped_q=addCapability">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="asynchronousLoad"></a>
# asynchronousLoad
asynchronousLoad(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=asynchronousLoad&unscoped_q=asynchronousLoad">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCapability"></a>
# getCapability
getCapability( java.lang.Class clazz ) &rarr; Object

attempt to get a capability.  null will be returned if the 
 capability doesn't exist.

### Parameters:
clazz - the capability class.

### Returns:
null or an implementation of a capability.

<a href="https://github.com/autoplot/dev/search?q=getCapability&unscoped_q=getCapability">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSet"></a>
# getDataSet
getDataSet( ProgressMonitor mon ) &rarr; QDataSet



### Parameters:
mon - a ProgressMonitor

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMetadata"></a>
# getMetadata
getMetadata( ProgressMonitor mon ) &rarr; Map

abstract class version returns an empty tree.  Override this method
 to provide metadata.

### Parameters:
mon - progress monitor

### Returns:
a java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getMetadata&unscoped_q=getMetadata">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMetadataModel"></a>
# getMetadataModel
getMetadataModel(  ) &rarr; MetadataModel

return a MetadataModel object that can make the metadata canonical.
 For example, ISTPMetadataModel interprets the metadata returned from CDF files,
 but this same model can be used with HDF files.  This returns a null model
 that does no interpretation, and some data sources will override this.

### Returns:
an org.autoplot.datasource.MetadataModel


<a href="https://github.com/autoplot/dev/search?q=getMetadataModel&unscoped_q=getMetadataModel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getProperties"></a>
# getProperties
getProperties(  ) &rarr; Map

return metadata in canonical form using the metadata model.  If there
 are no properties or a null model, then an empty map is returned.
 Note, getMetadataModel should return non-null, and getMetadata should return non-null,
 but this guards against the mistake.

### Returns:
a java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getProperties&unscoped_q=getProperties">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getURI"></a>
# getURI
getURI(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getURI&unscoped_q=getURI">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

