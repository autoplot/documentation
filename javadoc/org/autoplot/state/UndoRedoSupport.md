# org.autoplot.state.UndoRedoSupportUndoRedoSupport keeps track of a series of application states, providing
 "undo" and "redo" operations.
UndoRedoSupport( org.autoplot.ApplicationModel applicationModel )
Creates a new instance of UndoRedoSupport

***
<a name="PROP_REDOLABEL"></a>
# PROP_REDOLABEL



***
<a name="PROP_SIZE_LIMIT"></a>
# PROP_SIZE_LIMIT

name of the property containing the number of states kept

***
<a name="PROP_DEPTH"></a>
# PROP_DEPTH

property name of the current depth

***
<a name="PROP_SAVE_STATE_DEPTH"></a>
# PROP_SAVE_STATE_DEPTH

the number of states to keep in the states folder.  Presently this is only implemented so that 0 disables the feature.

***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
propertyName - a String
<br>listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addPropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="getDepth"></a>
# getDepth
getDepth(  ) &rarr; int

get the current depth, where depth can be lower than the number of
 states held, when redos can be done.

### Returns:
the current depth.

<a href="https://github.com/autoplot/dev/search?q=getDepth&unscoped_q=getDepth">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLongUndoDescription"></a>
# getLongUndoDescription
getLongUndoDescription( int i ) &rarr; String

used for feedback.

### Parameters:
i - an int

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getLongUndoDescription&unscoped_q=getLongUndoDescription">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRedoAction"></a>
# getRedoAction
getRedoAction(  ) &rarr; Action

get the action to trigger redo.

### Returns:
action that can be attached to button.

<a href="https://github.com/autoplot/dev/search?q=getRedoAction&unscoped_q=getRedoAction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRedoDescription"></a>
# getRedoDescription
getRedoDescription(  ) &rarr; String

get the longer description for the action, intended to be used for the tooltip.

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getRedoDescription&unscoped_q=getRedoDescription">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRedoLabel"></a>
# getRedoLabel
getRedoLabel(  ) &rarr; String

returns a label describing the redo operation, or null if the operation
 doesn't exist.

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getRedoLabel&unscoped_q=getRedoLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSaveStateDepth"></a>
# getSaveStateDepth
getSaveStateDepth(  ) &rarr; int

get the current number of persistent states stored in autoplot_data/state

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=getSaveStateDepth&unscoped_q=getSaveStateDepth">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSizeLimit"></a>
# getSizeLimit
getSizeLimit(  ) &rarr; int

get the number of states which will be kept

### Returns:
size

<a href="https://github.com/autoplot/dev/search?q=getSizeLimit&unscoped_q=getSizeLimit">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getUndoAction"></a>
# getUndoAction
getUndoAction(  ) &rarr; Action

get the action to trigger undo.

### Returns:
action that can be attached to button.

<a href="https://github.com/autoplot/dev/search?q=getUndoAction&unscoped_q=getUndoAction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getUndoDescription"></a>
# getUndoDescription
getUndoDescription(  ) &rarr; String

get the longer description for the action, intended to be used for the tooltip.

### Returns:
a human-readable description

<a href="https://github.com/autoplot/dev/search?q=getUndoDescription&unscoped_q=getUndoDescription">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getUndoLabel"></a>
# getUndoLabel
getUndoLabel(  ) &rarr; String

returns a label describing the undo operation, or null if the operation
 doesn't exist.

### Returns:
the level

<a href="https://github.com/autoplot/dev/search?q=getUndoLabel&unscoped_q=getUndoLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isIgnoringUpdates"></a>
# isIgnoringUpdates
isIgnoringUpdates(  ) &rarr; boolean

Getter for property ignoringUpdates.

### Returns:
Value of property ignoringUpdates.

<a href="https://github.com/autoplot/dev/search?q=isIgnoringUpdates&unscoped_q=isIgnoringUpdates">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="peekAt"></a>
# peekAt
peekAt( int pos ) &rarr; StateStackElement

allow scripts to peek into undo/redo stack for debugging.

### Parameters:
pos - an int

### Returns:
an org.autoplot.state.UndoRedoSupport.StateStackElement


<a href="https://github.com/autoplot/dev/search?q=peekAt&unscoped_q=peekAt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="pushState"></a>
# pushState
pushState( java.beans.PropertyChangeEvent ev ) &rarr; void

request that a state be pushed onto the state stack.

### Parameters:
ev - a PropertyChangeEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=pushState&unscoped_q=pushState">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

pushState( java.beans.PropertyChangeEvent ev, String label ) &rarr; void<br>
***
<a name="redo"></a>
# redo
redo(  ) &rarr; void

redo the state change that was undone, popping up the state stack one position.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=redo&unscoped_q=redo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="refreshUndoMultipleMenu"></a>
# refreshUndoMultipleMenu
refreshUndoMultipleMenu( javax.swing.JMenu undoMultipleMenu ) &rarr; void

create all the menu items for a JMenu offering undo targets.

### Parameters:
undoMultipleMenu - the menu

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=refreshUndoMultipleMenu&unscoped_q=refreshUndoMultipleMenu">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
propertyName - a String
<br>listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

removePropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="resetHistory"></a>
# resetHistory
resetHistory(  ) &rarr; void

reset the history, for example after a vap file is loaded.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resetHistory&unscoped_q=resetHistory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setIgnoringUpdates"></a>
# setIgnoringUpdates
setIgnoringUpdates( boolean ignoringUpdates ) &rarr; void

Setter for property ignoringUpdates.

### Parameters:
ignoringUpdates - New value of property ignoringUpdates.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setIgnoringUpdates&unscoped_q=setIgnoringUpdates">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSaveStateDepth"></a>
# setSaveStateDepth
setSaveStateDepth( int depth ) &rarr; void

set the number of persistent states to keep, or 0 will disable the feature.

### Parameters:
depth - zero or the number of states to keep.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSaveStateDepth&unscoped_q=setSaveStateDepth">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSizeLimit"></a>
# setSizeLimit
setSizeLimit( int size ) &rarr; void

set the number of states which will be kept

### Parameters:
size - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSizeLimit&unscoped_q=setSizeLimit">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="undo"></a>
# undo
undo(  ) &rarr; void

undo the last state change.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=undo&unscoped_q=undo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

undo( int level ) &rarr; void<br>
