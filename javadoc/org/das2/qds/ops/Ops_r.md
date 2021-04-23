***
<a name="rand"></a>
# <del>rand</del>
Deprecated: use randu instead
rand( int len0 ) &rarr; QDataSet<br>
rand( int len0, int len1 ) &rarr; QDataSet<br>
rand( int len0, int len1, int len2 ) &rarr; QDataSet<br>
***
<a name="randn"></a>
# randn
randn(  ) &rarr; QDataSet

return a rank 0 dataset of random numbers of a Gaussian (normal) distribution.

### Returns:
a rank 0 dataset of random numbers of a Gaussian (normal) distribution.

<a href="https://github.com/autoplot/dev/search?q=randn&unscoped_q=randn">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

randn( int len0 ) &rarr; QDataSet<br>
randn( int len0, int len1 ) &rarr; QDataSet<br>
randn( int len0, int len1, int len2 ) &rarr; QDataSet<br>
randn( int len0, int len1, int len2, int len3 ) &rarr; QDataSet<br>
***
<a name="randomSeed"></a>
# randomSeed
randomSeed(  ) &rarr; long

restart the random sequence used by randu and randn.  Note if there
 if there are multiple threads using random functions, this becomes 
 unpredictable.

### Returns:
the seed is returned.

<a href="https://github.com/autoplot/dev/search?q=randomSeed&unscoped_q=randomSeed">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

randomSeed( long seed ) &rarr; long<br>
***
<a name="randomn"></a>
# randomn
randomn( long seed ) &rarr; QDataSet

returns a rank 0 dataset of random numbers of a Gaussian (normal) distribution.
 System.currentTimeMillis() may be used for the seed.  Note this is unlike
 the IDL randomn function because the seed is not modified.  (Any long parameter in Jython
 and Java is read-only.)
 System.currentTimeMillis() may be used for the seed.

### Parameters:
seed - basis for the random number (which will not be modified).

### Returns:
rank 0 dataset

<a href="https://github.com/autoplot/dev/search?q=randomn&unscoped_q=randomn">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

randomn( long seed, int len0 ) &rarr; QDataSet<br>
randomn( long seed, int len0, int len1 ) &rarr; QDataSet<br>
randomn( long seed, int len0, int len1, int len2 ) &rarr; QDataSet<br>
randomn( long seed, int len0, int len1, int len2, int len3 ) &rarr; QDataSet<br>
***
<a name="randomu"></a>
# randomu
randomu( long seed ) &rarr; QDataSet

returns a rank 0 dataset of random numbers of a uniform distribution.
 System.currentTimeMillis() may be used for the seed.  Note this is unlike
 the IDL randomn function because the seed is not modified.  (Any long parameter in Jython
 and Java is read-only.)

### Parameters:
seed - basis for the random number (which will not be modified).

### Returns:
a rank 0 dataset of random uniform numbers from 0 to 1 but not including 1.

<a href="https://github.com/autoplot/dev/search?q=randomu&unscoped_q=randomu">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

randomu( long seed, int len0 ) &rarr; QDataSet<br>
randomu( long seed, int len0, int len1 ) &rarr; QDataSet<br>
randomu( long seed, int len0, int len1, int len2 ) &rarr; QDataSet<br>
randomu( long seed, int len0, int len1, int len2, int len3 ) &rarr; QDataSet<br>
***
<a name="randu"></a>
# randu
randu(  ) &rarr; QDataSet

returns a rank 0 dataset of random uniform numbers from 0 to 1 but not including 1.

### Returns:
a rank 0 dataset of random uniform numbers from 0 to 1 but not including 1.

<a href="https://github.com/autoplot/dev/search?q=randu&unscoped_q=randu">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

randu( int len0 ) &rarr; QDataSet<br>
randu( int len0, int len1 ) &rarr; QDataSet<br>
randu( int len0, int len1, int len2 ) &rarr; QDataSet<br>
randu( int len0, int len1, int len2, int len3 ) &rarr; QDataSet<br>
***
<a name="rebundle"></a>
# rebundle
rebundle( QDataSet bundle1, java.lang.String[] names ) &rarr; QDataSet

unbundle the names from the bundle, and rebundle them in the order 
 specified.

### Parameters:
bundle1 - a bundle of datasets
<br>names - the bundled dataset names

### Returns:
the new bundle
### See Also:
<a href='Ops_u.md#unbundle'>unbundle(QDataSet, java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=rebundle&unscoped_q=rebundle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

rebundle( QDataSet bundle1, int[] ii ) &rarr; QDataSet<br>
***
<a name="reduceBins"></a>
# reduceBins
reduceBins( QDataSet dep1 ) &rarr; QDataSet

reduce each bin to its center.  If the spacing is
 log, then geometric centers are used.

### Parameters:
dep1 - rank 2 [N,2] bins dataset, where bins are min,max boundaries.

### Returns:
rank 1 N element dataset

<a href="https://github.com/autoplot/dev/search?q=reduceBins&unscoped_q=reduceBins">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reduceMax"></a>
# reduceMax
reduceMax( QDataSet ds, int dim ) &rarr; QDataSet

reduce the dataset's rank by reporting the max of all the elements along a dimension.
 Only QUBEs are supported presently.

### Parameters:
ds - rank N qube dataset.
<br>dim - zero-based index number.

### Returns:
rank N-1 dataset.

<a href="https://github.com/autoplot/dev/search?q=reduceMax&unscoped_q=reduceMax">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

reduceMax( QDataSet ds, int dim, ProgressMonitor mon ) &rarr; QDataSet<br>
***
<a name="reduceMean"></a>
# reduceMean
reduceMean( QDataSet ds, int dim ) &rarr; QDataSet

reduce the dataset's rank by reporting the mean of all the elements along a dimension.
 Only QUBEs are supported presently.  Note this does not contain code that would remove
 large offsets from zero when making the average, so the number of points is limited.

### Parameters:
ds - rank N qube dataset.
<br>dim - zero-based index number.

### Returns:
rank N-1 qube dataset.

<a href="https://github.com/autoplot/dev/search?q=reduceMean&unscoped_q=reduceMean">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

reduceMean( QDataSet ds, int dim, ProgressMonitor mon ) &rarr; QDataSet<br>
***
<a name="reduceMedian"></a>
# reduceMedian
reduceMedian( QDataSet ds, int dim, ProgressMonitor mon ) &rarr; QDataSet

reduce the dataset's rank by reporting the median of all the elements along a dimension.
 Only QUBEs are supported presently.  Note the weights reported are the totals of the data going in to each
 median, typically the number of measurements compared (when all weights are 0 or 1).

### Parameters:
ds - rank N qube dataset.
<br>dim - zero-based index number.
<br>mon - progress monitor.

### Returns:
rank N-1 qube dataset

<a href="https://github.com/autoplot/dev/search?q=reduceMedian&unscoped_q=reduceMedian">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reduceMin"></a>
# reduceMin
reduceMin( QDataSet ds, int dim ) &rarr; QDataSet



### Parameters:
ds - a QDataSet
<br>dim - an int

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=reduceMin&unscoped_q=reduceMin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

reduceMin( QDataSet ds, int dim, ProgressMonitor mon ) &rarr; QDataSet<br>
***
<a name="reduceSum"></a>
# reduceSum
reduceSum( QDataSet ds, int dim ) &rarr; QDataSet

reduce the dataset's rank by reporting the sum of all the valid elements along a dimension.  The property 
 "WEIGHTS" will contain the sum of the weights.
 Only QUBEs are supported presently.  This is like the function "total," but skips invalid values.

### Parameters:
ds - rank N qube dataset.
<br>dim - zero-based index number.

### Returns:
rank N-1 dataset.
### See Also:
<a href='Ops_t.md#total'>total(QDataSet, int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=reduceSum&unscoped_q=reduceSum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reform"></a>
# reform
reform( QDataSet ds ) &rarr; QDataSet

Reshape the dataset to remove the first dimension with length 1, reducing
 its rank by 1.  Dependencies are also preserved.  If no indeces are found, then the dataset is returned.

### Parameters:
ds - rank N dataset

### Returns:
the dataset, or rank N-1 dataset with the first 1-element dimension removed.

<a href="https://github.com/autoplot/dev/search?q=reform&unscoped_q=reform">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

reform( QDataSet ds, int nrec, int[] qube ) &rarr; QDataSet<br>
reform( QDataSet ds, int[] qube ) &rarr; QDataSet<br>
reform( Object ds, int[] qube ) &rarr; QDataSet<br>
***
<a name="removeFill"></a>
# removeFill
removeFill( QDataSet ds ) &rarr; WritableDataSet

remove the fill values from the rank 1 dataset, returning a smaller dataset.
 This was introduced to support the mash-up dialog.

### Parameters:
ds - a QDataSet

### Returns:
dataset with the values removed.

<a href="https://github.com/autoplot/dev/search?q=removeFill&unscoped_q=removeFill">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeIndeces"></a>
# removeIndeces
removeIndeces( QDataSet vv, QDataSet indeces ) &rarr; QDataSet

remove the data at the indeces from the rank 1 dataset.  This can be
 used for example like so:
 <pre>
 
 ds= ripples(20)
 ds= removeIndeces( ds, where( valid(ds).eq(0) ) )
 print ds.length()
 
 </pre>

### Parameters:
vv - a rank 1 dataset
<br>indeces - the indeces to remove.

### Returns:
a dataset with the values removed.
### See Also:
<a href='https://github.com/autoplot/dev/blob/master/rfe/20190208/demoRemoveIndeces.jy'>https://github.com/autoplot/dev/blob/master/rfe/20190208/demoRemoveIndeces.jy</a> <br>
<a href='Ops_r.md#removeValues'>removeValues(QDataSet, QDataSet)</a> which inserts fill.<br>
<a href='Ops_w.md#where'>where(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=removeIndeces&unscoped_q=removeIndeces">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeValues"></a>
# removeValues
removeValues( QDataSet ds, QDataSet indeces ) &rarr; WritableDataSet

put fill data for these indeces

### Parameters:
ds - the rank 1 or greater dataset
<br>indeces - rank 1 indeces when ds is rank 1, or rank 2 [:,m] indeces for a rank m dataset.

### Returns:
the dataset with the data at the indeces made invalid.
### See Also:
<a href='Ops_p.md#putValues'>putValues(QDataSet, QDataSet, QDataSet)</a> <br>
<a href='Ops_w.md#where'>where(QDataSet)</a> <br>
<a href='Ops_r.md#removeIndeces'>removeIndeces(QDataSet, QDataSet)</a> which copies the data to remove the indeces.<br>

<a href="https://github.com/autoplot/dev/search?q=removeValues&unscoped_q=removeValues">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

removeValues( Object ds, Object indeces ) &rarr; WritableDataSet<br>
***
<a name="removeValuesGreaterThan"></a>
# removeValuesGreaterThan
removeValuesGreaterThan( QDataSet ds, QDataSet v ) &rarr; WritableDataSet

remove values in the dataset which are greater than the value.  
 This is a convenient method for the common case where we want to
 filter data by values within the data, introduced to support
 the data mash up dialog.

### Parameters:
ds - rank N dataset
<br>v - the value, a rank 0 scalar or dataset with compatible geometry

### Returns:
the dataset with these

<a href="https://github.com/autoplot/dev/search?q=removeValuesGreaterThan&unscoped_q=removeValuesGreaterThan">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

removeValuesGreaterThan( Object ds, Object v ) &rarr; WritableDataSet<br>
***
<a name="removeValuesLessThan"></a>
# removeValuesLessThan
removeValuesLessThan( QDataSet ds, QDataSet v ) &rarr; WritableDataSet

remove values in the dataset which are less than the value.
 This is a convenient method for the common case where we want to
 filter data by values within the data, introduced to support
 the data mash up dialog.  Note that this inserts fill where data is 
 to be removed.

### Parameters:
ds - rank N dataset
<br>v - the value, a rank 0 scalar or dataset with compatible geometry

### Returns:
the dataset with these

<a href="https://github.com/autoplot/dev/search?q=removeValuesLessThan&unscoped_q=removeValuesLessThan">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

removeValuesLessThan( Object ds, Object v ) &rarr; WritableDataSet<br>
***
<a name="replicate"></a>
# replicate
replicate( short val, int len0 ) &rarr; WritableDataSet

returns rank 1 dataset with value

### Parameters:
val - fill the dataset with this value.
<br>len0 - an int

### Returns:
an org.das2.qds.WritableDataSet


<a href="https://github.com/autoplot/dev/search?q=replicate&unscoped_q=replicate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

replicate( short val, int len0, int len1 ) &rarr; WritableDataSet<br>
replicate( short val, int len0, int len1, int len2 ) &rarr; WritableDataSet<br>
replicate( int val, int len0 ) &rarr; WritableDataSet<br>
replicate( int val, int len0, int len1 ) &rarr; WritableDataSet<br>
replicate( int val, int len0, int len1, int len2 ) &rarr; WritableDataSet<br>
replicate( long val, int len0 ) &rarr; WritableDataSet<br>
replicate( long val, int len0, int len1 ) &rarr; WritableDataSet<br>
replicate( long val, int len0, int len1, int len2 ) &rarr; WritableDataSet<br>
replicate( double val, int len0 ) &rarr; WritableDataSet<br>
replicate( double val, int len0, int len1 ) &rarr; WritableDataSet<br>
replicate( double val, int len0, int len1, int len2 ) &rarr; WritableDataSet<br>
replicate( double val, int len0, int len1, int len2, int len3 ) &rarr; WritableDataSet<br>
replicate( float val, int len0 ) &rarr; WritableDataSet<br>
replicate( float val, int len0, int len1 ) &rarr; WritableDataSet<br>
replicate( float val, int len0, int len1, int len2 ) &rarr; WritableDataSet<br>
replicate( QDataSet val, int len0 ) &rarr; MutablePropertyDataSet<br>
replicate( QDataSet val, int len0, int len1 ) &rarr; MutablePropertyDataSet<br>
***
<a name="rescale"></a>
# rescale
rescale( QDataSet data, QDataSet min, QDataSet max ) &rarr; QDataSet

calculate the range of data, then rescale it so that the smallest
 values becomes min and the largest values becomes max.

### Parameters:
data - rank 1 dataset (TODO: easily modify this to support rank N)
<br>min - rank 0 min
<br>max - rank 0 max

### Returns:
rescaled data.

<a href="https://github.com/autoplot/dev/search?q=rescale&unscoped_q=rescale">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rescaleRange"></a>
# rescaleRange
rescaleRange( QDataSet dr, double min, double max ) &rarr; QDataSet

returns rank 1 QDataSet range relative to range "dr", where 0. is the minimum, and 1. is the maximum.
 For example rescaleRange(ds,1,2) is scanNext, rescaleRange(ds,0.5,1.5) is zoomOut.  This is similar
 to the DatumRange rescale functions.

### Parameters:
dr - a QDataSet with bins and with nonzero width.
<br>min - the new min normalized with respect to this range.  0. is this range's min, 1 is this range's max, -1 is
 min-width.
<br>max - the new max normalized with respect to this range.  0. is this range's min, 1 is this range's max, -1 is
 min-width.

### Returns:
new rank 1 QDataSet range.

<a href="https://github.com/autoplot/dev/search?q=rescaleRange&unscoped_q=rescaleRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rescaleRangeLogLin"></a>
# rescaleRangeLogLin
rescaleRangeLogLin( QDataSet dr, double min, double max ) &rarr; QDataSet

like rescaleRange, but look at log/lin flag.

### Parameters:
dr - a QDataSet
<br>min - a double
<br>max - a double

### Returns:
two-element rank 1 QDataSet
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/QDataSet_S.md#SCALE_TYPE'>QDataSet#SCALE_TYPE</a> <br>

<a href="https://github.com/autoplot/dev/search?q=rescaleRangeLogLin&unscoped_q=rescaleRangeLogLin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reverse"></a>
# reverse
reverse( QDataSet ds ) &rarr; QDataSet

returns the reverse of the rank 1 dataset.

### Parameters:
ds - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=reverse&unscoped_q=reverse">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

reverse( Object ds ) &rarr; QDataSet<br>
***
<a name="rgbColorDataset"></a>
# rgbColorDataset
rgbColorDataset( QDataSet red, QDataSet green, QDataSet blue ) &rarr; QDataSet

create a dataset of RGB colors.  The output is
 int(red)*256*256 + int(green)*256 + int(blue)
 with the units of Units.rgbColor

### Parameters:
red - the red component, from 0 to 255
<br>green - the green component, from 0 to 255
<br>blue - the blue component, from 0 to 255

### Returns:
the rgb encoded colors.

<a href="https://github.com/autoplot/dev/search?q=rgbColorDataset&unscoped_q=rgbColorDataset">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="ripples"></a>
# ripples
ripples( int len0 ) &rarr; QDataSet

rank 1 dataset for demos and testing.

### Parameters:
len0 - number of elements in the first index

### Returns:
rank 1 dataset for demos and testing.

<a href="https://github.com/autoplot/dev/search?q=ripples&unscoped_q=ripples">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

ripples( int len0, int len1 ) &rarr; QDataSet<br>
ripples( int len0, int len1, int len2 ) &rarr; QDataSet<br>
ripples( int len0, int len1, int len2, int len3 ) &rarr; QDataSet<br>
***
<a name="ripplesJoinSpectrogramTimeSeries"></a>
# ripplesJoinSpectrogramTimeSeries
ripplesJoinSpectrogramTimeSeries( int len ) &rarr; QDataSet

return fake position data for testing
 result is rank 3 bundle [3,len/3,27*]

### Parameters:
len - the total number of records.

### Returns:
an example join spectrogram time series.
### See Also:
<a href='Schemes_i.md#irregularJoin'>Schemes#irregularJoin()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=ripplesJoinSpectrogramTimeSeries&unscoped_q=ripplesJoinSpectrogramTimeSeries">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="ripplesPitchAngleDistribution"></a>
# ripplesPitchAngleDistribution
ripplesPitchAngleDistribution(  ) &rarr; QDataSet

return an example of a QDataSet containing a pitch angle distribution.  This is
 a rank 2 dataset with angle in radians for DEPEND_0 and radius for DEPEND_1.

### Returns:
an example pitch angle distribution.

<a href="https://github.com/autoplot/dev/search?q=ripplesPitchAngleDistribution&unscoped_q=ripplesPitchAngleDistribution">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="ripplesSpectrogramTimeSeries"></a>
# ripplesSpectrogramTimeSeries
ripplesSpectrogramTimeSeries( int len ) &rarr; QDataSet

return fake position data for testing
 result is rank 2 bundle [len,27]

### Parameters:
len - the number of records

### Returns:
fake position data for testing

<a href="https://github.com/autoplot/dev/search?q=ripplesSpectrogramTimeSeries&unscoped_q=ripplesSpectrogramTimeSeries">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="ripplesTimeSeries"></a>
# ripplesTimeSeries
ripplesTimeSeries( int len ) &rarr; QDataSet

return fake rank 1 data timeseries for testing

### Parameters:
len - number of records

### Returns:
fake rank 1 data timeseries for testing

<a href="https://github.com/autoplot/dev/search?q=ripplesTimeSeries&unscoped_q=ripplesTimeSeries">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="ripplesVectorTimeSeries"></a>
# ripplesVectorTimeSeries
ripplesVectorTimeSeries( int len ) &rarr; QDataSet

return fake position data for testing.
 result is rank 2 bundle [len,3]

### Parameters:
len - number of records

### Returns:
vector time series.

<a href="https://github.com/autoplot/dev/search?q=ripplesVectorTimeSeries&unscoped_q=ripplesVectorTimeSeries">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="ripplesWaveformTimeSeries"></a>
# ripplesWaveformTimeSeries
ripplesWaveformTimeSeries( int len ) &rarr; QDataSet

return fake waveform data for testing
 result is rank 2 bundle [len,512]

### Parameters:
len - number of 512-element waveforms.

### Returns:
rank 2 waveform

<a href="https://github.com/autoplot/dev/search?q=ripplesWaveformTimeSeries&unscoped_q=ripplesWaveformTimeSeries">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="round"></a>
# round
round( QDataSet ds1 ) &rarr; QDataSet

element-wise round function.  0.5 is round up.

### Parameters:
ds1 - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=round&unscoped_q=round">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

round( double x ) &rarr; double<br>
round( Object x ) &rarr; QDataSet<br>
round( QDataSet ds1, int ndigits ) &rarr; QDataSet<br>
round( double x, int ndigits ) &rarr; double<br>
round( Object ds1, int ndigits ) &rarr; QDataSet<br>
