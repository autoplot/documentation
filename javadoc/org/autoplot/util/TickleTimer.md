# org.autoplot.util.TickleTimer

TickleTimer is a timer that fires once it's been left alone for 
 a while.  The idea is the keyboard can be pecked away and 
 the change event will not be fired until the keyboard is idle.

 java.util.Timer performs very similar functionality.

# TickleTimer( long delay, java.beans.PropertyChangeListener listener )


***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void



### Parameters:
l - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMessages"></a>
# getMessages
getMessages(  ) &rarr; List



### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=getMessages&unscoped_q=getMessages">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isRunning"></a>
# isRunning
isRunning(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isRunning&unscoped_q=isRunning">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void



### Parameters:
l - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="tickle"></a>
# tickle
tickle(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=tickle&unscoped_q=tickle">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

tickle( String message ) &rarr; void<br>
