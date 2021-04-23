# org.autoplot.scriptconsole.ScriptPanelSupportError annotations, saveAs, etc.
***
<a name="PROP_INTERRUPTABLE"></a>
# PROP_INTERRUPTABLE



***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addPropertyChangeListener( String name, java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="annotateError"></a>
# annotateError
annotateError( java.lang.Throwable ex ) &rarr; void

march through the stack trace looking for any Jython references.

### Parameters:
ex - the exception

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=annotateError&unscoped_q=annotateError">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

annotateError( PyException ex, int offset, PythonInterpreter interp ) &rarr; void<br>
***
<a name="getInterruptible"></a>
# getInterruptible
getInterruptible(  ) &rarr; InteractiveInterpreter

return the interruptible InteractiveInterpreter that runs the script.

### Returns:
the interruptible

<a href="https://github.com/autoplot/dev/search?q=getInterruptible&unscoped_q=getInterruptible">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSaveFile"></a>
# getSaveFile
getSaveFile(  ) &rarr; int

get the save file name with a save file dialog.

### Returns:
response code, such as JFileChooser.APPROVE_OPTION or JFileChooser.CANCEL_OPTION
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/javax/swing/JFileChooser.md#showSaveDialog'>javax.swing.JFileChooser#showSaveDialog(java.awt.Component)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getSaveFile&unscoped_q=getSaveFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

removePropertyChangeListener( String name, java.beans.PropertyChangeListener listener ) &rarr; void<br>
