# org.autoplot.datasource.AbstractDataSourceFormat

provides getParam to extensions and the file part.

***
<a name="getBooleanParam"></a>
# getBooleanParam
getBooleanParam( String name, boolean deflt ) &rarr; boolean

return the boolean parameter.  Note setUri must be called with
 the input URI.

### Parameters:
name - the parameter name.
<br>deflt - the default value should the parameter be missing or misformed.

### Returns:
the value

<a href="https://github.com/autoplot/dev/search?q=getBooleanParam&unscoped_q=getBooleanParam">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getParam"></a>
# getParam
getParam( String name, String deflt ) &rarr; String

return the string parameter.  Note setUri must be called with
 the input URI.

### Parameters:
name - the parameter name.
<br>deflt - the default value should the parameter be missing.

### Returns:
the value

<a href="https://github.com/autoplot/dev/search?q=getParam&unscoped_q=getParam">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getResourceURI"></a>
# getResourceURI
getResourceURI(  ) &rarr; URI

return the URI (file part) of the

### Returns:
a java.net.URI


<a href="https://github.com/autoplot/dev/search?q=getResourceURI&unscoped_q=getResourceURI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="maybeMkdirs"></a>
# maybeMkdirs
maybeMkdirs(  ) &rarr; void

If necessary attempt to create the folder which will contain the file, and
 throw an IOException if the folder cannot be created or written to.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=maybeMkdirs&unscoped_q=maybeMkdirs">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="streamData"></a>
# streamData
streamData( java.util.Map params, java.util.Iterator data, java.io.OutputStream out ) &rarr; boolean

return true if the format also supports streaming where each record is
 formatted (roughly) as it is received, and there is a bound on the total 
 size needed for any request.

### Parameters:
params - a java.util.Map
<br>data - a java.util.Iterator
<br>out - an OutputStream

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=streamData&unscoped_q=streamData">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

