# org.das2.qstream.PacketDescriptor



***
<a name="addPlane"></a>
# addPlane
addPlane( org.das2.qstream.PlaneDescriptor planeDescriptor ) &rarr; void



### Parameters:
planeDescriptor - a PlaneDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPlane&unscoped_q=addPlane">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="clone"></a>
# clone
clone(  ) &rarr; Object



### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=clone&unscoped_q=clone">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDomElement"></a>
# getDomElement
getDomElement(  ) &rarr; Element



### Returns:
org.w3c.dom.Element


<a href="https://github.com/autoplot/dev/search?q=getDomElement&unscoped_q=getDomElement">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPacketId"></a>
# getPacketId
getPacketId(  ) &rarr; int

return the packet ID, which is a number from 1-99.

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=getPacketId&unscoped_q=getPacketId">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlanes"></a>
# getPlanes
getPlanes(  ) &rarr; List

return the list of planes in an unmodifiable list.

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=getPlanes&unscoped_q=getPlanes">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isStream"></a>
# isStream
isStream(  ) &rarr; boolean

If true, then slices of the dataset fill each packet.

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isStream&unscoped_q=isStream">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDomElement"></a>
# setDomElement
setDomElement( org.w3c.dom.Element packetElement ) &rarr; void



### Parameters:
packetElement - an Element

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDomElement&unscoped_q=setDomElement">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPacketId"></a>
# setPacketId
setPacketId( int packetId ) &rarr; void

keep track of the packet ID, which is a number from 1-99.

### Parameters:
packetId - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPacketId&unscoped_q=setPacketId">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setStream"></a>
# setStream
setStream( boolean stream ) &rarr; void



### Parameters:
stream - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setStream&unscoped_q=setStream">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setStreamRank"></a>
# setStreamRank
setStreamRank( int streamRank ) &rarr; void

number of dimensions being streamed.  Zero means all the data is
 found in the first packet (no streaming).  One means a qube is being
 streamed.  Two means a this packet is one qube of a higher rank dataset.

### Parameters:
streamRank - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setStreamRank&unscoped_q=setStreamRank">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="sizeBytes"></a>
# sizeBytes
sizeBytes(  ) &rarr; int

calculate the number of bytes in each packet.

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=sizeBytes&unscoped_q=sizeBytes">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="streamRank"></a>
# streamRank
streamRank(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=streamRank&unscoped_q=streamRank">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

