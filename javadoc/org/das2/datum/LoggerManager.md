# org.das2.datum.LoggerManager

Central place that keeps track of loggers.  Note that both org.das2.util 
 and org.das2.datum have this same class, which is there to avoid coupling between the 
 packages.

# LoggerManager( )


***
<a name="getLogger"></a>
# getLogger
getLogger( String id ) &rarr; Logger

return the requested logger, but add it to the list of known loggers.

### Parameters:
id - a String

### Returns:
a java.util.logging.Logger


<a href="https://github.com/autoplot/dev/search?q=getLogger&unscoped_q=getLogger">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLoggers"></a>
# getLoggers
getLoggers(  ) &rarr; Set

return the list of known loggers.

### Returns:
a java.util.Set


<a href="https://github.com/autoplot/dev/search?q=getLoggers&unscoped_q=getLoggers">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

