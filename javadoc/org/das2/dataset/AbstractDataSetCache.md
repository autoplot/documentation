# org.das2.dataset.AbstractDataSetCacheKeeps keep track of cache statistics and to give consistent
 log messages, and provides the Entry class.
AbstractDataSetCache( )


***
<a name="hits"></a>
# hits



***
<a name="misses"></a>
# misses



***
<a name="coalese"></a>
# coalese
coalese( java.util.List result ) &rarr; DataSet

return the DataSet described by the set of DataSets if possible.

### Parameters:
result - a java.util.List

### Returns:
org.das2.dataset.DataSet


<a href="https://github.com/autoplot/dev/search?q=coalese&unscoped_q=coalese">[search for examples]</a>

***
<a name="haveStored"></a>
# haveStored
haveStored( org.das2.dataset.DataSetDescriptor dsd, org.das2.datum.CacheTag cacheTag ) &rarr; boolean



### Parameters:
dsd - a DataSetDescriptor
<br>cacheTag - a CacheTag

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=haveStored&unscoped_q=haveStored">[search for examples]</a>

***
<a name="isResetCache"></a>
# isResetCache
isResetCache(  ) &rarr; boolean

Getter for property resetCache.

### Returns:
Value of property resetCache.

<a href="https://github.com/autoplot/dev/search?q=isResetCache&unscoped_q=isResetCache">[search for examples]</a>

***
<a name="reset"></a>
# reset
reset(  ) &rarr; void

reset the internal state of the cache

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reset&unscoped_q=reset">[search for examples]</a>

***
<a name="retrieve"></a>
# retrieve
retrieve( org.das2.dataset.DataSetDescriptor dsd, org.das2.datum.CacheTag cacheTag ) &rarr; DataSet



### Parameters:
dsd - a DataSetDescriptor
<br>cacheTag - a CacheTag

### Returns:
org.das2.dataset.DataSet


<a href="https://github.com/autoplot/dev/search?q=retrieve&unscoped_q=retrieve">[search for examples]</a>

***
<a name="setResetCache"></a>
# setResetCache
setResetCache( boolean resetCache ) &rarr; void

Setter for property resetCache.

### Parameters:
resetCache - New value of property resetCache.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setResetCache&unscoped_q=setResetCache">[search for examples]</a>

***
<a name="store"></a>
# store
store( org.das2.dataset.DataSetDescriptor dsd, org.das2.datum.CacheTag cacheTag, org.das2.dataset.DataSet data ) &rarr; void



### Parameters:
dsd - a DataSetDescriptor
<br>cacheTag - a CacheTag
<br>data - a DataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=store&unscoped_q=store">[search for examples]</a>

