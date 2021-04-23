# org.autoplot.aggregator.AggregatingDataSourceFactory

ftp://cdaweb.gsfc.nasa.gov/pub/data/noaa/noaa14/$Y/noaa14_meped1min_sem_$Y$m$d_v01.cdf?timerange=2000-01-01

# AggregatingDataSourceFactory( )
Creates a new instance of AggregatingDataSourceFactory

***
<a name="PROB_NO_TIMERANGE_PROVIDED"></a>
# PROB_NO_TIMERANGE_PROVIDED



***
<a name="PROB_PARSE_ERROR_IN_TIMERANGE"></a>
# PROB_PARSE_ERROR_IN_TIMERANGE



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
<a name="getDelegateDataSourceFactory"></a>
# getDelegateDataSourceFactory
getDelegateDataSourceFactory( String surl ) &rarr; DataSourceFactory



### Parameters:
surl - a String

### Returns:
org.autoplot.datasource.DataSourceFactory


<a href="https://github.com/autoplot/dev/search?q=getDelegateDataSourceFactory&unscoped_q=getDelegateDataSourceFactory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDelegateDataSourceFactoryUri"></a>
# getDelegateDataSourceFactoryUri
getDelegateDataSourceFactoryUri( String suri, ProgressMonitor mon ) &rarr; String



### Parameters:
suri - the aggregation, containing the template and the timerange parameter.
<br>mon - a progress monitor.

### Returns:
the URI for each granule.

<a href="https://github.com/autoplot/dev/search?q=getDelegateDataSourceFactoryUri&unscoped_q=getDelegateDataSourceFactoryUri">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDescription"></a>
# getDescription
getDescription(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getDescription&unscoped_q=getDescription">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFileStorageModel"></a>
# getFileStorageModel
getFileStorageModel( String suri ) &rarr; FileStorageModel

return the FileStorageModel for the URI.

### Parameters:
suri - eg. file:/tmp/foo/$Y/$Y$m.dat

### Returns:
the FileStorageModel, eg. for $Y/$Y$m.dat.
### See Also:
<a href='#splitIndex'>splitIndex(java.lang.String)</a> which splits the static part from the agg part.<br>

<a href="https://github.com/autoplot/dev/search?q=getFileStorageModel&unscoped_q=getFileStorageModel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isFileResource"></a>
# isFileResource
isFileResource(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isFileResource&unscoped_q=isFileResource">[search for examples]</a>

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

***
<a name="setDelegateDataSourceFactory"></a>
# setDelegateDataSourceFactory
setDelegateDataSourceFactory( org.autoplot.datasource.DataSourceFactory delegateFactory ) &rarr; void



### Parameters:
delegateFactory - a DataSourceFactory

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDelegateDataSourceFactory&unscoped_q=setDelegateDataSourceFactory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="splitIndex"></a>
# splitIndex
splitIndex( String surl ) &rarr; int

return the index of the agg part of the uri.  Like 
 FileStorageModel.splitIndex(surl), but also treats * as $x.

### Parameters:
surl - the URI as a string.

### Returns:
the index of the first part of the aggregation, which will
 be one more than the position of the static part's last slash.

<a href="https://github.com/autoplot/dev/search?q=splitIndex&unscoped_q=splitIndex">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="supportsDiscovery"></a>
# supportsDiscovery
supportsDiscovery(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=supportsDiscovery&unscoped_q=supportsDiscovery">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

