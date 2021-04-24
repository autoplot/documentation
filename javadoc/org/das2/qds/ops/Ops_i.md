***
<a name="ifft"></a>
# ifft
ifft( QDataSet ds ) &rarr; QDataSet

Performs an inverse FFT on the provided rank 2 dataset of complex numbers.  
 A rank 2 dataset of complex numbers is returned.

### Parameters:
ds - a rank 2 dataset.

### Returns:
a rank 2 dataset of complex numbers.
### See Also:
<a href='Ops_f.md#fft'>Ops#fft(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=ifft&unscoped_q=ifft">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

ifft( QDataSet ds, QDataSet window, int stepFraction, ProgressMonitor mon ) &rarr; QDataSet<br>
***
<a name="imax"></a>
# imax
imax( QDataSet ds ) &rarr; int

return the index of the maximum value.  This is to avoid inefficient 
 code like "where(slice.eq( max(slice) ))[0]"

### Parameters:
ds - rank 1 dataset

### Returns:
the index of the maximum value, or -1 if the data is all fill.

<a href="https://github.com/autoplot/dev/search?q=imax&unscoped_q=imax">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

imax( Object ds ) &rarr; int<br>
***
<a name="imin"></a>
# imin
imin( QDataSet ds ) &rarr; int

return the index of the minimum value.  This is to avoid inefficient 
 code like "where(slice.eq( min(slice) ))[0]"

### Parameters:
ds - rank 1 dataset

### Returns:
the index of the maximum value, or -1 if the data is all fill.

<a href="https://github.com/autoplot/dev/search?q=imin&unscoped_q=imin">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

imin( Object ds ) &rarr; int<br>
***
<a name="indgen"></a>
# indgen
indgen( int len0 ) &rarr; QDataSet

returns rank 1 dataset with values [0,1,2,...]
 This returns an immutable dataset, so that it can
 be used in Jython like so: for i in indgen(200000).  Note before
 February 2018, this would return a mutable dataset, and now
 this returns an IndexGenDataSet, which is immutable.

### Parameters:
len0 - an int

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=indgen&unscoped_q=indgen">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

indgen( int len0, int len1 ) &rarr; QDataSet<br>
indgen( int len0, int len1, int len2 ) &rarr; QDataSet<br>
***
<a name="intarr"></a>
# intarr
intarr( int len0 ) &rarr; QDataSet

create a dataset filled with zeros, stored in 4-byte ints.

### Parameters:
len0 - the zeroth dimension length

### Returns:
rank 1 dataset filled with zeros.
### See Also:
<a href='Ops_z.md#zeros'>zeros(int)</a> <br>
<a href='Ops_d.md#dblarr'>dblarr(int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=intarr&unscoped_q=intarr">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

intarr( int len0, int len1 ) &rarr; QDataSet<br>
intarr( int len0, int len1, int len2 ) &rarr; QDataSet<br>
***
<a name="interpolate"></a>
# interpolate
interpolate( QDataSet vv, QDataSet findex ) &rarr; QDataSet

interpolate values from rank 1 dataset vv using fractional indeces 
 in rank N findex.  For example, findex=1.5 means interpolate
 the 1st and 2nd indeces with equal weight, 1.1 means
 90% of the first mixed with 10% of the second.  
 Only modest extrapolations where findex&gt;=-0.5 and findex&lt;=L-0.5 are allowed, where L is the number of points.
 The findex parameter must be dimensionless, to ensure that the caller is not passing in physical data.

 Note there is no check on CADENCE.
 Note nothing is done with DEPEND_0, presumably because was already calculated and used for findex.
 
 Here is an example use of this in Autoplot's Jython code:
 <pre>
 
xx= [1,2,3,4]
yy= [2,4,5,4]
xxx= linspace(0,5,100)
yyy= interpolate( yy, findex(xx,xxx) )

plot( xx, yy, symbolSize=20 )
plot( addPlotElement(0), xxx, yyy )
 
 </pre>

### Parameters:
vv - rank 1 dataset having length L that is the data to be interpolated.
<br>findex - rank N dataset of fractional indeces.  This must be dimensionless, between -0.5 and L-0.5 and is typically calculated by the findex command.

### Returns:
the result.
### See Also:
<a href='Ops_i.md#interpolateMod interpolateMod, for data like longitude where 259 deg is 2 degrees away from 1 deg'>interpolateMod interpolateMod, for data like longitude where 259 deg is 2 degrees away from 1 deg</a> interpolateMod, for data like longitude where 259 deg is 2 degrees away from 1 deg<br>

<a href="https://github.com/autoplot/dev/search?q=interpolate&unscoped_q=interpolate">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

interpolate( Object vv, Object findex ) &rarr; QDataSet<br>
interpolate( QDataSet vv, QDataSet findex0, QDataSet findex1 ) &rarr; QDataSet<br>
interpolate( Object vv, Object findex0, Object findex1 ) &rarr; QDataSet<br>
interpolate( QDataSet vv, QDataSet findex0, QDataSet findex1, QDataSet findex2 ) &rarr; QDataSet<br>
***
<a name="interpolateGrid"></a>
# interpolateGrid
interpolateGrid( QDataSet vv, QDataSet findex0, QDataSet findex1 ) &rarr; QDataSet

interpolate values from rank 2 dataset vv using fractional indeces
 in rank N findex, using bilinear interpolation.  Here the two rank1
 indexes form a grid and the result is rank 2.

### Parameters:
vv - rank 2 dataset.
<br>findex0 - rank 1 dataset of fractional indeces for the zeroth index.
<br>findex1 - rank 1 dataset of fractional indeces for the first index.

### Returns:
rank 2 dataset
### See Also:
<a href='Ops_f.md#findex findex, the 1-D findex command'>findex findex, the 1-D findex command</a> findex, the 1-D findex command<br>

<a href="https://github.com/autoplot/dev/search?q=interpolateGrid&unscoped_q=interpolateGrid">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

interpolateGrid( Object x, Object y, Object z ) &rarr; QDataSet<br>
***
<a name="interpolateMod"></a>
# interpolateMod
interpolateMod( QDataSet vv, QDataSet mod, QDataSet findex ) &rarr; QDataSet

like interpolate, but the findex is recalculated when the two bracketed points are closer in the 
 modulo space than they would be in the linear space.

### Parameters:
vv - rank 1 dataset that is the data to be interpolated. (e.g. longitude from 0 to 360deg)
<br>mod - rank 0 dataset that is the mod of the space (e.g. 360deg), or rank 1 where the range is specified (e.g. -180 to 180).
<br>findex - rank N dataset of fractional indeces.  This must be dimensionless and is typically calculated by the findex command.

### Returns:
the result, a rank 1 dataset with one element for each findex.
### See Also:
<a href='Ops_i.md#interpolate'>interpolate(QDataSet,QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=interpolateMod&unscoped_q=interpolateMod">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="irange"></a>
# irange
irange( double min, double max, int step ) &rarr; Iterator

mimic the Jython xrange function for use in loops.  The returns
 the integers in the sequence, like xrange, but avoids the confusing 
 "xrange" name and this also takes double
 values so that it can be used in graphics routines which use double.

### Parameters:
min - the first value
<br>max - the last value, plus one (exclusive).
<br>step - the increment between elements.

### Returns:
an iterator for the numbers in the interval.

<a href="https://github.com/autoplot/dev/search?q=irange&unscoped_q=irange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

irange( double min, double max ) &rarr; Iterator<br>
irange( double max ) &rarr; Iterator<br>
***
<a name="isAngleRange"></a>
# isAngleRange
isAngleRange( QDataSet ds, boolean strict ) &rarr; Double

return true if the dataset can be interpreted as radian degrees from 0 to PI or from 0 to 2*PI.

### Parameters:
ds - any QDataSet.
<br>strict - return null if it's not clear that the units are degrees.

### Returns:
the multiplier to make the dataset into radians, or null.

<a href="https://github.com/autoplot/dev/search?q=isAngleRange&unscoped_q=isAngleRange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isBundle"></a>
# isBundle
isBundle( QDataSet zds ) &rarr; boolean

return true if the dataset is a bundle.  It is rank 2 or rank 1, and
 has the last dimension a bundle dimension.

### Parameters:
zds - the dataset

### Returns:
true if the dataset is a bundle.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/examples/Schemes.md'>org.das2.qds.examples.Schemes</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isBundle&unscoped_q=isBundle">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isLegacyBundle"></a>
# isLegacyBundle
isLegacyBundle( QDataSet zds ) &rarr; boolean

return true if DEPEND_1 is set and its units are EnumerationUnits.  This
 was the pre-bundle way of representing a bundle of datasets.  It might
 be supported indefinitely, because it has some nice rules about the data.
 For example, bundled data must be of the same units since there is no place to put
 the property, and each bundled item must be rank 1.

### Parameters:
zds - rank 1 or rank 2 dataset

### Returns:
return true if DEPEND_1 is set and its units are EnumerationUnits.

<a href="https://github.com/autoplot/dev/search?q=isLegacyBundle&unscoped_q=isLegacyBundle">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isSafeName"></a>
# isSafeName
isSafeName( String name ) &rarr; boolean

returns true if the name is a Java-style identifier, starting
 with one of a-z, A-Z, or _; followed by a-z, A-Z, 0-9, or _; and
 note that only ASCII characters are allowed.

### Parameters:
name - a String

### Returns:
true if the name is a safe identifier name.

<a href="https://github.com/autoplot/dev/search?q=isSafeName&unscoped_q=isSafeName">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

