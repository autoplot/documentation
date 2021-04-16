# org.das2.client.QDataSetStreamHandlerRead the Das2Stream into a QDataSet.
QDataSetStreamHandler( )


***
<a name="MODE_SPLIT_BY_PACKET_DESCRIPTOR"></a>
# MODE_SPLIT_BY_PACKET_DESCRIPTOR



***
<a name="MODE_SPLIT_BY_NEW_PACKET_DESCRIPTOR"></a>
# MODE_SPLIT_BY_NEW_PACKET_DESCRIPTOR



***
<a name="collectDataSet"></a>
# collectDataSet
collectDataSet(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=collectDataSet&unscoped_q=collectDataSet">[search for examples]</a>

***
<a name="createBuilders"></a>
# createBuilders
createBuilders( org.das2.stream.PacketDescriptor pd ) &rarr; void



### Parameters:
pd - a PacketDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=createBuilders&unscoped_q=createBuilders">[search for examples]</a>

***
<a name="getDataSet"></a>
# getDataSet
getDataSet(  ) &rarr; QDataSet

return the dataset collected by the handler, or null if no records have been received.

### Returns:
the dataset collected by the handler, or null if no records have been received.

<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>

***
<a name="packet"></a>
# packet
packet( org.das2.stream.PacketDescriptor pd, Datum xTag, org.das2.datum.DatumVector[] vectors ) &rarr; void



### Parameters:
pd - a PacketDescriptor
<br>xTag - a Datum
<br>vectors - an org.das2.datum.DatumVector[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=packet&unscoped_q=packet">[search for examples]</a>

***
<a name="packetDescriptor"></a>
# packetDescriptor
packetDescriptor( org.das2.stream.PacketDescriptor pd ) &rarr; void



### Parameters:
pd - a PacketDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=packetDescriptor&unscoped_q=packetDescriptor">[search for examples]</a>

***
<a name="setMonitor"></a>
# setMonitor
setMonitor( ProgressMonitor monitor ) &rarr; void



### Parameters:
monitor - a ProgressMonitor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMonitor&unscoped_q=setMonitor">[search for examples]</a>

***
<a name="streamClosed"></a>
# streamClosed
streamClosed( org.das2.stream.StreamDescriptor sd ) &rarr; void



### Parameters:
sd - a StreamDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=streamClosed&unscoped_q=streamClosed">[search for examples]</a>

***
<a name="streamComment"></a>
# streamComment
streamComment( org.das2.stream.StreamComment sc ) &rarr; void



### Parameters:
sc - a StreamComment

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=streamComment&unscoped_q=streamComment">[search for examples]</a>

***
<a name="streamDescriptor"></a>
# streamDescriptor
streamDescriptor( org.das2.stream.StreamDescriptor sd ) &rarr; void



### Parameters:
sd - a StreamDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=streamDescriptor&unscoped_q=streamDescriptor">[search for examples]</a>

***
<a name="streamException"></a>
# streamException
streamException( org.das2.stream.StreamException se ) &rarr; void



### Parameters:
se - a StreamException

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=streamException&unscoped_q=streamException">[search for examples]</a>

