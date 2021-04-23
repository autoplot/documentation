# org.autoplot.dom.DomNodeControllerBase class for controller objects that are responsible for managing a node.
DomNodeController( org.autoplot.dom.DomNode node )


***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
propertyName - a String
<br>listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addPropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="changePerformed"></a>
# changePerformed
changePerformed( Object client, Object lockObject ) &rarr; void

the change is complete, and as far as the client is concerned, the canvas
 is valid.

### Parameters:
client - the object that is mutating the bean.
<br>lockObject - an object identifying the change.

### Returns:
void (returns nothing)

### See Also:
<a href='#registerPendingChange'>registerPendingChange(java.lang.Object, java.lang.Object)</a> <br>
<a href='#performingChange'>performingChange(java.lang.Object, java.lang.Object)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=changePerformed&unscoped_q=changePerformed">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getController"></a>
# getController
getController( org.autoplot.dom.DomNode n ) &rarr; DomNodeController

return the controller for the node, if it exists.
 This appeared to take a significant amount of time using introspection, 
 so was recoded.  Note this is much faster, but it's trivial either way
 and this runs the risk of a future new node not being handled.
 (Test on 2016-03-14 showed 1e6 invocations of with introspection took
 ~700ms, while this took 7ms.)

### Parameters:
n - the node

### Returns:
the controller or null.

<a href="https://github.com/autoplot/dev/search?q=getController&unscoped_q=getController">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isPendingChanges"></a>
# isPendingChanges
isPendingChanges(  ) &rarr; boolean

Some sort of processing is going on, so wait until idle.

### Returns:
true if there are changes pending.

<a href="https://github.com/autoplot/dev/search?q=isPendingChanges&unscoped_q=isPendingChanges">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isValueAdjusting"></a>
# isValueAdjusting
isValueAdjusting(  ) &rarr; boolean

the application state is rapidly changing.

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isValueAdjusting&unscoped_q=isValueAdjusting">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mutatorLock"></a>
# mutatorLock
mutatorLock(  ) &rarr; DomLock

lock the node so that others cannot modify it.  Call the lock object's lock method with a name for the operation,
 then unlock it when the operation is complete.  A try/finally block should be used in case exceptions occur, otherwise
 the application will be left in an unusable state!
 <tt>
 DomLock lock = dom.controller.mutatorLock();
 lock.lock( "Sync to Application" );
    do atomic operation...
 lock.unlock()
 </tt>

### Returns:
an org.autoplot.dom.ChangesSupport.DomLock


<a href="https://github.com/autoplot/dev/search?q=mutatorLock&unscoped_q=mutatorLock">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="pendingChanges"></a>
# pendingChanges
pendingChanges( java.util.Map changes ) &rarr; void

return a list of all the pending changes.  These are returned in a
 Map that goes from pending change to change manager.  Note this will
 recurse through all the children, so to see pending changes
 for the application, just call this on its controller.

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

### Parameters:
client - the object that is mutating the bean.
<br>lockObject - an object identifying the change.

### Returns:
void (returns nothing)

### See Also:
<a href='#registerPendingChange'>registerPendingChange(java.lang.Object, java.lang.Object)</a> <br>
<a href='#changePerformed'>changePerformed(java.lang.Object, java.lang.Object)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=performingChange&unscoped_q=performingChange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="printStats"></a>
# printStats
printStats(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=printStats&unscoped_q=printStats">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="registerPendingChange"></a>
# registerPendingChange
registerPendingChange( Object client, Object lockObject ) &rarr; void

the client knows a change will be coming, and the canvas' clients should
 know that its current state will change soon.  Example pending changes
 would be:
   layout because tick labels are changing
   data is loading

### Parameters:
client - the object that will perform the change.  This allows the
   canvas (and developers) identify who has registered the change.
<br>lockObject - object identifying the change.

### Returns:
void (returns nothing)

### See Also:
<a href='#performingChange'>performingChange(java.lang.Object, java.lang.Object)</a> <br>
<a href='#changePerformed'>changePerformed(java.lang.Object, java.lang.Object)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=registerPendingChange&unscoped_q=registerPendingChange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
propertyName - a String
<br>listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

removePropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void<br>
