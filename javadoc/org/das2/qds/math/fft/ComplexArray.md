# org.das2.qds.math.fft.ComplexArray

Interface for passing complex arrays to and from FFT routines.  The intent is
 that the complex array can be backed by data in any format.  Each elements is
 readable and writeable via get and set methods for the real and imaginary components.

# ComplexArray( )


***
<a name="magnitude"></a>
# magnitude
magnitude( org.das2.qds.math.fft.ComplexArray.Double array ) &rarr; double

returns the magnitudes of each element in an array

### Parameters:
array - a ComplexArray.Double

### Returns:
double[]


<a href="https://github.com/autoplot/dev/search?q=magnitude&unscoped_q=magnitude">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

magnitude( org.das2.qds.math.fft.ComplexArray.Double array, int i ) &rarr; double<br>
***
<a name="magnitude2"></a>
# magnitude2
magnitude2( org.das2.qds.math.fft.ComplexArray.Double array, int i ) &rarr; double

returns the magnitude of an element in an array.

### Parameters:
array - the complex array.
<br>i - the element index

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=magnitude2&unscoped_q=magnitude2">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="newArray"></a>
# newArray
newArray( double[] real ) &rarr; Double

Creates a new ComplexArray from an array of real numbers.  The complex
 components of each element in the resulting array is zero.

### Parameters:
real - a double[]

### Returns:
org.das2.qds.math.fft.ComplexArray.Double


<a href="https://github.com/autoplot/dev/search?q=newArray&unscoped_q=newArray">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

newArray( double[] real, double[] imag ) &rarr; Double<br>
newArray( float[] real ) &rarr; Float<br>
newArray( float[] real, float[] imag ) &rarr; Float<br>
***
<a name="newArrayCopy"></a>
# newArrayCopy
newArrayCopy( double[] real ) &rarr; Double

Creates a new ComplexArray from a float array representing real numbers, but
 copies the original array so that it is not modified.

### Parameters:
real - a double[]

### Returns:
org.das2.qds.math.fft.ComplexArray.Double


<a href="https://github.com/autoplot/dev/search?q=newArrayCopy&unscoped_q=newArrayCopy">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="realPart"></a>
# realPart
realPart( org.das2.qds.math.fft.ComplexArray.Double array ) &rarr; double

returns the real parts of each element in an array.

### Parameters:
array - a ComplexArray.Double

### Returns:
double[]


<a href="https://github.com/autoplot/dev/search?q=realPart&unscoped_q=realPart">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString( org.das2.qds.math.fft.ComplexArray.Float array ) &rarr; String

converts a ComplexArray into an array for debugging purposes.

### Parameters:
array - a ComplexArray.Float

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

toString( org.das2.qds.math.fft.ComplexArray.Double array ) &rarr; String<br>
