# org.das2.util.filesystem.HttpUtil

Utilities for HTTP protocol, such as a cache for the HEAD metadata.

# HttpUtil( )


***
<a name="checkRedirect"></a>
# checkRedirect
checkRedirect( java.net.URLConnection urlConnection ) &rarr; URLConnection

check for 301, 302 or 303 redirects, and return a new connection in this case.
 This should be called immediately before the urlConnection.connect call,
 as this must connect to get the response code.

### Parameters:
urlConnection - if an HttpUrlConnection, check for 301 or 302; return connection otherwise.

### Returns:
a connection, typically the same one as passed in.

<a href="https://github.com/autoplot/dev/search?q=checkRedirect&unscoped_q=checkRedirect">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="consumeStream"></a>
# consumeStream
consumeStream( java.io.InputStream err ) &rarr; void

nice clients consume both the stderr and stdout coming from websites.
 This reads everything off of the stream and closes it.
 http://docs.oracle.com/javase/1.5.0/docs/guide/net/http-keepalive.html 
 suggests that you "do not abandon connection"

### Parameters:
err - the input stream

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=consumeStream&unscoped_q=consumeStream">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="copyConnectProperties"></a>
# copyConnectProperties
copyConnectProperties( java.net.HttpURLConnection urlc, java.net.HttpURLConnection newConnection ) &rarr; void

copy over connection properties like Cookie and Accept-Encoding.

### Parameters:
urlc - a HttpURLConnection
<br>newConnection - a HttpURLConnection

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=copyConnectProperties&unscoped_q=copyConnectProperties">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMetadata"></a>
# getMetadata
getMetadata( java.net.URL url, java.util.Map props ) &rarr; Map

return the metadata about a URL.  This will support http, https,
 and ftp, and will check for redirects.  This will
 allow caching of head requests.

### Parameters:
url - ftp,https, or http URL
<br>props - if non-null, may be a map containing cookie.

### Returns:
the metadata
### See Also:
<a href='WebProtocol.md#META_EXIST'>WebProtocol#META_EXIST</a> <br>
<a href='WebProtocol.md#HTTP_RESPONSE_CODE'>WebProtocol#HTTP_RESPONSE_CODE</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getMetadata&unscoped_q=getMetadata">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

