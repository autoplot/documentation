# org.autoplot.EventThreadResponseMonitorThis utility regularly posts events on the event thread, and measures processing time.
 This should never be more than 500ms (warnLevel below).
 See org.das2.util.awt.LoggingEventQueue, which was a similar experiment from 2005.
 This now monitors the event thread for hung events.

 Bugs found: https://sourceforge.net/p/autoplot/bugs/863/
EventThreadResponseMonitor( )


***
<a name="addToMap"></a>
# addToMap
addToMap( String key, Object value ) &rarr; void

add to the information.

### Parameters:
key - see GuiExceptionManager
<br>value - an Object

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addToMap&unscoped_q=addToMap">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="dumpPendingEvents"></a>
# dumpPendingEvents
dumpPendingEvents(  ) &rarr; String

show all the events on the event thread by unqueuing and requeuing them.  This
 should not be used in production use.

### Returns:
String representation

<a href="https://github.com/autoplot/dev/search?q=dumpPendingEvents&unscoped_q=dumpPendingEvents">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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
<a name="start"></a>
# start
start(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=start&unscoped_q=start">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

