***
<a name="hanning"></a>
# hanning
hanning( QDataSet ds, int len ) &rarr; QDataSet

Apply Hanning (Hann) windows to the data to prepare for FFT.  The 
 data is reformed into a rank 2 dataset [N,len].  Hanning windows taper 
 the ends of the interval to remove noise caused by the discontinuity.
 This is deprecated, and windowFunction should be used.

### Parameters:
ds - a QDataSet
<br>len - an int

### Returns:
data[N,len] with the hanning window applied.
### See Also:
<a href='Ops_w.md#windowFunction'>windowFunction(org.das2.qds.ops.Ops.FFTFilterType, int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=hanning&unscoped_q=hanning">[search for examples]</a>

***
<a name="hashcodes"></a>
# hashcodes
hashcodes( QDataSet ds ) &rarr; QDataSet

return a rank 1 hashcodes of each record the dataset, with one hashcodes value for each record.  The 
 value of hashcodes should repeat if the record repeats.  
 
 NOTE: This is under-implemented and should not be used
 without understanding the code.

### Parameters:
ds - dataset with rank greater than 0.

### Returns:
rank 1 dataset.

<a href="https://github.com/autoplot/dev/search?q=hashcodes&unscoped_q=hashcodes">[search for examples]</a>

***
<a name="hilbert"></a>
# hilbert
hilbert( QDataSet ds ) &rarr; QDataSet

Perform the Hilbert function on the rank 1 dataset, similar to
 the hilbert function in IDL and Matlab.

### Parameters:
ds - rank 1 dataset of length n.

### Returns:
ds[n,2], complex array
### See Also:
<a href='Ops_h.md#hilbert'>hilbert(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=hilbert&unscoped_q=hilbert">[search for examples]</a>

***
<a name="hilbertSciPy"></a>
# hilbertSciPy
hilbertSciPy( QDataSet ds ) &rarr; QDataSet

Perform the Hilbert function on the rank 1 dataset, similar to
 the scipy.signal.hilbert function in SciPy.  The result is
 form differently than hilbert.

### Parameters:
ds - rank 1 dataset of length n.

### Returns:
ds[n,2], complex array
### See Also:
<a href='Ops_h.md#hilbert'>hilbert(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=hilbertSciPy&unscoped_q=hilbertSciPy">[search for examples]</a>

***
<a name="histogram"></a>
# histogram
histogram( QDataSet ds, double min, double max, double binSize ) &rarr; QDataSet

returns a rank 1 dataset that is a histogram of the data.  Note there
 will also be in the properties:
   count, the total number of valid values.
   nonZeroMin, the smallest non-zero, positive number

### Parameters:
ds - rank N dataset
<br>min - the min of the first bin.  If min=-1 and max=-1, then automatically set the min and max.
<br>max - the max of the last bin.
<br>binSize - the size of each bin.

### Returns:
a rank 1 dataset with each bin's count.  DEPEND_0 indicates the bin locations.

<a href="https://github.com/autoplot/dev/search?q=histogram&unscoped_q=histogram">[search for examples]</a>

histogram( QDataSet ds, Datum min, Datum max, Datum binsize ) &rarr; QDataSet<br>
histogram( QDataSet ds, String min, String max, String binsize ) &rarr; QDataSet<br>
histogram( QDataSet ds, int binCount ) &rarr; QDataSet<br>
***
<a name="histogram2d"></a>
# histogram2d
histogram2d( QDataSet x, QDataSet y, int[] bins, QDataSet xrange, QDataSet yrange ) &rarr; QDataSet

make a 2-D histogram of the data in x and y.  For example
<blockquote><pre>
x= randn(10000)+1
y= randn(10000)+4
zz= histogram2d( x,y, [30,30], dataset([0,8]), dataset([-2,6]) )
plot( zz )
</pre></blockquote>
 The result will be a rank 2 dataset with DEPEND_0 and DEPEND_1 indicating
 the bin locations.  If the xrange or yrange is dimensionless, then 
 use the units of x or y.

### Parameters:
x - the x values
<br>y - the y values
<br>bins - number of bins in x and y
<br>xrange - a rank 1 2-element bounds dataset, so that Units can be specified.
<br>yrange - a rank 1 2-element bounds dataset, so that Units can be specified.

### Returns:
a rank 2 dataset
### See Also:
<a href='Ops_h.md#histogram'>histogram(QDataSet, double, double, double)</a> <br>
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/util/Reduction_h.md#histogram2D'>org.das2.qds.util.Reduction#histogram2D(QDataSet, QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=histogram2d&unscoped_q=histogram2d">[search for examples]</a>

