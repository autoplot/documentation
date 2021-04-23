# org.das2.stream.DataTransferType



***
<a name="SUN_REAL4"></a>
# SUN_REAL4



***
<a name="SUN_REAL8"></a>
# SUN_REAL8



***
<a name="LITTLE_ENDIAN_REAL4"></a>
# LITTLE_ENDIAN_REAL4



***
<a name="LITTLE_ENDIAN_REAL8"></a>
# LITTLE_ENDIAN_REAL8



***
<a name="getByName"></a>
# getByName
getByName( String name ) &rarr; DataTransferType

returns the type or throws RuntimeException("Unsupported type")

### Parameters:
name - a String

### Returns:
an org.das2.stream.DataTransferType


<a href="https://github.com/autoplot/dev/search?q=getByName&unscoped_q=getByName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSizeBytes"></a>
# getSizeBytes
getSizeBytes(  ) &rarr; int

return the size of the item in bytes.

### Returns:
the size of the item in bytes.

<a href="https://github.com/autoplot/dev/search?q=getSizeBytes&unscoped_q=getSizeBytes">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isAscii"></a>
# isAscii
isAscii(  ) &rarr; boolean

If type terminates a line, then use \n to delineate

### Returns:
true if ascii

<a href="https://github.com/autoplot/dev/search?q=isAscii&unscoped_q=isAscii">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="read"></a>
# read
read( java.nio.ByteBuffer buffer ) &rarr; double

read the next value from the buffer and return the double representation.

### Parameters:
buffer - the buffer positioned at the next item.

### Returns:
the double representing.

<a href="https://github.com/autoplot/dev/search?q=read&unscoped_q=read">[search for examples]</a>

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

write the next value, represented as a double and interpreted with Units,
 to the buffer.

### Parameters:
d - the double representing.
<br>buffer - the buffer positioned at the next item.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=write&unscoped_q=write">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

