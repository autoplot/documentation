# org.das2.util.ByteBufferInputStream

An input stream that wraps an NIO ByteBuffer.  Reading from this stream
 will update the ByteBuffers position.  Calling mark() on this input stream
 will set the mark on the underlying buffer.

# ByteBufferInputStream( java.nio.ByteBuffer buffer )
Creates a new instance of ByteBufferInputStream

***
<a name="available"></a>
# available
available(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=available&unscoped_q=available">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="close"></a>
# close
close(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=close&unscoped_q=close">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getByteBuffer"></a>
# getByteBuffer
getByteBuffer(  ) &rarr; ByteBuffer



### Returns:
java.nio.ByteBuffer


<a href="https://github.com/autoplot/dev/search?q=getByteBuffer&unscoped_q=getByteBuffer">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mark"></a>
# mark
mark( int readlimit ) &rarr; void



### Parameters:
readlimit - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mark&unscoped_q=mark">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="markSupported"></a>
# markSupported
markSupported(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=markSupported&unscoped_q=markSupported">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="read"></a>
# read
read(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=read&unscoped_q=read">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

read( byte[] b ) &rarr; int<br>
read( byte[] b, int off, int len ) &rarr; int<br>
***
<a name="reset"></a>
# reset
reset(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reset&unscoped_q=reset">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="skip"></a>
# skip
skip( long n ) &rarr; long



### Parameters:
n - a long

### Returns:
long


<a href="https://github.com/autoplot/dev/search?q=skip&unscoped_q=skip">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

