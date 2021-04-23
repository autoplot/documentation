***
<a name="safeName"></a>
# safeName
safeName( String suggest ) &rarr; String

made a Java-style identifier from the provided string
 See Autoplot/src/scripts/safeName.jy which demonstrates this.

### Parameters:
suggest - a name, possibly containing spaces and illegal characters

### Returns:
a Java-style identifier

<a href="https://github.com/autoplot/dev/search?q=safeName&unscoped_q=safeName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="saferName"></a>
# saferName
saferName( String suggest ) &rarr; String

extra spaces and pipes cause problems in the Operations text field.  Provide so that data sources can provide
 safer names, while we test safe-name requirements on a broader test set.  Use of this method will allow us to see
 where changes are needed.  TODO: where is this used?

### Parameters:
suggest - a name, possibly containing pipes (|)

### Returns:
suggest, but with pipe converted to underscore.

<a href="https://github.com/autoplot/dev/search?q=saferName&unscoped_q=saferName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="sawtooth"></a>
# sawtooth
sawtooth( QDataSet t ) &rarr; QDataSet

generates a sawtooth from the tags, where a peak occurs with a period 2*PI.
 All values of T should be ge zero.  TODO: I think there should be a modp 
 function that is always positive. (-93 % 10 &rarr;7 though...)

### Parameters:
t - the independent values

### Returns:
/|/|/| sawtooth wave with a period of 2 PI.

<a href="https://github.com/autoplot/dev/search?q=sawtooth&unscoped_q=sawtooth">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="shortarr"></a>
# shortarr
shortarr( int len0 ) &rarr; QDataSet

create a dataset filled with zeros, stored in 2-byte signed shorts.
 Note that shortarr is equivalent to intarr in IDL, containing integer
 values from -32768 to 32767.

### Parameters:
len0 - the zeroth dimension length

### Returns:
rank 1 dataset filled with zeros.
### See Also:
<a href='Ops_z.md#zeros'>zeros(int)</a> <br>
<a href='Ops_d.md#dblarr'>dblarr(int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=shortarr&unscoped_q=shortarr">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

shortarr( int len0, int len1 ) &rarr; QDataSet<br>
shortarr( int len0, int len1, int len2 ) &rarr; QDataSet<br>
***
<a name="shuffle"></a>
# shuffle
shuffle( QDataSet ds ) &rarr; QDataSet

returns a rank 1 dataset of indeces that shuffle the rank 1 dataset ds
<blockquote><pre>
s= shuffle( ds )
dsShuffled= ds[s]
</pre></blockquote>

### Parameters:
ds - rank 1 dataset

### Returns:
rank 1 dataset of integer indeces.
### See Also:
<a href='Ops_s.md#sort'>sort(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=shuffle&unscoped_q=shuffle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

shuffle( Object ds ) &rarr; QDataSet<br>
***
<a name="signum"></a>
# signum
signum( QDataSet ds1 ) &rarr; QDataSet

Returns the signum function of the argument; zero if the argument is 
 zero, 1.0 if the argument is greater than zero, -1.0 if the argument 
 is less than zero.

### Parameters:
ds1 - a QDataSet

### Returns:
a QDataSet

### See Also:
<a href='Ops_c.md#copysign'>copysign</a> <br>
<a href='Ops_n.md#negate'>negate</a> <br>

<a href="https://github.com/autoplot/dev/search?q=signum&unscoped_q=signum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

signum( double x ) &rarr; double<br>
signum( Object x ) &rarr; QDataSet<br>
***
<a name="sin"></a>
# sin
sin( QDataSet ds ) &rarr; QDataSet

element-wise sin.

### Parameters:
ds - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=sin&unscoped_q=sin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

sin( double ds ) &rarr; double<br>
sin( Object ds ) &rarr; QDataSet<br>
***
<a name="sinh"></a>
# sinh
sinh( QDataSet ds ) &rarr; QDataSet

element-wise sinh.

### Parameters:
ds - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=sinh&unscoped_q=sinh">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

sinh( double ds ) &rarr; double<br>
sinh( Object ds ) &rarr; QDataSet<br>
***
<a name="size"></a>
# size
size( QDataSet ds ) &rarr; int

returns the number of elements in each index.  E.g:
<blockquote><pre>
 ds= zeros(3,4)
 print size(ds) # returns "3,4"
 </pre></blockquote>
 Note datasets need not have the same number of elements in each record.
 This is often the case however, and a "qube" dataset has this property.

### Parameters:
ds - a qube dataset.

### Returns:
the array containing number of elements in each index.

<a href="https://github.com/autoplot/dev/search?q=size&unscoped_q=size">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="slice0"></a>
# slice0
slice0( QDataSet ds, int idx ) &rarr; QDataSet



### Parameters:
ds - the rank N (N&gt;0) or more dataset
<br>idx - the index

### Returns:
rank N-1 dataset
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/QDataSet_s.md#slice'>QDataSet#slice(int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=slice0&unscoped_q=slice0">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

slice0( QDataSet ds, QDataSet sliceds ) &rarr; QDataSet<br>
***
<a name="slice1"></a>
# slice1
slice1( QDataSet ds, int idx ) &rarr; QDataSet



### Parameters:
ds - a QDataSet
<br>idx - an int

### Returns:
a QDataSet

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/DataSetOps_s.md#slice1'>org.das2.qds.DataSetOps#slice1(QDataSet, int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=slice1&unscoped_q=slice1">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

slice1( QDataSet ds, QDataSet sliceds ) &rarr; QDataSet<br>
***
<a name="slice2"></a>
# slice2
slice2( QDataSet ds, int idx ) &rarr; QDataSet



### Parameters:
ds - a QDataSet
<br>idx - an int

### Returns:
a QDataSet

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/DataSetOps_s.md#slice2'>org.das2.qds.DataSetOps#slice2(QDataSet, int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=slice2&unscoped_q=slice2">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

slice2( QDataSet ds, QDataSet sliceds ) &rarr; QDataSet<br>
***
<a name="slice3"></a>
# slice3
slice3( QDataSet ds, int idx ) &rarr; QDataSet



### Parameters:
ds - a QDataSet
<br>idx - an int

### Returns:
a QDataSet

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/DataSetOps_s.md#slice3'>org.das2.qds.DataSetOps#slice3(QDataSet, int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=slice3&unscoped_q=slice3">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

slice3( QDataSet ds, QDataSet sliceds ) &rarr; QDataSet<br>
***
<a name="slices"></a>
# slices
slices( QDataSet ds, java.lang.Object[] args ) &rarr; QDataSet

slice each dimension in one call, so that chaining isn't required to slice multiple dimensions at once.

### Parameters:
ds - the dataset
<br>args - varargs list of integers that are slice indeces, or "" or ":" to mean don't slice

### Returns:
the dataset with slices performed.

<a href="https://github.com/autoplot/dev/search?q=slices&unscoped_q=slices">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="smooth"></a>
# smooth
smooth( QDataSet ds, int size ) &rarr; QDataSet

run boxcar average over the dataset, returning a dataset of same geometry.  Points near the edge are simply copied from the
 source dataset.  The result dataset contains a property "weights" that is the weights for each point.  
 
 For rank 2 datasets, the smooth is done on the zeroth dimension, typically time.  Note IDL does the smooth 
 in both X and Y.

### Parameters:
ds - a rank 1 or rank 2 dataset of length N
<br>size - the number of adjacent bins to average

### Returns:
rank 1 or rank 2 dataset of length N
### See Also:
<a href='Ops_s.md#smooth2d'>smooth2d(QDataSet, int, int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=smooth&unscoped_q=smooth">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

smooth( Object ds, int size ) &rarr; QDataSet<br>
***
<a name="smooth1"></a>
# smooth1
smooth1( QDataSet ds, int size ) &rarr; QDataSet

smooth over the first dimension (not the zeroth).  For example,
 for ds[Time,Energy], this will smooth over energy.

### Parameters:
ds - rank 2 dataset.
<br>size - the boxcar size

### Returns:
smoothed dataset with the same geometry.

<a href="https://github.com/autoplot/dev/search?q=smooth1&unscoped_q=smooth1">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="smooth2d"></a>
# smooth2d
smooth2d( QDataSet ds, int n0, int n1 ) &rarr; QDataSet

smooth in both the first and second dimensions.  Presently, this just calls smooth and then smooth1.

### Parameters:
ds - rank 2 data
<br>n0 - the boxcar size in the first dimension
<br>n1 - the boxcar size in the second dimension

### Returns:
data with the same geometry
### See Also:
<a href='Ops_s.md#smooth'>smooth(QDataSet, int)</a> <br>
<a href='Ops_s.md#smooth1'>smooth1(QDataSet, int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=smooth2d&unscoped_q=smooth2d">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="smoothFit"></a>
# smoothFit
smoothFit( QDataSet xx, QDataSet yy, int size ) &rarr; QDataSet

run boxcar average over the dataset, returning a dataset of same geometry.  
 Points near the edge are fit to a line and replaced.  The result dataset 
 contains a property "weights" that is the weights for each point.

### Parameters:
xx - a rank 1 dataset of size N
<br>yy - a rank 1 dataset of size N
<br>size - the number of adjacent bins to average.  If size is greater than yy.length, size is reset to yy.length.

### Returns:
rank 1 dataset of size N

<a href="https://github.com/autoplot/dev/search?q=smoothFit&unscoped_q=smoothFit">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

smoothFit( Object xx, Object yy, int size ) &rarr; QDataSet<br>
***
<a name="sort"></a>
# sort
sort( QDataSet ds ) &rarr; QDataSet

returns a rank 1 dataset of indeces that sort the rank 1 dataset ds.
 This is not the dataset sorted.  For example:
<blockquote><pre>
ds= randn(2000)
s= sort( ds )
dsSorted= ds[s]
</pre></blockquote>
 Note the result will have the property MONOTONIC==Boolean.TRUE if 
 the data was sorted already.

### Parameters:
ds - rank 1 dataset

### Returns:
rank 1 dataset of indeces that sort the input dataset.
### See Also:
<a href='Ops_s.md#shuffle'>shuffle(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=sort&unscoped_q=sort">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

sort( Object ds ) &rarr; QDataSet<br>
***
<a name="sortInTime"></a>
# sortInTime
sortInTime( QDataSet ds ) &rarr; QDataSet

pick out the timetags and sort the data based on these.  This
 only works when a dataset has DEPEND_0.

### Parameters:
ds - a QDataSet

### Returns:
the data sorted by DEPEND_0.

<a href="https://github.com/autoplot/dev/search?q=sortInTime&unscoped_q=sortInTime">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="sqrt"></a>
# sqrt
sqrt( QDataSet ds ) &rarr; QDataSet

element-wise sqrt.  See Ops.pow to square a number.

### Parameters:
ds - the dataset

### Returns:
the square root of the dataset, which will contain NaN where the data is negative.
### See Also:
<a href='Ops_p.md#pow'>pow(QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=sqrt&unscoped_q=sqrt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

sqrt( double ds1 ) &rarr; double<br>
sqrt( Object ds1 ) &rarr; QDataSet<br>
***
<a name="square"></a>
# square
square( QDataSet t ) &rarr; QDataSet

generates a square from the tags, where a the signal is 1 from 0-PI, 0 from PI-2*PI, etc.

### Parameters:
t - the independent values.

### Returns:
square wave with a period of 2 PI.

<a href="https://github.com/autoplot/dev/search?q=square&unscoped_q=square">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="stddev"></a>
# stddev
stddev( Object o ) &rarr; QDataSet



### Parameters:
o - an Object

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=stddev&unscoped_q=stddev">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

stddev( QDataSet ds ) &rarr; QDataSet<br>
***
<a name="strarr"></a>
# strarr
strarr( int len0 ) &rarr; QDataSet

return a QDataSet containing empty strings.  This is used in Jython to create
 an array-like dataset where different strings are assigned after the array
 is made.

### Parameters:
len0 - the number of elements.

### Returns:
QDataSet with EnumerationUnits and all elements containing the value for "".

<a href="https://github.com/autoplot/dev/search?q=strarr&unscoped_q=strarr">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

strarr( int len0, int len1 ) &rarr; QDataSet<br>
***
<a name="subset"></a>
# subset
subset( QDataSet ds, QDataSet w ) &rarr; QDataSet

return the data at the indices given.  This will be a rank 1 QDataSet.
 Often the indices are created with the "where" function, for example:
 <code>
 QDataSet r= Ops.subset( ds, Ops.where( Ops.gt( ds, 1 ) ) )
 </code>
 will return the subset of ds where ds is greater than 1.

### Parameters:
ds - rank N array, N &gt; 0.
<br>w - rank 1 dataset of length l indexing a rank 1 array, or rank 2 ds[l,N] indexing a rank N array.

### Returns:
rank 1 indeces.
### See Also:
<a href='Ops_a.md#applyIndex'>applyIndex(QDataSet, QDataSet)</a> applyIndex, which does the same thing.<br>

<a href="https://github.com/autoplot/dev/search?q=subset&unscoped_q=subset">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="subtract"></a>
# subtract
subtract( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

subtract one dataset from another.

### Parameters:
ds1 - a rank N dataset
<br>ds2 - a rank M dataset with compatible geometry

### Returns:
the element-wise difference of the two datasets.

<a href="https://github.com/autoplot/dev/search?q=subtract&unscoped_q=subtract">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

subtract( Object ds1, Object ds2 ) &rarr; QDataSet<br>
***
<a name="synchronize"></a>
# synchronize
synchronize( QDataSet ds1, QDataSet ds ) &rarr; QDataSet

The first dataset's timetags are used to 
 synchronize the second dataset to a set of common timetags. Presently,
 only interpolation is used, but other methods may be introduced soon.
 Note that when one of the dataset's DEPEND_0 is not monotonic, a 
 monotonic subset of its points will be used.
 Ordinal units use the nearest neighbor interpolation.

### Parameters:
ds1 - the dataset providing timetags, or the timetags themselves.
<br>ds - the single datasets to synch up.

### Returns:
the single dataset evaluated at the other dataset's timetags.
### See Also:
<a href='Ops_s.md#synchronizeNN'>synchronizeNN(QDataSet, QDataSet)</a> <br>
<a href='Ops_s.md#synchronize'>synchronize(QDataSet, QDataSet...)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=synchronize&unscoped_q=synchronize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

synchronize( QDataSet dsTarget, org.das2.qds.QDataSet[] dsSources ) &rarr; List<br>
***
<a name="synchronizeNN"></a>
# synchronizeNN
synchronizeNN( QDataSet ds1, QDataSet ds ) &rarr; QDataSet

The first dataset's timetags are used to 
 synchronize the second dataset to a set of common timetags, using
 nearest neighbor interpolation. 
 Note that when one of the dataset's DEPEND_0 is not monotonic, a 
 monotonic subset of its points will be used.
 Ordinal units use the nearest neighbor interpolation.

### Parameters:
ds1 - the dataset providing timetags, or the timetags themselves.
<br>ds - the single datasets to synch up.

### Returns:
the single dataset evaluated at the other dataset's timetags.
### See Also:
<a href='Ops_s.md#synchronize'>synchronize(QDataSet, QDataSet)</a> <br>
<a href='Ops_s.md#synchronizeNN'>synchronizeNN(QDataSet, QDataSet...)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=synchronizeNN&unscoped_q=synchronizeNN">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

synchronizeNN( QDataSet ds1, org.das2.qds.QDataSet[] dss ) &rarr; List<br>
***
<a name="synchronizeOne"></a>
# synchronizeOne
synchronizeOne( QDataSet dsTarget, QDataSet dsSource ) &rarr; QDataSet

The first dataset's timetags are used to 
 synchronize the single dataset to common timetags. Presently,
 data from dsSource will be interpolated to create data at dsTarget timetag
 locations, but other methods may be introduced soon.
 Ordinal units use the nearest neighbor interpolation.

### Parameters:
dsTarget - the dataset providing timetags, or the timetags themselves.
<br>dsSource - the dataset to synch up.  Its timetags must be monotonically increasing and non-repeating.

### Returns:
the one dataset, synchronized.
### See Also:
<a href='Ops_s.md#synchronize'>synchronize(QDataSet, QDataSet...)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=synchronizeOne&unscoped_q=synchronizeOne">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

