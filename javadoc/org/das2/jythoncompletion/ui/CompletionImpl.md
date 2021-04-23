# org.das2.jythoncompletion.ui.CompletionImplImplementation of the completion processing.
 The visual related processing is done in AWT thread together
 with completion providers invocation and result set sorting.
 <br>
 The only thing that can be done outside of the AWT
 is hiding of the completion/documentation/tooltip.

 <p>
 The completion providers typically reschedule computation intensive
 collecting of their result set into an extra thread to keep the GUI responsive.
***
<a name="caretUpdate"></a>
# caretUpdate
caretUpdate( javax.swing.event.CaretEvent e ) &rarr; void



### Parameters:
e - a CaretEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=caretUpdate&unscoped_q=caretUpdate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="changedUpdate"></a>
# changedUpdate
changedUpdate( javax.swing.event.DocumentEvent e ) &rarr; void



### Parameters:
e - a DocumentEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=changedUpdate&unscoped_q=changedUpdate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createTestResultSet"></a>
# createTestResultSet
createTestResultSet( org.das2.jythoncompletion.support.CompletionTask task, int queryType ) &rarr; CompletionResultSetImpl



### Parameters:
task - a CompletionTask
<br>queryType - an int

### Returns:
org.das2.jythoncompletion.ui.CompletionResultSetImpl


<a href="https://github.com/autoplot/dev/search?q=createTestResultSet&unscoped_q=createTestResultSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="focusGained"></a>
# focusGained
focusGained( java.awt.event.FocusEvent e ) &rarr; void



### Parameters:
e - a FocusEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=focusGained&unscoped_q=focusGained">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="focusLost"></a>
# focusLost
focusLost( java.awt.event.FocusEvent e ) &rarr; void



### Parameters:
e - a FocusEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=focusLost&unscoped_q=focusLost">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="get"></a>
# get
get(  ) &rarr; CompletionImpl



### Returns:
org.das2.jythoncompletion.ui.CompletionImpl


<a href="https://github.com/autoplot/dev/search?q=get&unscoped_q=get">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hideAll"></a>
# hideAll
hideAll(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=hideAll&unscoped_q=hideAll">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hideCompletion"></a>
# hideCompletion
hideCompletion(  ) &rarr; boolean

May be called from any thread. The UI changes will be rescheduled into AWT.

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=hideCompletion&unscoped_q=hideCompletion">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

hideCompletion( boolean completionOnly ) &rarr; boolean<br>
***
<a name="hideDocumentation"></a>
# hideDocumentation
hideDocumentation(  ) &rarr; boolean

May be called from any thread. The UI changes will be rescheduled into AWT.

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=hideDocumentation&unscoped_q=hideDocumentation">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hideToolTip"></a>
# hideToolTip
hideToolTip(  ) &rarr; boolean

May be called from any thread. The UI changes will be rescheduled into AWT.

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=hideToolTip&unscoped_q=hideToolTip">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="insertUpdate"></a>
# insertUpdate
insertUpdate( javax.swing.event.DocumentEvent e ) &rarr; void



### Parameters:
e - a DocumentEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=insertUpdate&unscoped_q=insertUpdate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="keyPressed"></a>
# keyPressed
keyPressed( java.awt.event.KeyEvent e ) &rarr; void



### Parameters:
e - a KeyEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=keyPressed&unscoped_q=keyPressed">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="keyReleased"></a>
# keyReleased
keyReleased( java.awt.event.KeyEvent e ) &rarr; void



### Parameters:
e - a KeyEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=keyReleased&unscoped_q=keyReleased">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="keyTyped"></a>
# keyTyped
keyTyped( java.awt.event.KeyEvent e ) &rarr; void



### Parameters:
e - a KeyEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=keyTyped&unscoped_q=keyTyped">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mouseClicked"></a>
# mouseClicked
mouseClicked( java.awt.event.MouseEvent e ) &rarr; void



### Parameters:
e - a MouseEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mouseClicked&unscoped_q=mouseClicked">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="propertyChange"></a>
# propertyChange
propertyChange( java.beans.PropertyChangeEvent e ) &rarr; void

Expected to be called from the AWT only.

### Parameters:
e - a PropertyChangeEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=propertyChange&unscoped_q=propertyChange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeUpdate"></a>
# removeUpdate
removeUpdate( javax.swing.event.DocumentEvent e ) &rarr; void



### Parameters:
e - a DocumentEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeUpdate&unscoped_q=removeUpdate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTabIsCompletion"></a>
# setTabIsCompletion
setTabIsCompletion( boolean b ) &rarr; void



### Parameters:
b - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTabIsCompletion&unscoped_q=setTabIsCompletion">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showCompletion"></a>
# showCompletion
showCompletion(  ) &rarr; void

May be called from any thread but it will be rescheduled into AWT.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showCompletion&unscoped_q=showCompletion">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showDocumentation"></a>
# showDocumentation
showDocumentation(  ) &rarr; void

May be called from any thread but it will be rescheduled into AWT.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showDocumentation&unscoped_q=showDocumentation">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showToolTip"></a>
# showToolTip
showToolTip(  ) &rarr; void

May be called from any thread but it will be rescheduled into AWT.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showToolTip&unscoped_q=showToolTip">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="startPopup"></a>
# startPopup
startPopup( javax.swing.text.JTextComponent component ) &rarr; void



### Parameters:
component - a JTextComponent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=startPopup&unscoped_q=startPopup">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="valueChanged"></a>
# valueChanged
valueChanged( javax.swing.event.ListSelectionEvent e ) &rarr; void

Called from AWT when selection in the completion list pane changes.

### Parameters:
e - a ListSelectionEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=valueChanged&unscoped_q=valueChanged">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

