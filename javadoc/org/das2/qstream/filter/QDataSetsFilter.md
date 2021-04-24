# org.das2.qstream.filter.QDataSetsFilter

Use this to promote the abstraction of the stream to QDataSets.  This was
 introduced when it became clear that to introduce an FFT filter would be
 quite difficult with the StreamHandler interface.  For example, take a simple
 rank 2 spectrogram.  The DEPEND_1 tags can be encoded inline, or as a single
 packet.  It would be burdensome to have to handle both cases.

# QDataSetsFilter( )


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
<a name="setSink"></a>
# setSink
setSink( org.das2.qstream.filter.QDataSetsFilter.QDataSetSink sink ) &rarr; void



### Parameters:
sink - a QDataSetsFilter.QDataSetSink

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSink&unscoped_q=setSink">[search for examples]</a>
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

