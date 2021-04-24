# org.autoplot.netCDF.NetCDFDataSourceFactory

Factory for NetCDF and HDF5 data sources.

# NetCDFDataSourceFactory( )
Creates a new instance of NetCDFDataSourceFactory

***
<a name="getCapability"></a>
# getCapability
getCapability( java.lang.Class clazz ) &rarr; Object



### Parameters:
clazz - a java.lang.Class

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=getCapability&unscoped_q=getCapability">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCompletions"></a>
# getCompletions
getCompletions( org.autoplot.datasource.CompletionContext cc, ProgressMonitor mon ) &rarr; List



### Parameters:
cc - a CompletionContext
<br>mon - a ProgressMonitor

### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=getCompletions&unscoped_q=getCompletions">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSource"></a>
# getDataSource
getDataSource( java.net.URI uri ) &rarr; DataSource



### Parameters:
uri - an URI

### Returns:
org.autoplot.datasource.DataSource


<a href="https://github.com/autoplot/dev/search?q=getDataSource&unscoped_q=getDataSource">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMetadataModel"></a>
# getMetadataModel
getMetadataModel( java.net.URL url ) &rarr; MetadataModel



### Parameters:
url - an URL

### Returns:
org.autoplot.datasource.MetadataModel


<a href="https://github.com/autoplot/dev/search?q=getMetadataModel&unscoped_q=getMetadataModel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNumberOfRecords"></a>
# getNumberOfRecords
getNumberOfRecords( String surl, ProgressMonitor mon ) &rarr; int

return the number of records of the variable.  The file will be 
 downloaded if it is not available.  This was introduced because
 we had a huge file where we needed to read in so many blocks at a time,
 instead of the entire file.

### Parameters:
surl - the URI, including the variable to read.
<br>mon - the monitor

### Returns:
the number of records.

<a href="https://github.com/autoplot/dev/search?q=getNumberOfRecords&unscoped_q=getNumberOfRecords">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getParams"></a>
# getParams
getParams( java.net.URI ncFile, ProgressMonitor mon ) &rarr; Map



### Parameters:
ncFile - an URI
<br>mon - a ProgressMonitor

### Returns:
java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getParams&unscoped_q=getParams">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reject"></a>
# reject
reject( String surl, java.util.List problems, ProgressMonitor mon ) &rarr; boolean



### Parameters:
surl - a String
<br>problems - a java.util.List
<br>mon - a ProgressMonitor

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=reject&unscoped_q=reject">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

