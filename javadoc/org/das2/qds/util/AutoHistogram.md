# org.das2.qds.util.AutoHistogram

Self-configuring histogram dynamically adjusts range and bin size as data
 is added.  Also it tries to identify outlier points, which are available
 as a {@code Map<Double,Integer>} going from value to number observed.  Also for
 each bin, we keep track of a running mean and variance, which are useful for
 identifying continuous bins and total moments.  Introduced to support
 automatic cadence algorithm, should be generally useful in data discovery.

# AutoHistogram( )


***
<a name="USER_PROP_BIN_START"></a>
# USER_PROP_BIN_START



***
<a name="USER_PROP_BIN_WIDTH"></a>
# USER_PROP_BIN_WIDTH



***
<a name="USER_PROP_INVALID_COUNT"></a>
# USER_PROP_INVALID_COUNT



***
<a name="USER_PROP_OUTLIERS"></a>
# USER_PROP_OUTLIERS



***
<a name="USER_PROP_MIN_GT_ZERO"></a>
# USER_PROP_MIN_GT_ZERO



***
<a name="USER_PROP_TOTAL"></a>
# USER_PROP_TOTAL

Long, total number of valid points.

***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="binOf"></a>
# binOf
binOf( QDataSet hist, double d ) &rarr; int

convenient method for getting the bin location of a value from a completed
 histogram's metadata.  Note this is inefficient since it must do HashMap
 lookups to get the bin width and bin start, so use this carefully.

### Parameters:
hist - a QDataSet
<br>d - a double

### Returns:
the index of the bin for the point.

<a href="https://github.com/autoplot/dev/search?q=binOf&unscoped_q=binOf">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="doit"></a>
# doit
doit( QDataSet ds ) &rarr; QDataSet



### Parameters:
ds - a QDataSet

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=doit&unscoped_q=doit">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

doit( QDataSet ds, QDataSet wds ) &rarr; QDataSet<br>
***
<a name="getHistogram"></a>
# getHistogram
getHistogram(  ) &rarr; DDataSet

get the histogram of the data accumulated thus far.

### Returns:
an org.das2.qds.DDataSet


<a href="https://github.com/autoplot/dev/search?q=getHistogram&unscoped_q=getHistogram">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mean"></a>
# mean
mean( QDataSet hist ) &rarr; RankZeroDataSet

returns the mean of the dataset that has been histogrammed.

### Parameters:
hist - a QDataSet

### Returns:
an org.das2.qds.RankZeroDataSet


<a href="https://github.com/autoplot/dev/search?q=mean&unscoped_q=mean">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="moments"></a>
# moments
moments( QDataSet hist ) &rarr; RankZeroDataSet

returns the mean of the dataset that has been histogrammed.

### Parameters:
hist - a rank 1 dataset with each bin containing the count in each bin.  DEPEND_0 are the labels for
     each bin.  The property "means" returns a rank 1 dataset containing the means for each bin.  The
     property "stddevs" contains the standard deviation within each bin.

### Returns:
rank 0 dataset (a Datum) whose value is the mean, and the property("stddev") contains the standard deviation

<a href="https://github.com/autoplot/dev/search?q=moments&unscoped_q=moments">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="monoExtent"></a>
# monoExtent
monoExtent( QDataSet dep0 ) &rarr; QDataSet

fast extent only works when monotonic.
 Returns null if there is no valid data.

### Parameters:
dep0 - a QDataSet

### Returns:
rank 1 bins dataset or null

<a href="https://github.com/autoplot/dev/search?q=monoExtent&unscoped_q=monoExtent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="peakIds"></a>
# peakIds
peakIds( QDataSet hist ) &rarr; QDataSet

return a list of all the peaks in the histogram.  A peak is defined as a
 local maximum, then including the adjacent bins consistent with the peak
 population, and not belonging to another peak.

### Parameters:
hist - a QDataSet

### Returns:
QDataSet covarient with hist.

<a href="https://github.com/autoplot/dev/search?q=peakIds&unscoped_q=peakIds">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="peaks"></a>
# peaks
peaks( QDataSet hist ) &rarr; QDataSet

return a list of all the peaks in the histogram.  See peakIds to see
 how peaks are identified.  Once the bins of a peak
 have been identified, then the mean and stddev of each peak is returned.
 Note the stddev typically reads low, probably because the tails have been removed.

### Parameters:
hist - the result of AutoHistogram

### Returns:
QDataSet rank 1 dataset with length equal to the number of identified peaks

<a href="https://github.com/autoplot/dev/search?q=peaks&unscoped_q=peaks">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reset"></a>
# reset
reset(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reset&unscoped_q=reset">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="simpleRange"></a>
# simpleRange
simpleRange( QDataSet hist2 ) &rarr; QDataSet

returns the simple range, the min and the max containing the data.

### Parameters:
hist2 - the result of autoHistogram.

### Returns:
rank 1 bins dataset showing the min and max.  value(0) is the
 min, value(1) is the max.

<a href="https://github.com/autoplot/dev/search?q=simpleRange&unscoped_q=simpleRange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

