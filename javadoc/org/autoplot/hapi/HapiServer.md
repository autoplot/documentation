# org.autoplot.hapi.HapiServer

Utility methods for interacting with HAPI servers.

# HapiServer( )


***
<a name="UTF8"></a>
# UTF8

all transactions must be done in UTF-8

***
<a name="createURL"></a>
# createURL
createURL( java.net.URL server, String append ) &rarr; URL

return the URL by appending the text to the end of the server URL.  This
 avoids extra slashes, etc.

### Parameters:
server - an URL
<br>append - a String

### Returns:
a java.net.URL


<a href="https://github.com/autoplot/dev/search?q=createURL&unscoped_q=createURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

createURL( java.net.URL server, String append, java.util.Map singletonMap ) &rarr; URL<br>
***
<a name="getCatalog"></a>
# getCatalog
getCatalog( java.net.URL server ) &rarr; JSONArray

return the list of datasets available at the server.  
 This should not be called from the event thread.

### Parameters:
server - the root of the server, which should should contain "catalog"

### Returns:
list of catalog entries, which have "id" and "title" tags.

<a href="https://github.com/autoplot/dev/search?q=getCatalog&unscoped_q=getCatalog">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCatalogIds"></a>
# getCatalogIds
getCatalogIds( java.net.URL server ) &rarr; List

return the list of datasets available at the server.
 This should not be called from the event thread.

### Parameters:
server - the root of the server, which should should contain "catalog"

### Returns:
list of dataset ids

<a href="https://github.com/autoplot/dev/search?q=getCatalogIds&unscoped_q=getCatalogIds">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataURL"></a>
# getDataURL
getDataURL( java.net.URL server, String id, DatumRange tr, String parameters ) &rarr; URL

return the URL for data requests.

### Parameters:
server - an URL
<br>id - string like "data4" or "spase://..."
<br>tr - the time range
<br>parameters - zero-length, or a comma-delineated list of parameters.

### Returns:
the request, with the ID and parameters URL encoded.

<a href="https://github.com/autoplot/dev/search?q=getDataURL&unscoped_q=getDataURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInfo"></a>
# getInfo
getInfo( java.net.URL server, String id ) &rarr; JSONObject

return the info as a JSONObject.
 This should not be called from the event thread.

### Parameters:
server - HAPI server.
<br>id - the parameter id.

### Returns:
JSONObject containing information.

<a href="https://github.com/autoplot/dev/search?q=getInfo&unscoped_q=getInfo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInfoURL"></a>
# getInfoURL
getInfoURL( java.net.URL server, String id ) &rarr; URL

return the URL for getting info.

### Parameters:
server - an URL
<br>id - a String

### Returns:
a java.net.URL


<a href="https://github.com/autoplot/dev/search?q=getInfoURL&unscoped_q=getInfoURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getKnownServers"></a>
# getKnownServers
getKnownServers(  ) &rarr; List

get known servers.

### Returns:
known servers

<a href="https://github.com/autoplot/dev/search?q=getKnownServers&unscoped_q=getKnownServers">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getKnownServersArray"></a>
# getKnownServersArray
getKnownServersArray(  ) &rarr; String

get known servers

### Returns:
known servers

<a href="https://github.com/autoplot/dev/search?q=getKnownServersArray&unscoped_q=getKnownServersArray">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getParameters"></a>
# getParameters
getParameters( java.net.URL server, String id ) &rarr; JSONArray



### Parameters:
server - an URL
<br>id - a String

### Returns:
JSONArray


<a href="https://github.com/autoplot/dev/search?q=getParameters&unscoped_q=getParameters">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRange"></a>
# getRange
getRange( JSONObject info ) &rarr; DatumRange

return the range of available data. For example, Polar/Hydra data is available
 from 1996-03-20 to 2008-04-15.  Note this supports old schemas.

### Parameters:
info - a JSONObject

### Returns:
the range of available data.

<a href="https://github.com/autoplot/dev/search?q=getRange&unscoped_q=getRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSampleTimeRange"></a>
# getSampleTimeRange
getSampleTimeRange( JSONObject info ) &rarr; DatumRange

return a time which is a suitable time to discover the data.

### Parameters:
info - a JSONObject

### Returns:
a DatumRange


<a href="https://github.com/autoplot/dev/search?q=getSampleTimeRange&unscoped_q=getSampleTimeRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="listHapiServers"></a>
# listHapiServers
listHapiServers(  ) &rarr; List

add the default known servers, plus the ones we know about.  
 The zeroth server will be the last server used.
 This should not be called from the event thread.

### Returns:
list of server URLs.

<a href="https://github.com/autoplot/dev/search?q=listHapiServers&unscoped_q=listHapiServers">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="listHapiServersArray"></a>
# listHapiServersArray
listHapiServersArray(  ) &rarr; String

add the default known servers, plus the ones we know about.

### Returns:
list of servers

<a href="https://github.com/autoplot/dev/search?q=listHapiServersArray&unscoped_q=listHapiServersArray">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readFromCachedURL"></a>
# readFromCachedURL
readFromCachedURL( java.net.URL url, String type ) &rarr; String

return the resource, if cached, or null if the data is not cached.

### Parameters:
url - an URL
<br>type - "json" (the extension) or "" for no additional extension.

### Returns:
the data or null.

<a href="https://github.com/autoplot/dev/search?q=readFromCachedURL&unscoped_q=readFromCachedURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readFromFile"></a>
# readFromFile
readFromFile( java.io.File f ) &rarr; String

read the file into a string.

### Parameters:
f - non-empty file

### Returns:
String containing file contents.

<a href="https://github.com/autoplot/dev/search?q=readFromFile&unscoped_q=readFromFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readFromURL"></a>
# readFromURL
readFromURL( java.net.URL url, String type ) &rarr; String

read data from the URL.

### Parameters:
url - the URL to read from
<br>type - the extension to use for the cache file (JSON).

### Returns:
non-empty string

<a href="https://github.com/autoplot/dev/search?q=readFromURL&unscoped_q=readFromURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="urlEncode"></a>
# urlEncode
urlEncode( String id ) &rarr; String

make sure spaces are encoded.

### Parameters:
id - a String

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=urlEncode&unscoped_q=urlEncode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="writeToCachedURL"></a>
# writeToCachedURL
writeToCachedURL( java.net.URL url, String type, String data ) &rarr; void

write the data (for example, an info response) to a cache file.  This is called
 from readFromURL to cache the data.

### Parameters:
url - the resource location, query param id is handled specially, but others are ignored.
<br>type - "json" (the extension), or "" if no extension should be added.
<br>data - the data.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeToCachedURL&unscoped_q=writeToCachedURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

