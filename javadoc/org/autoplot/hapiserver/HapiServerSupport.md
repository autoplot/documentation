# org.autoplot.hapiserver.HapiServerSupport
HapiServerSupport( )


***
<a name="getCatalog"></a>
# getCatalog
getCatalog(  ) &rarr; JSONArray



### Returns:
JSONArray


<a href="https://github.com/autoplot/dev/search?q=getCatalog&unscoped_q=getCatalog">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCatalogIds"></a>
# getCatalogIds
getCatalogIds(  ) &rarr; List

return the list of datasets available at the server

### Returns:
list of dataset ids

<a href="https://github.com/autoplot/dev/search?q=getCatalogIds&unscoped_q=getCatalogIds">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getExampleRange"></a>
# getExampleRange
getExampleRange( JSONObject info ) &rarr; DatumRange



### Parameters:
info - a JSONObject

### Returns:
org.das2.datum.DatumRange


<a href="https://github.com/autoplot/dev/search?q=getExampleRange&unscoped_q=getExampleRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRange"></a>
# getRange
getRange( JSONObject info ) &rarr; DatumRange

return the range of available data. For example, Polar/Hydra data is available
 from 1996-03-20 to 2008-04-15.

### Parameters:
info - a JSONObject

### Returns:
the range of available data, or null if it is not available.

<a href="https://github.com/autoplot/dev/search?q=getRange&unscoped_q=getRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readJSON"></a>
# readJSON
readJSON( java.io.File jsonFile ) &rarr; JSONObject

read the JSONObject from the file.

### Parameters:
jsonFile - file containing JSONObject.

### Returns:
the JSONObject

<a href="https://github.com/autoplot/dev/search?q=readJSON&unscoped_q=readJSON">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

