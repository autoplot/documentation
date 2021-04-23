# org.das2.jythoncompletion.support.AsyncCompletionQuery

Defines query processing of an asynchronous completion task.
 <br>
 The {@link #query(CompletionResultSet, Document, int)} abstract method
 needs to be implemented to define the asynchronous querying behavior.
 <br>
 In addition filtering of the result set computed during querying
 can be implemented by overriding the
 {@link #canFilter(JTextComponent)} and {@link #filter(CompletionResultSet)}.

# AsyncCompletionQuery( )


***
<a name="isTaskCancelled"></a>
# isTaskCancelled
isTaskCancelled(  ) &rarr; boolean

Check whether the task corresponding to this query was cancelled.
 <br>
 Subclasses should check this flag and stop the query computation.

### Returns:
true if the task was cancelled or false if not.

<a href="https://github.com/autoplot/dev/search?q=isTaskCancelled&unscoped_q=isTaskCancelled">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

