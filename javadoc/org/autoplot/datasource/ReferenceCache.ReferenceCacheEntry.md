# org.autoplot.datasource.ReferenceCache.ReferenceCacheEntry

Keep track of the status of a load.  This keeps track of the thread that is actually
 loading the data and it's

***
<a name="exception"></a>
# exception
exception( java.lang.Exception ex ) &rarr; void

Notify the reference cache that the load resulted in an exception.
 Threads that are parked will continue

### Parameters:
ex - the exception that occurred during the load.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=exception&unscoped_q=exception">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="finished"></a>
# finished
finished( QDataSet ds ) &rarr; void

hand the dataset resulting from the completed load off to the reference cache.
 Threads that are parked will continue.  If the dataset is mutable, then a 
 copy is made.

### Parameters:
ds - null or the dataset resolved from the URI.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=finished&unscoped_q=finished">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="park"></a>
# park
park( ProgressMonitor mon ) &rarr; QDataSet

park this thread until the other guy has finished loading.

### Parameters:
mon - monitor that will monitor the load status.

### Returns:
the dataset

<a href="https://github.com/autoplot/dev/search?q=park&unscoped_q=park">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="shouldILoad"></a>
# shouldILoad
shouldILoad( java.lang.Thread t ) &rarr; boolean

query this to see if the current thread should load the resource, or just park while
 the loading thread loads the resource.

### Parameters:
t - the current thread (Thread.currentThread())

### Returns:
true if the data should be loaded.

<a href="https://github.com/autoplot/dev/search?q=shouldILoad&unscoped_q=shouldILoad">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="wasGarbageCollected"></a>
# wasGarbageCollected
wasGarbageCollected(  ) &rarr; boolean

returns true if the entry was loaded, but now has been garbage collected.

### Returns:
true if the reference was garbage collected and is no longer available.

<a href="https://github.com/autoplot/dev/search?q=wasGarbageCollected&unscoped_q=wasGarbageCollected">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

