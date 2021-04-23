# org.das2.qstream.StreamHandlerThis describes an object that is able to receive a stream from StreamTool.readStream, which breaks the stream up
 into descriptors and packets.  This was copied from das2's das2stream library to create QStream, which is to replace it.
 See http://das2.org/wiki/index.php/Das2/QStreams
***
<a name="packet"></a>
# packet
packet( org.das2.qstream.PacketDescriptor pd, java.nio.ByteBuffer data ) &rarr; void

receive a data packet from the stream.  The packet descriptor is used to describe the packet contents,
 and the ByteBuffer contains the bytes.  The byte buffer will have its position at the beginning of the data, and the limit
 will be the end of the data.  Note for filters, the buffer must be reset!

### Parameters:
pd - PacketDescriptor describing the data.
<br>data - ByteBuffer containing the data.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=packet&unscoped_q=packet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="packetDescriptor"></a>
# packetDescriptor
packetDescriptor( org.das2.qstream.PacketDescriptor pd ) &rarr; void

description of a new packet type. This packetDescriptor will also be sent as packets of data are received.

### Parameters:
pd - a PacketDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=packetDescriptor&unscoped_q=packetDescriptor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="streamClosed"></a>
# streamClosed
streamClosed( org.das2.qstream.StreamDescriptor sd ) &rarr; void

indicates the stream end is encountered.

### Parameters:
sd - a StreamDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=streamClosed&unscoped_q=streamClosed">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="streamComment"></a>
# streamComment
streamComment( org.das2.qstream.StreamComment sd ) &rarr; void

comments on the stream.

### Parameters:
sd - a StreamComment

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=streamComment&unscoped_q=streamComment">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="streamDescriptor"></a>
# streamDescriptor
streamDescriptor( org.das2.qstream.StreamDescriptor sd ) &rarr; void

initial description of the stream.  This contains global properties of the stream.
 TODO: should codes expect only one of these?  I think most probably do, but the spec says we should be able to pick up
 in the middle, implying that steamDescriptors may be resent.

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

This is used to indicate an exception occurred in the source.

### Parameters:
se - a StreamException

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=streamException&unscoped_q=streamException">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

