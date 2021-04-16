# org.das2.jythoncompletion.support.CompletionProviderThe basic interface of the code completion querying SPI. Various implementations can
 be registered per a document mime-type.
***
<a name="COMPLETION_QUERY_TYPE"></a>
# COMPLETION_QUERY_TYPE

The <code>int</code> value representing the query for a code completion.

***
<a name="DOCUMENTATION_QUERY_TYPE"></a>
# DOCUMENTATION_QUERY_TYPE

The <code>int</code> value representing the query for a documentation.

***
<a name="TOOLTIP_QUERY_TYPE"></a>
# TOOLTIP_QUERY_TYPE

The <code>int</code> value representing the query for a tooltip hint.

***
<a name="COMPLETION_ALL_QUERY_TYPE"></a>
# COMPLETION_ALL_QUERY_TYPE

The <code>int</code> value representing the query for an all code completion.

***
<a name="createTask"></a>
# createTask
createTask( int queryType, javax.swing.text.JTextComponent component ) &rarr; CompletionTask

Creates a task that performs a query of the given type on the given component.
 <br>
 This method is invoked in AWT thread only and the returned task
 may either be synchronous (if it's not complex)
 or it may be asynchonous
 (see {@link org.netbeans.spi.editor.completion.support.AsyncCompletionTask}).
 <br>
 The task usually inspects the component's document, the
 text up to the caret position and returns the appropriate result.

### Parameters:
queryType - a type ot the query. It can be one of the {@link #COMPLETION_QUERY_TYPE},
  {@link #COMPLETION_ALL_QUERY_TYPE}, {@link #DOCUMENTATION_QUERY_TYPE},
  or {@link #TOOLTIP_QUERY_TYPE} (but not their combination).
<br>component - a component on which the query is performed

### Returns:
a task performing the query.

<a href="https://github.com/autoplot/dev/search?q=createTask&unscoped_q=createTask">[search for examples]</a>

***
<a name="getAutoQueryTypes"></a>
# getAutoQueryTypes
getAutoQueryTypes( javax.swing.text.JTextComponent component, String typedText ) &rarr; int

Called by the code completion infrastructure to check whether a text just typed
 into a text component triggers an automatic query invocation.
 <br>
 If the particular query type is returned the infrastructure
 will then call {@link #createTask(int, JTextComponent)}.

### Parameters:
component - a component in which typing appeared
<br>typedText - a typed text

### Returns:
a combination of the {@link #COMPLETION_QUERY_TYPE}, {@link #COMPLETION_ALL_QUERY_TYPE},
         {@link #DOCUMENTATION_QUERY_TYPE}, and {@link #TOOLTIP_QUERY_TYPE}
         values, or zero if no query should be automatically invoked.

<a href="https://github.com/autoplot/dev/search?q=getAutoQueryTypes&unscoped_q=getAutoQueryTypes">[search for examples]</a>

