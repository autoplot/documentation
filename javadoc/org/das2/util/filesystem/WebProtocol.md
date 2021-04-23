# org.das2.util.filesystem.WebProtocol

template for web-based protocols to implement FileSystems

***
<a name="META_EXIST"></a>
# META_EXIST



***
<a name="META_COOKIE"></a>
# META_COOKIE



***
<a name="META_LAST_MODIFIED"></a>
# META_LAST_MODIFIED



***
<a name="META_CONTENT_LENGTH"></a>
# META_CONTENT_LENGTH



***
<a name="META_CONTENT_TYPE"></a>
# META_CONTENT_TYPE



***
<a name="META_ETAG"></a>
# META_ETAG



***
<a name="HTTP_RESPONSE_CODE"></a>
# HTTP_RESPONSE_CODE

kludge in place where the response code (200,302,401,etc) can be stored.

***
<a name="getInputStream"></a>
# getInputStream
getInputStream( org.das2.util.filesystem.WebFileObject fo, ProgressMonitor mon ) &rarr; InputStream

get an inputStream for the resource.  The client using the stream must make sure the stream is closed.

### Parameters:
fo - the resource
<br>mon - monitor for the stream.

### Returns:
the stream

<a href="https://github.com/autoplot/dev/search?q=getInputStream&unscoped_q=getInputStream">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMetadata"></a>
# getMetadata
getMetadata( org.das2.util.filesystem.WebFileObject fo ) &rarr; Map

return metadata for the resource.  This should include:
 <ul>
 <li>WebProtocol.META_EXIST, "true" or "false"
 <li>WebProtocol.META_LAST_MODIFIED, String.valueOf( fo.localFile.lastModified() )
 <li>WebProtocol.META_CONTENT_LENGTH, String.valueOf( fo.localFile.length() )
 <li>WebProtocol.META_CONTENT_TYPE, Files.probeContentType( fo.localFile.toPath() ) )
 </ul>

### Parameters:
fo - the resource

### Returns:
a java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getMetadata&unscoped_q=getMetadata">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

