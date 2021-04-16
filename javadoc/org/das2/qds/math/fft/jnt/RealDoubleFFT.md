# org.das2.qds.math.fft.jnt.RealDoubleFFTAbstract Class representing FFT's of real, double precision data.
 Concrete classes are typically named RealDoubleFFT_<i>method</i>, implement the
 FFT using some particular method.
 <P>
 The physical layout of the mathematical data d[i] in the array data is as follows:
<PRE>
    d[i] = data[i0 + stride*i]
</PRE>
 The FFT (D[i]) of real data (d[i]) is complex, but restricted by symmetry:
<PRE>
    D[n-i] = conj(D[i])
</PRE>
 It turns out that there are still n `independent' values, so the transformation
 can still be carried out in-place.
 However, each Real FFT method tends to leave the real and imaginary parts 
 distributed in the data array in its own unique arrangment.  
 <P>
 You must consult the documentation for the specific classes implementing
 RealDoubleFFT for the details.
 Note, however, that each class's backtransform and inverse methods understand
 thier own unique ordering of the transformed result and can invert it correctly.
RealDoubleFFT( int n )
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

backtransform( org.das2.qds.math.fft.ComplexArray.Double data, int i0, int stride ) &rarr; void<br>
***
<a name="inverse"></a>
# inverse
inverse( org.das2.qds.math.fft.ComplexArray.Double data ) &rarr; void

Compute the (nomalized) inverse FFT of data, leaving it in place.

### Parameters:
data - a ComplexArray.Double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=inverse&unscoped_q=inverse">[search for examples]</a>

inverse( org.das2.qds.math.fft.ComplexArray.Double data, int i0, int stride ) &rarr; void<br>
***
<a name="normalization"></a>
# normalization
normalization(  ) &rarr; double

Return the normalization factor.  
 Multiply the elements of the backtransform'ed data to get the normalized inverse.

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=normalization&unscoped_q=normalization">[search for examples]</a>

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

transform( org.das2.qds.math.fft.ComplexArray.Double data, int i0, int stride ) &rarr; void<br>
