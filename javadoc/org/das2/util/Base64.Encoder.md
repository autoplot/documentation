# org.das2.util.Base64.EncoderThis class implements an encoder for encoding byte data using
 the Base64 encoding scheme as specified in RFC 4648 and RFC 2045.

 <p> Instances of {@link Encoder} class are safe for use by
 multiple concurrent threads.

 <p> Unless otherwise noted, passing a {@code null} argument to
 a method of this class will cause a
 {@link java.lang.NullPointerException NullPointerException} to
 be thrown.
***
<a name="encode"></a>
# encode
encode( byte[] src ) &rarr; byte

Encodes all bytes from the specified byte array into a newly-allocated
 byte array using the {@link Base64} encoding scheme. The returned byte
 array is of the length of the resulting bytes.

### Parameters:
src - the byte array to encode

### Returns:
A newly-allocated byte array containing the resulting
          encoded bytes.

<a href="https://github.com/autoplot/dev/search?q=encode&unscoped_q=encode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

encode( byte[] src, byte[] dst ) &rarr; int<br>
encode( java.nio.ByteBuffer buffer ) &rarr; ByteBuffer<br>
***
<a name="encodeToString"></a>
# encodeToString
encodeToString( byte[] src ) &rarr; String

Encodes the specified byte array into a String using the {@link Base64}
 encoding scheme.

 <p> This method first encodes all input bytes into a base64 encoded
 byte array and then constructs a new String by using the encoded byte
 array and the {@link java.nio.charset.StandardCharsets#ISO_8859_1
 ISO-8859-1} charset.

 <p> In other words, an invocation of this method has exactly the same
 effect as invoking
  new String(encode(src), StandardCharsets.ISO_8859_1).

### Parameters:
src - the byte array to encode

### Returns:
A String containing the resulting Base64 encoded characters

<a href="https://github.com/autoplot/dev/search?q=encodeToString&unscoped_q=encodeToString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="withoutPadding"></a>
# withoutPadding
withoutPadding(  ) &rarr; Encoder

Returns an encoder instance that encodes equivalently to this one,
 but without adding any padding character at the end of the encoded
 byte data.

 <p> The encoding scheme of this encoder instance is unaffected by
 this invocation. The returned encoder instance should be used for
 non-padding encoding operation.

### Returns:
an equivalent encoder that encodes without adding any
         padding character at the end

<a href="https://github.com/autoplot/dev/search?q=withoutPadding&unscoped_q=withoutPadding">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="wrap"></a>
# wrap
wrap( java.io.OutputStream os ) &rarr; OutputStream

Wraps an output stream for encoding byte data using the {@link Base64}
 encoding scheme.

 <p> It is recommended to promptly close the returned output stream after
 use, during which it will flush all possible leftover bytes to the underlying
 output stream. Closing the returned output stream will close the underlying
 output stream.

### Parameters:
os - the output stream.

### Returns:
the output stream for encoding the byte data into the
          specified Base64 encoded format

<a href="https://github.com/autoplot/dev/search?q=wrap&unscoped_q=wrap">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

