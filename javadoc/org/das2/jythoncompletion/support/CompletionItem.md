# org.das2.jythoncompletion.support.CompletionItemThe interface representing a single item of the result list that can be displayed
 in the completion popup.
***
<a name="createDocumentationTask"></a>
# createDocumentationTask
createDocumentationTask(  ) &rarr; CompletionTask

Returns a task used to obtain a documentation associated with the item if there
 is any.

### Returns:
org.das2.jythoncompletion.support.CompletionTask


<a href="https://github.com/autoplot/dev/search?q=createDocumentationTask&unscoped_q=createDocumentationTask">[search for examples]</a>

***
<a name="createToolTipTask"></a>
# createToolTipTask
createToolTipTask(  ) &rarr; CompletionTask

Returns a task used to obtain a tooltip hint associated with the item if there
 is any.

### Returns:
org.das2.jythoncompletion.support.CompletionTask


<a href="https://github.com/autoplot/dev/search?q=createToolTipTask&unscoped_q=createToolTipTask">[search for examples]</a>

***
<a name="defaultAction"></a>
# defaultAction
defaultAction( javax.swing.text.JTextComponent component ) &rarr; void

Gets invoked when user presses <code>VK_ENTER</code> key
 or when she double-clicks on this item with the mouse cursor.
 <br/>
 This method gets invoked from AWT thread.

### Parameters:
component - non-null text component for which the completion was invoked.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=defaultAction&unscoped_q=defaultAction">[search for examples]</a>

***
<a name="getInsertPrefix"></a>
# getInsertPrefix
getInsertPrefix(  ) &rarr; CharSequence

Returns a text used for finding of a longest common prefix
 after the <i>TAB</i> gets pressed or when the completion is opened explicitly.
 <br>
 The completion infrastructure will evaluate the insert prefixes
 of all the items present in the visible result and finds the longest
 common prefix.

 <p>
 Generally the returned text does not need to contain all the information
 that gets inserted when the item is selected.
 <br>
 For example in java completion the field name should be returned for fields
 or a method name for methods (but not parameters)
 or a non-FQN name for classes.

### Returns:
non-null character sequence containing the insert prefix.
  <br>
  Returning an empty string will effectively disable the TAB completion
  as the longest common prefix will be empty.

<a href="https://github.com/autoplot/dev/search?q=getInsertPrefix&unscoped_q=getInsertPrefix">[search for examples]</a>

***
<a name="getPreferredWidth"></a>
# getPreferredWidth
getPreferredWidth( java.awt.Graphics g, java.awt.Font defaultFont ) &rarr; int

Get the preferred visual width of this item.
 <br>
 The visual height of the item is fixed to 16 points.

### Parameters:
g - graphics that can be used for determining the preferred width
  e.g. getting of the font metrics.
<br>defaultFont - default font used for rendering.

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getPreferredWidth&unscoped_q=getPreferredWidth">[search for examples]</a>

***
<a name="getSortPriority"></a>
# getSortPriority
getSortPriority(  ) &rarr; int

Returns the item's priority. A lower value means a lower index of the item
 in the completion result list.

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getSortPriority&unscoped_q=getSortPriority">[search for examples]</a>

***
<a name="getSortText"></a>
# getSortText
getSortText(  ) &rarr; CharSequence

Returns a text used to sort items alphabetically.

### Returns:
java.lang.CharSequence


<a href="https://github.com/autoplot/dev/search?q=getSortText&unscoped_q=getSortText">[search for examples]</a>

***
<a name="instantSubstitution"></a>
# instantSubstitution
instantSubstitution( javax.swing.text.JTextComponent component ) &rarr; boolean

When enabled for the item the instant substitution should process the item
 in the same way like when the item is displayed and Enter key gets pressed
 by the user.
 <br>
 Instant substitution is invoked when there would be just a single item 
 displayed in the completion popup window.
 <br>
 The implementation can invoke the {@link #defaultAction(JTextComponent)}
 if necessary.
 <br/>
 This method gets invoked from AWT thread.

### Parameters:
component - non-null text component for which the completion was invoked.

### Returns:
<code>true</code> if the instant substitution was successfully done.
  <code>false</code> means that the instant substitution should not be done
  for this item and the completion item should normally be displayed.

<a href="https://github.com/autoplot/dev/search?q=instantSubstitution&unscoped_q=instantSubstitution">[search for examples]</a>

***
<a name="processKeyEvent"></a>
# processKeyEvent
processKeyEvent( java.awt.event.KeyEvent evt ) &rarr; void

Process the key pressed when this completion item was selected
 in the completion popup window.
 <br/>
 This method gets invoked from AWT thread.

### Parameters:
evt - non-null key event of the pressed key. It should be consumed
  in case the item is sensitive to the given key. The source of this 
  event is the text component to which the corresponding action should
  be performed.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=processKeyEvent&unscoped_q=processKeyEvent">[search for examples]</a>

***
<a name="render"></a>
# render
render( java.awt.Graphics g, java.awt.Font defaultFont, java.awt.Color defaultColor, java.awt.Color backgroundColor, int width, int height, boolean selected ) &rarr; void

Render this item into the given graphics.

### Parameters:
g - graphics to render the item into.
<br>defaultFont - default font used for rendering.
<br>defaultColor - default color used for rendering.
<br>backgroundColor - color used for background.
<br>width - width of the area to render into.
<br>height - height of the are to render into.
<br>selected - whether this item is visually selected in the list
  into which the items are being rendered.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=render&unscoped_q=render">[search for examples]</a>

