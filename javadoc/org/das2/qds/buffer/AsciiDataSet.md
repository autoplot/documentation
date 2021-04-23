# org.das2.qds.buffer.AsciiDataSet

Sometimes you might just have numbers encoded in ASCII within a binary stream, 
 or fixed-length fields allow such parsing.

# AsciiDataSet( int rank, int reclen, int recoffs, int len0, int len1, int len2, int len3, java.nio.ByteBuffer back, Object type )
Like the other constructors, but the type is needed as well to get the 
 number of bytes.

***
<a name="putValue"></a>
# putValue
putValue( double d ) &rarr; void



### Parameters:
d - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putValue&unscoped_q=putValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

putValue( int i0, double d ) &rarr; void<br>
putValue( int i0, int i1, double d ) &rarr; void<br>
putValue( int i0, int i1, int i2, double d ) &rarr; void<br>
putValue( int i0, int i1, int i2, int i3, double d ) &rarr; void<br>
***
<a name="setLengthBytes"></a>
# setLengthBytes
setLengthBytes( int length ) &rarr; void



### Parameters:
length - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLengthBytes&unscoped_q=setLengthBytes">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="value"></a>
# value
value(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

value( int i0 ) &rarr; double<br>
value( int i0, int i1 ) &rarr; double<br>
value( int i0, int i1, int i2 ) &rarr; double<br>
value( int i0, int i1, int i2, int i3 ) &rarr; double<br>
