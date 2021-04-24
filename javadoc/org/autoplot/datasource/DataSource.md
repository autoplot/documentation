# org.autoplot.datasource.DataSource

Like the DataLoader of das2, but provides minimal dataset discovery metadata

***
<a name="asynchronousLoad"></a>
# asynchronousLoad
asynchronousLoad(  ) &rarr; boolean

loading the data is slow, so load the data asynchronously (on a separate thread).  This
should return true if getDataSet will take more than 100 milliseconds (interactive time).
 Note this is currently ignored, and may be indefinitely ignored.

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=asynchronousLoad&unscoped_q=asynchronousLoad">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCapability"></a>
# getCapability
getCapability( java.lang.Class clazz ) &rarr; Object

cookie jar of capabilities, see org.autoplot.datasource.capability.  Each capability can be 
 queried, and either an object implementing the capability or null is returned.  Example
 capabilities include:<table>
 <tr><td>TimeSeriesBrowse</td><td>which allows the user to request data from a different interval. </td></tr>
 <tr><td>Caching</td><td>which should be queried before the loader is called again.</td></tr>
 </table>
 Note the DataSourceFactory also has a getCapability method, solely to provide TimeSeriesBrowse so that 
 new URIs can be created in without reading data.

### Parameters:
clazz - a java.lang.Class

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=getCapability&unscoped_q=getCapability">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSet"></a>
# getDataSet
getDataSet( ProgressMonitor mon ) &rarr; QDataSet

retrieve the dataset.  This allowed to be sub-interactive or batch time scale, and will block
 until the dataset is produced.

 This may return null when no data is available, or NoDataInIntervalException can be thrown.

 If the user cancelled the operation, then java.io.InterrupedIOExcaption or
 better yet org.das2.CancelledOperationException should be called.  These will
 simply display "cancelled" (or similar) on the status bar.

### Parameters:
mon - a ProgressMonitor

### Returns:
the DataSet for the URI, or null if no data is available.

<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMetadata"></a>
# getMetadata
getMetadata( ProgressMonitor mon ) &rarr; Map

Return arbitrary metadata for the dataset.  This is a map of String to Objects,
 and to form a tree structure, property name may map to another Map&lt;String,Object&gt;.
 Note the order of the properties may be controlled by using LinkedHashMap for the
 implementation.  Even though this takes a monitor, it will be called after getDataSet,
 and the monitor may be safely ignored.
 This should return new HashMap() if no metadata is found.

### Parameters:
mon - a ProgressMonitor

### Returns:
a java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getMetadata&unscoped_q=getMetadata">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMetadataModel"></a>
# getMetadataModel
getMetadataModel(  ) &rarr; MetadataModel

return a MetadataModel that scrapes the Metadata tree returned to provide a
 set of properties identified in QDataSet.

### Returns:
an org.autoplot.datasource.MetadataModel


<a href="https://github.com/autoplot/dev/search?q=getMetadataModel&unscoped_q=getMetadataModel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getProperties"></a>
# getProperties
getProperties(  ) &rarr; Map

discovery properties for the dataset.  These should follow the QDataSet conventions, such as
 TITLE, LABEL, etc, and should mirror the structure of the dataset.  Note
 getMetadataModel().getProperties( getMetaData() ) should return the same thing.

### Returns:
the properties.

<a href="https://github.com/autoplot/dev/search?q=getProperties&unscoped_q=getProperties">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getURI"></a>
# getURI
getURI(  ) &rarr; String

return the fully-qualified URI of this data source, including the "vap+<ext>:" scheme.

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getURI&unscoped_q=getURI">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

