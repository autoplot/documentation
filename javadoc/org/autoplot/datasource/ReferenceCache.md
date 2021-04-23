# org.autoplot.datasource.ReferenceCacheProvide a cache of datasets that are in memory, so that the same data is not 
 loaded twice.  This first implementation uses WeakReferences, so that this 
 cache need not be emptied, but we will avoid the situation where the same 
 data is loaded twice.
***
<a name="PROP_ENABLE_REFERENCE_CACHE"></a>
# PROP_ENABLE_REFERENCE_CACHE

System property the enables the reference cache.  Clients should check this before using the cache with code like:
 <code>
 boolean useReferenceCache= "true".equals( System.getProperty( ReferenceCache.PROP_ENABLE_REFERENCE_CACHE, "false" ) );
 </code>

***
<a name="NULL"></a>
# NULL

marker dataset used to indicate null was loaded for the URI.  This
 dataset should not be used.

***
<a name="getDataSet"></a>
# getDataSet
getDataSet( String uri ) &rarr; QDataSet

Query to see if the dataset exists in the cache.  Null is returned if it 
 is not, or a QDataSet is returned if it is.
 NOTE: the entry might be ReferenceCache.NULL, meaning the load resulted in no data.

### Parameters:
uri - the URI that can be resolved into a dataset.

### Returns:
the dataset or null

<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInstance"></a>
# getInstance
getInstance(  ) &rarr; ReferenceCache

get the single instance of the ReferenceCache

### Returns:
an org.autoplot.datasource.ReferenceCache


<a href="https://github.com/autoplot/dev/search?q=getInstance&unscoped_q=getInstance">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getReferenceCacheEntry"></a>
# getReferenceCacheEntry
getReferenceCacheEntry( String uri ) &rarr; ReferenceCacheEntry

return the ReferenceCacheEntry, if any, for the URI.  This is to resolve
 the ambiguity of the getDataSet call.  Typically the status of the
 entry is called.

### Parameters:
uri - the URI that can be resolved into a dataset.

### Returns:
null or the ReferenceCacheEntry.

<a href="https://github.com/autoplot/dev/search?q=getReferenceCacheEntry&unscoped_q=getReferenceCacheEntry">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="offerDataSet"></a>
# offerDataSet
offerDataSet( String uri, QDataSet ds ) &rarr; void

like putDataSet, but if no one has requested this dataset, then simply add
 it to the cache of datasets in case someone else wants it.  Be sure to call
 this before the call to putDataSet that will release the lock.

### Parameters:
uri - the URI
<br>ds - the dataset

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=offerDataSet&unscoped_q=offerDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="park"></a>
# park
park( org.autoplot.datasource.ReferenceCache.ReferenceCacheEntry ent, ProgressMonitor monitor ) &rarr; void

park this thread until the other guy has finished loading.

### Parameters:
ent - a ReferenceCache.ReferenceCacheEntry
<br>monitor - the monitor of the load.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=park&unscoped_q=park">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="printStatus"></a>
# printStatus
printStatus(  ) &rarr; void

display the status of all the entries.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=printStatus&unscoped_q=printStatus">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reset"></a>
# reset
reset(  ) &rarr; void

explicitly remove entries from the cache.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reset&unscoped_q=reset">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="tidy"></a>
# tidy
tidy(  ) &rarr; void

remove all the entries that have been garbage collected.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=tidy&unscoped_q=tidy">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

