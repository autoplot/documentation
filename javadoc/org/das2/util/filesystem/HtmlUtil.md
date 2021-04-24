# org.das2.util.filesystem.HtmlUtil

HTML utilities, such as getting a directory listing, where a "file" is a link
 below the directory we are listing, and read a URL into a String.

# HtmlUtil( )


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
### See Also:
<a href='HttpUtil.md#checkRedirect'>HttpUtil#checkRedirect(java.net.URLConnection)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=checkRedirect&unscoped_q=checkRedirect">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="consumeStream"></a>
# consumeStream
consumeStream( java.io.InputStream err ) &rarr; void

nice clients consume both the stderr and stdout coming from websites.
 This reads everything off of the stream and closes it.
 http://docs.oracle.com/javase/1.5.0/docs/guide/net/http-keepalive.html suggests that you "do not abandon connection"

### Parameters:
err - the input stream

### Returns:
void (returns nothing)

### See Also:
<a href='HttpUtil.md#consumeStream'>HttpUtil#consumeStream(java.io.InputStream)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=consumeStream&unscoped_q=consumeStream">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDirectoryListing"></a>
# getDirectoryListing
getDirectoryListing( java.net.URL url, java.io.InputStream urlStream ) &rarr; URL

Get the listing of the web directory, returning links that are "under" the given URL.
 Note this does not handle off-line modes where we need to log into
 a website first, as is often the case for a hotel.

 This was refactored to support caching of listings by simply writing the content to disk.

### Parameters:
url - the address.
<br>urlStream - stream containing the URL content, which must be UTF-8 (or US-ASCII)

### Returns:
list of URIs referred to in the page.

<a href="https://github.com/autoplot/dev/search?q=getDirectoryListing&unscoped_q=getDirectoryListing">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getDirectoryListing( java.net.URL url, java.io.InputStream urlStream, boolean childCheck ) &rarr; URL<br>
getDirectoryListing( java.net.URL url ) &rarr; URL<br>
***
<a name="getInputStream"></a>
# getInputStream
getInputStream( java.net.URL url ) &rarr; InputStream

get the inputStream, following redirects if a 301 or 302 is encountered.  
 The scientist may be prompted for a password, but only if "user@" is
 in the URL.
 
 Note this does not explicitly close the connections
 to the server, and Java may not know to release the resources.  
 TODO: fix this by wrapping the input stream and closing the connection
 when the stream is closed.  This was done in Autoplot's DataSetURI.downloadResourceAsTempFile

### Parameters:
url - an URL

### Returns:
input stream
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/autoplot/datasource/DataSetURI.md#downloadResourceAsTempFile'>org.autoplot.datasource.DataSetURI#downloadResourceAsTempFile</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getInputStream&unscoped_q=getInputStream">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLinks"></a>
# getLinks
getLinks( java.net.URL url, String content ) &rarr; List

return the links found in the content, using url as the context.

### Parameters:
url - null or the url for the context.
<br>content - the html content.

### Returns:
a list of URLs.

<a href="https://github.com/autoplot/dev/search?q=getLinks&unscoped_q=getLinks">[search for examples]</a>
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
<br>props - a java.util.Map

### Returns:
the metadata
### See Also:
<a href='HttpUtil.md#getMetadata'>HttpUtil#getMetadata(java.net.URL, java.util.Map)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getMetadata&unscoped_q=getMetadata">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDirectory"></a>
# isDirectory
isDirectory( java.net.URL url ) &rarr; boolean



### Parameters:
url - an URL

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isDirectory&unscoped_q=isDirectory">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readToString"></a>
# readToString
readToString( java.net.URL url ) &rarr; String

read the contents of the URL into a string, assuming UTF-8 encoding.

### Parameters:
url - an URL

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=readToString&unscoped_q=readToString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

