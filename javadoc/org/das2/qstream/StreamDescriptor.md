# org.das2.qstream.StreamDescriptor

Description of the Stream, and manages resources for the stream.

# StreamDescriptor( javax.xml.parsers.DocumentBuilderFactory factory )


***
<a name="addDescriptor"></a>
# addDescriptor
addDescriptor( org.das2.qstream.Descriptor pd ) &rarr; void

add the descriptor to the stream, manually assigning it an id

### Parameters:
pd - a Descriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addDescriptor&unscoped_q=addDescriptor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addDescriptor( org.das2.qstream.Descriptor pd, int descriptorId ) &rarr; void<br>
***
<a name="descriptorId"></a>
# descriptorId
descriptorId( org.das2.qstream.Descriptor pd ) &rarr; int

get the id for the descriptor.  Note packetDescriptors contain the id, 
 but this is not used.

### Parameters:
pd - the packet descriptor.

### Returns:
the id

<a href="https://github.com/autoplot/dev/search?q=descriptorId&unscoped_q=descriptorId">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getByteOrder"></a>
# getByteOrder
getByteOrder(  ) &rarr; ByteOrder



### Returns:
java.nio.ByteOrder


<a href="https://github.com/autoplot/dev/search?q=getByteOrder&unscoped_q=getByteOrder">[search for examples]</a>
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
<a name="hasDescriptor"></a>
# hasDescriptor
hasDescriptor( org.das2.qstream.Descriptor pd0, int descriptorId ) &rarr; boolean

If a second PacketDescriptor contains the same descriptor information, then the PacketDescriptor can be
 dropped.  This was introduced when two daily streams appended did not create a valid stream.
 
 It has the descriptor if:
 * the number is the same
 * the planes within are the same ids.

### Parameters:
pd0 - a Descriptor
<br>descriptorId - an int

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=hasDescriptor&unscoped_q=hasDescriptor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isAsciiTypes"></a>
# isAsciiTypes
isAsciiTypes(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isAsciiTypes&unscoped_q=isAsciiTypes">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="newDocument"></a>
# newDocument
newDocument( org.das2.qstream.Descriptor descriptor ) &rarr; Document

get the XML document that will contain the descriptor.  Note that
 a QStream will have many XML documents, one for each descriptor.  This
 keeps track of the documents for each descriptor.

### Parameters:
descriptor - the descriptor

### Returns:
the Document, which will have elements added to it.

<a href="https://github.com/autoplot/dev/search?q=newDocument&unscoped_q=newDocument">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="retireDescriptor"></a>
# retireDescriptor
retireDescriptor( org.das2.qstream.Descriptor pd ) &rarr; void

indicate that no more packets will be sent with this descriptor.
 This will free up the number so it can be reused.

### Parameters:
pd - the descriptor.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=retireDescriptor&unscoped_q=retireDescriptor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="send"></a>
# send
send( org.das2.qstream.Descriptor pd, java.nio.channels.WritableByteChannel out ) &rarr; void



### Parameters:
pd - a Descriptor
<br>out - a WritableByteChannel

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=send&unscoped_q=send">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAsciiTypes"></a>
# setAsciiTypes
setAsciiTypes( boolean asciiTypes ) &rarr; void



### Parameters:
asciiTypes - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAsciiTypes&unscoped_q=setAsciiTypes">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setByteOrder"></a>
# setByteOrder
setByteOrder( java.nio.ByteOrder byteOrder ) &rarr; void



### Parameters:
byteOrder - a ByteOrder

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setByteOrder&unscoped_q=setByteOrder">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDomElement"></a>
# setDomElement
setDomElement( org.w3c.dom.Element element ) &rarr; void



### Parameters:
element - an Element

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDomElement&unscoped_q=setDomElement">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

