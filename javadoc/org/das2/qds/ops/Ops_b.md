***
<a name="binsWithin"></a>
# binsWithin
binsWithin( QDataSet ds, QDataSet bounds ) &rarr; QDataSet

return non-zero where the bins of ds are within the bounds.

### Parameters:
ds - rank 2 bins dataset
<br>bounds - a rank 1 bounding box.

### Returns:
rank 1 dataset containing non-zero where the condition is true.
### See Also:
<a href='Ops_w.md#within'>within(QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=binsWithin&unscoped_q=binsWithin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="binsWithout"></a>
# binsWithout
binsWithout( QDataSet ds, QDataSet bounds ) &rarr; QDataSet

return non-zero where the bins of ds are outside of the bounds.

### Parameters:
ds - rank 2 bins dataset
<br>bounds - a rank 1 bounding box.

### Returns:
rank 1 dataset containing non-zero where the condition is true.
### See Also:
<a href='Ops_b.md#binsWithin'>binsWithin(QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=binsWithout&unscoped_q=binsWithout">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bitwiseAnd"></a>
# bitwiseAnd
bitwiseAnd( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

bitwise AND operator treats the data as (32-bit) integers, and 
 returns the bit-wise AND.

### Parameters:
ds1 - a QDataSet
<br>ds2 - a QDataSet

### Returns:
bit-wise AND.

<a href="https://github.com/autoplot/dev/search?q=bitwiseAnd&unscoped_q=bitwiseAnd">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

bitwiseAnd( Object ds1, Object ds2 ) &rarr; QDataSet<br>
***
<a name="bitwiseOr"></a>
# bitwiseOr
bitwiseOr( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

bitwise OR operator treats the data as (32-bit) integers, and 
 returns the bit-wise OR.

### Parameters:
ds1 - a QDataSet
<br>ds2 - a QDataSet

### Returns:
bit-wise OR.

<a href="https://github.com/autoplot/dev/search?q=bitwiseOr&unscoped_q=bitwiseOr">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

bitwiseOr( Object ds1, Object ds2 ) &rarr; QDataSet<br>
***
<a name="bitwiseXor"></a>
# bitwiseXor
bitwiseXor( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

bitwise XOR (exclusive or) operator treats the data as (32-bit) integers, and 
 returns the bit-wise XOR.  Note there is no bitwise not, and this is because
 there are no shorts, bytes.  So to implement bitwise not for a 16 bit number
 you would have bitwiseXor( ds, dataset(2**16-1) ).

### Parameters:
ds1 - a QDataSet
<br>ds2 - a QDataSet

### Returns:
bit-wise XOR.
### See Also:
<a href='Ops_n.md#not'>not(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=bitwiseXor&unscoped_q=bitwiseXor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

bitwiseXor( Object ds1, Object ds2 ) &rarr; QDataSet<br>
***
<a name="buckshotInterpolate"></a>
# buckshotInterpolate
buckshotInterpolate( QDataSet xyz, QDataSet data, QDataSet xinterp, QDataSet yinterp, QDataSet zinterp ) &rarr; QDataSet

3-D interpolation performed by tesselating the space (with 4-point 
 tetrahedra) and doing interpolation.
 NOTE: this does not check units.

### Parameters:
xyz - rank 2 bundle of x,y,z data.
<br>data - rank 1 dependent data, a function of x,y,z.
<br>xinterp - the x locations to interpolate, rank 0, 1, or 2.
<br>yinterp - the y locations to interpolate
<br>zinterp - the z locations to interpolate

### Returns:
the interpolated data.

<a href="https://github.com/autoplot/dev/search?q=buckshotInterpolate&unscoped_q=buckshotInterpolate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

buckshotInterpolate( QDataSet xy, QDataSet data, QDataSet xinterp, QDataSet yinterp ) &rarr; QDataSet<br>
***
<a name="bundle"></a>
# bundle
bundle( QDataSet ds ) &rarr; QDataSet

bundle the dataset, making an initial bundle, adding a bundle dimension.

### Parameters:
ds - a rank N dataset

### Returns:
rank N+1 bundle dataset

<a href="https://github.com/autoplot/dev/search?q=bundle&unscoped_q=bundle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

bundle( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet<br>
bundle( QDataSet ds1, QDataSet ds2, QDataSet ds3 ) &rarr; QDataSet<br>
bundle( QDataSet ds1, QDataSet ds2, QDataSet ds3, QDataSet ds4 ) &rarr; QDataSet<br>
bundle( QDataSet ds1, QDataSet ds2, QDataSet ds3, QDataSet ds4, QDataSet ds5 ) &rarr; QDataSet<br>
bundle( QDataSet ds1, QDataSet ds2, QDataSet ds3, QDataSet ds4, QDataSet ds5, QDataSet ds6 ) &rarr; QDataSet<br>
bundle( QDataSet ds1, QDataSet ds2, QDataSet ds3, QDataSet ds4, QDataSet ds5, QDataSet ds6, QDataSet ds7 ) &rarr; QDataSet<br>
***
<a name="butterworth"></a>
# butterworth
butterworth( QDataSet in, int order, Datum f, boolean lowp ) &rarr; QDataSet

Perform Butterworth filter for high pass or low pass.

### Parameters:
in - the rank 1 waveform
<br>order - the order of the filter (2,3,4)
<br>f - the frequency, e.g. Units.hertz.createDatum(10)
<br>lowp - true for low pass, false for high pass.

### Returns:
the dataset in the same form.

<a href="https://github.com/autoplot/dev/search?q=butterworth&unscoped_q=butterworth">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

butterworth( QDataSet in, int order, Datum flow, Datum fhigh, boolean pass ) &rarr; QDataSet<br>
***
<a name="bytarr"></a>
# bytarr
bytarr( int len0 ) &rarr; QDataSet

create a dataset filled with zeros, stored in unsigned bytes.  Each
 element can contain numbers from 0 to 255.

### Parameters:
len0 - the zeroth dimension length

### Returns:
rank 1 dataset filled with zeros.
### See Also:
<a href='Ops_d.md#dblarr'>dblarr(int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=bytarr&unscoped_q=bytarr">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

bytarr( int len0, int len1 ) &rarr; QDataSet<br>
bytarr( int len0, int len1, int len2 ) &rarr; QDataSet<br>
