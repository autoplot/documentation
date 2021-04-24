# org.das2.qds.math.fft.jnt.RealDoubleFFT_Even

Computes FFT's of real, double precision data when n is even, by
 computing complex FFT.

# RealDoubleFFT_Even( int n )
Create an FFT for transforming n points of real, double precision data.

***
<a name="backtransform"></a>
# backtransform
backtransform( org.das2.qds.math.fft.ComplexArray.Double data ) &rarr; void

Compute the (unnomalized) inverse FFT of data, leaving it in place.

### Parameters:
data - a ComplexArray.Double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=backtransform&unscoped_q=backtransform">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

backtransform( org.das2.qds.math.fft.ComplexArray.Double data, int i0, int stride ) &rarr; void<br>
***
<a name="inverse"></a>
# inverse
inverse( org.das2.qds.math.fft.ComplexArray.Double data, int i0, int stride ) &rarr; void

Compute the (nomalized) inverse FFT of data, leaving it in place.

### Parameters:
data - a ComplexArray.Double
<br>i0 - an int
<br>stride - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=inverse&unscoped_q=inverse">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

inverse( org.das2.qds.math.fft.ComplexArray.Double data ) &rarr; void<br>
***
<a name="normalization"></a>
# normalization
normalization(  ) &rarr; double

Return the normalization factor.  
 Multiply the elements of the backtransform'ed data to get the normalized inverse.

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=normalization&unscoped_q=normalization">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toWraparoundOrder"></a>
# toWraparoundOrder
toWraparoundOrder( org.das2.qds.math.fft.ComplexArray.Double data ) &rarr; Double

Return data in wraparound order.
 i0 and stride are used to traverse data; the new array is in 
 packed (i0=0, stride=1) format.

### Parameters:
data - a ComplexArray.Double

### Returns:
org.das2.qds.math.fft.ComplexArray.Double

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/<a href="package-summary/html.md#wraparound">wraparound format</A>'><a href="package-summary.html#wraparound">wraparound format</A></a> <br>

<a href="https://github.com/autoplot/dev/search?q=toWraparoundOrder&unscoped_q=toWraparoundOrder">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

toWraparoundOrder( org.das2.qds.math.fft.ComplexArray.Double data, int i0, int stride ) &rarr; double<br>
***
<a name="transform"></a>
# transform
transform( org.das2.qds.math.fft.ComplexArray.Double data ) &rarr; void

Compute the Fast Fourier Transform of data leaving the result in data.

### Parameters:
data - a ComplexArray.Double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=transform&unscoped_q=transform">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

transform( org.das2.qds.math.fft.ComplexArray.Double data, int i0, int stride ) &rarr; void<br>
