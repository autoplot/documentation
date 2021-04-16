# org.das2.qds.DataSetIteratorIterator for accessing each value of a dataset.
 See http://jfaden.net:8080/hudson/job/autoplot-test037/ws/dataSetIterator.jy
***
<a name="createEmptyDs"></a>
# createEmptyDs
createEmptyDs(  ) &rarr; DDataSet

return a dataset that will have the same geometry at the
 dataset implied by each dimension iterator.  This is
 introduced to encapsulate this dangerous code to here where it could
 be done correctly.  Right now this assumes QUBES.

 Do not pass the result of this into the putValue of this iterator,
 the result should have its own iterator.

### Returns:
a dataset that will have the same geometry at the
 dataset implied by each dimension iterator.
### See Also:
<a href='QubeDataSetIterator.md#createEmptyDs'>QubeDataSetIterator#createEmptyDs()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=createEmptyDs&unscoped_q=createEmptyDs">[search for examples]</a>

***
<a name="getValue"></a>
# getValue
getValue( QDataSet ds ) &rarr; double

get the value from ds at the current iterator position.

### Parameters:
ds - a dataset with compatible geometry as the iterator's geometry.

### Returns:
the value of ds at the current iterator position.

<a href="https://github.com/autoplot/dev/search?q=getValue&unscoped_q=getValue">[search for examples]</a>

***
<a name="hasNext"></a>
# hasNext
hasNext(  ) &rarr; boolean

return true while the iterator has a next element.

### Returns:
true while the iterator has a next element.

<a href="https://github.com/autoplot/dev/search?q=hasNext&unscoped_q=hasNext">[search for examples]</a>

***
<a name="index"></a>
# index
index( int dim ) &rarr; int

return the current index for the dimension.

### Parameters:
dim - the dimension number (0&lt;=dim&lt;inputRank)

### Returns:
the current index.

<a href="https://github.com/autoplot/dev/search?q=index&unscoped_q=index">[search for examples]</a>

***
<a name="length"></a>
# length
length( int dim ) &rarr; int

return the length of the dimension, or the length reported by the 
 iterator.  Use caution, because this does not imply that the result 
 of the iteration is a qube and does not account for slices.  (TODO:
 does this mean that as we iterate through, the length depends on the
 current index?)

### Parameters:
dim - the dimension number (0&lt;=dim&lt;inputRank)

### Returns:
the length of the dimension

<a href="https://github.com/autoplot/dev/search?q=length&unscoped_q=length">[search for examples]</a>

***
<a name="next"></a>
# next
next(  ) &rarr; void

iterate to the next position.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=next&unscoped_q=next">[search for examples]</a>

***
<a name="putValue"></a>
# putValue
putValue( org.das2.qds.WritableDataSet ds, double v ) &rarr; void

replace the value in ds at the current iterator position.

### Parameters:
ds - a writable dataset with compatible geometry as the iterator's geometry.
<br>v - the value to insert.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putValue&unscoped_q=putValue">[search for examples]</a>

***
<a name="rank"></a>
# rank
rank(  ) &rarr; int

return the rank of the dataset which the iterator will walk through.
 Note this needn't be the same rank as the dataset!  For example,
 when QubeDataSetIterator walks through ds[:,0,:], the rank is 2 even 
 though ds is rank 3.

### Returns:
the rank of the dataset which the iterator will walk through.

<a href="https://github.com/autoplot/dev/search?q=rank&unscoped_q=rank">[search for examples]</a>

