# org.autoplot.datasource.DataSetSelectorSwing component for selecting dataset URIs.  This provides hooks for completions.
DataSetSelector( )
Creates new form DataSetSelector

***
<a name="PROP_RECENT"></a>
# PROP_RECENT



***
<a name="BUSY_ICON"></a>
# BUSY_ICON



***
<a name="FILEMAG_ICON"></a>
# FILEMAG_ICON



***
<a name="PROPERTY_MESSAGE"></a>
# PROPERTY_MESSAGE



***
<a name="FILE_NOT_FOUND"></a>
# FILE_NOT_FOUND



***
<a name="PROP_HIDEPLAYBUTTON"></a>
# PROP_HIDEPLAYBUTTON



***
<a name="PROP_PLOTITBUTTONVISIBLE"></a>
# PROP_PLOTITBUTTONVISIBLE



***
<a name="PROP_ENABLEDATASOURCE"></a>
# PROP_ENABLEDATASOURCE



***
<a name="PROP_TIMERANGE"></a>
# PROP_TIMERANGE



***
<a name="PROP_SUGGESTFSAGG"></a>
# PROP_SUGGESTFSAGG



***
<a name="PROP_SUGGESTFILES"></a>
# PROP_SUGGESTFILES



***
<a name="PROP_CARDSELECTED"></a>
# PROP_CARDSELECTED



***
<a name="addAbouts"></a>
# addAbouts
addAbouts(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addAbouts&unscoped_q=addAbouts">[search for examples]</a>

***
<a name="addActionListener"></a>
# addActionListener
addActionListener( java.awt.event.ActionListener listener ) &rarr; void

Registers ActionListener to receive events.

### Parameters:
listener - The listener to register.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addActionListener&unscoped_q=addActionListener">[search for examples]</a>

***
<a name="addCancelEscapeKey"></a>
# addCancelEscapeKey
addCancelEscapeKey( javax.swing.JDialog dialog ) &rarr; void

add a listener for escape key press, which will setVisible(false) and
 clear the dialog.

### Parameters:
dialog - a JDialog

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addCancelEscapeKey&unscoped_q=addCancelEscapeKey">[search for examples]</a>

***
<a name="addCompletionKeys"></a>
# addCompletionKeys
addCompletionKeys(  ) &rarr; void

THIS MUST BE CALLED AFTER THE COMPONENT IS ADDED.  
 This is so ENTER works properly.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addCompletionKeys&unscoped_q=addCompletionKeys">[search for examples]</a>

***
<a name="addSuggestFile"></a>
# addSuggestFile
addSuggestFile( String template ) &rarr; void

show completions for this regex.

### Parameters:
template - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addSuggestFile&unscoped_q=addSuggestFile">[search for examples]</a>

***
<a name="browseSourceType"></a>
# browseSourceType
browseSourceType(  ) &rarr; void

show the initial parameters completions for the type, or the
 editor, if that's available.
 This can be called from the event thread.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=browseSourceType&unscoped_q=browseSourceType">[search for examples]</a>

browseSourceType( java.util.List problems ) &rarr; void<br>
***
<a name="getAcceptPattern"></a>
# getAcceptPattern
getAcceptPattern(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getAcceptPattern&unscoped_q=getAcceptPattern">[search for examples]</a>

***
<a name="getBrowseButton"></a>
# getBrowseButton
getBrowseButton(  ) &rarr; JButton

automated GUI testing needs access to subcomponents.
 This provides access to the inspect/browse button that when pressed enters a GUI editor to graphically work on the URI.

### Returns:
the inspect/browse button

<a href="https://github.com/autoplot/dev/search?q=getBrowseButton&unscoped_q=getBrowseButton">[search for examples]</a>

***
<a name="getBrowseTypeExt"></a>
# getBrowseTypeExt
getBrowseTypeExt(  ) &rarr; String

Getter for property browseTypeExt.

### Returns:
Value of property browseTypeExt.

<a href="https://github.com/autoplot/dev/search?q=getBrowseTypeExt&unscoped_q=getBrowseTypeExt">[search for examples]</a>

***
<a name="getDefaultRecent"></a>
# getDefaultRecent
getDefaultRecent(  ) &rarr; List



### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=getDefaultRecent&unscoped_q=getDefaultRecent">[search for examples]</a>

***
<a name="getEditor"></a>
# getEditor
getEditor(  ) &rarr; JTextField

provide direct access to the editor component.
 This should not be used, because it makes it more difficult to 
 control and define the state.  
 Use this to add listeners for example, but do not modify the value.

### Returns:
the text editor

<a href="https://github.com/autoplot/dev/search?q=getEditor&unscoped_q=getEditor">[search for examples]</a>

***
<a name="getGoButton"></a>
# getGoButton
getGoButton(  ) &rarr; JButton

automated GUI testing needs access to subcomponents.
 This provides access to the green play button that when pressed fires off a "go" event

### Returns:
the green go button

<a href="https://github.com/autoplot/dev/search?q=getGoButton&unscoped_q=getGoButton">[search for examples]</a>

***
<a name="getMessage"></a>
# getMessage
getMessage(  ) &rarr; String

Getter for property message.

### Returns:
Value of property message.

<a href="https://github.com/autoplot/dev/search?q=getMessage&unscoped_q=getMessage">[search for examples]</a>

***
<a name="getOpenLocalAction"></a>
# getOpenLocalAction
getOpenLocalAction(  ) &rarr; Action



### Returns:
javax.swing.Action


<a href="https://github.com/autoplot/dev/search?q=getOpenLocalAction&unscoped_q=getOpenLocalAction">[search for examples]</a>

***
<a name="getOpenLocalVapAction"></a>
# getOpenLocalVapAction
getOpenLocalVapAction(  ) &rarr; Action



### Returns:
javax.swing.Action


<a href="https://github.com/autoplot/dev/search?q=getOpenLocalVapAction&unscoped_q=getOpenLocalVapAction">[search for examples]</a>

***
<a name="getPromptText"></a>
# getPromptText
getPromptText(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getPromptText&unscoped_q=getPromptText">[search for examples]</a>

***
<a name="getRecent"></a>
# getRecent
getRecent(  ) &rarr; List

Getter for property recent.

### Returns:
Value of property recent.

<a href="https://github.com/autoplot/dev/search?q=getRecent&unscoped_q=getRecent">[search for examples]</a>

***
<a name="getRecentMenu"></a>
# getRecentMenu
getRecentMenu(  ) &rarr; JMenu



### Returns:
javax.swing.JMenu


<a href="https://github.com/autoplot/dev/search?q=getRecentMenu&unscoped_q=getRecentMenu">[search for examples]</a>

***
<a name="getTimeRange"></a>
# getTimeRange
getTimeRange(  ) &rarr; DatumRange

get the timerange associated with this focus dataset.  This is typically
 the same as the xaxis range.

### Returns:
the timerange associated with this focus dataset.

<a href="https://github.com/autoplot/dev/search?q=getTimeRange&unscoped_q=getTimeRange">[search for examples]</a>

***
<a name="getValue"></a>
# getValue
getValue(  ) &rarr; String

Getter for property value.
 TODO: this should really be redone, returning the value property.

### Returns:
Value of property value.

<a href="https://github.com/autoplot/dev/search?q=getValue&unscoped_q=getValue">[search for examples]</a>

***
<a name="hasActionTrigger"></a>
# hasActionTrigger
hasActionTrigger( String suri ) &rarr; boolean

return true if the action trigger would be handled.

### Parameters:
suri - the URI.

### Returns:
true if the action trigger would be handled.

<a href="https://github.com/autoplot/dev/search?q=hasActionTrigger&unscoped_q=hasActionTrigger">[search for examples]</a>

***
<a name="hideCompletions"></a>
# hideCompletions
hideCompletions(  ) &rarr; void

force hide the completions list.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=hideCompletions&unscoped_q=hideCompletions">[search for examples]</a>

***
<a name="isCardSelected"></a>
# isCardSelected
isCardSelected(  ) &rarr; boolean

added to listen to changes, but this must also be set externally to switch back.

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isCardSelected&unscoped_q=isCardSelected">[search for examples]</a>

***
<a name="isEnableDataSource"></a>
# isEnableDataSource
isEnableDataSource(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isEnableDataSource&unscoped_q=isEnableDataSource">[search for examples]</a>

***
<a name="isExpertMode"></a>
# isExpertMode
isExpertMode(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isExpertMode&unscoped_q=isExpertMode">[search for examples]</a>

***
<a name="isHidePlayButton"></a>
# isHidePlayButton
isHidePlayButton(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isHidePlayButton&unscoped_q=isHidePlayButton">[search for examples]</a>

***
<a name="isPendingChanges"></a>
# isPendingChanges
isPendingChanges(  ) &rarr; boolean

provide access to timer for GUI testing.

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isPendingChanges&unscoped_q=isPendingChanges">[search for examples]</a>

***
<a name="isPlotItButtonVisible"></a>
# isPlotItButtonVisible
isPlotItButtonVisible(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isPlotItButtonVisible&unscoped_q=isPlotItButtonVisible">[search for examples]</a>

***
<a name="isSuggestFiles"></a>
# isSuggestFiles
isSuggestFiles(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isSuggestFiles&unscoped_q=isSuggestFiles">[search for examples]</a>

***
<a name="isSuggestFsAgg"></a>
# isSuggestFsAgg
isSuggestFsAgg(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isSuggestFsAgg&unscoped_q=isSuggestFsAgg">[search for examples]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

***
<a name="maybeAddFileNotFound"></a>
# maybeAddFileNotFound
maybeAddFileNotFound( String msg ) &rarr; String

there are two places in the code where FileNotFound messages 
 are passed in with just the file name.

### Parameters:
msg - the message, which might just be the filename.

### Returns:
the message clarified.

<a href="https://github.com/autoplot/dev/search?q=maybeAddFileNotFound&unscoped_q=maybeAddFileNotFound">[search for examples]</a>

***
<a name="maybePlot"></a>
# maybePlot
maybePlot( boolean allowModifiers ) &rarr; void

if the dataset requires parameters that aren't provided, then
 show completion list.  Otherwise, fire off event.

### Parameters:
allowModifiers - turn off any modifiers like shift or control.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=maybePlot&unscoped_q=maybePlot">[search for examples]</a>

maybePlot( int keyModifiers ) &rarr; void<br>
***
<a name="pickTimeRange"></a>
# pickTimeRange
pickTimeRange( java.awt.Component parent, DatumRange timeRange1, DatumRange timeRange2 ) &rarr; DatumRange

allow the user to pick one of two times, when it is ambiguous what they want.

### Parameters:
parent - null or the component to focus.
<br>timeRange1 - a DatumRange
<br>timeRange2 - a DatumRange

### Returns:
the timerange selected.

<a href="https://github.com/autoplot/dev/search?q=pickTimeRange&unscoped_q=pickTimeRange">[search for examples]</a>

pickTimeRange( java.awt.Component parent, java.util.List timeRange, java.util.List labels ) &rarr; DatumRange<br>
***
<a name="registerActionTrigger"></a>
# registerActionTrigger
registerActionTrigger( String regex, javax.swing.Action action ) &rarr; void

This is how we allow .vap files to be in the dataSetSelector.  We register
 a pattern for which an action is invoked.

### Parameters:
regex - regular expression for the trigger.
<br>action - the action to take.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=registerActionTrigger&unscoped_q=registerActionTrigger">[search for examples]</a>

***
<a name="registerBrowseTrigger"></a>
# registerBrowseTrigger
registerBrowseTrigger( String regex, javax.swing.Action action ) &rarr; void



### Parameters:
regex - a String
<br>action - an Action

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=registerBrowseTrigger&unscoped_q=registerBrowseTrigger">[search for examples]</a>

***
<a name="removeActionListener"></a>
# removeActionListener
removeActionListener( java.awt.event.ActionListener listener ) &rarr; void

Removes ActionListener from the list of listeners.

### Parameters:
listener - The listener to remove.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeActionListener&unscoped_q=removeActionListener">[search for examples]</a>

***
<a name="replacePlayButton"></a>
# replacePlayButton
replacePlayButton( javax.swing.Icon icon, javax.swing.AbstractAction action ) &rarr; void

rather than allowing clients to add buttons, which would make
 Matisse GUI builder less useful here, clients can replace the
 behavior of the play button.

### Parameters:
icon - an Icon
<br>action - an AbstractAction

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=replacePlayButton&unscoped_q=replacePlayButton">[search for examples]</a>

***
<a name="setAcceptPattern"></a>
# setAcceptPattern
setAcceptPattern( String acceptPattern ) &rarr; void

pattern for filenames allowed.  null means anything allowed.

### Parameters:
acceptPattern - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAcceptPattern&unscoped_q=setAcceptPattern">[search for examples]</a>

***
<a name="setAlternatePeer"></a>
# setAlternatePeer
setAlternatePeer( String title, String card ) &rarr; void



### Parameters:
title - a String
<br>card - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAlternatePeer&unscoped_q=setAlternatePeer">[search for examples]</a>

***
<a name="setBrowseTypeExt"></a>
# setBrowseTypeExt
setBrowseTypeExt( String browseTypeExt ) &rarr; void

Setter for property browseTypeExt.

### Parameters:
browseTypeExt - New value of property browseTypeExt.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setBrowseTypeExt&unscoped_q=setBrowseTypeExt">[search for examples]</a>

***
<a name="setCardSelected"></a>
# setCardSelected
setCardSelected( boolean cardSelected ) &rarr; void



### Parameters:
cardSelected - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCardSelected&unscoped_q=setCardSelected">[search for examples]</a>

***
<a name="setCardSelectedNoEventKludge"></a>
# setCardSelectedNoEventKludge
setCardSelectedNoEventKludge( boolean cardSelected ) &rarr; void



### Parameters:
cardSelected - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCardSelectedNoEventKludge&unscoped_q=setCardSelectedNoEventKludge">[search for examples]</a>

***
<a name="setDefaultRecent"></a>
# setDefaultRecent
setDefaultRecent( java.util.List recent ) &rarr; void

allow clients (e.g. Autoplot) to set a list of recent that new
 instances will use.

### Parameters:
recent - the list

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDefaultRecent&unscoped_q=setDefaultRecent">[search for examples]</a>

***
<a name="setDisableDataSources"></a>
# setDisableDataSources
setDisableDataSources( boolean b ) &rarr; void

allows the dataSetSelectorComboBox to be used to select files.

### Parameters:
b - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDisableDataSources&unscoped_q=setDisableDataSources">[search for examples]</a>

***
<a name="setEnableDataSource"></a>
# setEnableDataSource
setEnableDataSource( boolean enableDataSource ) &rarr; void

delegate down to datasource when doing completions.

### Parameters:
enableDataSource - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setEnableDataSource&unscoped_q=setEnableDataSource">[search for examples]</a>

***
<a name="setEnabled"></a>
# setEnabled
setEnabled( boolean enabled ) &rarr; void



### Parameters:
enabled - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setEnabled&unscoped_q=setEnabled">[search for examples]</a>

***
<a name="setExpertMode"></a>
# setExpertMode
setExpertMode( boolean expert ) &rarr; void



### Parameters:
expert - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setExpertMode&unscoped_q=setExpertMode">[search for examples]</a>

***
<a name="setHidePlayButton"></a>
# setHidePlayButton
setHidePlayButton( boolean hidePlayButton ) &rarr; void



### Parameters:
hidePlayButton - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setHidePlayButton&unscoped_q=setHidePlayButton">[search for examples]</a>

***
<a name="setMessage"></a>
# setMessage
setMessage( String message ) &rarr; void

Setter for property message.

### Parameters:
message - New value of property message.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMessage&unscoped_q=setMessage">[search for examples]</a>

***
<a name="setMonitorFactory"></a>
# setMonitorFactory
setMonitorFactory( org.das2.system.MonitorFactory factory ) &rarr; void



### Parameters:
factory - a MonitorFactory

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMonitorFactory&unscoped_q=setMonitorFactory">[search for examples]</a>

***
<a name="setPlayButton"></a>
# setPlayButton
setPlayButton( boolean t ) &rarr; void

if this is false, then the editor dialogs will show only "okay" and
 "plot below" is hidden.

### Parameters:
t - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPlayButton&unscoped_q=setPlayButton">[search for examples]</a>

***
<a name="setPlotItButtonVisible"></a>
# setPlotItButtonVisible
setPlotItButtonVisible( boolean plotItButtonVisible ) &rarr; void



### Parameters:
plotItButtonVisible - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPlotItButtonVisible&unscoped_q=setPlotItButtonVisible">[search for examples]</a>

***
<a name="setPromptText"></a>
# setPromptText
setPromptText( String text ) &rarr; void



### Parameters:
text - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPromptText&unscoped_q=setPromptText">[search for examples]</a>

***
<a name="setRecent"></a>
# setRecent
setRecent( java.util.List recent ) &rarr; void

Setter for property recent.  Should be called from the event thread.
 This sets defaultRecent as well, so other clients can get a list of 
 recent values.

### Parameters:
recent - New value of property recent.

### Returns:
void (returns nothing)

### See Also:
<a href='#getDefaultRecent'>getDefaultRecent()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setRecent&unscoped_q=setRecent">[search for examples]</a>

***
<a name="setSuggestFiles"></a>
# setSuggestFiles
setSuggestFiles( boolean suggestFiles ) &rarr; void



### Parameters:
suggestFiles - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSuggestFiles&unscoped_q=setSuggestFiles">[search for examples]</a>

***
<a name="setSuggestFsAgg"></a>
# setSuggestFsAgg
setSuggestFsAgg( boolean suggestFsAgg ) &rarr; void



### Parameters:
suggestFsAgg - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSuggestFsAgg&unscoped_q=setSuggestFsAgg">[search for examples]</a>

***
<a name="setTimeRange"></a>
# setTimeRange
setTimeRange( DatumRange timerange ) &rarr; void

set default timeRange when aggregation is used, or for dialogs.
 null is allowed, indicating there is no focus timerange

### Parameters:
timerange - a DatumRange

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTimeRange&unscoped_q=setTimeRange">[search for examples]</a>

***
<a name="setValue"></a>
# setValue
setValue( String value ) &rarr; void

Set the current value for the editor.  This does not fire an event, 
 so call maybePlot() to accept the value.

### Parameters:
value - the new URI.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setValue&unscoped_q=setValue">[search for examples]</a>

***
<a name="showCompletions"></a>
# showCompletions
showCompletions(  ) &rarr; void

show completions, as if the scientist had hit tab

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showCompletions&unscoped_q=showCompletions">[search for examples]</a>

***
<a name="showFileSystemCompletions"></a>
# showFileSystemCompletions
showFileSystemCompletions( boolean suggestFsAgg, boolean suggestFiles, String acceptRegex ) &rarr; void

Wrap DataSetURI.getFileSystemCompletions for action triggers.

### Parameters:
suggestFsAgg - include aggregations it sees.  These are a guess.
<br>suggestFiles - include files as well as aggregations.
<br>acceptRegex - if non-null, filenames must match this regex.  See Pattern.compile

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showFileSystemCompletions&unscoped_q=showFileSystemCompletions">[search for examples]</a>

***
<a name="showUserExceptionDialog"></a>
# showUserExceptionDialog
showUserExceptionDialog( java.awt.Component parent, String msg, String title, java.lang.Exception ex, int messageType ) &rarr; void

show the message, assuming that it is something that it's something for the user to fix, but provide details button.

### Parameters:
parent - a Component
<br>msg - a String
<br>title - a String
<br>ex - an Exception
<br>messageType - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showUserExceptionDialog&unscoped_q=showUserExceptionDialog">[search for examples]</a>

