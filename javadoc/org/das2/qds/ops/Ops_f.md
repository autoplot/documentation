***
<a name="fft"></a>
# fft
fft( QDataSet ds ) &rarr; QDataSet

Performs an FFT on the provided rank 1 dataset.  A rank 2 dataset of 
 complex numbers is returned.  The data must not contain fill and
 must be uniformly spaced.  DEPEND_0 is used to identify frequencies
 if available.

### Parameters:
ds - a rank 1 dataset.

### Returns:
a rank 2 dataset of complex numbers.
### See Also:
<a href='Schemes_r.md#rank2ComplexNumbers'>Schemes#rank2ComplexNumbers()</a> <br>
<a href='Ops_i.md#ifft'>Ops#ifft(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=fft&unscoped_q=fft">[search for examples]</a>

fft( QDataSet ds, QDataSet window, int stepFraction, ProgressMonitor mon ) &rarr; QDataSet<br>
***
<a name="fftFilter"></a>
# fftFilter
fftFilter( QDataSet ds, int len, org.das2.qds.ops.Ops.FFTFilterType filt ) &rarr; QDataSet

Apply windows to the data to prepare for FFT.  The data is reformed into a rank 2 dataset [N,len].
 The filter is applied to the data to remove noise caused by the discontinuity.
 This is deprecated, and windowFunction should be used so that the filter
 is applied to records just before each fft is performed to save space.

### Parameters:
ds - rank 1, 2, or 3 data
<br>len - size of the window.
<br>filt - FFTFilterType.Hanning or FFTFilterType.TenPercentEdgeCosine

### Returns:
data[N,len] with the window applied.

<a href="https://github.com/autoplot/dev/search?q=fftFilter&unscoped_q=fftFilter">[search for examples]</a>

***
<a name="fftPower"></a>
# fftPower
fftPower( QDataSet ds, int len, ProgressMonitor mon ) &rarr; QDataSet

create a power spectrum on the dataset by breaking it up and
 doing FFTs on each segment.  A unity (or "boxcar") window is used.

 data may be rank 1, rank 2, or rank 3.

 Looks for DEPEND_1.USER_PROPERTIES.FFT_Translation, which should
 be a rank 0 or rank 1 QDataSet.  If it is rank 1, then it should correspond
 to the DEPEND_0 dimension.

### Parameters:
ds - rank 2 dataset ds(N,M) with M&gt;len
<br>len - the number of elements to have in each fft.
<br>mon - a ProgressMonitor for the process

### Returns:
rank 2 FFT spectrum

<a href="https://github.com/autoplot/dev/search?q=fftPower&unscoped_q=fftPower">[search for examples]</a>

fftPower( QDataSet ds, QDataSet window, ProgressMonitor mon ) &rarr; QDataSet<br>
fftPower( QDataSet ds, int windowLen, int stepFraction, String windowName, ProgressMonitor mon ) &rarr; QDataSet<br>
fftPower( QDataSet ds, QDataSet window, int stepFraction, ProgressMonitor mon ) &rarr; QDataSet<br>
fftPower( QDataSet ds ) &rarr; QDataSet<br>
***
<a name="fftPowerMultiThread"></a>
# fftPowerMultiThread
fftPowerMultiThread( QDataSet ds, int len, ProgressMonitor mon ) &rarr; QDataSet

Experiment with multi-threaded FFTPower function.  This breaks up the 
 task into four independent tasks that can be run in parallel.

### Parameters:
ds - rank 2 dataset ds(N,M) with M&gt;len
<br>len - the number of elements to have in each fft.
<br>mon - a ProgressMonitor for the process

### Returns:
rank 2 FFT spectrum

<a href="https://github.com/autoplot/dev/search?q=fftPowerMultiThread&unscoped_q=fftPowerMultiThread">[search for examples]</a>

***
<a name="fftWindow"></a>
# fftWindow
fftWindow( QDataSet ds, int len ) &rarr; QDataSet

perform ffts on the rank 1 dataset to make a rank2 spectrogram.

### Parameters:
ds - rank 1 dataset
<br>len - the window length

### Returns:
rank 2 dataset.

<a href="https://github.com/autoplot/dev/search?q=fftWindow&unscoped_q=fftWindow">[search for examples]</a>

***
<a name="findex"></a>
# findex
findex( QDataSet uu, QDataSet vv ) &rarr; QDataSet

returns the "floating point index" of each element of vv within the monotonically
 increasing dataset uu.  This handy number is the index of the lower bound plus the
 fractional position between the two bounds.  For example, findex([100,110,120],111.2) is
 1.12 because it is just after the 1st element (110) and is 12% of the way from 110 to 120.
 The result dataset will have the same geometry as vv.  The result will be negative
 when the element of vv is below the smallest element of uu.  The result will be greater
 than or equal to the length of uu minus one when it is greater than all elements.
 When the monotonic dataset contains repeat values, the index of the first is returned.

 Paul Ricchiazzi wrote this routine first for IDL as a fast replacement for the interpol routine, but
 it is useful in other situations as well.

### Parameters:
uu - rank 1 monotonically increasing dataset, non-repeating, containing no fill values.
<br>vv - rank N dataset with values in the same physical dimension as uu.  Fill is allowed.

### Returns:
rank N dataset with the same geometry as vv.  It will have DEPEND_0=vv when vv is rank 1.

<a href="https://github.com/autoplot/dev/search?q=findex&unscoped_q=findex">[search for examples]</a>

findex( Object x, Object y ) &rarr; QDataSet<br>
***
<a name="findgen"></a>
# findgen
findgen( int len0 ) &rarr; QDataSet

returns rank 1 dataset with values [0.,1.,2.,...]

### Parameters:
len0 - an int

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=findgen&unscoped_q=findgen">[search for examples]</a>

findgen( int len0, int len1 ) &rarr; QDataSet<br>
findgen( int len0, int len1, int len2 ) &rarr; QDataSet<br>
findgen( int len0, int len1, int len2, int len3 ) &rarr; QDataSet<br>
***
<a name="finite"></a>
# finite
finite( QDataSet ds ) &rarr; QDataSet

returns 1 where the data is not NaN, Inf, etc  I needed this when I was working with
 the RBSP polar scatter script.  Note valid should be used to check for valid data, which
 also checks for NaN.

### Parameters:
ds - qdataset of any rank.

### Returns:
1 where the data is not Nan or Inf, 0 otherwise.

<a href="https://github.com/autoplot/dev/search?q=finite&unscoped_q=finite">[search for examples]</a>

***
<a name="flatten"></a>
# flatten
flatten( QDataSet ds ) &rarr; QDataSet

flatten a rank N dataset, though currently rank 4 is not supported.
 The result for rank 2 is an n,3 dataset of [x,y,z], or if there are no tags, just [z].
 The last index will be the dependent variable, and the first indeces will
 be the independent variables sorted by dimension.

### Parameters:
ds - the rank N dataset (note only Rank 2 is supported for now).

### Returns:
rank 2 dataset bundle
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/DataSetOps_f.md#flattenRank2'>org.das2.qds.DataSetOps#flattenRank2(QDataSet)</a> <br>
<a href='Ops_g.md#grid'>grid(QDataSet)</a> <br>
<a href='Ops_f.md#flattenWaveform'>flattenWaveform(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=flatten&unscoped_q=flatten">[search for examples]</a>

***
<a name="flattenWaveform"></a>
# flattenWaveform
flattenWaveform( QDataSet ds ) &rarr; QDataSet

flatten a rank 2 dataset where the y depend variable is just an offset from the xtag. 
 Note the new DEPEND_0 may have different units from ds.property(DEPEND_0).

### Parameters:
ds - rank 2 waveform with tags for DEPEND_0 and offsets for DEPEND_1

### Returns:
rank 1 waveform
### See Also:
<a href='Ops_f.md#flatten'>flatten(QDataSet)</a> <br>
<a href='DataSetOps_f.md#flattenWaveform'>DataSetOps#flattenWaveform(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=flattenWaveform&unscoped_q=flattenWaveform">[search for examples]</a>

***
<a name="floor"></a>
# floor
floor( QDataSet ds1 ) &rarr; QDataSet

element-wise floor function.

### Parameters:
ds1 - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=floor&unscoped_q=floor">[search for examples]</a>

floor( double x ) &rarr; double<br>
floor( Object ds1 ) &rarr; QDataSet<br>
***
<a name="fltarr"></a>
# fltarr
fltarr( int len0 ) &rarr; QDataSet

create a dataset filled with zeros, stored in 4-byte floats.

### Parameters:
len0 - the zeroth dimension length

### Returns:
rank 1 dataset filled with zeros.
### See Also:
<a href='Ops_z.md#zeros'>zeros(int)</a> <br>
<a href='Ops_d.md#dblarr'>dblarr(int)</a> <br>
<a href='Ops_s.md#strarr'>strarr(int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=fltarr&unscoped_q=fltarr">[search for examples]</a>

fltarr( int len0, int len1 ) &rarr; QDataSet<br>
fltarr( int len0, int len1, int len2 ) &rarr; QDataSet<br>
