# org.das2.util.DasProgressMonitorReadableByteChannel



# DasProgressMonitorReadableByteChannel( java.nio.channels.ReadableByteChannel in, ProgressMonitor monitor )
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
<a name="close"></a>
# close
close(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=close&unscoped_q=close">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getStreamLength"></a>
# getStreamLength
getStreamLength(  ) &rarr; long

Getter for property taskSize.

### Returns:
Value of property taskSize.

<a href="https://github.com/autoplot/dev/search?q=getStreamLength&unscoped_q=getStreamLength">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isOpen"></a>
# isOpen
isOpen(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isOpen&unscoped_q=isOpen">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="read"></a>
# read
read( java.nio.ByteBuffer dst ) &rarr; int



### Parameters:
dst - a ByteBuffer

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=read&unscoped_q=read">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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
setStreamLength( long taskSize ) &rarr; void

Setter for property taskSize.

### Parameters:
taskSize - New value of property taskSize.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setStreamLength&unscoped_q=setStreamLength">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

