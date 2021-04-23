# org.autoplot.AutoplotUI

The Autoplot application GUI.  This is the entry point for the application, wrapping the internal
 application model with conveniences like bookmarks, time range editors and history.

# AutoplotUI( org.autoplot.ApplicationModel model )
Creates new form AutoplotUI

***
<a name="CARD_DATA_SET_SELECTOR"></a>
# CARD_DATA_SET_SELECTOR



***
<a name="CARD_TIME_RANGE_SELECTOR"></a>
# CARD_TIME_RANGE_SELECTOR



***
<a name="WARNING_ICON"></a>
# WARNING_ICON

yellow triangle with exclamation point, used to indicate warning condition.

***
<a name="ERROR_ICON"></a>
# ERROR_ICON

red stop sign with exclamation point, using to indicate error condition.

***
<a name="BUSY_ICON"></a>
# BUSY_ICON

animated gif of swirling dots, used to indicate known busy state.

***
<a name="BUSY_OPAQUE_ICON"></a>
# BUSY_OPAQUE_ICON

animated gif of swirling dots, used to indicate known busy state.

***
<a name="READY_ICON"></a>
# READY_ICON

not used.

***
<a name="IDLE_ICON"></a>
# IDLE_ICON

empty 16x16 image used to indicate normal status.

***
<a name="READY_MESSAGE"></a>
# READY_MESSAGE

ready message.

***
<a name="PROP_EDITORCARD"></a>
# PROP_EDITORCARD



***
<a name="about"></a>
# about
about(  ) &rarr; void

show the about dialog, which has version information.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=about&unscoped_q=about">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="basicMode"></a>
# basicMode
basicMode(  ) &rarr; void

turn on basic mode, where users can only use the app for browsing existing products.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=basicMode&unscoped_q=basicMode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="clearBottomPanel"></a>
# clearBottomPanel
clearBottomPanel(  ) &rarr; void

remove any extra component added below the tabs.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=clearBottomPanel&unscoped_q=clearBottomPanel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="clearLeftPanel"></a>
# clearLeftPanel
clearLeftPanel(  ) &rarr; void

remove any extra component added to the left of the tabs.  This calls invokeLater to make sure
 the event is on the event thread.

### Returns:
void (returns nothing)

### See Also:
<a href='#setLeftPanel'>setLeftPanel(javax.swing.JComponent)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=clearLeftPanel&unscoped_q=clearLeftPanel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="clearRightPanel"></a>
# clearRightPanel
clearRightPanel(  ) &rarr; void

remove any extra component added to the right of the tabs.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=clearRightPanel&unscoped_q=clearRightPanel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="enterAddPlotElementDialog"></a>
# enterAddPlotElementDialog
enterAddPlotElementDialog(  ) &rarr; void

make this public before AGU.  Set the editor to the URI, then call this.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=enterAddPlotElementDialog&unscoped_q=enterAddPlotElementDialog">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getApplicationModel"></a>
# getApplicationModel
getApplicationModel(  ) &rarr; ApplicationModel

provide access to the universal application model.

### Returns:
access to the universal application model.

<a href="https://github.com/autoplot/dev/search?q=getApplicationModel&unscoped_q=getApplicationModel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataPanel"></a>
# getDataPanel
getDataPanel(  ) &rarr; DataPanel

return the data panel (for testing).

### Returns:
the data panel.

<a href="https://github.com/autoplot/dev/search?q=getDataPanel&unscoped_q=getDataPanel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSetSelector"></a>
# getDataSetSelector
getDataSetSelector(  ) &rarr; DataSetSelector

provide access to the dataSetSelector which browses and resets the plot URIs.

### Returns:
the dataSetSelector

<a href="https://github.com/autoplot/dev/search?q=getDataSetSelector&unscoped_q=getDataSetSelector">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDocumentModel"></a>
# getDocumentModel
getDocumentModel(  ) &rarr; Application

return the current state of this application window.  Note this is
 the actual and not a copy, so it should not be modified.

### Returns:
the application state.
### See Also:
<a href='#getDom'>getDom()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getDocumentModel&unscoped_q=getDocumentModel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDom"></a>
# getDom
getDom(  ) &rarr; Application

return the dom (application state) associated with this application.

### Returns:
the dom associated with this application.

<a href="https://github.com/autoplot/dev/search?q=getDom&unscoped_q=getDom">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDropTargetListener"></a>
# getDropTargetListener
getDropTargetListener(  ) &rarr; DropTargetListener

provide access to the dropTargetListener.  Presumably this was added for testing.

### Returns:
the dropListener.

<a href="https://github.com/autoplot/dev/search?q=getDropTargetListener&unscoped_q=getDropTargetListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getEditorCard"></a>
# getEditorCard
getEditorCard(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getEditorCard&unscoped_q=getEditorCard">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPersistentStateSupport"></a>
# getPersistentStateSupport
getPersistentStateSupport( org.autoplot.AutoplotUI parent, org.autoplot.ApplicationModel applicationModel ) &rarr; PersistentStateSupport



### Parameters:
parent - an AutoplotUI
<br>applicationModel - an ApplicationModel

### Returns:
org.autoplot.PersistentStateSupport


<a href="https://github.com/autoplot/dev/search?q=getPersistentStateSupport&unscoped_q=getPersistentStateSupport">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getProcessId"></a>
# getProcessId
getProcessId( String fallback ) &rarr; String

return the processID (pid), or the fallback if the pid cannot be found.

### Parameters:
fallback - the string (null is okay) to return when the pid cannot be found.

### Returns:
the process id or the fallback provided by the caller.

<a href="https://github.com/autoplot/dev/search?q=getProcessId&unscoped_q=getProcessId">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getScriptEditor"></a>
# getScriptEditor
getScriptEditor(  ) &rarr; EditorTextPane

access the editor for scripts, if available.  This was initially added 
 to provide a way to experiment with setting editor colors, but might be 
 useful for other purposes.

### Returns:
null or the editor panel
### See Also:
<a href='#getScriptPanel'>getScriptPanel()</a> which returns the panel<br>

<a href="https://github.com/autoplot/dev/search?q=getScriptEditor&unscoped_q=getScriptEditor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getScriptPanel"></a>
# getScriptPanel
getScriptPanel(  ) &rarr; JythonScriptPanel

Return the script editor panel.  Until v2020a_2 and 20200202a, this 
 returned the EditorTextPane rather than the tab itself.  This is 
 inconsistent with other calls.  For example:
 <pre>
 s= getApplication().getScriptPanel().getFilename() 
 print( 'script editor filename:' )
 print( s )
 </pre>

### Returns:
the editor panel in the script tab.
### See Also:
<a href='#getScriptEditor'>getScriptEditor()</a> which returns the editor itself.<br>

<a href="https://github.com/autoplot/dev/search?q=getScriptPanel&unscoped_q=getScriptPanel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTabs"></a>
# getTabs
getTabs(  ) &rarr; TearoffTabbedPane

provide access to the tabs so that component can be added

### Returns:
TabbedPane.

<a href="https://github.com/autoplot/dev/search?q=getTabs&unscoped_q=getTabs">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTickleTimer"></a>
# getTickleTimer
getTickleTimer(  ) &rarr; TickleTimer

access tickle timer, which triggers when things change.  This will go away!

### Returns:
an org.autoplot.util.TickleTimer


<a href="https://github.com/autoplot/dev/search?q=getTickleTimer&unscoped_q=getTickleTimer">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTimeRangeEditor"></a>
# getTimeRangeEditor
getTimeRangeEditor(  ) &rarr; TimeRangeEditor

provide access to the timeRangeEditor which controls dom.timerange.

### Returns:
the timeRangeEditor

<a href="https://github.com/autoplot/dev/search?q=getTimeRangeEditor&unscoped_q=getTimeRangeEditor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getUndoRedoSupport"></a>
# getUndoRedoSupport
getUndoRedoSupport(  ) &rarr; UndoRedoSupport

provide access to the undoRedoSupport.  Presumably this was added for testing.

### Returns:
the undoRedoSupport.

<a href="https://github.com/autoplot/dev/search?q=getUndoRedoSupport&unscoped_q=getUndoRedoSupport">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getWindowExtraHeight"></a>
# getWindowExtraHeight
getWindowExtraHeight(  ) &rarr; int

return the extra pixels needed by the GUI for borders and address bar.

### Returns:
the extra pixels needed by the GUI for borders and address bar.

<a href="https://github.com/autoplot/dev/search?q=getWindowExtraHeight&unscoped_q=getWindowExtraHeight">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getWindowExtraWidth"></a>
# getWindowExtraWidth
getWindowExtraWidth(  ) &rarr; int

return the extra pixels needed by the GUI for borders and address bar.

### Returns:
the extra pixels needed by the GUI for borders and address bar.

<a href="https://github.com/autoplot/dev/search?q=getWindowExtraWidth&unscoped_q=getWindowExtraWidth">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="handleSingleInstanceURI"></a>
# handleSingleInstanceURI
handleSingleInstanceURI( String suri, String pos ) &rarr; void

extract the code that handles the single instance so that we can model it for debugging.

### Parameters:
suri - the reentry URI
<br>pos - support the --position=3 switch to support servers.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=handleSingleInstanceURI&unscoped_q=handleSingleInstanceURI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isBasicMode"></a>
# isBasicMode
isBasicMode(  ) &rarr; boolean

true if the GUI is in basic mode, hiding functions for new users.  In basic mode users can only browse existing
 products.

### Returns:
true if the GUI is in basic mode

<a href="https://github.com/autoplot/dev/search?q=isBasicMode&unscoped_q=isBasicMode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isExpertMode"></a>
# isExpertMode
isExpertMode(  ) &rarr; boolean

true if the GUI is in expert mode, showing more functions for users comfortable with the application.

### Returns:
true if the GUI is in expert mode

<a href="https://github.com/autoplot/dev/search?q=isExpertMode&unscoped_q=isExpertMode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - the command line arguments

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="newApplication"></a>
# newApplication
newApplication(  ) &rarr; AutoplotUI

create a new application.  This is a convenience method for scripts.

### Returns:
an org.autoplot.AutoplotUI


<a href="https://github.com/autoplot/dev/search?q=newApplication&unscoped_q=newApplication">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="plotUri"></a>
# plotUri
plotUri( String uri ) &rarr; void

Attempt to plot the given URI, which may be rejected and its
 editor invoked.  This is the equivalent of typing in the URI in the 
 address bar and pressing the Go (green arrow) button.

### Parameters:
uri - the Autoplot URI.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=plotUri&unscoped_q=plotUri">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="raiseApplicationWindow"></a>
# raiseApplicationWindow
raiseApplicationWindow( java.awt.Frame frame ) &rarr; void

raise the application window
 http://stackoverflow.com/questions/309023/howto-bring-a-java-window-to-the-front

### Parameters:
frame - the frame

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=raiseApplicationWindow&unscoped_q=raiseApplicationWindow">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reloadTools"></a>
# reloadTools
reloadTools(  ) &rarr; void

looks for and adds tools on a new thread.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reloadTools&unscoped_q=reloadTools">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resetAction"></a>
# resetAction
resetAction( String name, javax.swing.Action a ) &rarr; void

Reset one of the actions in the File menu.  There don't appear to be any uses of 
 this odd function, so it might have been used with a script.

### Parameters:
name - the name of the action.
<br>a - the new action.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resetAction&unscoped_q=resetAction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resizeForCanvasSize"></a>
# resizeForCanvasSize
resizeForCanvasSize( int w, int h ) &rarr; double

resize the outer GUI attempting to get a fitted canvas size.  This fixes the
 problem where a loaded vap doesn't appear as it does when it was saved because
 the canvas is resized.

### Parameters:
w - the width
<br>h - the height

### Returns:
nominal scale factor

<a href="https://github.com/autoplot/dev/search?q=resizeForCanvasSize&unscoped_q=resizeForCanvasSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

resizeForCanvasSize( int w, int h, int extraW, int extraH ) &rarr; double<br>
***
<a name="resizeForDefaultCanvasSize"></a>
# resizeForDefaultCanvasSize
resizeForDefaultCanvasSize(  ) &rarr; void

reset to the size in defaults.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resizeForDefaultCanvasSize&unscoped_q=resizeForDefaultCanvasSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reviewBookmark"></a>
# reviewBookmark
reviewBookmark( String uri, int modifiers ) &rarr; void

give the user a chance to review the bookmark before using it.
 The user has selected the URI via the bookmarks and we will show it to
 them before using it.
 (rfe336)

### Parameters:
uri - the URI from the bookmarks or history.
<br>modifiers - key modifiers like KeyEvent.CTRL_MASK for plot below.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reviewBookmark&unscoped_q=reviewBookmark">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="runScriptTools"></a>
# runScriptTools
runScriptTools( String script ) &rarr; void

run the script, using the reference on the tools menu.  The security is going to be a bit different soon.
 This should be called from the event thread because it creates GUI components.

### Parameters:
script - the URI of the script to run

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=runScriptTools&unscoped_q=runScriptTools">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setBottomPanel"></a>
# setBottomPanel
setBottomPanel( javax.swing.JComponent c ) &rarr; void

add the component (typically a JPanel) below the tabs and above the 
 status indicator

### Parameters:
c - null or the component to add

### Returns:
void (returns nothing)

### See Also:
<a href='#setLeftPanel'>setLeftPanel(javax.swing.JComponent)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setBottomPanel&unscoped_q=setBottomPanel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setEditorCard"></a>
# setEditorCard
setEditorCard( String editorCard ) &rarr; void



### Parameters:
editorCard - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setEditorCard&unscoped_q=setEditorCard">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setExpertMode"></a>
# setExpertMode
setExpertMode( boolean expert ) &rarr; void

set the application expert mode flag to restrict the app for browsing.

### Parameters:
expert - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setExpertMode&unscoped_q=setExpertMode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLeftPanel"></a>
# setLeftPanel
setLeftPanel( javax.swing.JComponent c ) &rarr; void

add the component (typically a JPanel) to the left
 side of the application.

### Parameters:
c - null or the component to add

### Returns:
void (returns nothing)

### See Also:
<a href='ScriptContext.md#addTab'>ScriptContext#addTab(java.lang.String, javax.swing.JComponent)</a> <br>
<a href='#clearLeftPanel'>clearLeftPanel()</a> <br>
<a href='#setRightPanel'>setRightPanel(javax.swing.JComponent)</a> <br>
<a href='#setBottomPanel'>setBottomPanel(javax.swing.JComponent)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setLeftPanel&unscoped_q=setLeftPanel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setMessage"></a>
# setMessage
setMessage( String message ) &rarr; void

set the message in the lower left corner of the application.

### Parameters:
message - the message to display

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMessage&unscoped_q=setMessage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

setMessage( javax.swing.Icon icon, String message ) &rarr; void<br>
***
<a name="setRightPanel"></a>
# setRightPanel
setRightPanel( javax.swing.JComponent c ) &rarr; void

add the component (typically a JPanel) to the right
 side of the application.

### Parameters:
c - null or the component to add

### Returns:
void (returns nothing)

### See Also:
<a href='#setLeftPanel'>setLeftPanel(javax.swing.JComponent)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setRightPanel&unscoped_q=setRightPanel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSize"></a>
# setSize
setSize( int width, int height ) &rarr; void



### Parameters:
width - an int
<br>height - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSize&unscoped_q=setSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

setSize( java.awt.Dimension d ) &rarr; void<br>
***
<a name="setStatus"></a>
# setStatus
setStatus( String message ) &rarr; void

set the status message, with "busy:" or "warning:" prefix.

### Parameters:
message - the message to display

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setStatus&unscoped_q=setStatus">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

setStatus( javax.swing.Icon icon, String message ) &rarr; void<br>
***
<a name="switchToEditorCard"></a>
# switchToEditorCard
switchToEditorCard( String selector ) &rarr; void



### Parameters:
selector - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=switchToEditorCard&unscoped_q=switchToEditorCard">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

