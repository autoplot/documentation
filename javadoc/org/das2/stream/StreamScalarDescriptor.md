# org.das2.stream.StreamScalarDescriptor

This is a rank 1 element of a packet, either a dependent or independent 
 parameter.

# StreamScalarDescriptor( org.w3c.dom.Element element )


# StreamScalarDescriptor( )


***
<a name="clone"></a>
# clone
clone(  ) &rarr; Object



### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=clone&unscoped_q=clone">[search for examples]</a>

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
<a name="getDataTransferType"></a>
# getDataTransferType
getDataTransferType(  ) &rarr; DataTransferType



### Returns:
org.das2.stream.DataTransferType


<a href="https://github.com/autoplot/dev/search?q=getDataTransferType&unscoped_q=getDataTransferType">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getName"></a>
# getName
getName(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getName&unscoped_q=getName">[search for examples]</a>

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
<a name="getUnits"></a>
# getUnits
getUnits(  ) &rarr; Units



### Returns:
org.das2.datum.Units


<a href="https://github.com/autoplot/dev/search?q=getUnits&unscoped_q=getUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="read"></a>
# read
read( java.nio.ByteBuffer input ) &rarr; DatumVector



### Parameters:
input - a ByteBuffer

### Returns:
org.das2.datum.DatumVector


<a href="https://github.com/autoplot/dev/search?q=read&unscoped_q=read">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataTransferType"></a>
# setDataTransferType
setDataTransferType( org.das2.stream.DataTransferType transferType ) &rarr; void



### Parameters:
transferType - a DataTransferType

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataTransferType&unscoped_q=setDataTransferType">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setName"></a>
# setName
setName( String name ) &rarr; void



### Parameters:
name - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setName&unscoped_q=setName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setUnits"></a>
# setUnits
setUnits( Units units ) &rarr; void



### Parameters:
units - an Units

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUnits&unscoped_q=setUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="write"></a>
# write
write( org.das2.datum.DatumVector input, java.nio.ByteBuffer output ) &rarr; void



### Parameters:
input - a DatumVector
<br>output - a ByteBuffer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=write&unscoped_q=write">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

