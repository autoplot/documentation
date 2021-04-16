# org.das2.util.LoggerManagerCentral place that keeps track of loggers.  Note that both org.das.datum 
 and org.das2.datum have this same class, which is there to avoid coupling between the 
 packages.
LoggerManager( )


***
<a name="addHandlerToAll"></a>
# addHandlerToAll
addHandlerToAll( java.util.logging.Handler handler ) &rarr; void

Add the handler to all loggers created by this manager, and all
 future.  Only call this once!  I would think that adding a handler to 
 the root would essentially add the handler to all loggers, but it doesn't 
 seem to.

### Parameters:
handler - e.g. GraphicalLogHandler

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addHandlerToAll&unscoped_q=addHandlerToAll">[search for examples]</a>

***
<a name="clearTimer"></a>
# clearTimer
clearTimer(  ) &rarr; void

explicitly remove this timer.

### Returns:
void (returns nothing)

### See Also:
<a href='#resetTimer'>resetTimer()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=clearTimer&unscoped_q=clearTimer">[search for examples]</a>

***
<a name="getLogger"></a>
# getLogger
getLogger( String id ) &rarr; Logger

return the requested logger, but add it to the list of known loggers.

### Parameters:
id - the name

### Returns:
the Logger

<a href="https://github.com/autoplot/dev/search?q=getLogger&unscoped_q=getLogger">[search for examples]</a>

***
<a name="getLoggers"></a>
# getLoggers
getLoggers(  ) &rarr; Set

return the list of known loggers.

### Returns:
the list of known loggers.

<a href="https://github.com/autoplot/dev/search?q=getLoggers&unscoped_q=getLoggers">[search for examples]</a>

***
<a name="isEnableTimers"></a>
# isEnableTimers
isEnableTimers(  ) &rarr; boolean

return enableTimers property.

### Returns:
enableTimers property.

<a href="https://github.com/autoplot/dev/search?q=isEnableTimers&unscoped_q=isEnableTimers">[search for examples]</a>

***
<a name="isUseTimeTaggingLoggers"></a>
# isUseTimeTaggingLoggers
isUseTimeTaggingLoggers(  ) &rarr; boolean

are we keeping track of log message times, so we can sort loggers by 
 how recently messages were posted?

### Returns:
true if we are keeping track of log message times.

<a href="https://github.com/autoplot/dev/search?q=isUseTimeTaggingLoggers&unscoped_q=isUseTimeTaggingLoggers">[search for examples]</a>

***
<a name="logExitGuiEvent"></a>
# logExitGuiEvent
logExitGuiEvent( java.awt.event.ActionEvent e ) &rarr; void

call this at the end of the GUI event to measure time to respond.

### Parameters:
e - the focus event.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=logExitGuiEvent&unscoped_q=logExitGuiEvent">[search for examples]</a>

logExitGuiEvent( javax.swing.event.ChangeEvent e ) &rarr; void<br>
logExitGuiEvent( java.awt.event.ItemEvent e ) &rarr; void<br>
logExitGuiEvent( java.awt.event.FocusEvent e ) &rarr; void<br>
***
<a name="logGuiEvent"></a>
# logGuiEvent
logGuiEvent( java.awt.event.ActionEvent e ) &rarr; void

provide easy way to log all GUI events.

### Parameters:
e - an ActionEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=logGuiEvent&unscoped_q=logGuiEvent">[search for examples]</a>

logGuiEvent( javax.swing.event.ChangeEvent e ) &rarr; void<br>
logGuiEvent( java.awt.event.ItemEvent e ) &rarr; void<br>
logGuiEvent( java.awt.event.FocusEvent e ) &rarr; void<br>
***
<a name="logPropertyChangeEvent"></a>
# logPropertyChangeEvent
logPropertyChangeEvent( java.beans.PropertyChangeEvent e ) &rarr; void

log property change events.  (I realized I spend a lot of time debugging walking 
 through the property change fire event code, and I should just add a 
 log message to all propertyChange codes.)

### Parameters:
e - a PropertyChangeEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=logPropertyChangeEvent&unscoped_q=logPropertyChangeEvent">[search for examples]</a>

logPropertyChangeEvent( java.beans.PropertyChangeEvent e, String source ) &rarr; void<br>
***
<a name="markTime"></a>
# markTime
markTime(  ) &rarr; void

mark the time using the thread name.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=markTime&unscoped_q=markTime">[search for examples]</a>

markTime( String message ) &rarr; void<br>
***
<a name="readConfiguration"></a>
# readConfiguration
readConfiguration(  ) &rarr; void

A slightly more transparent logging configuration would provide feedback
 about what configuration file it's loading.  This will echo
 when the configuration file would be.
 
 The idea is when you are completely frustrated with not getting the logger
 to behave, you can add:
 org.das2.util.LoggerManager.readConfiguration() 
 to your code.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=readConfiguration&unscoped_q=readConfiguration">[search for examples]</a>

readConfiguration( String configfile ) &rarr; void<br>
***
<a name="resetTimer"></a>
# resetTimer
resetTimer(  ) &rarr; void

reset the timer.  The lifecycle is like so:<ul>
 <li>LoggerManager.setTimerLogfile("/tmp/mylogfile.txt") 
 <li>LoggerManager.resetTimer("big task");
 <li>LoggerManager.markTime("done loading");
 <li>LoggerManager.markTime("calculated data");
 <li>LoggerManager.clearTimer();  
 </ul>
 Note the timers are stored with weak references to the threads, so 
 clearTimer needn't be called.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resetTimer&unscoped_q=resetTimer">[search for examples]</a>

resetTimer( String task ) &rarr; void<br>
***
<a name="setEnableTimers"></a>
# setEnableTimers
setEnableTimers( boolean enableTimers ) &rarr; void

if enableTimers is true, then resetTimer and markTime have 
 an effect.  Each thread can have a timer to measure the execution 
 time for a process.

### Parameters:
enableTimers - true to enable timers

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setEnableTimers&unscoped_q=setEnableTimers">[search for examples]</a>

***
<a name="setTimerLogfile"></a>
# setTimerLogfile
setTimerLogfile( String f ) &rarr; void

channel the logging information to here, setEnableTimers(false) to close.

### Parameters:
f - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTimerLogfile&unscoped_q=setTimerLogfile">[search for examples]</a>

***
<a name="setUseTimeTaggingLoggers"></a>
# setUseTimeTaggingLoggers
setUseTimeTaggingLoggers( boolean t ) &rarr; void



### Parameters:
t - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUseTimeTaggingLoggers&unscoped_q=setUseTimeTaggingLoggers">[search for examples]</a>

