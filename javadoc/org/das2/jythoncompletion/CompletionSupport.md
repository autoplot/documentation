# org.das2.jythoncompletion.CompletionSupport

support functions for Jython editor completions.

***
<a name="checkJavaSubClass"></a>
# checkJavaSubClass
checkJavaSubClass( javax.swing.text.JTextComponent editor ) &rarr; CompletionContext

is the carot within a subclass of an identifiable Java class?
 TODO: this is a proof-of-concept kludge right now, where it just looks for g.*

### Parameters:
editor - a JTextComponent

### Returns:
null or the CompletionContext for this.

<a href="https://github.com/autoplot/dev/search?q=checkJavaSubClass&unscoped_q=checkJavaSubClass">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCompletionContext"></a>
# getCompletionContext
getCompletionContext( javax.swing.text.JTextComponent editor ) &rarr; CompletionContext

get the completion context for the editor at the carot position.

### Parameters:
editor - the editor component containing the script and the carot position.

### Returns:
the completion context

<a href="https://github.com/autoplot/dev/search?q=getCompletionContext&unscoped_q=getCompletionContext">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getCompletionContext( String line, int pos, int i0, int i1, int i2 ) &rarr; CompletionContext<br>
