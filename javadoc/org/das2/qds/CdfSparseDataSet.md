# org.das2.qds.CdfSparseDataSetdataset for modeling when data values repeat.  Instead of storing 
 copies of the data, the get method looks up the index.  For example:
 <pre>
 ds= CdfSparseDataSet(1,200)
 ds.putValues( 0, dataset(1) )
 ds.putValues( 10, dataset(2) )
 ds.putValues( 110, dataset(3) )
 plot( ds )
 </pre>
CdfSparseDataSet( int rank, int length )
create the DataSet with the given length.

***
<a name="datasetCount"></a>
# datasetCount
datasetCount(  ) &rarr; int

return the number of different datasets.

### Returns:
the number of different datasets.

<a href="https://github.com/autoplot/dev/search?q=datasetCount&unscoped_q=datasetCount">[search for examples]</a>

***
<a name="length"></a>
# length
length(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=length&unscoped_q=length">[search for examples]</a>

length( int i0 ) &rarr; int<br>
length( int i0, int i1 ) &rarr; int<br>
length( int i0, int i1, int i2 ) &rarr; int<br>
***
<a name="putValues"></a>
# putValues
putValues( int i0, QDataSet ds ) &rarr; void

insert these values into the dataset.

### Parameters:
i0 - the insertion index, these must be inserted in order.
<br>ds - the dataset for this index and those after.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putValues&unscoped_q=putValues">[search for examples]</a>

***
<a name="rank"></a>
# rank
rank(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=rank&unscoped_q=rank">[search for examples]</a>

***
<a name="setLength"></a>
# setLength
setLength( int length ) &rarr; void

allow clients to reset the length.

### Parameters:
length - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLength&unscoped_q=setLength">[search for examples]</a>

***
<a name="slice"></a>
# slice
slice( int i0 ) &rarr; QDataSet



### Parameters:
i0 - an int

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=slice&unscoped_q=slice">[search for examples]</a>

***
<a name="trim"></a>
# trim
trim( int i0, int i1 ) &rarr; QDataSet



### Parameters:
i0 - an int
<br>i1 - an int

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=trim&unscoped_q=trim">[search for examples]</a>

***
<a name="value"></a>
# value
value( int i0 ) &rarr; double



### Parameters:
i0 - an int

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

value( int i0, int i1 ) &rarr; double<br>
value( int i0, int i1, int i2 ) &rarr; double<br>
value( int i0, int i1, int i2, int i3 ) &rarr; double<br>
