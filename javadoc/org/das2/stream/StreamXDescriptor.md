# org.das2.stream.StreamXDescriptor



# StreamXDescriptor( )


# StreamXDescriptor( org.w3c.dom.Element element )


***
<a name="clone"></a>
# clone
clone(  ) &rarr; Object



### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=clone&unscoped_q=clone">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBase"></a>
# getBase
getBase(  ) &rarr; Datum



### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getBase&unscoped_q=getBase">[search for examples]</a>
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
<a name="readDatum"></a>
# readDatum
readDatum( java.nio.ByteBuffer input ) &rarr; Datum



### Parameters:
input - a ByteBuffer

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=readDatum&unscoped_q=readDatum">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setBase"></a>
# setBase
setBase( Datum base ) &rarr; void



### Parameters:
base - a Datum

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setBase&unscoped_q=setBase">[search for examples]</a>
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

***
<a name="writeDatum"></a>
# writeDatum
writeDatum( Datum datum, java.nio.ByteBuffer output ) &rarr; void



### Parameters:
datum - a Datum
<br>output - a ByteBuffer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeDatum&unscoped_q=writeDatum">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

