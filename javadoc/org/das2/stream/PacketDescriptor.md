# org.das2.stream.PacketDescriptor

Represents the global properties of the stream, that are accessible to
 datasets within.

# PacketDescriptor( org.w3c.dom.Element element )
creates a new PacketDescriptor

# PacketDescriptor( int id, org.w3c.dom.Element element )
creates a new PacketDescriptor

# PacketDescriptor( )


***
<a name="addYDescriptor"></a>
# addYDescriptor
addYDescriptor( org.das2.stream.SkeletonDescriptor y ) &rarr; void



### Parameters:
y - a SkeletonDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addYDescriptor&unscoped_q=addYDescriptor">[search for examples]</a>
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
<a name="createLegacyPacketDescriptor"></a>
# createLegacyPacketDescriptor
createLegacyPacketDescriptor( java.util.Map dsdf ) &rarr; PacketDescriptor



### Parameters:
dsdf - a java.util.Map

### Returns:
org.das2.stream.PacketDescriptor


<a href="https://github.com/autoplot/dev/search?q=createLegacyPacketDescriptor&unscoped_q=createLegacyPacketDescriptor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDOMElement"></a>
# getDOMElement
getDOMElement( org.w3c.dom.Document document ) &rarr; Element



### Parameters:
document - a Document

### Returns:
org.w3c.dom.Element


<a href="https://github.com/autoplot/dev/search?q=getDOMElement&unscoped_q=getDOMElement">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getId"></a>
# getId
getId(  ) &rarr; int

return the ID associated with this packet type, or -99 if no id
 has been assigned.

### Returns:
the id or -99

<a href="https://github.com/autoplot/dev/search?q=getId&unscoped_q=getId">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getProperties"></a>
# getProperties
getProperties(  ) &rarr; Map



### Returns:
java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getProperties&unscoped_q=getProperties">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getProperty"></a>
# getProperty
getProperty( String name ) &rarr; Object



### Parameters:
name - a String

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=getProperty&unscoped_q=getProperty">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSizeBytes"></a>
# getSizeBytes
getSizeBytes(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getSizeBytes&unscoped_q=getSizeBytes">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getXDescriptor"></a>
# getXDescriptor
getXDescriptor(  ) &rarr; StreamXDescriptor



### Returns:
org.das2.stream.StreamXDescriptor


<a href="https://github.com/autoplot/dev/search?q=getXDescriptor&unscoped_q=getXDescriptor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getYCount"></a>
# getYCount
getYCount(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getYCount&unscoped_q=getYCount">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getYDescriptor"></a>
# getYDescriptor
getYDescriptor( int index ) &rarr; SkeletonDescriptor



### Parameters:
index - an int

### Returns:
org.das2.stream.SkeletonDescriptor


<a href="https://github.com/autoplot/dev/search?q=getYDescriptor&unscoped_q=getYDescriptor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getYDescriptors"></a>
# getYDescriptors
getYDescriptors(  ) &rarr; List

Returns a List of SkeletonDescriptor instances that represent the y
 planes in a packet.  The List is unmodifiable and will throw an exception
 if any attempt is made to alter the list.  The contents of the list will
 not be updated if a yDescriptor is added to this packet descriptor.

### Returns:
a List of y planes

<a href="https://github.com/autoplot/dev/search?q=getYDescriptors&unscoped_q=getYDescriptors">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="read"></a>
# read
read( java.nio.ByteBuffer input ) &rarr; DatumVector



### Parameters:
input - a ByteBuffer

### Returns:
org.das2.datum.DatumVector[]


<a href="https://github.com/autoplot/dev/search?q=read&unscoped_q=read">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setProperty"></a>
# setProperty
setProperty( String name, Object value ) &rarr; void



### Parameters:
name - a String
<br>value - an Object

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setProperty&unscoped_q=setProperty">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setXDescriptor"></a>
# setXDescriptor
setXDescriptor( org.das2.stream.StreamXDescriptor x ) &rarr; void



### Parameters:
x - a StreamXDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setXDescriptor&unscoped_q=setXDescriptor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="write"></a>
# write
write( Datum xTag, org.das2.datum.DatumVector[] vectors, java.nio.ByteBuffer output ) &rarr; void



### Parameters:
xTag - a Datum
<br>vectors - an org.das2.datum.DatumVector[]
<br>output - a ByteBuffer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=write&unscoped_q=write">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

