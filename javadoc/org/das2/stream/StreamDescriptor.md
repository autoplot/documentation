# org.das2.stream.StreamDescriptor

Represents the global properties of the stream, that are accessible to
 datasets within.

# StreamDescriptor( org.w3c.dom.Element element )
Creates a new instance of StreamProperties

# StreamDescriptor( )


***
<a name="addYMulti"></a>
# addYMulti
addYMulti( org.das2.stream.StreamScalarDescriptor y ) &rarr; void



### Parameters:
y - a StreamScalarDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addYMulti&unscoped_q=addYMulti">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addYScan"></a>
# addYScan
addYScan( org.das2.stream.StreamYScanDescriptor y ) &rarr; void



### Parameters:
y - a StreamYScanDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addYScan&unscoped_q=addYScan">[search for examples]</a>

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
<a name="createHeader"></a>
# createHeader
createHeader( org.w3c.dom.Document document ) &rarr; String



### Parameters:
document - a Document

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=createHeader&unscoped_q=createHeader">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createLegacyDescriptor"></a>
# createLegacyDescriptor
createLegacyDescriptor( java.io.BufferedReader in ) &rarr; StreamDescriptor



### Parameters:
in - a BufferedReader

### Returns:
org.das2.stream.StreamDescriptor


<a href="https://github.com/autoplot/dev/search?q=createLegacyDescriptor&unscoped_q=createLegacyDescriptor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCompression"></a>
# getCompression
getCompression(  ) &rarr; String

Getter for property compression.

### Returns:
Value of property compression.

<a href="https://github.com/autoplot/dev/search?q=getCompression&unscoped_q=getCompression">[search for examples]</a>

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
<a name="getYDescriptors"></a>
# getYDescriptors
getYDescriptors(  ) &rarr; List



### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=getYDescriptors&unscoped_q=getYDescriptors">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parseHeader"></a>
# parseHeader
parseHeader( java.io.Reader header ) &rarr; Document



### Parameters:
header - a Reader

### Returns:
org.w3c.dom.Document


<a href="https://github.com/autoplot/dev/search?q=parseHeader&unscoped_q=parseHeader">[search for examples]</a>

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
<a name="setCompression"></a>
# setCompression
setCompression( String compression ) &rarr; void

Setter for property compression.

### Parameters:
compression - New value of property compression.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCompression&unscoped_q=setCompression">[search for examples]</a>

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
write( org.das2.datum.DatumVector input, java.nio.ByteBuffer output ) &rarr; void



### Parameters:
input - a DatumVector
<br>output - a ByteBuffer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=write&unscoped_q=write">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

