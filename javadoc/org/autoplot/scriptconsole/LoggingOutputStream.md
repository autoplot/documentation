# org.autoplot.scriptconsole.LoggingOutputStreammakes stderr and stdout loggable.
 from http://blogs.sun.com/nickstephen/entry/java_redirecting_system_out_and
 An OutputStream that writes contents to a Logger upon each call to flush()
LoggingOutputStream( java.util.logging.Logger logger, java.util.logging.Level level )
Constructor

***
<a name="flush"></a>
# flush
flush(  ) &rarr; void

upon flush() write the existing contents of the OutputStream
 to the logger as a log record.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=flush&unscoped_q=flush">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

