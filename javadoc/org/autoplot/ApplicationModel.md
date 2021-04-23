# org.autoplot.ApplicationModelInternal model of the application to separate model from view.
 Note this is the legacy model that still remains from the first implementation
 of Autoplot, and represents the most simple application.
ApplicationModel( )


***
<a name="PROP_PROMPT"></a>
# PROP_PROMPT



***
<a name="PREF_RECENT"></a>
# PREF_RECENT



***
<a name="PROPERTY_RECENT"></a>
# PROPERTY_RECENT



***
<a name="PROPERTY_BOOKMARKS"></a>
# PROPERTY_BOOKMARKS



***
<a name="PROP_NAME"></a>
# PROP_NAME



***
<a name="PROP_VAPFILE"></a>
# PROP_VAPFILE



***
<a name="addDasPeersToApp"></a>
# addDasPeersToApp
addDasPeersToApp(  ) &rarr; void

This needs to be called after the application model is initialized and
 preferably from the event thread.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addDasPeersToApp&unscoped_q=addDasPeersToApp">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addDasPeersToAppAndWait"></a>
# addDasPeersToAppAndWait
addDasPeersToAppAndWait(  ) &rarr; void

addDasPeers should be called from the event thread.  This is intended to support old code that
 was loose about this with minimal impact on code.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addDasPeersToAppAndWait&unscoped_q=addDasPeersToAppAndWait">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addException"></a>
# addException
addException( String suri, java.lang.Exception exx ) &rarr; void

Record exceptions the same way we would record successful plots.
 This checks the system property "enableLogExceptions" and
 if "true" the exception is logged.  
 See HOME/autoplot_data/bookmarks/exceptions.txt.

### Parameters:
suri - the URI we were trying to plot.
<br>exx - the exception we got instead.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addException&unscoped_q=addException">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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
<a name="addRecent"></a>
# addRecent
addRecent( String suri ) &rarr; void

Add the URI to the recently used list, and to the user's
 autoplot_data/bookmarks/history.txt.  No interpretation is done
 and pngwalk: and script: uris are acceptable.

### Parameters:
suri - the URI to add.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addRecent&unscoped_q=addRecent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createState"></a>
# createState
createState( boolean deep ) &rarr; Application

creates an ApplicationState object representing the current state.

### Parameters:
deep - if true, do a deeper, more expensive gathering of state.  In the initial implementation, this calculates the embedded dataset.

### Returns:
ApplicationState object

<a href="https://github.com/autoplot/dev/search?q=createState&unscoped_q=createState">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="dataSource"></a>
# dataSource
dataSource(  ) &rarr; DataSource



### Returns:
org.autoplot.datasource.DataSource


<a href="https://github.com/autoplot/dev/search?q=dataSource&unscoped_q=dataSource">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="doAutoLayout"></a>
# doAutoLayout
doAutoLayout(  ) &rarr; void

trigger autolayout, which adjusts the margins so that labels aren't cut off.  Note
 LayoutListener has similar code.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=doAutoLayout&unscoped_q=doAutoLayout">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="doOpenVap"></a>
# doOpenVap
doOpenVap( java.io.File f, java.util.LinkedHashMap deltas ) &rarr; void

Load the vap file at f, apply additional modifications to the DOM, then
 sync the application to this.  Deltas with names in all caps (e.g. PWD or FILE) 
 will be applied to the vap, looking for %{PWD} or %{FILE}:
 <li>PWD will be set to the current working directory of the vap file.

### Parameters:
f - a .vap file.
<br>deltas - list property name, property value pairs to apply to the
   vap DOM after it's loaded.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=doOpenVap&unscoped_q=doOpenVap">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

doOpenVap( java.io.InputStream in, java.util.LinkedHashMap deltas ) &rarr; void<br>
***
<a name="exit"></a>
# exit
exit(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=exit&unscoped_q=exit">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCanvas"></a>
# getCanvas
getCanvas(  ) &rarr; DasCanvas



### Returns:
org.das2.graph.DasCanvas


<a href="https://github.com/autoplot/dev/search?q=getCanvas&unscoped_q=getCanvas">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSourceFilterController"></a>
# getDataSourceFilterController
getDataSourceFilterController(  ) &rarr; DataSourceController

see ScriptPanelSupport

### Returns:
an org.autoplot.dom.DataSourceController


<a href="https://github.com/autoplot/dev/search?q=getDataSourceFilterController&unscoped_q=getDataSourceFilterController">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSourceURL"></a>
# getDataSourceURL
getDataSourceURL(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getDataSourceURL&unscoped_q=getDataSourceURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDocumentModel"></a>
# getDocumentModel
getDocumentModel(  ) &rarr; Application

return the dom containing the state of this application

### Returns:
an org.autoplot.dom.Application


<a href="https://github.com/autoplot/dev/search?q=getDocumentModel&unscoped_q=getDocumentModel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getExceptionHandler"></a>
# getExceptionHandler
getExceptionHandler(  ) &rarr; ExceptionHandler



### Returns:
org.das2.util.ExceptionHandler


<a href="https://github.com/autoplot/dev/search?q=getExceptionHandler&unscoped_q=getExceptionHandler">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLegacyBookmarks"></a>
# getLegacyBookmarks
getLegacyBookmarks(  ) &rarr; List

Read the default bookmarks in, or those from the user's "bookmarks" pref node.

### Returns:
the bookmarks of the legacy user.

<a href="https://github.com/autoplot/dev/search?q=getLegacyBookmarks&unscoped_q=getLegacyBookmarks">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getName"></a>
# getName
getName(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getName&unscoped_q=getName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPrompt"></a>
# getPrompt
getPrompt(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getPrompt&unscoped_q=getPrompt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRecent"></a>
# getRecent
getRecent(  ) &rarr; List

Get the recent URIs, from autoplot_data/bookmarks/bookmarks.recent.xml

### Returns:
the recent URIs

<a href="https://github.com/autoplot/dev/search?q=getRecent&unscoped_q=getRecent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getRecent( String filter, int limit ) &rarr; Map<br>
getRecent( java.util.regex.Pattern p, int limit ) &rarr; Map<br>
***
<a name="getStylePanelMaybeCached"></a>
# getStylePanelMaybeCached
getStylePanelMaybeCached( org.autoplot.RenderType renderType ) &rarr; StylePanel

return a GUI controller for the RenderType, using a cached instance if
 available.

### Parameters:
renderType - a RenderType

### Returns:
an org.autoplot.PlotStylePanel.StylePanel


<a href="https://github.com/autoplot/dev/search?q=getStylePanelMaybeCached&unscoped_q=getStylePanelMaybeCached">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getThumbnail"></a>
# getThumbnail
getThumbnail( int height ) &rarr; BufferedImage

return a thumbnail for the state.  TODO: multiple steps produces better result.  See http://www.philreeve.com/java_high_quality_thumbnails.php

### Parameters:
height - the height in pixels

### Returns:
the thumbnail, or null if one cannot be created

<a href="https://github.com/autoplot/dev/search?q=getThumbnail&unscoped_q=getThumbnail">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getVapFile"></a>
# getVapFile
getVapFile(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getVapFile&unscoped_q=getVapFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isApplet"></a>
# isApplet
isApplet(  ) &rarr; boolean

An early version of Autoplot worked as an applet.  The applet mode
 is no longer supported.

### Returns:
true if this is an applet.

<a href="https://github.com/autoplot/dev/search?q=isApplet&unscoped_q=isApplet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isApplication"></a>
# isApplication
isApplication(  ) &rarr; boolean

Return true if this is running as an application.

### Returns:
true if this is running as an application.

<a href="https://github.com/autoplot/dev/search?q=isApplication&unscoped_q=isApplication">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isHeadless"></a>
# isHeadless
isHeadless(  ) &rarr; boolean

Return true if the application is headless.

### Returns:
true if the application is headless.

<a href="https://github.com/autoplot/dev/search?q=isHeadless&unscoped_q=isHeadless">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isRestoringState"></a>
# isRestoringState
isRestoringState(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isRestoringState&unscoped_q=isRestoringState">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isSandboxed"></a>
# isSandboxed
isSandboxed(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isSandboxed&unscoped_q=isSandboxed">[search for examples]</a>

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
<a name="restoreState"></a>
# restoreState
restoreState( org.autoplot.dom.Application state ) &rarr; void

set the application state.

### Parameters:
state - an Application

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=restoreState&unscoped_q=restoreState">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setApplet"></a>
# setApplet
setApplet( boolean v ) &rarr; void



### Parameters:
v - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setApplet&unscoped_q=setApplet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setCanvasSize"></a>
# setCanvasSize
setCanvasSize( int width, int height ) &rarr; void

set the canvas size, to the extent that this is possible.

### Parameters:
width - width in pixels
<br>height - height in pixels

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCanvasSize&unscoped_q=setCanvasSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataSet"></a>
# setDataSet
setDataSet( QDataSet ds ) &rarr; void

Just plot this dataset.  No capabilities, no URLs.  Metadata is set to
 allow inspection of dataset.

### Parameters:
ds - a dataset

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSet&unscoped_q=setDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

setDataSet( int chNum, String label, QDataSet ds ) &rarr; void<br>
setDataSet( int chNum, String label, QDataSet ds, boolean reset ) &rarr; void<br>
setDataSet( int chNum, String label, String suri ) &rarr; void<br>
***
<a name="setDataSource"></a>
# setDataSource
setDataSource( org.autoplot.datasource.DataSource dataSource ) &rarr; void



### Parameters:
dataSource - a DataSource

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSource&unscoped_q=setDataSource">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataSourceURL"></a>
# setDataSourceURL
setDataSourceURL( String suri ) &rarr; void

Plot this URI, without checking to see if the URI is valid by 
 checking reject of the data source.
 When using the AutoplotUI, it is preferable to use AutoplotUI.plotUri, 
 which will have the effect of typing in the URI and hitting the "go" 
 arrow button.

### Parameters:
suri - the URI

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSourceURL&unscoped_q=setDataSourceURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setExceptionHandler"></a>
# setExceptionHandler
setExceptionHandler( org.das2.util.ExceptionHandler eh ) &rarr; void

Set the code that will handle uncaught exceptions.  This could be a
 GUI that shows the user the problem and submits bug reports.  This could
 also simply call exit with a non-zero return code for headless use.

### Parameters:
eh - an ExceptionHandler

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setExceptionHandler&unscoped_q=setExceptionHandler">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFocus"></a>
# setFocus
setFocus( int chNum ) &rarr; void

Just set the focus to the given dataSourceFilter index.  plotElements and dataSourceFilters
 are added until the index exists.  This is introduced to support code where we reenter
 Autoplot with the position switch, and we can to then call maybePlot so that completions can
 happen.

### Parameters:
chNum - the index of the DataSourceFilter to use.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFocus&unscoped_q=setFocus">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLocation"></a>
# setLocation
setLocation( int x, int y ) &rarr; void

set the location of the application container.  This will generally
 have some small offset from the canvas.

### Parameters:
x - the upper-left corner location.
<br>y - the upper-left corner location.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLocation&unscoped_q=setLocation">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setName"></a>
# setName
setName( String name ) &rarr; void



### Parameters:
name - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setName&unscoped_q=setName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPrompt"></a>
# setPrompt
setPrompt( String prompt ) &rarr; void

Set the prompt used for command line sessions.  By default this is 
 "autoplot> ".

### Parameters:
prompt - the new one-line prompt

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPrompt&unscoped_q=setPrompt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setResizeRequestListener"></a>
# setResizeRequestListener
setResizeRequestListener( org.autoplot.ApplicationModel.ResizeRequestListener listener ) &rarr; void

set the code which will handle resize requests, for example if
 a .vap is loaded.

### Parameters:
listener - the listener.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setResizeRequestListener&unscoped_q=setResizeRequestListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRestoringState"></a>
# setRestoringState
setRestoringState( boolean b ) &rarr; void



### Parameters:
b - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRestoringState&unscoped_q=setRestoringState">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSandboxed"></a>
# setSandboxed
setSandboxed( boolean sandboxed ) &rarr; void

mark that the app is running in sandboxed mode, though note that
 this does not add the security manager.

### Parameters:
sandboxed - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSandboxed&unscoped_q=setSandboxed">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setVapFile"></a>
# setVapFile
setVapFile( String vapFile ) &rarr; void

handy property to contain the current file name.

### Parameters:
vapFile - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setVapFile&unscoped_q=setVapFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showMessage"></a>
# showMessage
showMessage( String message, String title, int messageType ) &rarr; void

Show a message to the scientist.  This will handle headless mode
 by printing to stderr.

### Parameters:
message - the message to show
<br>title - a title for the dialog
<br>messageType - JOptionPane.WARNING_MESSAGE, JOptionPane.INFORMATION_MESSAGE, JOptionPane.PLAIN_MESSAGE,

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showMessage&unscoped_q=showMessage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="waitUntilIdle"></a>
# <del>waitUntilIdle</del>
Deprecated: use waitUntilIdle() instead.
waitUntilIdle(  ) &rarr; void<br>
