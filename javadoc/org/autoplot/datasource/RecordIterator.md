# org.autoplot.datasource.RecordIteratorIntroduce class to hold code for iterating through any dataset.  
 This will detect the time series browse capability and streaming.
 So if the data source is already streaming, then this is trivial.  If
 not, then it will request chunks of data from the time series browse
 and handle them one chunk at a time.  And additional trim can be used,
 see constrainDepend0.
RecordIterator( String suri, DatumRange timeRange )
create a new RecordIterator for the given URI and time range.

RecordIterator( String suri, DatumRange timeRange, boolean allowStream )
create a new RecordIterator for the given URI and time range.

***
<a name="collect"></a>
# collect
collect( java.util.Iterator qds ) &rarr; QDataSet

do the opposite function, collect all the records and return a dataset.

### Parameters:
qds - a java.util.Iterator

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=collect&unscoped_q=collect">[search for examples]</a>

***
<a name="constrainDepend0"></a>
# constrainDepend0
constrainDepend0( DatumRange dr ) &rarr; void

limit the data returned such that only data within the datum range
 provided are returned.

### Parameters:
dr - the timerange.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=constrainDepend0&unscoped_q=constrainDepend0">[search for examples]</a>

***
<a name="hasNext"></a>
# hasNext
hasNext(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=hasNext&unscoped_q=hasNext">[search for examples]</a>

***
<a name="next"></a>
# next
next(  ) &rarr; QDataSet



### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=next&unscoped_q=next">[search for examples]</a>

***
<a name="remove"></a>
# remove
remove(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=remove&unscoped_q=remove">[search for examples]</a>

***
<a name="resortFields"></a>
# resortFields
resortFields( int[] sort ) &rarr; void

get a subset or rearrange the fields of each record.

### Parameters:
sort - an int[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resortFields&unscoped_q=resortFields">[search for examples]</a>

