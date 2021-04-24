# org.das2.jythoncompletion.support.AsyncCompletionTask

Asynchronous completion task allowing asynchronous query execution
 through {@link AsyncCompletionQuery}.
 <br>
 This is a final class and all the logic must be defined
 in an implementation of {@link AsyncCompletionQuery} that must
 be passed to constructor of this task.

# AsyncCompletionTask( org.das2.jythoncompletion.support.AsyncCompletionQuery query, javax.swing.text.JTextComponent component )
Construct asynchronous task for the given component.

# AsyncCompletionTask( org.das2.jythoncompletion.support.AsyncCompletionQuery query )
Constructor for the case when there is no valid component
 which can happen when creating task for documentation or tooltip computation.

***
<a name="cancel"></a>
# cancel
cancel(  ) &rarr; void

Called by completion infrastructure to cancel the running task.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=cancel&unscoped_q=cancel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="query"></a>
# query
query( org.das2.jythoncompletion.support.CompletionResultSet resultSet ) &rarr; void

Called by completion infrastructure in AWT thread to populate
 the given result set with data.

### Parameters:
resultSet - a CompletionResultSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=query&unscoped_q=query">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="refresh"></a>
# refresh
refresh( org.das2.jythoncompletion.support.CompletionResultSet resultSet ) &rarr; void

Called by completion infrastructure in AWT thread once there
 is a change in the component (caret position changes or document
 gets modified).
 <br>
 The results should be fired into the newly provided completion listener.

### Parameters:
resultSet - a CompletionResultSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=refresh&unscoped_q=refresh">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="run"></a>
# run
run(  ) &rarr; void

This method will be run() from the RequestProcessor during
 performing of the query.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=run&unscoped_q=run">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

