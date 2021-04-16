# org.das2.util.Base64This class consists exclusively of static methods for obtaining
 encoders and decoders for the Base64 encoding scheme. The
 implementation of this class supports the following types of Base64
 as specified in
 <a href="http://www.ietf.org/rfc/rfc4648.txt">RFC 4648</a> and
 <a href="http://www.ietf.org/rfc/rfc2045.txt">RFC 2045</a>.

 <ul>
 <li><a name="basic"><b>Basic</b></a>
 <p> Uses "The Base64 Alphabet" as specified in Table 1 of
     RFC 4648 and RFC 2045 for encoding and decoding operation.
     The encoder does not add any line feed (line separator)
     character. The decoder rejects data that contains characters
     outside the base64 alphabet.</p></li>

 <li><a name="url"><b>URL and Filename safe</b></a>
 <p> Uses the "URL and Filename safe Base64 Alphabet" as specified
     in Table 2 of RFC 4648 for encoding and decoding. The
     encoder does not add any line feed (line separator) character.
     The decoder rejects data that contains characters outside the
     base64 alphabet.</p></li>

 <li><a name="mime"><b>MIME</b></a>
 <p> Uses the "The Base64 Alphabet" as specified in Table 1 of
     RFC 2045 for encoding and decoding operation. The encoded output
     must be represented in lines of no more than 76 characters each
     and uses a carriage return {@code '\r'} followed immediately by
     a linefeed {@code '\n'} as the line separator. No line separator
     is added to the end of the encoded output. All line separators
     or other characters not found in the base64 alphabet table are
     ignored in decoding operation.</p></li>
 </ul>

 <p> Unless otherwise noted, passing a {@code null} argument to a
 method of this class will cause a {@link java.lang.NullPointerException
 NullPointerException} to be thrown.
***
<a name="getDecoder"></a>
# getDecoder
getDecoder(  ) &rarr; Decoder

Returns a {@link Decoder} that decodes using the
 <a href="#basic">Basic</a> type base64 encoding scheme.

### Returns:
A Base64 decoder.

<a href="https://github.com/autoplot/dev/search?q=getDecoder&unscoped_q=getDecoder">[search for examples]</a>

***
<a name="getEncoder"></a>
# getEncoder
getEncoder(  ) &rarr; Encoder

Returns a {@link Encoder} that encodes using the
 <a href="#basic">Basic</a> type base64 encoding scheme.

### Returns:
A Base64 encoder.

<a href="https://github.com/autoplot/dev/search?q=getEncoder&unscoped_q=getEncoder">[search for examples]</a>

***
<a name="getMimeDecoder"></a>
# getMimeDecoder
getMimeDecoder(  ) &rarr; Decoder

Returns a {@link Decoder} that decodes using the
 <a href="#mime">MIME</a> type base64 decoding scheme.

### Returns:
A Base64 decoder.

<a href="https://github.com/autoplot/dev/search?q=getMimeDecoder&unscoped_q=getMimeDecoder">[search for examples]</a>

***
<a name="getMimeEncoder"></a>
# getMimeEncoder
getMimeEncoder(  ) &rarr; Encoder

Returns a {@link Encoder} that encodes using the
 <a href="#mime">MIME</a> type base64 encoding scheme.

### Returns:
A Base64 encoder.

<a href="https://github.com/autoplot/dev/search?q=getMimeEncoder&unscoped_q=getMimeEncoder">[search for examples]</a>

getMimeEncoder( int lineLength, byte[] lineSeparator ) &rarr; Encoder<br>
***
<a name="getUrlDecoder"></a>
# getUrlDecoder
getUrlDecoder(  ) &rarr; Decoder

Returns a {@link Decoder} that decodes using the
 <a href="#url">URL and Filename safe</a> type base64
 encoding scheme.

### Returns:
A Base64 decoder.

<a href="https://github.com/autoplot/dev/search?q=getUrlDecoder&unscoped_q=getUrlDecoder">[search for examples]</a>

***
<a name="getUrlEncoder"></a>
# getUrlEncoder
getUrlEncoder(  ) &rarr; Encoder

Returns a {@link Encoder} that encodes using the
 <a href="#url">URL and Filename safe</a> type base64
 encoding scheme.

### Returns:
A Base64 encoder.

<a href="https://github.com/autoplot/dev/search?q=getUrlEncoder&unscoped_q=getUrlEncoder">[search for examples]</a>

