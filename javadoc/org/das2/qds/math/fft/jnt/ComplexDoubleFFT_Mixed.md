# org.das2.qds.math.fft.jnt.ComplexDoubleFFT_MixedComputes FFT's of complex, double precision data of arbitrary length n.
 This class uses the Mixed Radix method; it has special methods to handle
 factors 2, 3, 4, 5, 6 and 7, as well as a general factor.
 <P>
 This method appears to be faster than the Radix2 method, when both methods apply,
 but requires extra storage (which ComplexDoubleFFT_Mixed manages itself).
 <P>
 See {@link ComplexDoubleFFT ComplexDoubleFFT} for details of data layout.
ComplexDoubleFFT_Mixed( int n )


***
<a name="backtransform"></a>
# backtransform
backtransform( org.das2.qds.math.fft.ComplexArray.Double data, int i0, int stride ) &rarr; void



### Parameters:
data - a ComplexArray.Double
<br>i0 - an int
<br>stride - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=backtransform&unscoped_q=backtransform">[search for examples]</a>

***
<a name="transform"></a>
# transform
transform( org.das2.qds.math.fft.ComplexArray.Double data, int i0, int stride ) &rarr; void



### Parameters:
data - a ComplexArray.Double
<br>i0 - an int
<br>stride - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=transform&unscoped_q=transform">[search for examples]</a>

