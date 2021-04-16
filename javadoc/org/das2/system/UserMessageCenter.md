# org.das2.system.UserMessageCenter
***
<a name="getDefault"></a>
# getDefault
getDefault(  ) &rarr; UserMessageCenter



### Returns:
org.das2.system.UserMessageCenter


<a href="https://github.com/autoplot/dev/search?q=getDefault&unscoped_q=getDefault">[search for examples]</a>

***
<a name="notifyUser"></a>
# notifyUser
notifyUser( Object source, String message ) &rarr; void

Notify the user of the message, coalescing redundant messages from the same
 source, etc.

### Parameters:
source - an Object
<br>message - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=notifyUser&unscoped_q=notifyUser">[search for examples]</a>

notifyUser( Object source, java.lang.Throwable e ) &rarr; void<br>
