# org.das2.dasml.PersistentStateSupport
PersistentStateSupport( org.das2.graph.DasCanvas canvas, String extension )
Provides a means for saving the application persistently, undo/redo support (TODO).
  canvas is the canvas to be serialized, extension identifies the application.  Note that
  internal changes to das may break saved files.

PersistentStateSupport( java.awt.Component parent, org.das2.dasml.PersistentStateSupport.SerializationStrategy strategy, String extension )


PersistentStateSupport( )
Creates a new instance of PersistentStateSupport

***
<a name="PROPERTY_OPENING"></a>
# PROPERTY_OPENING



***
<a name="PROPERTY_SAVING"></a>
# PROPERTY_SAVING



***
<a name="PROPERTY_DIRTY"></a>
# PROPERTY_DIRTY



***
<a name="PROPERTY_CURRENT_FILE"></a>
# PROPERTY_CURRENT_FILE



***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void

Adds a PropertyChangeListener to the listener list.

### Parameters:
l - The listener to add.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="close"></a>
# <del>close</del>
Deprecated: What is the purpose of this method?
***
<a name="createCurrentFileLabel"></a>
# createCurrentFileLabel
createCurrentFileLabel(  ) &rarr; JLabel



### Returns:
javax.swing.JLabel


<a href="https://github.com/autoplot/dev/search?q=createCurrentFileLabel&unscoped_q=createCurrentFileLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createOpenAction"></a>
# createOpenAction
createOpenAction(  ) &rarr; Action



### Returns:
javax.swing.Action


<a href="https://github.com/autoplot/dev/search?q=createOpenAction&unscoped_q=createOpenAction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createOpenRecentMenu"></a>
# createOpenRecentMenu
createOpenRecentMenu(  ) &rarr; JMenu



### Returns:
javax.swing.JMenu


<a href="https://github.com/autoplot/dev/search?q=createOpenRecentMenu&unscoped_q=createOpenRecentMenu">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createQuitAction"></a>
# createQuitAction
createQuitAction(  ) &rarr; Action

In the future, this should prompt for save if the app is dirty.

### Returns:
javax.swing.Action


<a href="https://github.com/autoplot/dev/search?q=createQuitAction&unscoped_q=createQuitAction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createSaveAction"></a>
# createSaveAction
createSaveAction(  ) &rarr; Action



### Returns:
javax.swing.Action


<a href="https://github.com/autoplot/dev/search?q=createSaveAction&unscoped_q=createSaveAction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createSaveAsAction"></a>
# createSaveAsAction
createSaveAsAction(  ) &rarr; Action



### Returns:
javax.swing.Action


<a href="https://github.com/autoplot/dev/search?q=createSaveAsAction&unscoped_q=createSaveAsAction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createSaveMenuItem"></a>
# createSaveMenuItem
createSaveMenuItem(  ) &rarr; JMenuItem



### Returns:
javax.swing.JMenuItem


<a href="https://github.com/autoplot/dev/search?q=createSaveMenuItem&unscoped_q=createSaveMenuItem">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCurrentFile"></a>
# getCurrentFile
getCurrentFile(  ) &rarr; File



### Returns:
java.io.File


<a href="https://github.com/autoplot/dev/search?q=getCurrentFile&unscoped_q=getCurrentFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isCurrentFileOpened"></a>
# isCurrentFileOpened
isCurrentFileOpened(  ) &rarr; boolean

Property currentFileOpened indicates if the current file has ever been opened.  This
 is to handle the initial state where the current file is set, but should not be
 displayed because it has not been opened.

### Returns:
Value of property currentFileOpened.

<a href="https://github.com/autoplot/dev/search?q=isCurrentFileOpened&unscoped_q=isCurrentFileOpened">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDirty"></a>
# isDirty
isDirty(  ) &rarr; boolean

Getter for property dirty.

### Returns:
Value of property dirty.

<a href="https://github.com/autoplot/dev/search?q=isDirty&unscoped_q=isDirty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isOpening"></a>
# isOpening
isOpening(  ) &rarr; boolean

Property loading is true when a load operation is being performed.

### Returns:
Value of property loading.

<a href="https://github.com/autoplot/dev/search?q=isOpening&unscoped_q=isOpening">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isSaving"></a>
# isSaving
isSaving(  ) &rarr; boolean

Property saving is true when a save operation is being performed.

### Returns:
Value of property saving.

<a href="https://github.com/autoplot/dev/search?q=isSaving&unscoped_q=isSaving">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="markDirty"></a>
# markDirty
markDirty(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=markDirty&unscoped_q=markDirty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void

Removes a PropertyChangeListener from the listener list.

### Parameters:
l - The listener to remove.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="saveAs"></a>
# saveAs
saveAs(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=saveAs&unscoped_q=saveAs">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setCurrentFile"></a>
# setCurrentFile
setCurrentFile( java.io.File currentFile ) &rarr; void



### Parameters:
currentFile - a File

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCurrentFile&unscoped_q=setCurrentFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setCurrentFileOpened"></a>
# setCurrentFileOpened
setCurrentFileOpened( boolean currentFileOpened ) &rarr; void

Setter for property currentFileOpened.

### Parameters:
currentFileOpened - New value of property currentFileOpened.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCurrentFileOpened&unscoped_q=setCurrentFileOpened">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDirty"></a>
# setDirty
setDirty( boolean dirty ) &rarr; void

Setter for property dirty.

### Parameters:
dirty - New value of property dirty.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDirty&unscoped_q=setDirty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

