# org.das2.qds.buffer.UByteDataSetUnsigned Byte.  This also contains a method
 for extracting the data at a location as a string.
UByteDataSet( int rank, int reclen, int recoffs, int len0, int len1, int len2, int len3, java.nio.ByteBuffer back )


***
<a name="collectString"></a>
# collectString
collectString( java.nio.charset.Charset charset ) &rarr; String

efficiently return the data contained in the bytes presuming a string
 encoding.  This is useful when the data is mostly binary but parts
 are text data.  This is typically used with trim to extract text portions
 of data.  This code shows how the length of each record in a U.S.G.S.
 DEM file is extracted:
 <pre>
 from java.nio.charset import Charset
 usascii= Charset.forName( 'US-ASCII' )
 ds=getDataSet( 'vap+bin:%s?byteOffset=858&byteLength=6' % fil.toURI() )
 from java.lang import Integer
 ncol= Integer.parseUnsignedInt( ds.collectString( usascii ).strip() )
 print ncol
 </pre>

### Parameters:
charset - a Charset

### Returns:
the string
### See Also:
<a href='https://github.com/autoplot/dev/blob/master/demos/20190529/readUsgsDem.jyds'>https://github.com/autoplot/dev/blob/master/demos/20190529/readUsgsDem.jyds</a> <br>

<a href="https://github.com/autoplot/dev/search?q=collectString&unscoped_q=collectString">[search for examples]</a>

***
<a name="putValue"></a>
# putValue
putValue( double d ) &rarr; void



### Parameters:
d - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putValue&unscoped_q=putValue">[search for examples]</a>

putValue( int i0, double d ) &rarr; void<br>
putValue( int i0, int i1, double d ) &rarr; void<br>
putValue( int i0, int i1, int i2, double d ) &rarr; void<br>
putValue( int i0, int i1, int i2, int i3, double d ) &rarr; void<br>
***
<a name="value"></a>
# value
value(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

value( int i0 ) &rarr; double<br>
value( int i0, int i1 ) &rarr; double<br>
value( int i0, int i1, int i2 ) &rarr; double<br>
value( int i0, int i1, int i2, int i3 ) &rarr; double<br>
