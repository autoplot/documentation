# org.das2.util.DasProgressMonitorInputStream



# DasProgressMonitorInputStream( java.io.InputStream in, ProgressMonitor monitor )
Creates a new instance of DasProgressMonitorInputStream

***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void

Adds a PropertyChangeListener to the listener list.

### Parameters:
l - The listener to add.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addRunWhenClosedRunnable"></a>
# addRunWhenClosedRunnable
addRunWhenClosedRunnable( java.lang.Runnable run ) &rarr; void

should an action be needed when the transaction is complete, for example
 closing a network connection, this can be used.

### Parameters:
run - a Runnable

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addRunWhenClosedRunnable&unscoped_q=addRunWhenClosedRunnable">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="close"></a>
# close
close(  ) &rarr; void

close resources needed and set the monitor finished flag.  If
 and runWhenClosedRunnables have been added, call them.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=close&unscoped_q=close">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getStreamLength"></a>
# getStreamLength
getStreamLength(  ) &rarr; long

the length of the stream in bytes.  Note often the length is not known,
 and it is by default 1000000.

### Returns:
length of the stream in bytes, or 10000000.

<a href="https://github.com/autoplot/dev/search?q=getStreamLength&unscoped_q=getStreamLength">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="read"></a>
# read
read(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=read&unscoped_q=read">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

read( byte[] b ) &rarr; int<br>
read( byte[] b, int off, int len ) &rarr; int<br>
***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void

Removes a PropertyChangeListener from the listener list.

### Parameters:
l - The listener to remove.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setEnableProgressPosition"></a>
# setEnableProgressPosition
setEnableProgressPosition( boolean value ) &rarr; void

disable/enable setting of progress position, true by default.  Transfer 
 rate will still be reported. This is introduced in case another agent 
 (the das2Stream reader, in particular) can set the progress position 
 more accurately.

### Parameters:
value - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setEnableProgressPosition&unscoped_q=setEnableProgressPosition">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setStreamLength"></a>
# setStreamLength
setStreamLength( long streamLength ) &rarr; void

set the length of the stream in bytes.

### Parameters:
streamLength - the length of the stream in bytes.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setStreamLength&unscoped_q=setStreamLength">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

