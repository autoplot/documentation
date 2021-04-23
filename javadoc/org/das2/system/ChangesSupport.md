# org.das2.system.ChangesSupportSupport class for encapsulating implementation of pendingChanges and mutator locks.
 PendingChanges are a way of notifying the bean and other clients using the bean that changes are coming to
 the bean.
 mutatorLock() is a way for a client to get exclusive, read-only access to a bean.  This also sets the valueAdjusting
 property.

 See http://das2.org/wiki/index.php/Pending_changes (Wiki was lost, but may be recoverable.)
ChangesSupport( java.beans.PropertyChangeSupport pcs, Object parent )
if the propertyChangeSupport is provided, then change messages will be sent to
 it directly.  If null, then one is created with the parent as the source.

***
<a name="PROP_PENDINGCHANGES"></a>
# PROP_PENDINGCHANGES



***
<a name="PROP_VALUEADJUSTING"></a>
# PROP_VALUEADJUSTING



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
<a name="changePerformed"></a>
# changePerformed
changePerformed( Object client, Object lockObject ) &rarr; void

the change is complete, and as far as the client is concerned, 
 the canvas is valid.

### Parameters:
client - the object that is mutating the bean.
<br>lockObject - an object identifying the change.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=changePerformed&unscoped_q=changePerformed">[search for examples]</a>

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

true if someone has registered a pending change.

### Returns:
true if someone has registered a pending change.

<a href="https://github.com/autoplot/dev/search?q=isPendingChanges&unscoped_q=isPendingChanges">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

isPendingChanges( Object lockObject ) &rarr; boolean<br>
***
<a name="isValueAdjusting"></a>
# isValueAdjusting
isValueAdjusting(  ) &rarr; boolean

true when the bean state is rapidly changing.

### Returns:
true when the bean state is rapidly changing.

<a href="https://github.com/autoplot/dev/search?q=isValueAdjusting&unscoped_q=isValueAdjusting">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mutatorLock"></a>
# mutatorLock
mutatorLock(  ) &rarr; Lock

one client will have write access to the bean, and when unlock
 is called, a "valueAdjusting" property change event is fired.
 In the future, this
 will return null if the lock is already out, but for now,
 clients should check the valueIsAdjusting property.

### Returns:
the lock or null.

<a href="https://github.com/autoplot/dev/search?q=mutatorLock&unscoped_q=mutatorLock">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="pendingChanges"></a>
# pendingChanges
pendingChanges( java.util.Map changes ) &rarr; void

return a list of all the pending changes.  These are returned in a
 Map that goes from pending change to change manager.

### Parameters:
changes - a Map to which the changes will be added.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=pendingChanges&unscoped_q=pendingChanges">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="performingChange"></a>
# performingChange
performingChange( Object client, Object lockObject ) &rarr; void

performingChange tells that the change is about to be performed.  This
 is a place holder in case we use a mutator lock, but currently does
 nothing.  If the change has not been registered, it will be registered implicitly.
 This will increment the internal count of how many times the change
 ought to occur.

### Parameters:
client - the object that is mutating the bean.
<br>lockObject - an object identifying the change.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=performingChange&unscoped_q=performingChange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="registerPendingChange"></a>
# registerPendingChange
registerPendingChange( Object client, Object lockObject ) &rarr; void

the client knows a change will be coming, and the canvas' clients should
 know that its current state will change soon.  Example pending changes
 would be:<ul>
   <li>layout because tick labels are changing
   <li>data is loading
 </ul>
 Note, it is okay to call this multiple times for the same client and lock object.

### Parameters:
client - the object that will perform the change.  This allows the
   canvas (and developers) identify who has registered the change.
<br>lockObject - object identifying the change.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=registerPendingChange&unscoped_q=registerPendingChange">[search for examples]</a>

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

