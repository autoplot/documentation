# org.autoplot.idlsupport.ReadIDLSav

Read data from IDL Save Files.  This was written using
 http://www.physics.wisc.edu/~craigm/idl/savefmt/node20.html
 https://cow.physics.wisc.edu/~craigm/idl/savefmt.pdf
 and https://github.com/scipy/scipy/blob/master/scipy/io/idl.py
 for reference, and with no involvement from individuals at
 Harris Geospacial.  No warrenties are implied and this must
 be used at your own risk.

# ReadIDLSav( )


***
<a name="isArray"></a>
# isArray
isArray( java.nio.ByteBuffer in, String name ) &rarr; boolean

return true if the name refers to an array

### Parameters:
in - ByteBuffer for the entire file
<br>name - the variable name

### Returns:
td.isStructure();

<a href="https://github.com/autoplot/dev/search?q=isArray&unscoped_q=isArray">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isStructure"></a>
# isStructure
isStructure( java.nio.ByteBuffer in, String name ) &rarr; boolean

return true if the name refers to a structure

### Parameters:
in - ByteBuffer for the entire file
<br>name - the variable name

### Returns:
true if the name refers to a structure

<a href="https://github.com/autoplot/dev/search?q=isStructure&unscoped_q=isStructure">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readArrayDataIntoArrayOfArrays"></a>
# readArrayDataIntoArrayOfArrays
readArrayDataIntoArrayOfArrays( org.autoplot.idlsupport.ReadIDLSav.ArrayData data ) &rarr; Object

read the data into 1-D and 2-D arrays.  This is provided for reference, but 
 can be extended to 3-D and higher arrays, if the need arrises.

### Parameters:
data - a ReadIDLSav.ArrayData

### Returns:
an Object


<a href="https://github.com/autoplot/dev/search?q=readArrayDataIntoArrayOfArrays&unscoped_q=readArrayDataIntoArrayOfArrays">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readFileIntoByteBuffer"></a>
# readFileIntoByteBuffer
readFileIntoByteBuffer( java.io.File f ) &rarr; ByteBuffer



### Parameters:
f - a File

### Returns:
java.nio.ByteBuffer


<a href="https://github.com/autoplot/dev/search?q=readFileIntoByteBuffer&unscoped_q=readFileIntoByteBuffer">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readStructDesc"></a>
# readStructDesc
readStructDesc( java.nio.ByteBuffer rec ) &rarr; StructDesc



### Parameters:
rec - a ByteBuffer

### Returns:
org.autoplot.idlsupport.ReadIDLSav.StructDesc


<a href="https://github.com/autoplot/dev/search?q=readStructDesc&unscoped_q=readStructDesc">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readTagDesc"></a>
# readTagDesc
readTagDesc( java.nio.ByteBuffer in, String name ) &rarr; TagDesc

scan through the IDLSav and retrieve information about the array.

### Parameters:
in - the idlsav loaded into a ByteBuffer.
<br>name - the name of the array

### Returns:
an org.autoplot.idlsupport.ReadIDLSav.TagDesc


<a href="https://github.com/autoplot/dev/search?q=readTagDesc&unscoped_q=readTagDesc">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readVar"></a>
# readVar
readVar( java.nio.ByteBuffer in, String name ) &rarr; Object

scan through the IDLSav and return just the one variable.

### Parameters:
in - a ByteBuffer
<br>name - a String

### Returns:
an Object


<a href="https://github.com/autoplot/dev/search?q=readVar&unscoped_q=readVar">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readVarNames"></a>
# readVarNames
readVarNames( java.nio.ByteBuffer in ) &rarr; String

list the names in the IDLSav file.  This is only the supported
 variable types.

### Parameters:
in - a ByteBuffer

### Returns:
the names found.

<a href="https://github.com/autoplot/dev/search?q=readVarNames&unscoped_q=readVarNames">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readVars"></a>
# readVars
readVars( java.nio.ByteBuffer in ) &rarr; Map



### Parameters:
in - a ByteBuffer

### Returns:
java.util.Map


<a href="https://github.com/autoplot/dev/search?q=readVars&unscoped_q=readVars">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

