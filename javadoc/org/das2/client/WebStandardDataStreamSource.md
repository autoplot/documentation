# org.das2.client.WebStandardDataStreamSource
WebStandardDataStreamSource( org.das2.client.DasServer server, java.net.URL url )


***
<a name="authenticate"></a>
# authenticate
authenticate( String restrictedResourceLabel ) &rarr; void



### Parameters:
restrictedResourceLabel - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=authenticate&unscoped_q=authenticate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDasServer"></a>
# getDasServer
getDasServer(  ) &rarr; DasServer



### Returns:
org.das2.client.DasServer


<a href="https://github.com/autoplot/dev/search?q=getDasServer&unscoped_q=getDasServer">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDevel"></a>
# getDevel
getDevel(  ) &rarr; String

use the develop version of the reader instead of the
 production version.

### Returns:
the devel string used instead of production server.

<a href="https://github.com/autoplot/dev/search?q=getDevel&unscoped_q=getDevel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInputStream"></a>
# getInputStream
getInputStream( org.das2.client.StreamDataSetDescriptor dsd, Datum start, Datum end ) &rarr; InputStream



### Parameters:
dsd - a StreamDataSetDescriptor
<br>start - a Datum
<br>end - a Datum

### Returns:
java.io.InputStream


<a href="https://github.com/autoplot/dev/search?q=getInputStream&unscoped_q=getInputStream">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getKey"></a>
# getKey
getKey(  ) &rarr; Key

Getter for property key.

### Returns:
Value of property key.

<a href="https://github.com/autoplot/dev/search?q=getKey&unscoped_q=getKey">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLastRequestURL"></a>
# getLastRequestURL
getLastRequestURL(  ) &rarr; String

Getter for property lastRequestURL.

### Returns:
Value of property lastRequestURL.

<a href="https://github.com/autoplot/dev/search?q=getLastRequestURL&unscoped_q=getLastRequestURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getReducedInputStream"></a>
# getReducedInputStream
getReducedInputStream( org.das2.client.StreamDataSetDescriptor dsd, Datum start, Datum end, Datum timeResolution ) &rarr; InputStream



### Parameters:
dsd - a StreamDataSetDescriptor
<br>start - a Datum
<br>end - a Datum
<br>timeResolution - a Datum

### Returns:
java.io.InputStream


<a href="https://github.com/autoplot/dev/search?q=getReducedInputStream&unscoped_q=getReducedInputStream">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isCompress"></a>
# isCompress
isCompress(  ) &rarr; boolean

Getter for property compress.

### Returns:
Value of property compress.

<a href="https://github.com/autoplot/dev/search?q=isCompress&unscoped_q=isCompress">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isLegacyStream"></a>
# isLegacyStream
isLegacyStream(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isLegacyStream&unscoped_q=isLegacyStream">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isRedirect"></a>
# isRedirect
isRedirect(  ) &rarr; boolean

Getter for property redirect.

### Returns:
Value of property redirect.

<a href="https://github.com/autoplot/dev/search?q=isRedirect&unscoped_q=isRedirect">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reset"></a>
# reset
reset(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reset&unscoped_q=reset">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setCompress"></a>
# setCompress
setCompress( boolean compress ) &rarr; void

Setter for property compress.

### Parameters:
compress - New value of property compress.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCompress&unscoped_q=setCompress">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDevel"></a>
# setDevel
setDevel( String devel ) &rarr; void

use the develop version of the reader instead of the
 production version.  If a reader was in dasHome/readers,
 then use the one in /home/DEVEL/readers/ instead.

### Parameters:
devel - string identifying the developer.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDevel&unscoped_q=setDevel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLastRequestURL"></a>
# setLastRequestURL
setLastRequestURL( String url ) &rarr; void



### Parameters:
url - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLastRequestURL&unscoped_q=setLastRequestURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRedirect"></a>
# setRedirect
setRedirect( boolean redirect ) &rarr; void

Setter for property redirect.

### Parameters:
redirect - New value of property redirect.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRedirect&unscoped_q=setRedirect">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

