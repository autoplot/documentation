# org.autoplot.scriptconsole.LogConsole

GUI for graphically handling log records.  This defines a Handler, and has
 methods for turning off console logging. (Another class should be used to 
 log stderr and stdout messages.)  Users can dump the records to a file for
 remote analysis.

# LogConsole( )
Creates new form LogConsole

***
<a name="RECORD_SIZE_LIMIT"></a>
# RECORD_SIZE_LIMIT



***
<a name="PROP_SEARCHTEXT"></a>
# PROP_SEARCHTEXT



***
<a name="PROP_LOGSTATUS"></a>
# PROP_LOGSTATUS

status is the highest LOG Level seen in the past 300ms.

***
<a name="PROP_SHOWONLYHIGHLITED"></a>
# PROP_SHOWONLYHIGHLITED



***
<a name="PROP_SCRIPTCONTEXT"></a>
# PROP_SCRIPTCONTEXT



***
<a name="addConsoleListener"></a>
# addConsoleListener
addConsoleListener( java.awt.event.ActionListener listener ) &rarr; void

add method for listening to the console messages.  Note this
 may change!

### Parameters:
listener - an ActionListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addConsoleListener&unscoped_q=addConsoleListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getHandler"></a>
# getHandler
getHandler(  ) &rarr; Handler

create a handler that listens for log messages.  This handler is added
 to the Loggers that should be displayed here.  Also, the log levels of
 the Loggers should be set to ALL, since the filtering is done here.
 For example:
 <blockquote><pre><small>
    Handler h = lc.getHandler();
    Logger.getLogger("autoplot").setLevel(Level.ALL);
    Logger.getLogger("autoplot").addHandler(h);
</small></pre></blockquote>

### Returns:
handler for receiving messages.

<a href="https://github.com/autoplot/dev/search?q=getHandler&unscoped_q=getHandler">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLogStatus"></a>
# getLogStatus
getLogStatus(  ) &rarr; Level



### Returns:
java.util.logging.Level


<a href="https://github.com/autoplot/dev/search?q=getLogStatus&unscoped_q=getLogStatus">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getScriptContext"></a>
# getScriptContext
getScriptContext(  ) &rarr; Map



### Returns:
java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getScriptContext&unscoped_q=getScriptContext">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSearchText"></a>
# getSearchText
getSearchText(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getSearchText&unscoped_q=getSearchText">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isShowOnlyHighlited"></a>
# isShowOnlyHighlited
isShowOnlyHighlited(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isShowOnlyHighlited&unscoped_q=isShowOnlyHighlited">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="logConsoleMessages"></a>
# logConsoleMessages
logConsoleMessages(  ) &rarr; void

create loggers that log messages sent to System.err and System.out.
 This is used with turnOffConsoleHandlers.  This checks to see if
 stderr and stdout are already logging, for example when a second application
 is launched in the same jvm.

### Returns:
void (returns nothing)

### See Also:
<a href='turnOffConsoleHandlers.md'>turnOffConsoleHandlers</a> <br>

<a href="https://github.com/autoplot/dev/search?q=logConsoleMessages&unscoped_q=logConsoleMessages">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLevel"></a>
# setLevel
setLevel( int level ) &rarr; void



### Parameters:
level - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLevel&unscoped_q=setLevel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setScriptContext"></a>
# setScriptContext
setScriptContext( java.util.Map scriptContext ) &rarr; void



### Parameters:
scriptContext - a java.util.Map

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setScriptContext&unscoped_q=setScriptContext">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSearchText"></a>
# setSearchText
setSearchText( String searchText ) &rarr; void



### Parameters:
searchText - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSearchText&unscoped_q=setSearchText">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setShowLevel"></a>
# setShowLevel
setShowLevel( boolean selected ) &rarr; void



### Parameters:
selected - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setShowLevel&unscoped_q=setShowLevel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setShowLoggerId"></a>
# setShowLoggerId
setShowLoggerId( boolean selected ) &rarr; void



### Parameters:
selected - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setShowLoggerId&unscoped_q=setShowLoggerId">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setShowOnlyHighlited"></a>
# setShowOnlyHighlited
setShowOnlyHighlited( boolean showOnlyHighlited ) &rarr; void



### Parameters:
showOnlyHighlited - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setShowOnlyHighlited&unscoped_q=setShowOnlyHighlited">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setShowThreads"></a>
# setShowThreads
setShowThreads( boolean selected ) &rarr; void



### Parameters:
selected - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setShowThreads&unscoped_q=setShowThreads">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setShowTimeStamps"></a>
# setShowTimeStamps
setShowTimeStamps( boolean selected ) &rarr; void



### Parameters:
selected - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setShowTimeStamps&unscoped_q=setShowTimeStamps">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="turnOffConsoleHandlers"></a>
# turnOffConsoleHandlers
turnOffConsoleHandlers(  ) &rarr; void

iterate through the Handlers, looking for ConsoleHandlers, and turning
 them off.

### Returns:
void (returns nothing)

### See Also:
<a href='logConsoleMessages.md'>logConsoleMessages</a> <br>

<a href="https://github.com/autoplot/dev/search?q=turnOffConsoleHandlers&unscoped_q=turnOffConsoleHandlers">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="undoLogConsoleMessages"></a>
# undoLogConsoleMessages
undoLogConsoleMessages(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=undoLogConsoleMessages&unscoped_q=undoLogConsoleMessages">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="update"></a>
# update
update(  ) &rarr; void

note this is generally called from a timer that coalesces events.  But
 may be called explicitly in response to a user event as well.  
 This should be called on the event thread!

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=update&unscoped_q=update">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

