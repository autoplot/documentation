# org.das2.qds.math.fft.jnt.ComplexFloatFFT

Abstract Class representing FFT's of complex, single precision data.
 Concrete classes are typically named ComplexFloatFFT_<i>method</i>, implement the
 FFT using some particular method.
 <P>
 Complex data is represented by 2 double values in sequence: the real and imaginary
 parts.  Thus, in the default case (i0=0, stride=2), N data points is represented
 by a double array dimensioned to 2*N.  To support 2D (and higher) transforms,
 an offset, i0 (where the first element starts) and stride (the distance from the
 real part of one value, to the next: at least 2 for complex values) can be supplied.
 The physical layout in the array data, of the mathematical data d[i] is as follows:
<PRE>
    Re(d[i]) = data[i0 + stride*i]
    Im(d[i]) = data[i0 + stride*i+1]
</PRE>
 The transformed data is returned in the original data array in
 <a href="package-summary.html#wraparound">wrap-around</A> order.

# ComplexFloatFFT( int n )
Create an FFT for transforming n points of Complex, single precision data.

***
<a name="backtransform"></a>
# backtransform
backtransform( org.das2.qds.math.fft.ComplexArray.Float data ) &rarr; void

Compute the (unnomalized) inverse FFT of data, leaving it in place.

### Parameters:
data - a ComplexArray.Float

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=backtransform&unscoped_q=backtransform">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

backtransform( org.das2.qds.math.fft.ComplexArray.Float data, int i0, int stride ) &rarr; void<br>
***
<a name="getInstance"></a>
# getInstance
getInstance( int n ) &rarr; ComplexFloatFFT

Creates an instance of a subclass of ComplexFloatFFT appropriate for data
 of n elements.

### Parameters:
n - an int

### Returns:
org.das2.qds.math.fft.jnt.ComplexFloatFFT


<a href="https://github.com/autoplot/dev/search?q=getInstance&unscoped_q=getInstance">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="inverse"></a>
# inverse
inverse( org.das2.qds.math.fft.ComplexArray.Float data ) &rarr; void

Compute the (nomalized) inverse FFT of data, leaving it in place.

### Parameters:
data - a ComplexArray.Float

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=inverse&unscoped_q=inverse">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

inverse( org.das2.qds.math.fft.ComplexArray.Float data, int i0, int stride ) &rarr; void<br>
***
<a name="normalization"></a>
# normalization
normalization(  ) &rarr; float

Return the normalization factor.  
 Multiply the elements of the backtransform'ed data to get the normalized inverse.

### Returns:
float


<a href="https://github.com/autoplot/dev/search?q=normalization&unscoped_q=normalization">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="transform"></a>
# transform
transform( org.das2.qds.math.fft.ComplexArray.Float data ) &rarr; void

Compute the Fast Fourier Transform of data leaving the result in data.
 The array data must be dimensioned (at least) 2*n, consisting of alternating
 real and imaginary parts.

### Parameters:
data - a ComplexArray.Float

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=transform&unscoped_q=transform">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

transform( org.das2.qds.math.fft.ComplexArray.Float data, int i0, int stride ) &rarr; void<br>
