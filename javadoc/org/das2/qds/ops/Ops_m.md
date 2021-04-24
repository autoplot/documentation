***
<a name="magnitude"></a>
# magnitude
magnitude( QDataSet ds ) &rarr; QDataSet

return the magnitudes of vectors in a rank 1 or greater dataset (typically
 rank 2).  The last index should be the cartesian dimension.  For example,
<blockquote><pre><small>
 ds= getDataSet('http://autoplot.org/data/autoplot.cdf?BGSM') # BGSM[Epoch=24,cart=3]
 m= magnitude(ds)
</small></pre></blockquote>
 For rank 0, this just returns the absolute value, but with the same units.

### Parameters:
ds - dataset of Rank N.

### Returns:
dataset of Rank N-1.
### See Also:
<a href='Ops_a.md#abs'>abs(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=magnitude&unscoped_q=magnitude">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

magnitude( Object ds1 ) &rarr; QDataSet<br>
***
<a name="maybeCopy"></a>
# maybeCopy
maybeCopy( QDataSet ads0 ) &rarr; WritableDataSet

Copy the dataset to an ArrayDataSet only if the dataset is not already an ArrayDataSet
 or BufferDataSet.
 Note this does not consider the mutability of the data.  If the dataset is not mutable, then the
 original data could be returned (probably).

### Parameters:
ads0 - a dataset.

### Returns:
an ArrayDataSet or BufferDataSet

<a href="https://github.com/autoplot/dev/search?q=maybeCopy&unscoped_q=maybeCopy">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mean"></a>
# mean
mean( QDataSet ds ) &rarr; QDataSet

Mean function that returns the average of the valid elements of a rank N dataset

### Parameters:
ds - rank N dataset

### Returns:
rank 0 dataset
### See Also:
<a href='Ops_m.md#mode'>mode</a> <br>
<a href='Ops_m.md#median'>median</a> <br>
<a href='Ops_v.md#variance'>variance(QDataSet)</a> <br>
<a href='Ops_m.md#meanAverageDeviation'>meanAverageDeviation(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=mean&unscoped_q=mean">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

mean( Object o ) &rarr; QDataSet<br>
***
<a name="meanAverageDeviation"></a>
# meanAverageDeviation
meanAverageDeviation( QDataSet ds ) &rarr; QDataSet

return the Mean Average Deviation (MAD) of the rank N dataset.  
 The result will contain the USER_PROPERTIES with a map containing 
 the mean and number of points.

### Parameters:
ds - the rank N dataset.

### Returns:
the rank 0 mean average deviation of the dataset.
### See Also:
<a href='Ops_m.md#mean'>mean(QDataSet)</a> <br>
<a href='BinAverage_b.md#binMeanAverageDeviation'>BinAverage#binMeanAverageDeviation(QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=meanAverageDeviation&unscoped_q=meanAverageDeviation">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="median"></a>
# median
median( Object o ) &rarr; QDataSet



### Parameters:
o - an Object

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=median&unscoped_q=median">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

median( QDataSet ds ) &rarr; QDataSet<br>
***
<a name="medianFilter"></a>
# medianFilter
medianFilter( QDataSet ds, int size ) &rarr; QDataSet

1-D median filter with a boxcar of the given size.  The first size/2
 elements, and the last size/2 elements are copied from the input.

### Parameters:
ds - rank 1 or rank 2 dataset.  Future implementations may support higher rank data.
<br>size - the boxcar size

### Returns:
rank 1 or rank 2 dataset.
### See Also:
<a href='Ops_s.md#smooth'>smooth(QDataSet, int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=medianFilter&unscoped_q=medianFilter">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="merge"></a>
# merge
merge( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

Merge the two sorted rank N datasets, using their DEPEND_0 datasets, into one rank N dataset.  
 If neither dataset has DEPEND_0, then this will use the datasets themselves.  When ds1 occurs "before" ds2, then this 
 is the same as concatenate.
 When there is a collision where two data points are coincident, use ds1[j].  This is fuzzy, based on the depend_0 cadence of ds1.
 When ds1 is null (or None), use ds2.
 Thanks to: http://stackoverflow.com/questions/5958169/how-to-merge-two-sorted-arrays-into-a-sorted-array

### Parameters:
ds1 - rank N dataset, or null.
<br>ds2 - rank N dataset

### Returns:
dataset of rank N with elements interleaved.
### See Also:
<a href='Ops_c.md#concatenate'>concatenate(QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=merge&unscoped_q=merge">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mod"></a>
# mod
mod( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

element-wise mod of two datasets with compatible geometry.
 This should support Units.t2000 mod "24 hours" to get result in hours.

### Parameters:
ds1 - the numerator
<br>ds2 - the divisor

### Returns:
the remainder after the division

<a href="https://github.com/autoplot/dev/search?q=mod&unscoped_q=mod">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

mod( Object ds1, Object ds2 ) &rarr; QDataSet<br>
***
<a name="mode"></a>
# mode
mode( QDataSet ds ) &rarr; QDataSet

return the most frequently occurring element of the valid elements of a rank N dataset

### Parameters:
ds - rank N dataset.

### Returns:
the rank 0 dataset
### See Also:
<a href='Ops_m.md#mean'>mean</a> <br>
<a href='Ops_m.md#median'>median</a> <br>

<a href="https://github.com/autoplot/dev/search?q=mode&unscoped_q=mode">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="modp"></a>
# modp
modp( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

element-wise mod of two datasets with compatible geometry.  This returns
 a positive number for -18 % 10.  This is Python's behavior.
 This should support Units.t2000 mod "24 hours" to get result in hours.

### Parameters:
ds1 - the numerator
<br>ds2 - the divisor

### Returns:
the remainder after the division

<a href="https://github.com/autoplot/dev/search?q=modp&unscoped_q=modp">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

modp( Object ds1, Object ds2 ) &rarr; QDataSet<br>
***
<a name="monotonicSubset"></a>
# monotonicSubset
monotonicSubset( QDataSet ds ) &rarr; MutablePropertyDataSet

ensure that there are no non-monotonic or repeat records, by removing
 the first N-1 records of N repeated records.  
 
 Warning: this was extracted from AggregatingDataSource to support BufferDataSets,
 and is minimally implemented.
 
 When ds has property QDataSet.DEPEND_0, then this is used to identify the
 monotonic subset.  When ds is a set of timetags, then these are used.

### Parameters:
ds - MutablePropertyDataSet, which must be writable.

### Returns:
dataset, possibly with records removed.

<a href="https://github.com/autoplot/dev/search?q=monotonicSubset&unscoped_q=monotonicSubset">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="multiply"></a>
# multiply
multiply( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

element-wise multiply of two datasets with compatible geometry.
 Presently, either ds1 or ds2 should be dimensionless.
 TODO: units improvements.

### Parameters:
ds1 - a QDataSet
<br>ds2 - a QDataSet

### Returns:
a QDataSet

### See Also:
<a href='Ops_m.md#multiplyUnits'>multiplyUnits</a> <br>

<a href="https://github.com/autoplot/dev/search?q=multiply&unscoped_q=multiply">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

multiply( Object ds1, Object ds2 ) &rarr; QDataSet<br>
