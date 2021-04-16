# org.das2.qds.DDataSetrank 0,1,2,3 or 4 dataset backed by double array (8 byte real numbers).
***
<a name="version"></a>
# version



***
<a name="accumValue"></a>
# <del>accumValue</del>
Deprecated: use addValue
accumValue( int i0, int i1, double value ) &rarr; void<br>
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

addValue( int i0, int i1, double value ) &rarr; void<br>
addValue( int i0, int i1, int i2, double value ) &rarr; void<br>
***
<a name="addValues"></a>
# addValues
addValues( QDataSet ds, QDataSet wds ) &rarr; void

add all valid values of ds to this dataset.
 This does not reconcile rank, see CoerceUtil.

### Parameters:
ds - a QDataSet
<br>wds - a QDataSet

### Returns:
void (returns nothing)

### See Also:
<a href='CoerceUtil.md#coerce'>CoerceUtil#coerce(QDataSet, QDataSet, boolean, QDataSet[])</a> <br>

<a href="https://github.com/autoplot/dev/search?q=addValues&unscoped_q=addValues">[search for examples]</a>

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

***
<a name="copyElements"></a>
# copyElements
copyElements( org.das2.qds.DDataSet src, int srcpos, org.das2.qds.DDataSet dest, int destpos, int nrec ) &rarr; void

copy elements of src DDataSet into dest DDataSet, with System.arraycopy.
 src and dst must have the same geometry, except for dim 0.  Allows for
 aliasing when higher dimension element count matches.

### Parameters:
src - source dataset
<br>srcpos - source dataset first dimension index.
<br>dest - destination dataset
<br>destpos - destination dataset first dimension index.
<br>nrec - number of records to copy.  Note this is different than the other copyElements!

### Returns:
void (returns nothing)

### See Also:
<a href='#copyElements'>copyElements(org.das2.qds.DDataSet, int, org.das2.qds.DDataSet, int, int, boolean)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=copyElements&unscoped_q=copyElements">[search for examples]</a>

copyElements( org.das2.qds.DDataSet src, int srcpos, org.das2.qds.DDataSet dest, int destpos, int len, boolean checkAlias ) &rarr; void<br>
***
<a name="create"></a>
# create
create( int[] qube ) &rarr; DDataSet

Makes an array from array of dimension sizes.  The result will have
 rank qube.length().

### Parameters:
qube - array specifying the rank and size of each dimension

### Returns:
the array as a QDataSet

<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

***
<a name="createRank0"></a>
# createRank0
createRank0(  ) &rarr; DDataSet

create a rank 1 dataset backed by array of doubles.

### Returns:
rank 0 dataset backed by double.

<a href="https://github.com/autoplot/dev/search?q=createRank0&unscoped_q=createRank0">[search for examples]</a>

***
<a name="createRank1"></a>
# createRank1
createRank1( int len0 ) &rarr; DDataSet

create a rank 1 dataset backed by array of doubles.

### Parameters:
len0 - length of the dimension

### Returns:
rank 1 qube dataset of backed by array of doubles.

<a href="https://github.com/autoplot/dev/search?q=createRank1&unscoped_q=createRank1">[search for examples]</a>

***
<a name="createRank1Bins"></a>
# createRank1Bins
createRank1Bins( double min, double max, Units u ) &rarr; DDataSet

convenient method for creating DatumRanges bins datasets.

### Parameters:
min - the minumum value
<br>max - the maximum value
<br>u - the ratiometric or time location units

### Returns:
the rank1 bins dataset

<a href="https://github.com/autoplot/dev/search?q=createRank1Bins&unscoped_q=createRank1Bins">[search for examples]</a>

***
<a name="createRank2"></a>
# createRank2
createRank2( int len0, int len1 ) &rarr; DDataSet

create a rank 2 qube dataset backed by array of doubles.

### Parameters:
len0 - length of the dimension
<br>len1 - length of the dimension

### Returns:
rank 2 qube dataset of backed by array of doubles.

<a href="https://github.com/autoplot/dev/search?q=createRank2&unscoped_q=createRank2">[search for examples]</a>

***
<a name="createRank3"></a>
# createRank3
createRank3( int len0, int len1, int len2 ) &rarr; DDataSet

create a rank 3 qube dataset backed by array of doubles.

### Parameters:
len0 - length of the dimension
<br>len1 - length of the dimension
<br>len2 - length of the dimension

### Returns:
rank 3 qube dataset of backed by array of doubles.

<a href="https://github.com/autoplot/dev/search?q=createRank3&unscoped_q=createRank3">[search for examples]</a>

***
<a name="createRank4"></a>
# createRank4
createRank4( int len0, int len1, int len2, int len3 ) &rarr; DDataSet

create a rank 4 qube dataset backed by array of doubles.

### Parameters:
len0 - length of the dimension
<br>len1 - length of the dimension
<br>len2 - length of the dimension
<br>len3 - length of the dimension

### Returns:
rank 4 qube dataset of backed by array of doubles.

<a href="https://github.com/autoplot/dev/search?q=createRank4&unscoped_q=createRank4">[search for examples]</a>

***
<a name="putValue"></a>
# putValue
putValue( double value ) &rarr; void



### Parameters:
value - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putValue&unscoped_q=putValue">[search for examples]</a>

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

***
<a name="trim"></a>
# trim
trim( int start, int end ) &rarr; QDataSet



### Parameters:
start - an int
<br>end - an int

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=trim&unscoped_q=trim">[search for examples]</a>

***
<a name="value"></a>
# value
value(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

value( int i0 ) &rarr; double<br>
value( int i0, int i1 ) &rarr; double<br>
value( int i0, int i1, int i2 ) &rarr; double<br>
value( int i0, int i1, int i2, int i3 ) &rarr; double<br>
***
<a name="wrap"></a>
# wrap
wrap( double[] data, int[] qube ) &rarr; DDataSet

Wraps an array from array of dimension sizes.  The result will have
 rank qube.length().  For rank 0, data is 1-element array.

### Parameters:
data - array containing the data, with the last dimension contiguous in memory.
<br>qube - array specifying the rank and size of each dimension

### Returns:
the array as a QDataSet

<a href="https://github.com/autoplot/dev/search?q=wrap&unscoped_q=wrap">[search for examples]</a>

wrap( double[] back, int rank, int len0, int len1, int len2 ) &rarr; DDataSet<br>
wrap( double[] back ) &rarr; DDataSet<br>
wrap( double[] back, int nx, int ny ) &rarr; DDataSet<br>
wrap( double[] back, int rank, int len0, int len1, int len2, int len3 ) &rarr; DDataSet<br>
wrap( double[] xx, Units xunits ) &rarr; DDataSet<br>
***
<a name="wrapRank2"></a>
# wrapRank2
wrapRank2( double[] back, int n1 ) &rarr; DDataSet

creates a DDataSet by wrapping an existing array, and aliasing it to rank2.
 Note the last index is packed closest in memory.

### Parameters:
back - a double[]
<br>n1 - the size of the second dimension.

### Returns:
an org.das2.qds.DDataSet


<a href="https://github.com/autoplot/dev/search?q=wrapRank2&unscoped_q=wrapRank2">[search for examples]</a>

***
<a name="wrapRank3"></a>
# wrapRank3
wrapRank3( double[] back, int n1, int n2 ) &rarr; DDataSet

creates a DDataSet by wrapping an existing array, and aliasing it to rank2.
 Note the last index is packed closest in memory.  The first index length
 is calculated from the size of the array.

### Parameters:
back - a double[]
<br>n1 - the size of the second index.
<br>n2 - the size of the third index.

### Returns:
an org.das2.qds.DDataSet


<a href="https://github.com/autoplot/dev/search?q=wrapRank3&unscoped_q=wrapRank3">[search for examples]</a>

