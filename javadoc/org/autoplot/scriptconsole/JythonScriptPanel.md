# org.autoplot.scriptconsole.JythonScriptPanelGUI for editing and running Jython scripts.
JythonScriptPanel( org.autoplot.AutoplotUI app, org.autoplot.datasource.DataSetSelector selector )
Creates new form JythonScriptPanel

***
<a name="PROP_FILENAME"></a>
# PROP_FILENAME



***
<a name="PROP_DIRTY"></a>
# PROP_DIRTY



***
<a name="addMenuItem"></a>
# addMenuItem
addMenuItem( javax.swing.JMenuItem menu ) &rarr; void

add the menu or menu item to the editor context menu.

### Parameters:
menu - a JMenuItem

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addMenuItem&unscoped_q=addMenuItem">[search for examples]</a>

***
<a name="getAnnotationsSupport"></a>
# getAnnotationsSupport
getAnnotationsSupport(  ) &rarr; EditorAnnotationsSupport

provide access to the annotations support, so that errors
 can be marked on the editor.  This may cause bugs as there
 are issues like ensuring the exception marked belongs to the code,
 and it should not be used without reservation.

### Returns:
the annotations support.

<a href="https://github.com/autoplot/dev/search?q=getAnnotationsSupport&unscoped_q=getAnnotationsSupport">[search for examples]</a>

***
<a name="getConsoleListener"></a>
# getConsoleListener
getConsoleListener(  ) &rarr; ActionListener

return action listener listening for action commands containing source:linenum

### Returns:
a java.awt.event.ActionListener


<a href="https://github.com/autoplot/dev/search?q=getConsoleListener&unscoped_q=getConsoleListener">[search for examples]</a>

***
<a name="getEditorPanel"></a>
# getEditorPanel
getEditorPanel(  ) &rarr; EditorTextPane

returns the editor

### Returns:
the editor

<a href="https://github.com/autoplot/dev/search?q=getEditorPanel&unscoped_q=getEditorPanel">[search for examples]</a>

***
<a name="getFilename"></a>
# getFilename
getFilename(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getFilename&unscoped_q=getFilename">[search for examples]</a>

***
<a name="getRunningScript"></a>
# getRunningScript
getRunningScript(  ) &rarr; File

return the name of the script that the panel is busy running, or null.
 When this is non-null, don't load other scripts.

### Returns:
null or the running script.

<a href="https://github.com/autoplot/dev/search?q=getRunningScript&unscoped_q=getRunningScript">[search for examples]</a>

***
<a name="getScrollPane"></a>
# getScrollPane
getScrollPane(  ) &rarr; JScrollPane

returns the JScrollPane containing the editor so that special applications can control what's visible.

### Returns:
the JScrollPane containing the editor

<a href="https://github.com/autoplot/dev/search?q=getScrollPane&unscoped_q=getScrollPane">[search for examples]</a>

***
<a name="isDirty"></a>
# isDirty
isDirty(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isDirty&unscoped_q=isDirty">[search for examples]</a>

***
<a name="loadExampleUri"></a>
# loadExampleUri
loadExampleUri( String uri ) &rarr; void

this downloads the URI and loads the local version into the editor.

### Parameters:
uri - the URI

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=loadExampleUri&unscoped_q=loadExampleUri">[search for examples]</a>

***
<a name="loadFile"></a>
# loadFile
loadFile( java.io.File file ) &rarr; boolean

allow clients to tell this to load a file.

### Parameters:
file - the .jy or .jyds file.

### Returns:
false if the editor is dirty, true if the file is loaded.

<a href="https://github.com/autoplot/dev/search?q=loadFile&unscoped_q=loadFile">[search for examples]</a>

***
<a name="resetUndo"></a>
# resetUndo
resetUndo(  ) &rarr; void

reset the undo history.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resetUndo&unscoped_q=resetUndo">[search for examples]</a>

***
<a name="setDirty"></a>
# setDirty
setDirty( boolean dirty ) &rarr; void

set the flag indicating the script has been modified.

### Parameters:
dirty - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDirty&unscoped_q=setDirty">[search for examples]</a>

***
<a name="setFilename"></a>
# setFilename
setFilename( String filename ) &rarr; void



### Parameters:
filename - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFilename&unscoped_q=setFilename">[search for examples]</a>

***
<a name="setRunningScript"></a>
# setRunningScript
setRunningScript( java.io.File f ) &rarr; void

set the current script that is running.  This will prevent 
 automatic loads from occurring.

### Parameters:
f - a File

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRunningScript&unscoped_q=setRunningScript">[search for examples]</a>

