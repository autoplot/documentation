# org.das2.qstream.StreamTool

Code for reading streams.  This sends packets to a StreamHandler.

# StreamTool( )
Creates a new instance of StreamTool

***
<a name="advanceTo"></a>
# advanceTo
advanceTo( java.io.InputStream in, byte[] delim ) &rarr; byte



### Parameters:
in - an InputStream
<br>delim - a byte[]

### Returns:
byte[]


<a href="https://github.com/autoplot/dev/search?q=advanceTo&unscoped_q=advanceTo">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="formatHeader"></a>
# formatHeader
formatHeader( org.w3c.dom.Document document, java.io.Writer writer ) &rarr; void



### Parameters:
document - a Document
<br>writer - a Writer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=formatHeader&unscoped_q=formatHeader">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readStream"></a>
# readStream
readStream( java.nio.channels.ReadableByteChannel stream, org.das2.qstream.StreamHandler handler ) &rarr; void



### Parameters:
stream - a ReadableByteChannel
<br>handler - a StreamHandler

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=readStream&unscoped_q=readStream">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readXML"></a>
# readXML
readXML( java.io.PushbackInputStream in ) &rarr; byte

Read off XML data from the InputStream up to the termination of the XML.
 XML data is returned in a byte array.  The InputStream is left just
 following the XML terminator.  Processing is done with as little interpretation
 as possible, so invalid XML will cause problems with little feedback about
 what's wrong.

### Parameters:
in - a PushbackInputStream

### Returns:
byte[]


<a href="https://github.com/autoplot/dev/search?q=readXML&unscoped_q=readXML">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

readXML( java.nio.ByteBuffer input ) &rarr; ByteBuffer<br>
