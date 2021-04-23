# org.autoplot.server.RequestHandlerHandles requests coming in from the server.
 TODO: check against --script option in Autoplot.  JythonMain had a problem with imports.
RequestHandler( )


***
<a name="handleRequest"></a>
# handleRequest
handleRequest( java.io.InputStream in, org.autoplot.ApplicationModel model, java.io.OutputStream out, org.autoplot.server.RequestListener rlistener ) &rarr; String

process the python code in data.  
 return null or in the future the data to send back.

### Parameters:
in - an InputStream
<br>model - an ApplicationModel
<br>out - an OutputStream
<br>rlistener - the

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=handleRequest&unscoped_q=handleRequest">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

