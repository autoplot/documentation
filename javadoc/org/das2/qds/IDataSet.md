# org.das2.qds.IDataSetrank 0,1,2,3 or 4 dataset backed by int array (4 byte signed numbers).
 Note access to the array is still done via doubles.
***
<a name="version"></a>
# version



***
<a name="addValue"></a>
# addValue
addValue( int i0, double value ) &rarr; void

add this value to the current value.

### Parameters:
i0 - the index
<br>value - the value, which is cast to this internal type.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addValue&unscoped_q=addValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addValue( int i0, int i1, double value ) &rarr; void<br>
***
<a name="capability"></a>
# capability
capability( java.lang.Class clazz ) &rarr; Object

TODO: this is untested, but is left in to demonstrate how the capability
 method should be implemented.  Clients should use this instead of
 casting the class to the capability class.

### Parameters:
clazz - the class, such as WritableDataSet.class

### Returns:
null or the capability if exists, such as WritableDataSet

<a href="https://github.com/autoplot/dev/search?q=capability&unscoped_q=capability">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="create"></a>
# create
create( int[] qube ) &rarr; IDataSet

Makes an array from array of dimension sizes.  The result will have
 rank qube.length().

### Parameters:
qube - array specifying the rank and size of each dimension

### Returns:
the array as a QDataSet

<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRank0"></a>
# createRank0
createRank0(  ) &rarr; IDataSet

create a rank 0 dataset backed by array of ints.

### Returns:
rank 0 dataset backed by double.

<a href="https://github.com/autoplot/dev/search?q=createRank0&unscoped_q=createRank0">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRank1"></a>
# createRank1
createRank1( int len0 ) &rarr; IDataSet

create a rank 1 dataset backed by array of ints.

### Parameters:
len0 - length of the dimension

### Returns:
rank 1 qube dataset of backed by array of ints.

<a href="https://github.com/autoplot/dev/search?q=createRank1&unscoped_q=createRank1">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRank2"></a>
# createRank2
createRank2( int len0, int len1 ) &rarr; IDataSet

create a rank 2 qube dataset backed by array of ints.

### Parameters:
len0 - length of the dimension
<br>len1 - length of the dimension

### Returns:
rank 2 qube dataset of backed by array of ints.

<a href="https://github.com/autoplot/dev/search?q=createRank2&unscoped_q=createRank2">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRank3"></a>
# createRank3
createRank3( int len0, int len1, int len2 ) &rarr; IDataSet

create a rank 3 qube dataset backed by array of ints.

### Parameters:
len0 - length of the dimension
<br>len1 - length of the dimension
<br>len2 - length of the dimension

### Returns:
rank 3 qube dataset of backed by array of shorts.

<a href="https://github.com/autoplot/dev/search?q=createRank3&unscoped_q=createRank3">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRank4"></a>
# createRank4
createRank4( int len0, int len1, int len2, int len3 ) &rarr; IDataSet

create a rank 4 qube dataset backed by array of ints.

### Parameters:
len0 - length of the dimension
<br>len1 - length of the dimension
<br>len2 - length of the dimension
<br>len3 - length of the dimension

### Returns:
rank 4 qube dataset of backed by array of ints.

<a href="https://github.com/autoplot/dev/search?q=createRank4&unscoped_q=createRank4">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putValue"></a>
# putValue
putValue( double value ) &rarr; void



### Parameters:
value - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putValue&unscoped_q=putValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

putValue( int i0, double value ) &rarr; void<br>
putValue( int i0, int i1, double value ) &rarr; void<br>
putValue( int i0, int i1, int i2, double value ) &rarr; void<br>
putValue( int i0, int i1, int i2, int i3, double value ) &rarr; void<br>
***
<a name="slice"></a>
# slice
slice( int i ) &rarr; QDataSet

the slice operator is better implemented here.  Presently, we
 use System.arraycopy to copy out the data, but this could be
 re-implemented along with an offset parameter so the original data
 can be used to back the data.

### Parameters:
i - the index

### Returns:
a rank N-1 slice of the data.

<a href="https://github.com/autoplot/dev/search?q=slice&unscoped_q=slice">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="trim"></a>
# trim
trim( int start, int end ) &rarr; QDataSet

trim operator copies the data into a new dataset.

### Parameters:
start - the first index
<br>end - the last index, exclusive

### Returns:
a shorter dataset of the same rank.

<a href="https://github.com/autoplot/dev/search?q=trim&unscoped_q=trim">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="value"></a>
# value
value(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

value( int i0 ) &rarr; double<br>
value( int i0, int i1 ) &rarr; double<br>
value( int i0, int i1, int i2 ) &rarr; double<br>
value( int i0, int i1, int i2, int i3 ) &rarr; double<br>
***
<a name="wrap"></a>
# wrap
wrap( int[] data, int[] qube ) &rarr; IDataSet

Wraps an array from array of dimension sizes.  The result will have
 rank qube.length().  For rank 0, data is 1-element array.

### Parameters:
data - array containing the data, with the last dimension contiguous in memory.
<br>qube - array specifying the rank and size of each dimension

### Returns:
the array as a QDataSet

<a href="https://github.com/autoplot/dev/search?q=wrap&unscoped_q=wrap">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

wrap( int[] back, int rank, int len0, int len1, int len2 ) &rarr; IDataSet<br>
wrap( int[] back, int rank, int len0, int len1, int len2, int len3 ) &rarr; IDataSet<br>
wrap( int[] back ) &rarr; IDataSet<br>
wrap( int[] back, int nx, int ny ) &rarr; IDataSet<br>
wrap( int[] back, int nx, int ny, int nz ) &rarr; IDataSet<br>
