# org.das2.util.awt.LoggingEventQueueTool for debugging event queue stuff.  This can be used to log the event
 queue, or insert breakpoints, etc.
 Toolkit.getDefaultToolkit().getSystemEventQueue().push(new LoggingEventQueue());
***
<a name="dumpPendingEvents"></a>
# dumpPendingEvents
dumpPendingEvents(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dumpPendingEvents&unscoped_q=dumpPendingEvents">[search for examples]</a>

***
<a name="getInstance"></a>
# getInstance
getInstance(  ) &rarr; LoggingEventQueue



### Returns:
org.das2.util.awt.LoggingEventQueue


<a href="https://github.com/autoplot/dev/search?q=getInstance&unscoped_q=getInstance">[search for examples]</a>

***
<a name="postEvent"></a>
# postEvent
postEvent( java.awt.AWTEvent theEvent ) &rarr; void



### Parameters:
theEvent - an AWTEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=postEvent&unscoped_q=postEvent">[search for examples]</a>
