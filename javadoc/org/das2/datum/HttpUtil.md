# org.das2.datum.HttpUtilUtilities for HTTP protocol, such handling redirects.
 This was needed to support Orbits.
HttpUtil( )


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


<a href="https://github.com/autoplot/dev/search?q=consumeStream&unscoped_q=consumeStream">[search for examples]</a>

