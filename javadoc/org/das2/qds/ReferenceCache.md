# org.das2.qds.ReferenceCacheProvide a cache of datasets that are in memory, so that the same data is not loaded twice.  This first implementation
 uses WeakReferences, so that this cache need not be emptied, but we will avoid the situation where the same data is loaded
 twice.
***
<a name="getDataSet"></a>
# getDataSet
getDataSet( String uri ) &rarr; QDataSet

Query to see if the dataset exists in the cache.  Null is returned if it is not, or a QDataSet is returned if it is.

### Parameters:
uri - the URI that can be resolved into a dataset.

### Returns:
the dataset or null

<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>

***
<a name="getDataSetOrLock"></a>
# getDataSetOrLock
getDataSetOrLock( String uri, ProgressMonitor monitor ) &rarr; ReferenceCacheEntry

Get a ReferenceCacheEntry for the URI, which will indicate the thread which has been designated as the load thread.
<blockquote><pre><small>
rcent= ReferenceCache.getInstance().getDataSetOrLock( this.tsb.getURI(), mon);
if ( !rcent.shouldILoad( Thread.currentThread() ) ) { 
   QDataSet result= rcent.park( mon );

</small></pre></blockquote>

 Be sure to use try/finally when using this cache!

### Parameters:
uri - the URI to load.
<br>monitor - to monitor the load.

### Returns:
the ReferenceCacheEntry

<a href="https://github.com/autoplot/dev/search?q=getDataSetOrLock&unscoped_q=getDataSetOrLock">[search for examples]</a>

***
<a name="getInstance"></a>
# getInstance
getInstance(  ) &rarr; ReferenceCache

get the single instance of the ReferenceCache

### Returns:
an org.das2.qds.ReferenceCache


<a href="https://github.com/autoplot/dev/search?q=getInstance&unscoped_q=getInstance">[search for examples]</a>

***
<a name="park"></a>
# park
park( org.das2.qds.ReferenceCache.ReferenceCacheEntry ent, ProgressMonitor monitor ) &rarr; void

park this thread until the other guy has finished loading.

### Parameters:
ent - a ReferenceCache.ReferenceCacheEntry
<br>monitor - the monitor of the load.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=park&unscoped_q=park">[search for examples]</a>

***
<a name="printStatus"></a>
# printStatus
printStatus(  ) &rarr; void

display the status of all the entries.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=printStatus&unscoped_q=printStatus">[search for examples]</a>

***
<a name="putDataSet"></a>
# putDataSet
putDataSet( String uri, QDataSet ds ) &rarr; void

put the dataset into the ReferenceCache.  If it is mutable, then a copy is
 made.

### Parameters:
uri - a String
<br>ds - a QDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putDataSet&unscoped_q=putDataSet">[search for examples]</a>

***
<a name="reset"></a>
# reset
reset(  ) &rarr; void

explicitly remove entries from the cache.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reset&unscoped_q=reset">[search for examples]</a>

***
<a name="tidy"></a>
# tidy
tidy(  ) &rarr; void

remove all the entries that have been garbage collected.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=tidy&unscoped_q=tidy">[search for examples]</a>

