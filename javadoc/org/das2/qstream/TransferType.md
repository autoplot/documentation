# org.das2.qstream.TransferType

A transfer type is an encoding of a double on to the stream.  It must have a fixed length in bytes.
 Some are pure ASCII, and isAscii can be used to check this.

# TransferType( )


***
<a name="allocate"></a>
# allocate
allocate( int recordLengthBytes, java.nio.ByteOrder byteOrder ) &rarr; ByteBuffer

convenient method which gently reminds that the ByteOrder needs to be
 specified with ByteBuffers.  ByteBuffers are created with big endian 
 turned on, but more often little endian is used.

### Parameters:
recordLengthBytes - an int
<br>byteOrder - a ByteOrder

### Returns:
the byte buffer with the order set.

<a href="https://github.com/autoplot/dev/search?q=allocate&unscoped_q=allocate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getForName"></a>
# getForName
getForName( String ttype, java.util.Map properties ) &rarr; TransferType

returns a TranferType for the given name, or null if none is found.

### Parameters:
ttype - a String
<br>properties - map of dataset properties.  Introduced to pass in time Unit to AsciiTimeTransferType without unduly coupling codes.

### Returns:
returns a TranferType for the given name, or null if none is found.

<a href="https://github.com/autoplot/dev/search?q=getForName&unscoped_q=getForName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isAscii"></a>
# isAscii
isAscii(  ) &rarr; boolean

return true if the transfer type uses ASCII-encodings to represent data.
 It's assumed in this case that trailing whitespace can be modified for
 readability.

### Returns:
true if the type is ASCII-based.

<a href="https://github.com/autoplot/dev/search?q=isAscii&unscoped_q=isAscii">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="name"></a>
# name
name(  ) &rarr; String

return a string identifying the TransferType.

### Returns:
the name

<a href="https://github.com/autoplot/dev/search?q=name&unscoped_q=name">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="read"></a>
# read
read( java.nio.ByteBuffer buffer ) &rarr; double

read the data from the buffer.  The implementations will increment the 
 buffer's position by sizeBytes.

### Parameters:
buffer - the container for the transfer type.

### Returns:
the value read

<a href="https://github.com/autoplot/dev/search?q=read&unscoped_q=read">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="sizeBytes"></a>
# sizeBytes
sizeBytes(  ) &rarr; int

return the number of bytes used by the transfer type.

### Returns:
the size of the type in bytes.

<a href="https://github.com/autoplot/dev/search?q=sizeBytes&unscoped_q=sizeBytes">[search for examples]</a>

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
write( double d, java.nio.ByteBuffer buffer ) &rarr; void

write the data to the buffer.  The buffer's position should be incremented by sizeBytes.

### Parameters:
d - the value to write.
<br>buffer - the byte buffer positioned to receive sizeByte bytes.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=write&unscoped_q=write">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

