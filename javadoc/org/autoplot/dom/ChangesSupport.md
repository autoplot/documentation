# org.autoplot.dom.ChangesSupportSupport class for encapsulating implementation of pendingChanges and mutator locks.

 PendingChanges are a way of notifying the bean and other clients using the bean that changes are coming to
 the bean.  Clients should use registerPendingChange to indicate that changes are coming.
 performingChange indicates the change is in progress.  changePerformed indicates to other clients
 and the bean that the change is complete.  For example, event thread registers pending change
 and creates runnable object.  A new thread is started.  On the new thread, performingChange
 and changePerformed is called.

 mutatorLock() is a way for a client to get exclusive, read-only access to a bean.
 This also sets the valueAdjusting property.  WARNING: this is improperly implemented,
 and clients must check valueIsAdjusting to see if another lock is out.

 See http://das2.org/wiki/index.php/Pending_changes
***
<a name="PROP_PENDINGCHANGES"></a>
# PROP_PENDINGCHANGES



***
<a name="PROP_VALUEADJUSTING"></a>
# PROP_VALUEADJUSTING

null, "", or a description of the change

***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getChangesPending"></a>
# getChangesPending
getChangesPending(  ) &rarr; Map

return a map listing the pending changes.  This is a thread-safe
 read-only copy.

### Returns:
a map listing the pending changes.

<a href="https://github.com/autoplot/dev/search?q=getChangesPending&unscoped_q=getChangesPending">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isPendingChanges"></a>
# isPendingChanges
isPendingChanges(  ) &rarr; boolean

someone has registered a pending change.
 See getChangesPending.

### Returns:
true if someone has registered a pending change.

<a href="https://github.com/autoplot/dev/search?q=isPendingChanges&unscoped_q=isPendingChanges">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

isPendingChanges( Object lockObject ) &rarr; boolean<br>
***
<a name="isValueAdjusting"></a>
# isValueAdjusting
isValueAdjusting(  ) &rarr; String

Check if the bean state is rapidly changing.  This
 returns the lock message, or null if the value
 is not adjusting.

### Returns:
null or a message indicating that the value is adjusting.

<a href="https://github.com/autoplot/dev/search?q=isValueAdjusting&unscoped_q=isValueAdjusting">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

