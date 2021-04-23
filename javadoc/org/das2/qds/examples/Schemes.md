# org.das2.qds.examples.Schemes

For the various QDataSet schemes, show examples and documentation for
 each.  This was motivated when trying to describe the output of 
 org.das2.graph.ContoursRenderer.doAutorange()
 
 Note all QDataSets are "duck-typed," meaning if they happen to meet the 
 requirements of an interface then they are an instance of the interface.

# Schemes( )


***
<a name="angleDistribution"></a>
# angleDistribution
angleDistribution(  ) &rarr; QDataSet

return example angle distribution.

### Returns:
example angle distribution.

<a href="https://github.com/autoplot/dev/search?q=angleDistribution&unscoped_q=angleDistribution">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

angleDistribution( int i ) &rarr; QDataSet<br>
***
<a name="boundingBox"></a>
# boundingBox
boundingBox(  ) &rarr; QDataSet

return a bounding box for the data.  This is a rank 2 dataset where
 ds[0,:] shows the bounds for the first dimension and ds[1,:] shows the
 bounds for the second dimension.  Therefor ds[0,0] is the minumum extent
 of the first dimension, and ds[0,1] is the maximum.
 Note this can be extended to any number
 of dimensions (cube or hypercube).
 
 Note,
<blockquote><pre>
from org.das2.qds.examples import Schemes
ds= Schemes.boundingBox()
print asDatumRange(ds.slice(0))
</pre></blockquote>

### Returns:
a bounding box for the data.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/DataSetUtil.md#asDatumRange'>org.das2.qds.DataSetUtil#asDatumRange(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=boundingBox&unscoped_q=boundingBox">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bundleDataSet"></a>
# bundleDataSet
bundleDataSet(  ) &rarr; QDataSet

return an example bundle dataset that bundles timetags, a rank 1 dataset
 and a rank 1 dataset.

### Returns:
an example bundle dataset
### See Also:
<a href='#complexBundleDataSet'>complexBundleDataSet()</a> which has differing rank.<br>

<a href="https://github.com/autoplot/dev/search?q=bundleDataSet&unscoped_q=bundleDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bundleDescriptor"></a>
# bundleDescriptor
bundleDescriptor(  ) &rarr; QDataSet

return data that describes the columns of another dataset.  Note these
 are typically not found in APIs.

### Returns:
data that describes the columns of another dataset.

<a href="https://github.com/autoplot/dev/search?q=bundleDescriptor&unscoped_q=bundleDescriptor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="complexBundleDataSet"></a>
# complexBundleDataSet
complexBundleDataSet(  ) &rarr; QDataSet

return bundle with Time, Density, Speed, and Flux, to demonstrate
 a bundle of datasets with differing rank.

### Returns:
bundle with Time, Density, Speed, and Flux
### See Also:
<a href='#complexBundleDataSet2'>complexBundleDataSet2()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=complexBundleDataSet&unscoped_q=complexBundleDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="complexBundleDataSet2"></a>
# complexBundleDataSet2
complexBundleDataSet2(  ) &rarr; QDataSet

A complexBundleDataSet is a set of datasets which have different rank.  The
 rank 2 datasets take multiple columns of the dataset, and rank 3 and 4 datasets
 are unrolled to make them rank 2 and the property ELEMENT_DIMENSIONS is used
 to re-form them.  This returns an example bundle dataset that bundles timetags, density, velocity, and flux.
 Yes, this was coded this twice, not realizing it was already done.  This code
 is probably easier to read, so it is left in.

### Returns:
an example bundle dataset
### See Also:
<a href='#complexBundleDataSet'>complexBundleDataSet()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=complexBundleDataSet2&unscoped_q=complexBundleDataSet2">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="complexCoordinateSystemDepend"></a>
# complexCoordinateSystemDepend
complexCoordinateSystemDepend(  ) &rarr; QDataSet

returns the QDataSet used to identify the columns of a complex coordinate frame.

### Returns:
the QDataSet used to identify the columns of a complex coordinate frame.

<a href="https://github.com/autoplot/dev/search?q=complexCoordinateSystemDepend&unscoped_q=complexCoordinateSystemDepend">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="compositeImage"></a>
# compositeImage
compositeImage(  ) &rarr; QDataSet

return an example of a compositeImage.

### Returns:
image[320,240,3]

<a href="https://github.com/autoplot/dev/search?q=compositeImage&unscoped_q=compositeImage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="eventsList"></a>
# eventsList
eventsList(  ) &rarr; QDataSet

return example events list.  This is a four-column rank 2 dataset with
 start time, end time, RGB color, and ordinal data for the message.

### Returns:
example events list.

<a href="https://github.com/autoplot/dev/search?q=eventsList&unscoped_q=eventsList">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="irregularJoin"></a>
# irregularJoin
irregularJoin(  ) &rarr; QDataSet

return a rank 3 irregular join of three datasets, 
 the first is 13 records of 27 energies, 
 the second is 13 records of 20 energies, and
 the third is 14 records of 24 energies.

### Returns:
a rank 3 irregular join.

<a href="https://github.com/autoplot/dev/search?q=irregularJoin&unscoped_q=irregularJoin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isAngleDistribution"></a>
# isAngleDistribution
isAngleDistribution( QDataSet ds ) &rarr; boolean

return true if the data is an angle distribution.

### Parameters:
ds - a dataset

### Returns:
true if the data is an angle distribution.

<a href="https://github.com/autoplot/dev/search?q=isAngleDistribution&unscoped_q=isAngleDistribution">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isBoundingBox"></a>
# isBoundingBox
isBoundingBox( QDataSet ds ) &rarr; boolean

return true if the data is a boundingBox.

### Parameters:
ds - a dataset

### Returns:
true if the dataset is a bounding box.

<a href="https://github.com/autoplot/dev/search?q=isBoundingBox&unscoped_q=isBoundingBox">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isBundleDataSet"></a>
# isBundleDataSet
isBundleDataSet( QDataSet ds ) &rarr; boolean

return true if the data is a bundle dataset

### Parameters:
ds - a dataset

### Returns:
true if the data is a bundle dataset

<a href="https://github.com/autoplot/dev/search?q=isBundleDataSet&unscoped_q=isBundleDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isBundleDescriptor"></a>
# isBundleDescriptor
isBundleDescriptor( QDataSet bds ) &rarr; boolean

return true if the data describes the columns of another dataset.

### Parameters:
bds - a QDataSet

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isBundleDescriptor&unscoped_q=isBundleDescriptor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isComplexCoordinateSystemDepend"></a>
# isComplexCoordinateSystemDepend
isComplexCoordinateSystemDepend( QDataSet dep ) &rarr; boolean

return true if the data is length 2, rank 1, and has "ComplexNumber" as the COORDINATE_FRAME.

### Parameters:
dep - a QDataSet

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isComplexCoordinateSystemDepend&unscoped_q=isComplexCoordinateSystemDepend">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isComplexNumbers"></a>
# isComplexNumbers
isComplexNumbers( QDataSet ds1 ) &rarr; boolean

return true if the data represents an array of complex numbers, containing the property COORDINATE_FRAME
 on the last DEPEND, which is equal to "ComplexNumber"

### Parameters:
ds1 - a dataset

### Returns:
true if the data represents an array of complex numbers.
### See Also:
<a href='Ops.md#checkComplexArgument'>Ops#checkComplexArgument(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isComplexNumbers&unscoped_q=isComplexNumbers">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isCompositeImage"></a>
# isCompositeImage
isCompositeImage( QDataSet ds ) &rarr; boolean

return true if the dataset is a composite image, and is plottable
 with the RGBImageRenderer

### Parameters:
ds - a dataset

### Returns:
true if the dataset is a composite image.

<a href="https://github.com/autoplot/dev/search?q=isCompositeImage&unscoped_q=isCompositeImage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isEventsList"></a>
# isEventsList
isEventsList( QDataSet ds ) &rarr; boolean

return true if the data is an events list.

### Parameters:
ds - a dataset

### Returns:
true if the data is an events list.

<a href="https://github.com/autoplot/dev/search?q=isEventsList&unscoped_q=isEventsList">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isIrregularJoin"></a>
# isIrregularJoin
isIrregularJoin( QDataSet ds ) &rarr; boolean

return true if the data is a join of datasets of different cadences or lengths.

### Parameters:
ds - a QDataSet

### Returns:
return true if the data is a join of datasets of different cadences or lengths.

<a href="https://github.com/autoplot/dev/search?q=isIrregularJoin&unscoped_q=isIrregularJoin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isLegacyXYZScatter"></a>
# isLegacyXYZScatter
isLegacyXYZScatter( QDataSet zds ) &rarr; boolean

Many of Autoplot's codes use the "legacyXYZScatter" QDataSet scheme,
 where the X tags are in DEPEND_0, the Y tags are the QDataSet, and
 PLANE_0 contains the Z values.

### Parameters:
zds - a QDataSet

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isLegacyXYZScatter&unscoped_q=isLegacyXYZScatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isRank1AlongTrajectory"></a>
# isRank1AlongTrajectory
isRank1AlongTrajectory( QDataSet ds ) &rarr; boolean

return true if the data is rank 1 along a trajectory

### Parameters:
ds - a dataset

### Returns:
true if the data is rank 1 along a trajectory

<a href="https://github.com/autoplot/dev/search?q=isRank1AlongTrajectory&unscoped_q=isRank1AlongTrajectory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isRank1AtXYScatter"></a>
# isRank1AtXYScatter
isRank1AtXYScatter( QDataSet ds ) &rarr; boolean

is a Z that is a function of X and Y of a xyScatter.

### Parameters:
ds - a QDataSet

### Returns:
true if is a Z that is a function of X and Y of a xyScatter.

<a href="https://github.com/autoplot/dev/search?q=isRank1AtXYScatter&unscoped_q=isRank1AtXYScatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isRank2Bins"></a>
# isRank2Bins
isRank2Bins( QDataSet dep ) &rarr; boolean

return true if the data is a rank 2 list of M bins.  The data
 will have rank=2 and the property BINS_1='min,max'

### Parameters:
dep - a QDataSet

### Returns:
true if the data is a rank 2 list of M bins

<a href="https://github.com/autoplot/dev/search?q=isRank2Bins&unscoped_q=isRank2Bins">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isRank2Waveform"></a>
# isRank2Waveform
isRank2Waveform( QDataSet ds ) &rarr; boolean

return true if the data is a rank 2 waveform.

### Parameters:
ds - a dataset

### Returns:
true if the data is a rank 2 waveform.

<a href="https://github.com/autoplot/dev/search?q=isRank2Waveform&unscoped_q=isRank2Waveform">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isRank2WaveformRank2Offsets"></a>
# isRank2WaveformRank2Offsets
isRank2WaveformRank2Offsets( QDataSet ds ) &rarr; boolean

return true if the data is a rank 2 waveform with rank 2 offsets.

### Parameters:
ds - a dataset

### Returns:
true if the data is a rank 2 waveform.

<a href="https://github.com/autoplot/dev/search?q=isRank2WaveformRank2Offsets&unscoped_q=isRank2WaveformRank2Offsets">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isRank3Waveform"></a>
# isRank3Waveform
isRank3Waveform( QDataSet ds ) &rarr; boolean

return true if the data is a rank 3 join of rank 2 waveforms.

### Parameters:
ds - a dataset

### Returns:
true if the data is a rank 3 waveform.

<a href="https://github.com/autoplot/dev/search?q=isRank3Waveform&unscoped_q=isRank3Waveform">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isScalarSeriesWithErrors"></a>
# isScalarSeriesWithErrors
isScalarSeriesWithErrors( QDataSet ds ) &rarr; boolean

return true is the data is a simple series of scalars with errors.

### Parameters:
ds - dataset

### Returns:
true is the data is a simple series of scalars with errors.

<a href="https://github.com/autoplot/dev/search?q=isScalarSeriesWithErrors&unscoped_q=isScalarSeriesWithErrors">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isScalarTimeSeries"></a>
# isScalarTimeSeries
isScalarTimeSeries( QDataSet ds ) &rarr; boolean

return true if the data is a simple time series of scalars.

### Parameters:
ds - a dataset

### Returns:
true if the data is a simple spectrogram.

<a href="https://github.com/autoplot/dev/search?q=isScalarTimeSeries&unscoped_q=isScalarTimeSeries">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isSimpleSpectrogram"></a>
# isSimpleSpectrogram
isSimpleSpectrogram( QDataSet ds ) &rarr; boolean

return true if the data is a simple spectrogram, which is 
 rank 2, and not a small bundle.

### Parameters:
ds - a dataset

### Returns:
true if the data is a simple spectrogram.

<a href="https://github.com/autoplot/dev/search?q=isSimpleSpectrogram&unscoped_q=isSimpleSpectrogram">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isSimpleSpectrogramTimeSeries"></a>
# isSimpleSpectrogramTimeSeries
isSimpleSpectrogramTimeSeries( QDataSet ds ) &rarr; boolean

return true if the data is a simple spectrogram.

### Parameters:
ds - a dataset

### Returns:
true if the data is a simple spectrogram.

<a href="https://github.com/autoplot/dev/search?q=isSimpleSpectrogramTimeSeries&unscoped_q=isSimpleSpectrogramTimeSeries">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isTimeSeries"></a>
# isTimeSeries
isTimeSeries( QDataSet ds ) &rarr; boolean

returns true if the dataset is a time series.  This is either something 
 that has DEPEND_0 as a dataset with time location units, or a join of 
 other datasets that are time series.

### Parameters:
ds - a dataset

### Returns:
true if the dataset is a time series.
### See Also:
<a href='SemanticOps.md#isTimeSeries'>SemanticOps#isTimeSeries(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isTimeSeries&unscoped_q=isTimeSeries">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isTrajectory"></a>
# isTrajectory
isTrajectory( QDataSet ds ) &rarr; boolean

return true is the data is a trajectory

### Parameters:
ds - a dataset

### Returns:
true if the data is a trajectory

<a href="https://github.com/autoplot/dev/search?q=isTrajectory&unscoped_q=isTrajectory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isUniformCadence"></a>
# isUniformCadence
isUniformCadence( QDataSet ds ) &rarr; boolean

return true of the data has a uniform cadence.  Note that 
 the CADENCE property is ignored.

### Parameters:
ds - a rank 1 dataset

### Returns:
true if the data has uniform cadence.

<a href="https://github.com/autoplot/dev/search?q=isUniformCadence&unscoped_q=isUniformCadence">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isUniformRatiometricCadence"></a>
# isUniformRatiometricCadence
isUniformRatiometricCadence( QDataSet ds ) &rarr; boolean

return true of the data has a uniform cadence.  Note that 
 the CADENCE property is ignored.

### Parameters:
ds - a rank 1 dataset

### Returns:
true if the data has uniform cadence.

<a href="https://github.com/autoplot/dev/search?q=isUniformRatiometricCadence&unscoped_q=isUniformRatiometricCadence">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isVectorTimeSeries"></a>
# isVectorTimeSeries
isVectorTimeSeries( QDataSet ds ) &rarr; boolean

return true if the data is a vector time series.

### Parameters:
ds - a dataset

### Returns:
true if the data is a vector time series.

<a href="https://github.com/autoplot/dev/search?q=isVectorTimeSeries&unscoped_q=isVectorTimeSeries">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isXYScatter"></a>
# isXYScatter
isXYScatter( QDataSet ds ) &rarr; boolean

is a xyScatter data set.

### Parameters:
ds - a QDataSet

### Returns:
true if is a xyScatter data set.

<a href="https://github.com/autoplot/dev/search?q=isXYScatter&unscoped_q=isXYScatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isXYZScatter"></a>
# isXYZScatter
isXYZScatter( QDataSet zds ) &rarr; boolean



### Parameters:
zds - a QDataSet

### Returns:
true is it is an xyzScatter scheme.
### See Also:
<a href='#xyzScatter'>xyzScatter()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isXYZScatter&unscoped_q=isXYZScatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="legacyXYZScatter"></a>
# legacyXYZScatter
legacyXYZScatter(  ) &rarr; QDataSet

Many code use this form of data to represent Z(X,Y).  This is not preferred,
 and ds[n;x,y,z] should be used instead.  This is available for testing.

### Returns:
rank 1 dataset with DEPEND_0 and PLANE_0 properties.
### See Also:
<a href='#rank1AtXYScatter'>rank1AtXYScatter</a> <br>

<a href="https://github.com/autoplot/dev/search?q=legacyXYZScatter&unscoped_q=legacyXYZScatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rank1AlongTrajectory"></a>
# rank1AlongTrajectory
rank1AlongTrajectory(  ) &rarr; QDataSet

return a rank 1 dataset that depends on a trajectory through a space,
 which is not supported currently.

### Returns:
rank 1 dataset with DEPEND_0 a trajectory.

<a href="https://github.com/autoplot/dev/search?q=rank1AlongTrajectory&unscoped_q=rank1AlongTrajectory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rank1AtXYScatter"></a>
# rank1AtXYScatter
rank1AtXYScatter(  ) &rarr; QDataSet

Here there is a Z that is a function of X and Y of a xyScatter.

### Returns:
rank 1 dataset that has bundle for DEPEND_0.
### See Also:
<a href='#xyzScatter'>xyzScatter()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=rank1AtXYScatter&unscoped_q=rank1AtXYScatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rank2Bins"></a>
# rank2Bins
rank2Bins(  ) &rarr; QDataSet

return a rank 2 dataset that is a list of bins.

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=rank2Bins&unscoped_q=rank2Bins">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rank2ComplexNumbers"></a>
# rank2ComplexNumbers
rank2ComplexNumbers(  ) &rarr; QDataSet

return a complex rank 2 dataset, N by 2, which can be thought of as a 1-D array of N complex numbers

### Returns:
a complex rank 2 dataset ds[N,2]
### See Also:
<a href='#isComplexNumbers'>isComplexNumbers(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=rank2ComplexNumbers&unscoped_q=rank2ComplexNumbers">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rank2Waveform"></a>
# rank2Waveform
rank2Waveform(  ) &rarr; QDataSet

return a rank 2 waveform, where the waveform is stored in packets.
 DEPEND_0 is the time for each packet, and DEPEND_1 is the difference in
 time for each measurement to the packet time.  Note the additional requirement
 that the offsets be uniform, e.g.:
<blockquote><pre>
from org.das2.qds.examples import Schemes
ds= Schemes.rank2Waveform()
deltaT= ds.property( QDataSet.DEPEND_1 )
ddeltaT= diffs(dep1)
print ddeltaT[0], ddeltT[-1] # should be the same
</pre></blockquote>

### Returns:
rank 2 waveform.

<a href="https://github.com/autoplot/dev/search?q=rank2Waveform&unscoped_q=rank2Waveform">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rank2WaveformRank2Offsets"></a>
# rank2WaveformRank2Offsets
rank2WaveformRank2Offsets(  ) &rarr; QDataSet

return a rank 2 waveform, but DEPEND_1 which contains the offsets is also  
 rank 2.  This was introduced to support study where short waveform-like
 structures were identified.

### Returns:
a rank 2 waveform, but with rank 2 time-varying DEPEND_1 offsets.

<a href="https://github.com/autoplot/dev/search?q=rank2WaveformRank2Offsets&unscoped_q=rank2WaveformRank2Offsets">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rank3Waveform"></a>
# rank3Waveform
rank3Waveform(  ) &rarr; QDataSet

return a join of rank 2 waveforms, also called a rank 3 waveform.

### Returns:
rank 3 waveform

<a href="https://github.com/autoplot/dev/search?q=rank3Waveform&unscoped_q=rank3Waveform">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="scalarSeriesWithErrors"></a>
# scalarSeriesWithErrors
scalarSeriesWithErrors(  ) &rarr; QDataSet

return a rank 1 scalar series with errors.

### Returns:
a rank 1 scalar series with errors.

<a href="https://github.com/autoplot/dev/search?q=scalarSeriesWithErrors&unscoped_q=scalarSeriesWithErrors">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="scalarTimeSeries"></a>
# scalarTimeSeries
scalarTimeSeries(  ) &rarr; QDataSet

return a rank 1 scalar time series.

### Returns:
a rank 1 scalar time series.

<a href="https://github.com/autoplot/dev/search?q=scalarTimeSeries&unscoped_q=scalarTimeSeries">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="simpleSpectrogram"></a>
# simpleSpectrogram
simpleSpectrogram(  ) &rarr; QDataSet

return a rank 2 simple spectrogram, which has two indeces.

### Returns:
rank 2 simple spectrogram

<a href="https://github.com/autoplot/dev/search?q=simpleSpectrogram&unscoped_q=simpleSpectrogram">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="simpleSpectrogramTimeSeries"></a>
# simpleSpectrogramTimeSeries
simpleSpectrogramTimeSeries(  ) &rarr; QDataSet

return a rank 2 simple spectrogram, which has two indeces
 and is a TimeSeries.

### Returns:
simple spectrogram time series

<a href="https://github.com/autoplot/dev/search?q=simpleSpectrogramTimeSeries&unscoped_q=simpleSpectrogramTimeSeries">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="trajectory"></a>
# trajectory
trajectory(  ) &rarr; QDataSet

return a trajectory through a space

### Returns:
rank 2 dataset

<a href="https://github.com/autoplot/dev/search?q=trajectory&unscoped_q=trajectory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="uniformCadence"></a>
# uniformCadence
uniformCadence(  ) &rarr; QDataSet

uniform cadence is when each tag is the same distance apart, within a reasonable threshold.

### Returns:
dataset with uniform cadence

<a href="https://github.com/autoplot/dev/search?q=uniformCadence&unscoped_q=uniformCadence">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="uniformRatiometricCadence"></a>
# uniformRatiometricCadence
uniformRatiometricCadence(  ) &rarr; QDataSet

uniform ratiometric cadence is when the tags are uniform in log space.

### Returns:
dataset with uniform ratiometric cadence.

<a href="https://github.com/autoplot/dev/search?q=uniformRatiometricCadence&unscoped_q=uniformRatiometricCadence">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="vectorTimeSeries"></a>
# vectorTimeSeries
vectorTimeSeries(  ) &rarr; QDataSet

return a rank 2 vectorTimeSeries, which is a bundle
 of m rank 1 measurements.  This tacitly asserts orthogonality,
 but the bundled data should at least all be rank 1 and in the same units.
<blockquote><pre>
from org.das2.qds.examples import Schemes
ds= Schemes.vectorTimeSeries()
plot( magnitude( ds ) )
plot( unbundle( ds, 0 ) )
</pre></blockquote>
 dataset&rarr;rank2bundle&rarr;vectorTimeSeries.

### Returns:
rank 2 vector time series.

<a href="https://github.com/autoplot/dev/search?q=vectorTimeSeries&unscoped_q=vectorTimeSeries">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="xyScatter"></a>
# xyScatter
xyScatter(  ) &rarr; QDataSet

"scatter" is meant to indicate there is no connection between 
 successive points, and that there is no dependence indicates no 
 clean relation between the bundled datasets.

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=xyScatter&unscoped_q=xyScatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="xyzScatter"></a>
# xyzScatter
xyzScatter(  ) &rarr; QDataSet

This will be the preferred way to represent X,Y &rarr; Z.  This shows
 a problem, however, where there is no way to indicate the dependencies
 for the columns.  The Z column can have DEPENDNAME_0, but how does one
 declare the dependence on Y as well?  
 In https://sourceforge.net/p/autoplot/bugs/1710/, I propose 
 CONTEXT_0=field0,field2, which seems like it would work nicely.

### Returns:
a QDataSet

### See Also:
<a href='#rank1AlongTrajectory'>rank1AlongTrajectory()</a> <br>
<a href='#rank1AtXYScatter'>rank1AtXYScatter()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=xyzScatter&unscoped_q=xyzScatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

