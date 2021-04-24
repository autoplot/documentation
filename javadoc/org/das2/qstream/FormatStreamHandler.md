# org.das2.qstream.FormatStreamHandler

Writes the stream based on the messages sent to it.  This overlaps with the SimpleStreamFormatter,
 but was needed to support streams.  The SimpleStreamFormatter took a QDataSet and formatted it.  This formats
 based on the callbacks.

 Note the library was poorly designed, and this is pretty simple because most of the hard work is buried within
 the StreamDescriptor.  StreamDescriptor should be simplified, and the code should be moved to here.

# FormatStreamHandler( )


***
<a name="createStreamDescriptor"></a>
# createStreamDescriptor
createStreamDescriptor( String name, boolean asciiTypes, boolean isBigEndian ) &rarr; StreamDescriptor

create a stream descriptor packet.  TODO: createPacketDescriptor.  See SerialStreamFormatter for examples of how this
 would be done.

### Parameters:
name - a String
<br>asciiTypes - a boolean
<br>isBigEndian - a boolean

### Returns:
an org.das2.qstream.StreamDescriptor


<a href="https://github.com/autoplot/dev/search?q=createStreamDescriptor&unscoped_q=createStreamDescriptor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="packet"></a>
# packet
packet( org.das2.qstream.PacketDescriptor pd, java.nio.ByteBuffer data ) &rarr; void



### Parameters:
pd - a PacketDescriptor
<br>data - a ByteBuffer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=packet&unscoped_q=packet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="packetDescriptor"></a>
# packetDescriptor
packetDescriptor( org.das2.qstream.PacketDescriptor pd ) &rarr; void



### Parameters:
pd - a PacketDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=packetDescriptor&unscoped_q=packetDescriptor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setOutputStream"></a>
# setOutputStream
setOutputStream( java.io.OutputStream outs ) &rarr; void



### Parameters:
outs - an OutputStream

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setOutputStream&unscoped_q=setOutputStream">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setWritableByteChannel"></a>
# setWritableByteChannel
setWritableByteChannel( java.nio.channels.WritableByteChannel outs ) &rarr; void



### Parameters:
outs - a WritableByteChannel

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setWritableByteChannel&unscoped_q=setWritableByteChannel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="streamClosed"></a>
# streamClosed
streamClosed( org.das2.qstream.StreamDescriptor sd ) &rarr; void



### Parameters:
sd - a StreamDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=streamClosed&unscoped_q=streamClosed">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="streamComment"></a>
# streamComment
streamComment( org.das2.qstream.StreamComment se ) &rarr; void



### Parameters:
se - a StreamComment

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=streamComment&unscoped_q=streamComment">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="streamDescriptor"></a>
# streamDescriptor
streamDescriptor( org.das2.qstream.StreamDescriptor sd ) &rarr; void



### Parameters:
sd - a StreamDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=streamDescriptor&unscoped_q=streamDescriptor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="streamException"></a>
# streamException
streamException( org.das2.qstream.StreamException se ) &rarr; void



### Parameters:
se - a StreamException

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=streamException&unscoped_q=streamException">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

