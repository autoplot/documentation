# org.das2.qstream.StreamCommentStreamComment allows comments to be put onto the stream.
 TODO: consider that comments should be sourced by the stream producer, but what about comments from filters?
   That is, if I'm a filter and I produce comments, should I throw out the comments I receive?
StreamComment( String type, String message )


***
<a name="TYPE_TASK_PROGRESS"></a>
# TYPE_TASK_PROGRESS

task progress comments are either of the form:
 
 <pre>
 {@code
   [xx]000000<comment type='taskProgress' message='0 of 100'>   or
   [xx]000000<comment type='taskProgress' message='0 of -1'> for indeterminate
 }
 </pre>

 These are currently unimplemented!

***
<a name="TYPE_LOG"></a>
# TYPE_LOG

log comments are of the form:
 <pre>
 {@code
   [xx]000000<comment type='log:FINE' message='calc fine process'>   or
   [xx]000000<comment type='log:INFO' message='reading calibration'>
 }
 </pre>
 
 Note the log level should be requested by the client.

***
<a name="getDomElement"></a>
# getDomElement
getDomElement(  ) &rarr; Element



### Returns:
org.w3c.dom.Element


<a href="https://github.com/autoplot/dev/search?q=getDomElement&unscoped_q=getDomElement">[search for examples]</a>

***
<a name="setMessage"></a>
# setMessage
setMessage( String message ) &rarr; void



### Parameters:
message - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMessage&unscoped_q=setMessage">[search for examples]</a>

***
<a name="setType"></a>
# setType
setType( String type ) &rarr; void



### Parameters:
type - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setType&unscoped_q=setType">[search for examples]</a>

