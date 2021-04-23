# org.das2.qds.DataSetOps

Useful operations for QDataSets, such as slice2, leafTrim.
 TODO: identify which functions appear here instead of Ops.java.

# DataSetOps( )


***
<a name="DS_LENGTH_LIMIT"></a>
# DS_LENGTH_LIMIT

absolute length limit for plots.  This is used to limit the elements used in autoranging, etc.

***
<a name="applyIndex"></a>
# applyIndex
applyIndex( QDataSet ds, QDataSet indices ) &rarr; QDataSet

return the dataset with records rearranged according to indices.

### Parameters:
ds - rank N dataset, where N>0
<br>indices - rank 1 dataset, length m.

### Returns:
length m rank N dataset.
### See Also:
<a href='#applyIndex'>applyIndex(QDataSet, int, QDataSet, boolean)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=applyIndex&unscoped_q=applyIndex">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

applyIndex( QDataSet ds, int idim, QDataSet sort, boolean deps ) &rarr; WritableDataSet<br>
***
<a name="applyIndexInSitu"></a>
# applyIndexInSitu
applyIndexInSitu( org.das2.qds.WritableDataSet ds, QDataSet sort ) &rarr; void

apply the sort to the data on the zeroth dimension.  The dataset
 must be mutable, and the dataset itself is modified.  This was introduced
 to support AggregatingDataSource but should be generally useful.

### Parameters:
ds - a writable dataset that is still mutable.
<br>sort - the new sort indeces.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=applyIndexInSitu&unscoped_q=applyIndexInSitu">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="boundsContains"></a>
# boundsContains
boundsContains( QDataSet bounds, Datum xValue, Datum yValue ) &rarr; boolean

return true of the bounds overlaps with the x and y values.

### Parameters:
bounds - bounding box
<br>xValue - the x range
<br>yValue - the y range

### Returns:
true of the bounds overlap

<a href="https://github.com/autoplot/dev/search?q=boundsContains&unscoped_q=boundsContains">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bundleNames"></a>
# bundleNames
bundleNames( QDataSet bundleDs ) &rarr; String

return the names of the dataset that can be unbundled.

### Parameters:
bundleDs - a QDataSet

### Returns:
and array of the bundle names.
### See Also:
<a href='DataSetOps.md#unbundle'>DataSetOps#unbundle(QDataSet, java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=bundleNames&unscoped_q=bundleNames">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="changesDimensions"></a>
# changesDimensions
changesDimensions( String p ) &rarr; boolean

indicate if this one operator changes the dimensions.  For example, 
 |smooth doesn't change the dimensions, but fftPower and slice do.

### Parameters:
p - the filter, e.g. "|smooth"

### Returns:
true if the dimensions change.

<a href="https://github.com/autoplot/dev/search?q=changesDimensions&unscoped_q=changesDimensions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

changesDimensions( String c0, String c1 ) &rarr; boolean<br>
***
<a name="dbAboveBackgroundDim0"></a>
# dbAboveBackgroundDim0
dbAboveBackgroundDim0( QDataSet ds, double level ) &rarr; QDataSet

normalize the level-th percentile from:
   rank 1: each element (same as removeBackground1)
   rank 2: each column of the dataset
   rank 3: each column of each rank 2 dataset slice.
 There must be at least 10 elements.  If the data is already in dB, then the result is a difference.
 This is assuming the units are similar to voltage, not a power, we think,
 containing code like 20 * Math.log10( ds / background ).

### Parameters:
ds - a QDataSet
<br>level - the percentile level, e.g. 10= 10%

### Returns:
the result dataset, in dB above background.

<a href="https://github.com/autoplot/dev/search?q=dbAboveBackgroundDim0&unscoped_q=dbAboveBackgroundDim0">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="dbAboveBackgroundDim1"></a>
# dbAboveBackgroundDim1
dbAboveBackgroundDim1( QDataSet ds, double level ) &rarr; QDataSet

normalize the nth-level percentile from:<ul>
   <li>rank 1: each element 
   <li>rank 2: each row of the dataset
   <li>rank 3: each row of each rank 2 dataset slice.
 </ul>
 If the data is already in dB, then the result is a difference.
 This is assuming the units are similar to voltage, not a power, we think,
 containing code like 20 * Math.log10( ds / background ).

### Parameters:
ds - a QDataSet
<br>level - the percentile level, e.g. 10= 10%

### Returns:
the result dataset, in dB above background.

<a href="https://github.com/autoplot/dev/search?q=dbAboveBackgroundDim1&unscoped_q=dbAboveBackgroundDim1">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

dbAboveBackgroundDim1( QDataSet ds, double level, boolean power ) &rarr; QDataSet<br>
***
<a name="dependBounds"></a>
# dependBounds
dependBounds( QDataSet ds ) &rarr; QDataSet

return a bounding qube of the independent dimensions containing
 the dataset.  If r is the result of the function, then for<ul>
   <li>rank 1: r.slice(0) x bounds, r.slice(1) y bounds
   <li>rank 2 waveform: r.slice(0) x bounds, r.slice(1) y bounds
   <li>rank 2 table:r.slice(0) x bounds  r.slice(1)  DEPEND_0 bounds.
   <li>rank 3 table:r.slice(0) x bounds  r.slice(1)  DEPEND_0 bounds.
 </ul>

### Parameters:
ds - rank 1,2, or 3 dataset.

### Returns:
a bounding qube of the independent dimensions

<a href="https://github.com/autoplot/dev/search?q=dependBounds&unscoped_q=dependBounds">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="dependBoundsSimple"></a>
# dependBoundsSimple
dependBoundsSimple( QDataSet ds ) &rarr; QDataSet

return a bounding qube of the independent dimensions containing
 the dataset.  If r is the result of the function, then for<ul>
   <li>rank 1: r.slice(0) x bounds, r.slice(1) y bounds
   <li>rank 2 waveform: r.slice(0) x bounds, r.slice(1) y bounds
   <li>rank 2 table:r.slice(0) x bounds  r.slice(1)  DEPEND_0 bounds.
   <li>rank 3 table:r.slice(0) x bounds  r.slice(1)  DEPEND_0 bounds.
 </ul>
 This does not take DELTA_PLUS and DELTA_MINUS into account.
 When all the data is fill, ds[0,0] will be positive infinity.

### Parameters:
ds - a rank 1,2, or 3 dataset.

### Returns:
a bounding qube of the independent dimensions

<a href="https://github.com/autoplot/dev/search?q=dependBoundsSimple&unscoped_q=dependBoundsSimple">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="flattenBundleDescriptor"></a>
# flattenBundleDescriptor
flattenBundleDescriptor( QDataSet bundle1 ) &rarr; QDataSet

returns a bundle descriptor roughly equivalent to the BundleDescriptor
 passed in, but will describe each dataset as if it were rank 1.  This
 is useful for when the client can't work with mixed rank bundles anyway
 (like display data).

### Parameters:
bundle1 - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=flattenBundleDescriptor&unscoped_q=flattenBundleDescriptor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="flattenRank2"></a>
# flattenRank2
flattenRank2( QDataSet ds ) &rarr; QDataSet

flatten a rank 2 dataset.  The result is a n,3 dataset
 of [x,y,f].
 History:<ul>
   <li> modified for use in PW group.
   <li> missing DEPEND_1 resulted in NullPointerException, so just use 0,1,2,..,n instead and always have rank 2 result.
 </ul>

### Parameters:
ds - rank 2 table dataset

### Returns:
rank 2 dataset that is that is array of (x,y,f).

<a href="https://github.com/autoplot/dev/search?q=flattenRank2&unscoped_q=flattenRank2">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="flattenRank3"></a>
# flattenRank3
flattenRank3( QDataSet ds ) &rarr; QDataSet

flatten a rank 3 dataset.  The result is a n,4 dataset
 of [x,y,z,f], or if there are no tags just rank 1 f.

### Parameters:
ds - rank 3 table dataset

### Returns:
rank 2 dataset that is array of (x,y,z,f) or rank 1 f.

<a href="https://github.com/autoplot/dev/search?q=flattenRank3&unscoped_q=flattenRank3">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="flattenWaveform"></a>
# flattenWaveform
flattenWaveform( QDataSet ds ) &rarr; QDataSet

flatten a rank 2 dataset where the y depend variable is just an offset from the xtag.  This is
 a nice example of the advantage of using a class to represent the data: this requires no additional
 storage to handle the huge waveform.  Note the new DEPEND_0 may have different units from ds.property(DEPEND_0).

### Parameters:
ds - rank 2 waveform with tags for DEPEND_0 and offsets for DEPEND_1

### Returns:
rank 1 waveform

<a href="https://github.com/autoplot/dev/search?q=flattenWaveform&unscoped_q=flattenWaveform">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBackgroundLevel"></a>
# getBackgroundLevel
getBackgroundLevel( QDataSet ds, double level ) &rarr; QDataSet

Get the background level by sorting the data.  The result is rank one less than the input rank.

### Parameters:
ds - rank 1, 2, or rank 3 join.
<br>level - the level between 0 and 100.

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=getBackgroundLevel&unscoped_q=getBackgroundLevel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getComponentType"></a>
# getComponentType
getComponentType( QDataSet ds ) &rarr; Class

return the class type that can accurately store data in this 
 dataset.  This was motivated by DDataSets and FDataSets, but also
 IndexGenDataSets.

### Parameters:
ds - the dataset.

### Returns:
the class that can store this type.  double.class is returned when the class cannot be identified.
### See Also:
<a href='ArrayDataSet.md#create'>ArrayDataSet#create(java.lang.Class, int[])</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getComponentType&unscoped_q=getComponentType">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNthPercentileSort"></a>
# getNthPercentileSort
getNthPercentileSort( QDataSet ds, double n ) &rarr; QDataSet

returns the value from within a distribution that is the nth percentile division.  This
 returns a fill dataset (Units.dimensionless.getFillDouble()) when the data is all fill.

### Parameters:
ds - the dataset
<br>n - percent between 0 and 100.

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=getNthPercentileSort&unscoped_q=getNthPercentileSort">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="grid"></a>
# grid
grid( QDataSet ds ) &rarr; QDataSet

takes rank 2 link (x,y,z) and makes a table from it z(x,y)

### Parameters:
ds - rank 2 link (x,y,z)

### Returns:
a table from it z(x,y)

<a href="https://github.com/autoplot/dev/search?q=grid&unscoped_q=grid">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="histogram"></a>
# histogram
histogram( QDataSet ds, double min, double max, double binsize ) &rarr; QDataSet

returns a rank 1 dataset that is a histogram of the data.  Note there
 will also be in the properties:
   count, the total number of valid values.
   nonZeroMin, the smallest non-zero, positive number

### Parameters:
ds - rank N dataset
<br>min - the min of the first bin.  If min=-1 and max=-1, then automatically set the min and max.
<br>max - the max of the last bin.
<br>binsize - the size of each bin.

### Returns:
a rank 1 dataset with each bin's count.  DEPEND_0 indicates the bin locations.

<a href="https://github.com/autoplot/dev/search?q=histogram&unscoped_q=histogram">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="indexOfBundledDataSet"></a>
# indexOfBundledDataSet
indexOfBundledDataSet( QDataSet bundleDs, String name ) &rarr; int

return the index of the named bundled dataset.  This cleans up
 the name so that is contains just a Java-style identifier.  Also, ch_1 is
 always implicitly index 1.  
 Last, if safe names created from labels match that this is used. For example,
<blockquote><pre>
bds=ripplesVectorTimeSeries(100)
2==indexOfBundledDataSet( bds, "Z" ) 
</pre></blockquote>
 demonstrates its use.
 
 Last, extraneous spaces and underscores are removed to see if this will result in a match.

### Parameters:
bundleDs - a bundle dataset with the property BUNDLE_1 or DEPEND_1 having EnumerationUnits, (or BUNDLE_0 for a rank 1 dataset).
<br>name - the named dataset.

### Returns:
the index or -1 if the name is not found.

<a href="https://github.com/autoplot/dev/search?q=indexOfBundledDataSet&unscoped_q=indexOfBundledDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isProcessAsync"></a>
# isProcessAsync
isProcessAsync( String c ) &rarr; boolean

return true if the process described in c is probably a slow
 process that should be done asynchronously.  For example, do
 a long fft on a different thread and use a progress monitor.  Processes
 that take a trivial, constant amount of time should return false, and
 may be completed on the event thread,etc.

### Parameters:
c - process string, as in sprocess.

### Returns:
true if the process described in c is probably a slow process

<a href="https://github.com/autoplot/dev/search?q=isProcessAsync&unscoped_q=isProcessAsync">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="leafTrim"></a>
# leafTrim
leafTrim( QDataSet ds, int start, int end ) &rarr; MutablePropertyDataSet

pull out a subset of the dataset by reducing the number of columns in the
 last dimension.  This does not reduce rank.  This assumes the dataset has no
 row with length&gt;end.
 This is extended to support rank 4 datasets.
 TODO: This probably doesn't handle bundles property.
 TODO: slice and trim should probably be implemented here for efficiently.

### Parameters:
ds - rank 1 or more dataset
<br>start - first index to include.
<br>end - last index, exclusive

### Returns:
dataset of the same rank.

<a href="https://github.com/autoplot/dev/search?q=leafTrim&unscoped_q=leafTrim">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="makePropertiesMutable"></a>
# makePropertiesMutable
makePropertiesMutable( QDataSet dataset ) &rarr; MutablePropertyDataSet

return a dataset that has mutable properties.  If the dataset parameter already has, then the 
 dataset is returned.  If the dataset is a MutablePropertyDataSet but the immutable flag is
 set, then the dataset is wrapped to make the properties mutable.

### Parameters:
dataset - dataset

### Returns:
a MutablePropertyDataSet that is has a wrapper around the dataset, or the dataset.
### See Also:
<a href='DataSetWrapper.md'>DataSetWrapper</a> <br>

<a href="https://github.com/autoplot/dev/search?q=makePropertiesMutable&unscoped_q=makePropertiesMutable">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="makeWritable"></a>
# makeWritable
makeWritable( QDataSet dataset ) &rarr; WritableDataSet

return a dataset that is writable.  If the dataset parameter of this idempotent
 function is already writable, then the 
 dataset is returned.  If the dataset is a WritableDataSet but the immutable flag is
 set, then the a copy is returned.

### Parameters:
dataset - a QDataSet

### Returns:
a WritableDataSet that is either a copy of the read-only dataset provided, or the parameter writable dataset provided.

<a href="https://github.com/autoplot/dev/search?q=makeWritable&unscoped_q=makeWritable">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="moment"></a>
# moment
moment( QDataSet ds ) &rarr; RankZeroDataSet

performs the moment (mean,variance,etc) on the dataset.

### Parameters:
ds - rank N QDataSet.

### Returns:
rank 0 dataset of the mean.  Properties contain other stats:
   stddev, RankZeroDataSet
   validCount, Integer, the number valid measurements
   invalidCount, Integer, the number of invalid measurements

<a href="https://github.com/autoplot/dev/search?q=moment&unscoped_q=moment">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="processDataSet"></a>
# processDataSet
processDataSet( String c, QDataSet fillDs, ProgressMonitor mon ) &rarr; QDataSet

apply process to the data.  This is like sprocess, except that the component can be extracted as the first step.
 In general these can be done on the same thread (like
 slice1), but some are slow (like fftPower).  This is a copy of PlotElementController.processDataSet.

### Parameters:
c - the process string, like "bgsmx|slice0(9)|histogram()"
<br>fillDs - the input dataset.
<br>mon - a monitor for the processing

### Returns:
dataset resulting form filters.

<a href="https://github.com/autoplot/dev/search?q=processDataSet&unscoped_q=processDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeElement"></a>
# removeElement
removeElement( int[] array, int index ) &rarr; int

removes the index-th element from the array.

### Parameters:
array - length N array
<br>index - the index to remove

### Returns:
array without the element, length N-1.

<a href="https://github.com/autoplot/dev/search?q=removeElement&unscoped_q=removeElement">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="slice"></a>
# slice
slice( QDataSet ds, int dimension, int index ) &rarr; MutablePropertyDataSet

slice on the dimension.  This saves from the pain of having this branch
 all over the code.

### Parameters:
ds - the rank N data to slice.
<br>dimension - the dimension to slice, 0 is the first.
<br>index - the index to slice at.

### Returns:
the rank N-1 result.

<a href="https://github.com/autoplot/dev/search?q=slice&unscoped_q=slice">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="slice0"></a>
# slice0
slice0( QDataSet ds, int index ) &rarr; MutablePropertyDataSet

slice on the first dimension.  Note the function ds.slice(index) was
 added later and will typically be more efficient.  This will create a new
 Slice0DataSet.  
 
 DO NOT try to optimize this by calling native trim, some native slice
 implementations call this.
 
 TODO: This actually needs a bit more study, because there are codes that
 talk about not using the native slice because it copies data and they just
 want metadata.  This probably is because Slice0DataSet doesn't check for 
 immutability, and really should be copying.  This needs to be fixed, 
 making sure the result of this call is immutable, and the native slice
 really should be more efficient, always.

### Parameters:
ds - rank 1 or more dataset
<br>index - the index to slice at

### Returns:
rank 0 or more dataset.
### See Also:
<a href='QDataSet.md#slice'>QDataSet#slice(int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=slice0&unscoped_q=slice0">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="slice1"></a>
# slice1
slice1( QDataSet ds, int index ) &rarr; MutablePropertyDataSet

slice dataset operator assumes a qube dataset
 by picking the index-th element of dataset's second dimension, without
 regard to tags.

### Parameters:
ds - rank 2 or more dataset
<br>index - the index to slice at

### Returns:
rank 1 or more dataset.

<a href="https://github.com/autoplot/dev/search?q=slice1&unscoped_q=slice1">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="slice2"></a>
# slice2
slice2( QDataSet ds, int index ) &rarr; MutablePropertyDataSet

slice dataset operator assumes a qube dataset
 by picking the index-th element of dataset's second dimension, without
 regard to tags.

### Parameters:
ds - rank 3 or more dataset
<br>index - the index to slice at.

### Returns:
rank 2 or more dataset.

<a href="https://github.com/autoplot/dev/search?q=slice2&unscoped_q=slice2">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="slice3"></a>
# slice3
slice3( QDataSet ds, int index ) &rarr; MutablePropertyDataSet

slice dataset operator assumes a qube dataset
 by picking the index-th element of dataset's second dimension, without
 regard to tags.

### Parameters:
ds - rank 4 or more dataset.
<br>index - index to slice at

### Returns:
rank 3 or more dataset.

<a href="https://github.com/autoplot/dev/search?q=slice3&unscoped_q=slice3">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="sliceProperties"></a>
# sliceProperties
sliceProperties( java.util.Map properties, int sliceDimension ) &rarr; Map

we've sliced a dataset, removing an index.  move the properties.  This was Ops.sliceProperties
 For example, after slicing the zeroth dimension (time), what was DEPEND_1 is
 becomes DEPEND_0.

### Parameters:
properties - the properties to slice.
<br>sliceDimension - the dimension to slice at (0,1,2...QDataSet.MAX_HIGH_RANK)

### Returns:
the properties after the slice.

<a href="https://github.com/autoplot/dev/search?q=sliceProperties&unscoped_q=sliceProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="sliceProperties0"></a>
# sliceProperties0
sliceProperties0( int index, java.util.Map props ) &rarr; Map

method to help dataset implementations implement slice.
 2010-09-23: support rank 2 DEPEND_2 and DEPEND_3
 2010-09-23: add BINS_1 and BUNDLE_1, Slice0DataSet calls this.
 2010-02-24: BUNDLE_0 handled.
 2011-03-25: add WEIGHTS_PLANE

### Parameters:
index - the index to slice at in the zeroth index.
<br>props - the properties to slice.

### Returns:
the properties after the slice.

<a href="https://github.com/autoplot/dev/search?q=sliceProperties0&unscoped_q=sliceProperties0">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="sort"></a>
# sort
sort( QDataSet ds ) &rarr; QDataSet

returns a list of indeces that sort the dataset.  I don't like this implementation, because
 it requires that an array of Integers (not int[]) be created.  Invalid measurements are not indexed in
 the returned dataset.
 If the sort is monotonic, then the property MONOTONIC will be Boolean.TRUE.

### Parameters:
ds - rank 1 dataset, possibly containing fill.

### Returns:
indeces that sort the data.

<a href="https://github.com/autoplot/dev/search?q=sort&unscoped_q=sort">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="sprocess"></a>
# sprocess
sprocess( String c, QDataSet fillDs, ProgressMonitor mon ) &rarr; QDataSet

sprocess implements the poorly-named filters string / process string of Autoplot, allowing
 clients to "pipe" data through a chain of operations.  For example, the filters string 
 "|slice0(9)|histogram()" will slice on the ninth index and then take a histogram of that
 result.  See http://www.papco.org/wiki/index.php/DataReductionSpecs (TODO: wiki page was lost,
 which could probably be recovered.)  There's a big problem here:
 if the command is not recognized, then it is ignored.  We should probably change this,
 but the change should be at a major version change in case it breaks things.

### Parameters:
c - process string like "slice0(9)|histogram()"
<br>fillDs - The dataset loaded from the data source controller, with initial filters (like fill) applied.
<br>mon - monitor for the processing.

### Returns:
the dataset after the process string is applied.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/<a href="http://autoplot/org/developer/dataset/filters">http://autoplot/org/developer/dataset/filters</a>.md'><a href="http://autoplot.org/developer.dataset.filters">http://autoplot.org/developer.dataset.filters</a></a> <br>
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/<a href="http://autoplot/org/developer/panel_rank_reduction">http://autoplot/org/developer/panel_rank_reduction</a>.md'><a href="http://autoplot.org/developer.panel_rank_reduction">http://autoplot.org/developer.panel_rank_reduction</a></a> <br>

<a href="https://github.com/autoplot/dev/search?q=sprocess&unscoped_q=sprocess">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="suggestFillForComponentType"></a>
# suggestFillForComponentType
suggestFillForComponentType( java.lang.Class c ) &rarr; double

return a fill value that is representable by the type.

### Parameters:
c - the class type, including double.class, float.class, etc.

### Returns:
a fill value that is representable by the type.

<a href="https://github.com/autoplot/dev/search?q=suggestFillForComponentType&unscoped_q=suggestFillForComponentType">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="transpose2"></a>
# transpose2
transpose2( QDataSet ds ) &rarr; QDataSet

transpose the rank 2 qube dataset so the rows are columns and the columns are rows.

### Parameters:
ds - rank 2 Qube DataSet.

### Returns:
rank 2 Qube DataSet

<a href="https://github.com/autoplot/dev/search?q=transpose2&unscoped_q=transpose2">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="trim"></a>
# trim
trim( QDataSet ds, int offset, int len ) &rarr; MutablePropertyDataSet

reduce the number of elements in the dataset to the dim 0 indeces specified.
 This does not change the rank of the dataset.

 DO NOT try to optimize this by calling native trim, some native trim 
 implementations call this.

### Parameters:
ds - the dataset
<br>offset - the offset
<br>len - the length, (not the stop index!)

### Returns:
trimmed dataset

<a href="https://github.com/autoplot/dev/search?q=trim&unscoped_q=trim">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

trim( QDataSet dep, int start, int stop, int stride ) &rarr; MutablePropertyDataSet<br>
***
<a name="unbundle"></a>
# unbundle
unbundle( QDataSet bundleDs, String name ) &rarr; QDataSet

Extract the named bundled dataset.  For example, extract B_x from bundle of components.

### Parameters:
bundleDs - a bundle of datasets
<br>name - the name of the bundled dataset, or "ch_&lt;i&gt;" where i is the dataset number

### Returns:
the named dataset
### See Also:
<a href='#unbundle'>unbundle(QDataSet, int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=unbundle&unscoped_q=unbundle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

unbundle( QDataSet bundleDs, int ib ) &rarr; QDataSet<br>
unbundle( QDataSet bundleDs, int ib, boolean highRank ) &rarr; QDataSet<br>
***
<a name="unbundleDefaultDataSet"></a>
# unbundleDefaultDataSet
unbundleDefaultDataSet( QDataSet bundleDs ) &rarr; QDataSet

extract the dataset that is dependent on others, or the last one.  
 For example, the dataset ds[:,"x,y"] &rarr; y[:]

### Parameters:
bundleDs - a bundle of datasets

### Returns:
the default dataset
### See Also:
<a href='Schemes.md#bundleDataSet'>Schemes#bundleDataSet()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=unbundleDefaultDataSet&unscoped_q=unbundleDefaultDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

