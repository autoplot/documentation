# org.das2.dataset.NullDataSetCache

DataSetCache that does no caching at all.  This is useful for batch
 mode or when dataset caching is undesirable.

# NullDataSetCache( )


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

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reset"></a>
# reset
reset(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reset&unscoped_q=reset">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

