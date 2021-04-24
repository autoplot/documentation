# org.autoplot.scriptconsole.GuiExceptionHandler

This is the original das2 Exception handler dialog, but modified to
 support submitting an error report to a server.

 The server is hard-coded to be https://jfaden.net/RTEReceiver/LargeUpload.jsp,
 TODO: add runtime property to set this.  This client will submit a file containing the
 report to the server.  The filename is a client-side calculated hash of the stack trace
 and timestamp.  The server is expecting a multi-part post, containing:
   "secret"="secret"
   "todo"="upload"
   "uploadfile"= the file to upload.
 TODO: refactor the error reporting stuff because it should be useful for headless
 applications as well.

# GuiExceptionHandler( )


***
<a name="USER_ID"></a>
# USER_ID



***
<a name="EMAIL"></a>
# EMAIL



***
<a name="FOCUS_URI"></a>
# FOCUS_URI



***
<a name="PENDING_FOCUS_URI"></a>
# PENDING_FOCUS_URI



***
<a name="APP_COUNT"></a>
# APP_COUNT



***
<a name="INCLDOM"></a>
# INCLDOM



***
<a name="INCLSCREEN"></a>
# INCLSCREEN



***
<a name="APP_MODEL"></a>
# APP_MODEL



***
<a name="UNDO_REDO_SUPPORT"></a>
# UNDO_REDO_SUPPORT



***
<a name="THROWABLE"></a>
# THROWABLE



***
<a name="BUILD_INFO"></a>
# BUILD_INFO



***
<a name="LOG_RECORDS"></a>
# LOG_RECORDS



***
<a name="formatReport"></a>
# formatReport
formatReport( java.util.Map data, boolean uncaught, String userComments ) &rarr; String

data is a map containing the keys:<ul>
 <li>THROWABLE, the throwable
 <li>BUILD_INFO, string array of human-readable build information
 <li>LOG_RECORDS, list of log records.
 <li>USER_ID, user id.
 <li>EMAIL, email.
 <li>FOCUS_URI the current focus uri.
 <li>PENDING_FOCUS_URI the pending focus uri 
 <li>APP_COUNT the number of instances running.
 <li>INCLSCREEN Boolean.TRUE if the user should include a screen shot.
 <li>APP_MODEL the application object.
 </ul>

### Parameters:
data - map of data
<br>uncaught - true if the exception was uncaught
<br>userComments - additional comments from the user.

### Returns:
the formatted report.

<a href="https://github.com/autoplot/dev/search?q=formatReport&unscoped_q=formatReport">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="handle"></a>
# handle
handle( java.lang.Throwable t ) &rarr; void



### Parameters:
t - a Throwable

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=handle&unscoped_q=handle">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="handleUncaught"></a>
# handleUncaught
handleUncaught( java.lang.Throwable t ) &rarr; void



### Parameters:
t - a Throwable

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=handleUncaught&unscoped_q=handleUncaught">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hashCode"></a>
# hashCode
hashCode( java.lang.StackTraceElement[] ee ) &rarr; int

create a hashCode identifying the stack trace location.

### Parameters:
ee - the stack trace.

### Returns:
the hash

<a href="https://github.com/autoplot/dev/search?q=hashCode&unscoped_q=hashCode">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

hashCode( java.lang.Throwable t ) &rarr; int<br>
***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="safe"></a>
# safe
safe( String s ) &rarr; String



### Parameters:
s - a String

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=safe&unscoped_q=safe">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setApplicationModel"></a>
# setApplicationModel
setApplicationModel( org.autoplot.ApplicationModel appModel ) &rarr; void



### Parameters:
appModel - an ApplicationModel

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setApplicationModel&unscoped_q=setApplicationModel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFocusURI"></a>
# setFocusURI
setFocusURI( String uri ) &rarr; void



### Parameters:
uri - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFocusURI&unscoped_q=setFocusURI">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLogConsole"></a>
# setLogConsole
setLogConsole( org.autoplot.scriptconsole.LogConsole lc ) &rarr; void



### Parameters:
lc - a LogConsole

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLogConsole&unscoped_q=setLogConsole">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setScriptPanel"></a>
# setScriptPanel
setScriptPanel( org.autoplot.scriptconsole.JythonScriptPanel scriptPanel ) &rarr; void

indicate the script panel where errors can be shown.

### Parameters:
scriptPanel - a JythonScriptPanel

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setScriptPanel&unscoped_q=setScriptPanel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setUndoRedoSupport"></a>
# setUndoRedoSupport
setUndoRedoSupport( org.autoplot.state.UndoRedoSupport undoRedoSupport ) &rarr; void



### Parameters:
undoRedoSupport - an UndoRedoSupport

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUndoRedoSupport&unscoped_q=setUndoRedoSupport">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="submitFeedback"></a>
# submitFeedback
submitFeedback( java.lang.Throwable t ) &rarr; void



### Parameters:
t - a Throwable

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=submitFeedback&unscoped_q=submitFeedback">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="submitRuntimeException"></a>
# submitRuntimeException
submitRuntimeException( java.lang.Throwable t, boolean uncaught ) &rarr; void



### Parameters:
t - a Throwable
<br>uncaught - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=submitRuntimeException&unscoped_q=submitRuntimeException">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

