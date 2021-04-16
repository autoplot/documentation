# org.das2.math.fft.GeneralFFTProvides forward and reverse FFT methods for any number of elements.  The FFTs
 are implemented using a modified version of the jnt.FFT package from NIST.  This
 version operates on ComplexArray objects that may be backed by das2 data sets
 avoiding unnecessary copies.
GeneralFFT( int n, boolean doublePrecision, boolean real )
Initialize the FFT object by constructing wave tables that can be repeatly used.

***
<a name="invTransform"></a>
# invTransform
invTransform( org.das2.math.fft.ComplexArray.Double data ) &rarr; void

perform the inverse transform on the array in situ.

### Parameters:
data - a ComplexArray.Double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=invTransform&unscoped_q=invTransform">[search for examples]</a>

invTransform( org.das2.math.fft.ComplexArray.Float data ) &rarr; void<br>
***
<a name="newDoubleFFT"></a>
# newDoubleFFT
newDoubleFFT( int n ) &rarr; GeneralFFT

creates an FFT object that operates on a ComplexArray.Double of n elements.

### Parameters:
n - an int

### Returns:
org.das2.math.fft.GeneralFFT


<a href="https://github.com/autoplot/dev/search?q=newDoubleFFT&unscoped_q=newDoubleFFT">[search for examples]</a>

***
<a name="newFloatFFT"></a>
# newFloatFFT
newFloatFFT( int n ) &rarr; GeneralFFT

creates an FFT object that operates on a ComplexArray.Float of n elements.

### Parameters:
n - an int

### Returns:
org.das2.math.fft.GeneralFFT


<a href="https://github.com/autoplot/dev/search?q=newFloatFFT&unscoped_q=newFloatFFT">[search for examples]</a>

***
<a name="size"></a>
# size
size(  ) &rarr; int

return the number of points in the fft.

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=size&unscoped_q=size">[search for examples]</a>

***
<a name="transform"></a>
# transform
transform( org.das2.math.fft.ComplexArray.Double data ) &rarr; void

perform the forward transform on the array in situ.

### Parameters:
data - a ComplexArray.Double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=transform&unscoped_q=transform">[search for examples]</a>

transform( org.das2.math.fft.ComplexArray.Float data ) &rarr; void<br>
