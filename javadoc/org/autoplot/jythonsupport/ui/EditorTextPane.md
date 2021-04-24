# org.autoplot.jythonsupport.ui.EditorTextPane

Special editor for Jython scripts, adding undo and redo actions, bigger/smaller
 keystrokes and the action "plot."  A property "font" is managed as well, which
 was introduced when the jython mode in the jsyntaxpane editor was using a poor choice.

# EditorTextPane( )


***
<a name="getEditorAnnotationsSupport"></a>
# getEditorAnnotationsSupport
getEditorAnnotationsSupport(  ) &rarr; EditorAnnotationsSupport



### Returns:
org.autoplot.jythonsupport.ui.EditorAnnotationsSupport


<a href="https://github.com/autoplot/dev/search?q=getEditorAnnotationsSupport&unscoped_q=getEditorAnnotationsSupport">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInitializeRunnable"></a>
# getInitializeRunnable
getInitializeRunnable(  ) &rarr; Runnable



### Returns:
java.lang.Runnable


<a href="https://github.com/autoplot/dev/search?q=getInitializeRunnable&unscoped_q=getInitializeRunnable">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getToolTipText"></a>
# getToolTipText
getToolTipText( java.awt.event.MouseEvent event ) &rarr; String



### Parameters:
event - a MouseEvent

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getToolTipText&unscoped_q=getToolTipText">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="loadFile"></a>
# loadFile
loadFile( java.io.File f ) &rarr; void



### Parameters:
f - a File

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=loadFile&unscoped_q=loadFile">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="loadFileToString"></a>
# loadFileToString
loadFileToString( java.io.File f ) &rarr; String

copy the file into a string using readLine and a StringBuilder.

### Parameters:
f - the file

### Returns:
the string contents.

<a href="https://github.com/autoplot/dev/search?q=loadFileToString&unscoped_q=loadFileToString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDocument"></a>
# setDocument
setDocument( javax.swing.text.Document doc ) &rarr; void

Ed and I verified that this is being set off of the event thread.

### Parameters:
doc - a Document

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDocument&unscoped_q=setDocument">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setEditorAnnotationsSupport"></a>
# setEditorAnnotationsSupport
setEditorAnnotationsSupport( org.autoplot.jythonsupport.ui.EditorAnnotationsSupport support ) &rarr; void



### Parameters:
support - an EditorAnnotationsSupport

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setEditorAnnotationsSupport&unscoped_q=setEditorAnnotationsSupport">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFont"></a>
# setFont
setFont( java.awt.Font font ) &rarr; void



### Parameters:
font - a Font

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFont&unscoped_q=setFont">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showCompletionsView"></a>
# showCompletionsView
showCompletionsView(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showCompletionsView&unscoped_q=showCompletionsView">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

