# org.das2.jythoncompletion.JythonCompletionTask

Completions for Jython code.  The completion task is created with the
 editor configured for completions (code and caret position within code),
 and "query" is called which will fill a CompletionResultSet.

# JythonCompletionTask( javax.swing.text.JTextComponent t )
create the completion task on the text component, using its content and caret position.

***
<a name="CLIENT_PROPERTY_INTERPRETER_PROVIDER"></a>
# CLIENT_PROPERTY_INTERPRETER_PROVIDER



***
<a name="__CLASSTYPE"></a>
# __CLASSTYPE



***
<a name="cancel"></a>
# cancel
cancel(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=cancel&unscoped_q=cancel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="doQuery"></a>
# doQuery
doQuery( org.das2.jythoncompletion.CompletionContext cc, org.das2.jythoncompletion.support.CompletionResultSet resultSet ) &rarr; int

perform the completions query.  This is the heart of Jython completions.

### Parameters:
cc - a CompletionContext
<br>resultSet - a CompletionResultSet

### Returns:
the count

<a href="https://github.com/autoplot/dev/search?q=doQuery&unscoped_q=doQuery">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="escapeHtml"></a>
# escapeHtml
escapeHtml( String s ) &rarr; String



### Parameters:
s - a String

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=escapeHtml&unscoped_q=escapeHtml">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getIconFor"></a>
# getIconFor
getIconFor( Object jm ) &rarr; ImageIcon

return an identifying icon for the object, or null.

### Parameters:
jm - java.lang.reflect.Method, or PyInteger, etc.

### Returns:
the icon or null.

<a href="https://github.com/autoplot/dev/search?q=getIconFor&unscoped_q=getIconFor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getImportableCompletions"></a>
# getImportableCompletions
getImportableCompletions( String source, org.das2.jythoncompletion.CompletionContext cc, org.das2.jythoncompletion.support.CompletionResultSet result ) &rarr; int

get completions by looking at importLookup.jy, which is a list of commonly imported codes.

### Parameters:
source - the script source.
<br>cc - a CompletionContext
<br>result - a CompletionResultSet

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=getImportableCompletions&unscoped_q=getImportableCompletions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLastLine"></a>
# getLastLine
getLastLine( String script ) &rarr; String



### Parameters:
script - a String

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getLastLine&unscoped_q=getLastLine">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLocalsCompletions"></a>
# getLocalsCompletions
getLocalsCompletions( PythonInterpreter interp, org.das2.jythoncompletion.CompletionContext cc, org.das2.jythoncompletion.support.CompletionResultSet rs ) &rarr; int



### Parameters:
interp - a PythonInterpreter
<br>cc - a CompletionContext
<br>rs - a CompletionResultSet

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getLocalsCompletions&unscoped_q=getLocalsCompletions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getLocalsCompletions( PythonInterpreter interp, org.das2.jythoncompletion.CompletionContext cc ) &rarr; List<br>
***
<a name="keySort"></a>
# keySort
keySort( java.util.List key, java.util.List[] lists ) &rarr; void

sorts all the lists by the first list.  
 See http://stackoverflow.com/questions/15400514/syncronized-sorting-between-two-arraylists/24688828#24688828
 Note the key list must be repeated for it to be sorted as well!

### Parameters:
key - the list used to sort
<br>lists - the lists to be sorted, often containing the key as well.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=keySort&unscoped_q=keySort">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="query"></a>
# query
query( org.das2.jythoncompletion.support.CompletionResultSet arg0 ) &rarr; void



### Parameters:
arg0 - a CompletionResultSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=query&unscoped_q=query">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reduceObject"></a>
# reduceObject
reduceObject( java.util.List signatures, java.util.List labels, java.util.List argss ) &rarr; void



### Parameters:
signatures - a java.util.List
<br>labels - a java.util.List
<br>argss - a java.util.List

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reduceObject&unscoped_q=reduceObject">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="refresh"></a>
# refresh
refresh( org.das2.jythoncompletion.support.CompletionResultSet arg0 ) &rarr; void



### Parameters:
arg0 - a CompletionResultSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=refresh&unscoped_q=refresh">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="trimLinesToMakeValid"></a>
# trimLinesToMakeValid
trimLinesToMakeValid( String script ) &rarr; String

introduced to see if we can pop a little code from the end, in case we
 are within a triple-quoted string.

### Parameters:
script - the script

### Returns:
the script, possibly with a few fewer lines.
### See Also:
<a href='SimplifyScriptSupport.md#alligatorParse'>SimplifyScriptSupport#alligatorParse(java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=trimLinesToMakeValid&unscoped_q=trimLinesToMakeValid">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

