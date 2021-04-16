# org.das2.qstream.filter.ReduceFilterReduce packets of the same type by combining packets together.  Currently this
 just does linear averages of the data, but this can easily be extended to support
 other combinations, such as min and max.
ReduceFilter( )


***
<a name="packet"></a>
# packet
packet( org.das2.qstream.PacketDescriptor pd, java.nio.ByteBuffer data ) &rarr; void

accumulate data into packets by reducing them.

### Parameters:
pd - a PacketDescriptor
<br>data - a ByteBuffer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=packet&unscoped_q=packet">[search for examples]</a>

***
<a name="packetDescriptor"></a>
# packetDescriptor
packetDescriptor( org.das2.qstream.PacketDescriptor pd ) &rarr; void



### Parameters:
pd - a PacketDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=packetDescriptor&unscoped_q=packetDescriptor">[search for examples]</a>

***
<a name="setCadence"></a>
# setCadence
setCadence( Datum cadence ) &rarr; void

set the cadence to reduce to target the data.  This should be convertible to seconds.
 Note we assume all packets have the same offset units (e.g. microseconds).

### Parameters:
cadence - a Datum

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCadence&unscoped_q=setCadence">[search for examples]</a>

***
<a name="setSink"></a>
# setSink
setSink( org.das2.qstream.StreamHandler sink ) &rarr; void

set the sink for the stream components as they are processed.

### Parameters:
sink - a StreamHandler

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSink&unscoped_q=setSink">[search for examples]</a>

***
<a name="streamClosed"></a>
# streamClosed
streamClosed( org.das2.qstream.StreamDescriptor sd ) &rarr; void



### Parameters:
sd - a StreamDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=streamClosed&unscoped_q=streamClosed">[search for examples]</a>

***
<a name="streamComment"></a>
# streamComment
streamComment( org.das2.qstream.StreamComment se ) &rarr; void



### Parameters:
se - a StreamComment

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=streamComment&unscoped_q=streamComment">[search for examples]</a>

***
<a name="streamDescriptor"></a>
# streamDescriptor
streamDescriptor( org.das2.qstream.StreamDescriptor sd ) &rarr; void



### Parameters:
sd - a StreamDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=streamDescriptor&unscoped_q=streamDescriptor">[search for examples]</a>

***
<a name="streamException"></a>
# streamException
streamException( org.das2.qstream.StreamException se ) &rarr; void



### Parameters:
se - a StreamException

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=streamException&unscoped_q=streamException">[search for examples]</a>

