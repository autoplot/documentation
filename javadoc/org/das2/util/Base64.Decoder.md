# org.das2.util.Base64.DecoderThis class implements a decoder for decoding byte data using the
 Base64 encoding scheme as specified in RFC 4648 and RFC 2045.

 <p> The Base64 padding character {@code '='} is accepted and
 interpreted as the end of the encoded byte data, but is not
 required. So if the final unit of the encoded byte data only has
 two or three Base64 characters (without the corresponding padding
 character(s) padded), they are decoded as if followed by padding
 character(s). If there is a padding character present in the
 final unit, the correct number of padding character(s) must be
 present, otherwise {@code IllegalArgumentException} (
 {@code IOException} when reading from a Base64 stream) is thrown
 during decoding.

 <p> Instances of {@link Decoder} class are safe for use by
 multiple concurrent threads.

 <p> Unless otherwise noted, passing a {@code null} argument to
 a method of this class will cause a
 {@link java.lang.NullPointerException NullPointerException} to
 be thrown.
***
<a name="decode"></a>
# decode
decode( byte[] src ) &rarr; byte

Decodes all bytes from the input byte array using the {@link Base64}
 encoding scheme, writing the results into a newly-allocated output
 byte array. The returned byte array is of the length of the resulting
 bytes.

### Parameters:
src - the byte array to decode

### Returns:
A newly-allocated byte array containing the decoded bytes.

<a href="https://github.com/autoplot/dev/search?q=decode&unscoped_q=decode">[search for examples]</a>

decode( String src ) &rarr; byte<br>
decode( byte[] src, byte[] dst ) &rarr; int<br>
decode( java.nio.ByteBuffer buffer ) &rarr; ByteBuffer<br>
***
<a name="wrap"></a>
# wrap
wrap( java.io.InputStream is ) &rarr; InputStream

Returns an input stream for decoding {@link Base64} encoded byte stream.

 <p> The  read  methods of the returned  InputStream will
 throw  IOException when reading bytes that cannot be decoded.

 <p> Closing the returned input stream will close the underlying
 input stream.

### Parameters:
is - the input stream

### Returns:
the input stream for decoding the specified Base64 encoded
          byte stream

<a href="https://github.com/autoplot/dev/search?q=wrap&unscoped_q=wrap">[search for examples]</a>

