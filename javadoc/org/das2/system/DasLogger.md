# org.das2.system.DasLogger



# DasLogger( )


***
<a name="DISABLE_RELOAD"></a>
# DISABLE_RELOAD



***
<a name="APPLICATION_LOG"></a>
# APPLICATION_LOG

messages having to do with the application-specific Das 2 Application

***
<a name="SYSTEM_LOG"></a>
# SYSTEM_LOG

system messages such as RequestProcessor activity

***
<a name="GUI_LOG"></a>
# GUI_LOG

events, gestures, user feedback

***
<a name="GRAPHICS_LOG"></a>
# GRAPHICS_LOG

renders, drawing

***
<a name="RENDERER_LOG"></a>
# RENDERER_LOG

renderer's logger

***
<a name="DATA_OPERATIONS_LOG"></a>
# DATA_OPERATIONS_LOG

rebinning  and dataset operators

***
<a name="DATA_TRANSFER_LOG"></a>
# DATA_TRANSFER_LOG

internet transactions, file I/O

***
<a name="FILESYSTEM_LOG"></a>
# FILESYSTEM_LOG

virtual file system activities

***
<a name="DASML_LOG"></a>
# DASML_LOG

das2 application description files

***
<a name="addHandlerToAll"></a>
# addHandlerToAll
addHandlerToAll( java.util.logging.Handler h ) &rarr; void



### Parameters:
h - a Handler

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addHandlerToAll&unscoped_q=addHandlerToAll">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDebugLogger"></a>
# getDebugLogger
getDebugLogger(  ) &rarr; Logger

logger for messages to developers

### Returns:
java.util.logging.Logger


<a href="https://github.com/autoplot/dev/search?q=getDebugLogger&unscoped_q=getDebugLogger">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLogger"></a>
# getLogger
getLogger(  ) &rarr; Logger

logger for messages to end users

### Returns:
java.util.logging.Logger


<a href="https://github.com/autoplot/dev/search?q=getLogger&unscoped_q=getLogger">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getLogger( org.das2.system.LoggerId loggerId ) &rarr; Logger<br>
getLogger( org.das2.system.LoggerId loggerId, String identifier ) &rarr; Logger<br>
***
<a name="printStatus"></a>
# printStatus
printStatus(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=printStatus&unscoped_q=printStatus">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reload"></a>
# reload
reload(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reload&unscoped_q=reload">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeAllHandlers"></a>
# removeAllHandlers
removeAllHandlers(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeAllHandlers&unscoped_q=removeAllHandlers">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setUpHandler"></a>
# setUpHandler
setUpHandler( String name ) &rarr; void

add the one handler to all...

### Parameters:
name - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUpHandler&unscoped_q=setUpHandler">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

