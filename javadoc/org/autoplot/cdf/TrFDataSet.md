# org.autoplot.cdf.TrFDataSet

hacked DDataSet implementation does transpose for column major files.
 rank 1,2,or 3 dataset backed by double array.  Note this is not
 simply a transpose of DDataSet, as the name implies.  The zeroth index is 
 the same, and the remaining index are reversed.
 
 Mutable datasets warning: No dataset should be mutable once it is accessible to the
 rest of the system.  This would require clients make defensive copies which would 
 seriously degrade performance.

***
<a name="version"></a>
# version



***
<a name="append"></a>
# append
append( org.autoplot.cdf.TrFDataSet ds ) &rarr; void

append the second dataset onto this dataset.  Not thread safe!!!
 TODO: this really should return a new dataset.  Presumably this is to avoid copies, but currently it copies anyway!

### Parameters:
ds - a TrFDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=append&unscoped_q=append">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="capability"></a>
# capability
capability( java.lang.Class clazz ) &rarr; Object

TODO: this is untested, but is left in to demonstrate how the capability
 method should be implemented.  Clients should use this instead of
 casting the class to the capability class.

### Parameters:
clazz - a java.lang.Class

### Returns:
an Object


<a href="https://github.com/autoplot/dev/search?q=capability&unscoped_q=capability">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="copy"></a>
# copy
copy( QDataSet ds ) &rarr; TrFDataSet

copies the dataset into a writeable dataset, and all of its depend datasets as well.
 An optimized copy is used when the argument is a DDataSet.

### Parameters:
ds - a QDataSet

### Returns:
org.autoplot.cdf.TrFDataSet


<a href="https://github.com/autoplot/dev/search?q=copy&unscoped_q=copy">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="copyElements"></a>
# copyElements
copyElements( org.autoplot.cdf.TrFDataSet src, int srcpos, org.autoplot.cdf.TrFDataSet dest, int destpos, int len ) &rarr; void

copy elements of src DDataSet into dest DDataSet, with System.arraycopy.
 src and dst must have the same geometry, except for dim 0.  Allows for
 aliasing when higher dimension element count matches.

### Parameters:
src - a TrFDataSet
<br>srcpos - an int
<br>dest - a TrFDataSet
<br>destpos - an int
<br>len - number of records to copy.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=copyElements&unscoped_q=copyElements">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

copyElements( org.autoplot.cdf.TrFDataSet src, int srcpos, org.autoplot.cdf.TrFDataSet dest, int destpos, int len, boolean checkAlias ) &rarr; void<br>
***
<a name="create"></a>
# create
create( int[] qube ) &rarr; TrFDataSet

Makes an array from array of dimension sizes.  The result will have
 rank qube.length().

### Parameters:
qube - array specifying the rank and size of each dimension

### Returns:
DDataSet

<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRank1"></a>
# createRank1
createRank1( int len0 ) &rarr; TrFDataSet



### Parameters:
len0 - an int

### Returns:
org.autoplot.cdf.TrFDataSet


<a href="https://github.com/autoplot/dev/search?q=createRank1&unscoped_q=createRank1">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRank2"></a>
# createRank2
createRank2( int len0, int len1 ) &rarr; TrFDataSet



### Parameters:
len0 - an int
<br>len1 - an int

### Returns:
org.autoplot.cdf.TrFDataSet


<a href="https://github.com/autoplot/dev/search?q=createRank2&unscoped_q=createRank2">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRank3"></a>
# createRank3
createRank3( int len0, int len1, int len2 ) &rarr; TrFDataSet



### Parameters:
len0 - an int
<br>len1 - an int
<br>len2 - an int

### Returns:
org.autoplot.cdf.TrFDataSet


<a href="https://github.com/autoplot/dev/search?q=createRank3&unscoped_q=createRank3">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRank4"></a>
# createRank4
createRank4( int len0, int len1, int len2, int len3 ) &rarr; TrFDataSet



### Parameters:
len0 - an int
<br>len1 - an int
<br>len2 - an int
<br>len3 - an int

### Returns:
org.autoplot.cdf.TrFDataSet


<a href="https://github.com/autoplot/dev/search?q=createRank4&unscoped_q=createRank4">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="join"></a>
# <del>join</del>
Deprecated: use append instead.
***
<a name="length"></a>
# length
length(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=length&unscoped_q=length">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

length( int i ) &rarr; int<br>
length( int i0, int i1 ) &rarr; int<br>
length( int i0, int i1, int i2 ) &rarr; int<br>
***
<a name="maybeCopy"></a>
# maybeCopy
maybeCopy( QDataSet ds ) &rarr; TrFDataSet

Copy the dataset to a DDataSet only if the dataset is not already a DDataSet.

### Parameters:
ds - a QDataSet

### Returns:
an org.autoplot.cdf.TrFDataSet


<a href="https://github.com/autoplot/dev/search?q=maybeCopy&unscoped_q=maybeCopy">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putLength"></a>
# putLength
putLength( int len ) &rarr; void

Shorten the dataset by changing it's dim 0 length parameter.  The same backing array is used, 
 so the element that remain ill be the same.
 can only shorten!

### Parameters:
len - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putLength&unscoped_q=putLength">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putProperty"></a>
# putProperty
putProperty( String name, Object value ) &rarr; void



### Parameters:
name - a String
<br>value - an Object

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putProperty&unscoped_q=putProperty">[search for examples]</a>

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
<a name="rank"></a>
# rank
rank(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=rank&unscoped_q=rank">[search for examples]</a>

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
<a name="trim"></a>
# trim
trim( int start, int end ) &rarr; QDataSet

trim operator copies the data into a new dataset.

### Parameters:
start - an int
<br>end - an int

### Returns:
a QDataSet


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
wrap( float[] data, int[] qube ) &rarr; TrFDataSet

Wraps an array from array of dimension sizes.  The result will have
 rank qube.length().

### Parameters:
data - array containing the data, with the last dimension contiguous in memory.
<br>qube - array specifying the rank and size of each dimension

### Returns:
DDataSet

<a href="https://github.com/autoplot/dev/search?q=wrap&unscoped_q=wrap">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

wrap( float[] back ) &rarr; TrFDataSet<br>
wrap( float[] back, int nx, int ny ) &rarr; TrFDataSet<br>
wrap( float[] back, int rank, int len0, int len1, int len2 ) &rarr; TrFDataSet<br>
wrap( float[] back, int rank, int len0, int len1, int len2, int len3 ) &rarr; TrFDataSet<br>
***
<a name="wrapRank2"></a>
# wrapRank2
wrapRank2( float[] back, int n1 ) &rarr; TrFDataSet

creates a DDataSet by wrapping an existing array, and aliasing it to rank2.
 Note the last index is packed closest in memory.

### Parameters:
back - a float[]
<br>n1 - the size of the second dimension.

### Returns:
org.autoplot.cdf.TrFDataSet


<a href="https://github.com/autoplot/dev/search?q=wrapRank2&unscoped_q=wrapRank2">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="wrapRank3"></a>
# wrapRank3
wrapRank3( float[] back, int n1, int n2 ) &rarr; TrFDataSet

creates a DDataSet by wrapping an existing array, and aliasing it to rank2.
 Note the last index is packed closest in memory.  The first index length
 is calculated from the size of the array.

### Parameters:
back - a float[]
<br>n1 - the size of the second index.
<br>n2 - the size of the third index.

### Returns:
org.autoplot.cdf.TrFDataSet


<a href="https://github.com/autoplot/dev/search?q=wrapRank3&unscoped_q=wrapRank3">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

