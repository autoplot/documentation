# org.das2.jythoncompletion.ui.CompletionLayout

Layout of the completion, documentation and tooltip popup windows.

***
<a name="COMPLETION_ITEM_HEIGHT"></a>
# COMPLETION_ITEM_HEIGHT



***
<a name="clearDocumentationHistory"></a>
# clearDocumentationHistory
clearDocumentationHistory(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=clearDocumentationHistory&unscoped_q=clearDocumentationHistory">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getEditorComponent"></a>
# getEditorComponent
getEditorComponent(  ) &rarr; JTextComponent



### Returns:
javax.swing.text.JTextComponent


<a href="https://github.com/autoplot/dev/search?q=getEditorComponent&unscoped_q=getEditorComponent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSelectedCompletionItem"></a>
# getSelectedCompletionItem
getSelectedCompletionItem(  ) &rarr; CompletionItem



### Returns:
org.das2.jythoncompletion.support.CompletionItem


<a href="https://github.com/autoplot/dev/search?q=getSelectedCompletionItem&unscoped_q=getSelectedCompletionItem">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSelectedIndex"></a>
# getSelectedIndex
getSelectedIndex(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getSelectedIndex&unscoped_q=getSelectedIndex">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hideCompletion"></a>
# hideCompletion
hideCompletion(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=hideCompletion&unscoped_q=hideCompletion">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hideDocumentation"></a>
# hideDocumentation
hideDocumentation(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=hideDocumentation&unscoped_q=hideDocumentation">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hideToolTip"></a>
# hideToolTip
hideToolTip(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=hideToolTip&unscoped_q=hideToolTip">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isCompletionVisible"></a>
# isCompletionVisible
isCompletionVisible(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isCompletionVisible&unscoped_q=isCompletionVisible">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDocumentationVisible"></a>
# isDocumentationVisible
isDocumentationVisible(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isDocumentationVisible&unscoped_q=isDocumentationVisible">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isToolTipVisible"></a>
# isToolTipVisible
isToolTipVisible(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isToolTipVisible&unscoped_q=isToolTipVisible">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="processKeyEvent"></a>
# processKeyEvent
processKeyEvent( java.awt.event.KeyEvent evt ) &rarr; void



### Parameters:
evt - a KeyEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=processKeyEvent&unscoped_q=processKeyEvent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setEditorComponent"></a>
# setEditorComponent
setEditorComponent( javax.swing.text.JTextComponent editorComponent ) &rarr; void



### Parameters:
editorComponent - a JTextComponent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setEditorComponent&unscoped_q=setEditorComponent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showCompletion"></a>
# showCompletion
showCompletion( java.util.List data, String title, int anchorOffset, javax.swing.event.ListSelectionListener listSelectionListener, String shortcutHint, int selectedIndex ) &rarr; void



### Parameters:
data - a java.util.List
<br>title - a String
<br>anchorOffset - an int
<br>listSelectionListener - a ListSelectionListener
<br>shortcutHint - a String
<br>selectedIndex - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showCompletion&unscoped_q=showCompletion">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showDocumentation"></a>
# showDocumentation
showDocumentation( org.das2.jythoncompletion.support.CompletionDocumentation doc, int anchorOffset ) &rarr; void



### Parameters:
doc - a CompletionDocumentation
<br>anchorOffset - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showDocumentation&unscoped_q=showDocumentation">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showToolTip"></a>
# showToolTip
showToolTip( javax.swing.JToolTip toolTip, int anchorOffset ) &rarr; void



### Parameters:
toolTip - a JToolTip
<br>anchorOffset - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showToolTip&unscoped_q=showToolTip">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

