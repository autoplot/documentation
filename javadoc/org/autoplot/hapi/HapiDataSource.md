# org.autoplot.hapi.HapiDataSource

HAPI data source uses transactions with HAPI servers to collect data.

# HapiDataSource( java.net.URI uri )


***
<a name="FILL_VALUE"></a>
# FILL_VALUE



***
<a name="cacheFolder"></a>
# cacheFolder
cacheFolder( java.net.URL url, String id ) &rarr; File

return the folder containing data for this id.

### Parameters:
url - the hapi URL, such as http://jfaden.net/HapiServerDemo/hapi
<br>id - the ID, such as "Iowa City Conditions"

### Returns:
the folder containing the cache.

<a href="https://github.com/autoplot/dev/search?q=cacheFolder&unscoped_q=cacheFolder">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSet"></a>
# getDataSet
getDataSet( ProgressMonitor monitor ) &rarr; QDataSet



### Parameters:
monitor - a ProgressMonitor

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSetViaBinary"></a>
# getDataSetViaBinary
getDataSetViaBinary( int totalFields, ProgressMonitor monitor, java.net.URL url, org.autoplot.hapi.HapiDataSource.ParamDescription[] pds, DatumRange tr, int nparam, int[] nfields, String useCacheUriParam ) &rarr; QDataSet

read the interval using binary.

### Parameters:
totalFields - an int
<br>monitor - a ProgressMonitor
<br>url - an URL
<br>pds - an org.autoplot.hapi.HapiDataSource.ParamDescription[]
<br>tr - a DatumRange
<br>nparam - an int
<br>nfields - an int[]
<br>useCacheUriParam - a String

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=getDataSetViaBinary&unscoped_q=getDataSetViaBinary">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSetViaCsv"></a>
# getDataSetViaCsv
getDataSetViaCsv( int totalFields, ProgressMonitor monitor, java.net.URL url, org.autoplot.hapi.HapiDataSource.ParamDescription[] pds, DatumRange tr, int nparam, int[] nfields, String useCacheUriParam ) &rarr; QDataSet

read the interval using CSV.

### Parameters:
totalFields - an int
<br>monitor - a ProgressMonitor
<br>url - an URL
<br>pds - an org.autoplot.hapi.HapiDataSource.ParamDescription[]
<br>tr - a DatumRange
<br>nparam - an int
<br>nfields - an int[]
<br>useCacheUriParam - a String

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=getDataSetViaCsv&unscoped_q=getDataSetViaCsv">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getHapiCache"></a>
# getHapiCache
getHapiCache(  ) &rarr; String

return the local folder of the cache for HAPI data.  This will end with
 a slash.

### Returns:
the local folder of the cache for HAPI data.

<a href="https://github.com/autoplot/dev/search?q=getHapiCache&unscoped_q=getHapiCache">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getParameterDescriptions"></a>
# getParameterDescriptions
getParameterDescriptions( JSONObject doc ) &rarr; ParamDescription



### Parameters:
doc - a JSONObject

### Returns:
org.autoplot.hapi.HapiDataSource.ParamDescription[]


<a href="https://github.com/autoplot/dev/search?q=getParameterDescriptions&unscoped_q=getParameterDescriptions">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="printCacheStats"></a>
# printCacheStats
printCacheStats(  ) &rarr; void

print the cache stats.

### Returns:
void (returns nothing)

### See Also:
<a href='https://sourceforge.net/p/autoplot/bugs/1996/'>https://sourceforge.net/p/autoplot/bugs/1996/</a> <br>

<a href="https://github.com/autoplot/dev/search?q=printCacheStats&unscoped_q=printCacheStats">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

