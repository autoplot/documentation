# org.autoplot.netCDF.AbstractIOSP
AbstractIOSP( )


***
<a name="isValidFile"></a>
# isValidFile
isValidFile( RandomAccessFile raf ) &rarr; boolean

Return false. Netcdf will not automatically determine that this IOSP should handle the given file.
 Use this IOSP only if it is specified in the ncml.

### Parameters:
raf - a RandomAccessFile

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isValidFile&unscoped_q=isValidFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="sendIospMessage"></a>
# sendIospMessage
sendIospMessage( Object message ) &rarr; Object

Called by NetCDF passing in the contents of the ncml "iospParam" attribute.
 Assumes that message is a String of key,value pairs: "k1=v1 k2=v2"
 Ignores return value.

### Parameters:
message - an Object

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=sendIospMessage&unscoped_q=sendIospMessage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

