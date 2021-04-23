# org.das2.qds.util.BinAverageutility class providing methods for bin averaging.
***
<a name="binAverage"></a>
# binAverage
binAverage( QDataSet ds, QDataSet newTags0 ) &rarr; DDataSet

returns a dataset with tags specified by newTags0.  Data from <tt>ds</tt>
 are averaged together when they fall into the same bin.  Note the result
 will have the property WEIGHTS.

### Parameters:
ds - a rank 1 dataset, no fill
<br>newTags0 - a rank 1 tags dataset, that must be MONOTONIC.

### Returns:
rank 1 dataset with DEPEND_0 = newTags.
### See Also:
<a href='#rebin'>rebin(QDataSet, QDataSet, QDataSet)</a> <br>
<a href='#binAverage'>binAverage(QDataSet, QDataSet )</a> <br>
<a href='#binAverage'>binAverage(QDataSet, QDataSet, QDataSet )</a> <br>

<a href="https://github.com/autoplot/dev/search?q=binAverage&unscoped_q=binAverage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

binAverage( QDataSet ds, QDataSet newTags0, QDataSet newTags1 ) &rarr; DDataSet<br>
***
<a name="binAverageBundle"></a>
# binAverageBundle
binAverageBundle( QDataSet ds, QDataSet dep0, QDataSet dep1, QDataSet dep2 ) &rarr; DDataSet

takes rank 2 bundle (x,y,z,f) and averages it into rank 3 qube f(x,y,z).  This is 
 similar to what happens in the spectrogram routine.

### Parameters:
ds - rank 2 bundle(x,y,z,f)
<br>dep0 - the rank 1 depend0 for the result, which must be uniformly spaced.
<br>dep1 - the rank 1 depend1 for the result, which must be uniformly spaced.
<br>dep2 - the rank 1 depend2 for the result, which must be uniformly spaced.

### Returns:
rank 3 dataset of z averages with depend_0, depend_1, and depend_2.  WEIGHTS contains the total weight for each bin.
### See Also:
<a href='#rebinBundle'>rebinBundle(QDataSet, QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=binAverageBundle&unscoped_q=binAverageBundle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

binAverageBundle( QDataSet ds, QDataSet dep0, QDataSet dep1 ) &rarr; DDataSet<br>
***
<a name="binMeanAverageDeviation"></a>
# binMeanAverageDeviation
binMeanAverageDeviation( QDataSet ads, QDataSet ds ) &rarr; DDataSet

takes rank 2 bundle (x,y,z) and averages in table z(x,y) and computes the
 mean average deviation in each bin.

### Parameters:
ads - rank 2 grid of averages
<br>ds - rank 2 bundle(x,y,z)

### Returns:
rank 2 dataset of z averages with depend_0 and depend_1.  WEIGHTS contains the total weight for each bin.
### See Also:
<a href='#rebin'>rebin(QDataSet, QDataSet, QDataSet)</a> <br>
<a href='#rebinBundle'>rebinBundle(QDataSet, QDataSet, QDataSet, QDataSet)</a> <br>
<a href='Ops.md#meanAverageDeviation'>Ops#meanAverageDeviation(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=binMeanAverageDeviation&unscoped_q=binMeanAverageDeviation">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="boxcar"></a>
# boxcar
boxcar( QDataSet ds, int size ) &rarr; DDataSet

run boxcar average over the dataset, returning a dataset of same geometry.  Points near the edge are simply copied from the
 source dataset.  The result dataset contains a property "weights" that is the weights for each point.

### Parameters:
ds - a rank 1 dataset of size N
<br>size - the number of adjacent bins to average

### Returns:
rank 1 dataset of size N

<a href="https://github.com/autoplot/dev/search?q=boxcar&unscoped_q=boxcar">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rebin"></a>
# rebin
rebin( QDataSet ds, QDataSet newTags0 ) &rarr; DDataSet

returns a dataset with tags specified by newTags0.  Data from <tt>ds</tt>
 are averaged together when they fall into the same bin.  Note the result
 will have the property WEIGHTS.

### Parameters:
ds - a rank 1 dataset, no fill
<br>newTags0 - a rank 1 tags dataset, that must be MONOTONIC.

### Returns:
rank 1 dataset with DEPEND_0 = newTags.
### See Also:
<a href='#rebin'>rebin(QDataSet, QDataSet, QDataSet)</a> <br>
<a href='#binAverage'>binAverage(QDataSet, QDataSet )</a> <br>

<a href="https://github.com/autoplot/dev/search?q=rebin&unscoped_q=rebin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

rebin( QDataSet ds, QDataSet newTags0, QDataSet newTags1 ) &rarr; DDataSet<br>
rebin( QDataSet ds, int n0 ) &rarr; QDataSet<br>
rebin( QDataSet ds, int n0, int n1 ) &rarr; QDataSet<br>
rebin( QDataSet ds, int n0, int n1, int n2 ) &rarr; QDataSet<br>
***
<a name="rebinBundle"></a>
# <del>rebinBundle</del>
Deprecated: see binAverageBundle
rebinBundle( QDataSet ds, QDataSet dep0, QDataSet dep1 ) &rarr; DDataSet<br>
***
<a name="residuals"></a>
# residuals
residuals( QDataSet ds, int boxcarSize ) &rarr; QDataSet

returns number of stddev from adjacent data.

### Parameters:
ds - a QDataSet
<br>boxcarSize - an int

### Returns:
QDataSet

<a href="https://github.com/autoplot/dev/search?q=residuals&unscoped_q=residuals">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

