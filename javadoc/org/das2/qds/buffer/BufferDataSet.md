# org.das2.qds.buffer.BufferDataSet

rank 1, 2, 3, and 4 datasets backed by NIO buffers.  These have the 
 advantage that data can be stored outside of the JVM, and in fact they 
 can be backed by a huge file on disk.  
 
 This code was copied from BinaryDataSource.

# BufferDataSet( int rank, int reclen, int recoffs, int len0, int len1, int len2, Object type, java.nio.ByteBuffer back )
Create a new BufferDataSet of the given type.  Simple sanity checks are made, including:<ul>
   <li>rank 1 dataset may not have len1&gt;1.
   <li>reclen cannot be shorter than the byte length of the field type. 
   <li>buffer must have room for the dataset
 </ul>

# BufferDataSet( int rank, int reclen, int recoffs, int len0, int len1, int len2, int len3, Object type, java.nio.ByteBuffer back )
Create a new BufferDataSet of the given type.  Simple sanity checks are made, including:<ul>
   <li>rank 1 dataset may not have len1&gt;1.
   <li>reclen cannot be shorter than the byte length of the field type. 
   <li>buffer must have room for the dataset
 </ul>

# BufferDataSet( int rank, int reclen, int recoffs, Object bitByte, int len0, int len1, int len2, int len3, Object type, java.nio.ByteBuffer back )
Create a new BufferDataSet of the given type.  Simple sanity checks are made, including:<ul>
   <li>rank 1 dataset may not have len1&gt;1.
   <li>reclen cannot be shorter than the byte length of the field type. 
   <li>buffer must have room for the dataset
 </ul>

***
<a name="DOUBLE"></a>
# DOUBLE

the data is in 8 byte doubles.

***
<a name="FLOAT"></a>
# FLOAT

the data is in 4 byte floats.

***
<a name="TRUNCATEDFLOAT"></a>
# TRUNCATEDFLOAT

the data is in 16 bit real that has exponent like a FLOAT but mantissa precision is reduced.

***
<a name="VAX_FLOAT"></a>
# VAX_FLOAT

VAX floats.

***
<a name="INT24"></a>
# INT24

three-byte ints.

***
<a name="UINT24"></a>
# UINT24

three-byte unsigned ints.

***
<a name="NYBBLE"></a>
# NYBBLE

four-bit unsigned ints.

***
<a name="LONG"></a>
# LONG

8 byte signed longs.

***
<a name="INT"></a>
# INT

4 byte signed integers.

***
<a name="INTEGER"></a>
# INTEGER

4 byte signed integers, INT is canonical but INTEGER should be accepted.

***
<a name="UINT"></a>
# UINT

4 byte unsigned integers.  Note 4-byte signed ints are used to store the data 
 which is unpacked in the value() method.

***
<a name="SHORT"></a>
# SHORT

2 byte short integer.

***
<a name="USHORT"></a>
# USHORT

2 byte unsigned short.

***
<a name="BYTE"></a>
# BYTE

1 byte signed byte.

***
<a name="UBYTE"></a>
# UBYTE

1 byte unsigned byte.

***
<a name="BYTES"></a>
# BYTES

constructor units are in bytes.

***
<a name="BITS"></a>
# BITS

constructor units are in bits.

***
<a name="about"></a>
# about
about(  ) &rarr; void

print some info about this BufferDataSet.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=about&unscoped_q=about">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="append"></a>
# append
append( org.das2.qds.buffer.BufferDataSet ds ) &rarr; void

append the dataset with the same geometry but different number of records (zeroth dim)
 to this.  An IllegalArgumentException is thrown when there is not enough room.  
 See grow(newRecCount).
 Not thread safe--we need to go through and make it so...

### Parameters:
ds - a BufferDataSet

### Returns:
void (returns nothing)

### See Also:
<a href='#grow'>grow(int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=append&unscoped_q=append">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

append( org.das2.qds.buffer.BufferDataSet ths, org.das2.qds.buffer.BufferDataSet ds ) &rarr; BufferDataSet<br>
***
<a name="bitCount"></a>
# bitCount
bitCount( Object type ) &rarr; int



### Parameters:
type - an Object

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=bitCount&unscoped_q=bitCount">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="byteCount"></a>
# byteCount
byteCount( Object type ) &rarr; int

return the number of bytes of each type (double=8, etc).

### Parameters:
type - DOUBLE, FLOAT, UBYTE, TIME28, etc.

### Returns:
8, 4, 1, etc.

<a href="https://github.com/autoplot/dev/search?q=byteCount&unscoped_q=byteCount">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="canAppend"></a>
# canAppend
canAppend( org.das2.qds.buffer.BufferDataSet ds ) &rarr; boolean

return true if the dataset can be appended.  Note this assumes that the
 same length, etc.  This just checks that we have the number of spare records
 in the backing store.

### Parameters:
ds - dataset of the same rank and len1, len2, and len3.

### Returns:
true if the dataset can be appended.

<a href="https://github.com/autoplot/dev/search?q=canAppend&unscoped_q=canAppend">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="compact"></a>
# compact
compact(  ) &rarr; BufferDataSet

get ride of extra spaces between records.

### Returns:
new BufferDataSet without gaps.

<a href="https://github.com/autoplot/dev/search?q=compact&unscoped_q=compact">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="copy"></a>
# copy
copy( QDataSet ds ) &rarr; BufferDataSet

return a copy of the data.  If the data is a BufferDataSet, then a new BufferDataSet
 is used for the copy.  
 
 Note this does not consider isMutable.  If the dataset is not mutable, then the
 original data could be returned (probably).

### Parameters:
ds - any qube dataset.

### Returns:
a BufferDataSet copy of the dataset.

<a href="https://github.com/autoplot/dev/search?q=copy&unscoped_q=copy">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

copy( Object type, QDataSet ds ) &rarr; BufferDataSet<br>
***
<a name="create"></a>
# create
create( int rank, Object type, int len0, int[] size ) &rarr; BufferDataSet

create a dataset backed by the given type.

### Parameters:
rank - the rank of the data
<br>type - DOUBLE, FLOAT, UINT, etc
<br>len0 - number of records (ignored for rank 0).
<br>size - size of each record

### Returns:
BufferDataSet of the given type.

<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRank0"></a>
# createRank0
createRank0( Object type ) &rarr; BufferDataSet

create a rank 0 dataset backed by the given type.

### Parameters:
type - DOUBLE, FLOAT, UINT, etc

### Returns:
BufferDataSet of the given type.

<a href="https://github.com/autoplot/dev/search?q=createRank0&unscoped_q=createRank0">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRank1"></a>
# createRank1
createRank1( Object type, int len0 ) &rarr; BufferDataSet

create a rank 1 dataset backed by the given type.

### Parameters:
type - DOUBLE, FLOAT, UINT, etc
<br>len0 - length of the zeroth index

### Returns:
BufferDataSet of the given type.

<a href="https://github.com/autoplot/dev/search?q=createRank1&unscoped_q=createRank1">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRank2"></a>
# createRank2
createRank2( Object type, int len0, int len1 ) &rarr; BufferDataSet

create a rank 2 dataset backed by the given type.

### Parameters:
type - DOUBLE, FLOAT, UINT, etc
<br>len0 - length of the zeroth index
<br>len1 - length of the first index

### Returns:
BufferDataSet of the given type.

<a href="https://github.com/autoplot/dev/search?q=createRank2&unscoped_q=createRank2">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRank3"></a>
# createRank3
createRank3( Object type, int len0, int len1, int len2 ) &rarr; BufferDataSet

create a rank 3 dataset backed by the given type.

### Parameters:
type - DOUBLE, FLOAT, UINT, etc
<br>len0 - length of the zeroth index
<br>len1 - length of the first index
<br>len2 - length of the second index

### Returns:
BufferDataSet of the given type.

<a href="https://github.com/autoplot/dev/search?q=createRank3&unscoped_q=createRank3">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRank4"></a>
# createRank4
createRank4( Object type, int len0, int len1, int len2, int len3 ) &rarr; BufferDataSet

create a rank 4 dataset backed by the given type.

### Parameters:
type - DOUBLE, FLOAT, UINT, etc
<br>len0 - length of the zeroth index
<br>len1 - length of the first index
<br>len2 - length of the second index
<br>len3 - length of the third index

### Returns:
BufferDataSet of the given type.

<a href="https://github.com/autoplot/dev/search?q=createRank4&unscoped_q=createRank4">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCompatibleComponentType"></a>
# getCompatibleComponentType
getCompatibleComponentType(  ) &rarr; Class

return the Java type that is capable of containing elements of this dataset.
 For unsigned types, the next Java class is used, for example int.class is
 used to store unsigned shorts.

### Returns:
double.class, float.class, long.class, etc.

<a href="https://github.com/autoplot/dev/search?q=getCompatibleComponentType&unscoped_q=getCompatibleComponentType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFieldStride"></a>
# getFieldStride
getFieldStride(  ) &rarr; int

return the number of bytes to advance for each field.

### Returns:
the number of bytes to advance for each field.

<a href="https://github.com/autoplot/dev/search?q=getFieldStride&unscoped_q=getFieldStride">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRecordStride"></a>
# getRecordStride
getRecordStride(  ) &rarr; int

return the number of bytes to advance for each record.

### Returns:
the number of bytes to advance for each record.

<a href="https://github.com/autoplot/dev/search?q=getRecordStride&unscoped_q=getRecordStride">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getType"></a>
# getType
getType(  ) &rarr; Object

return the type of this dataset, for example BufferDataSet.INT, BufferDataSet.DOUBLE, etc...

### Returns:
the type of this dataset.

<a href="https://github.com/autoplot/dev/search?q=getType&unscoped_q=getType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="grow"></a>
# grow
grow( int newRecCount ) &rarr; void

grow the internal store so that append may be used to resize the 
 dataset.  This simply grows the internal buffer, so for example length()
 will return the same value after.

### Parameters:
newRecCount - the new record count, generally larger than the old rec count.

### Returns:
void (returns nothing)

### See Also:
<a href='#append'>append(org.das2.qds.buffer.BufferDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=grow&unscoped_q=grow">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="guessBackingStore"></a>
# guessBackingStore
guessBackingStore( QDataSet ds ) &rarr; Object

guess the type of the backing store, returning double.class
 if it cannot be determined.

### Parameters:
ds - the dataset

### Returns:
the backing store class, one of double.class, float.class, etc.

<a href="https://github.com/autoplot/dev/search?q=guessBackingStore&unscoped_q=guessBackingStore">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isCompact"></a>
# isCompact
isCompact(  ) &rarr; boolean

returns true if the dataset is compact, meaning that there
 are no gaps between records, and no byte offset.

### Returns:
true if the dataset is compact

<a href="https://github.com/autoplot/dev/search?q=isCompact&unscoped_q=isCompact">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="jvmMemory"></a>
# jvmMemory
jvmMemory(  ) &rarr; int

estimate the jvmMemory occupied by this dataset, looking at the NIO buffer
 to see if it is direct as has no JVM memory cost, or if it has been made into
 an array.

### Returns:
the estimated number bytes that the dataSet occupies.

<a href="https://github.com/autoplot/dev/search?q=jvmMemory&unscoped_q=jvmMemory">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="length"></a>
# length
length(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=length&unscoped_q=length">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

length( int i ) &rarr; int<br>
length( int i0, int i1 ) &rarr; int<br>
length( int i0, int i1, int i2 ) &rarr; int<br>
***
<a name="makeDataSet"></a>
# makeDataSet
makeDataSet( int rank, int reclen, int recoffs, int len0, int len1, int len2, int len3, java.nio.ByteBuffer buf, Object type ) &rarr; BufferDataSet

Make a BufferDataSet of the given type.

### Parameters:
rank - the rank (number of indeces) of the data.
<br>reclen - length in bytes of each record.  This may be longer than len1*len2*len3*byteCount(type)
<br>recoffs - byte offset of each record
<br>len0 - number of elements in the first index
<br>len1 - number of elements in the second index
<br>len2 - number of elements in the third index
<br>len3 - number of elements in the fourth index
<br>buf - ByteBuffer containing the data, which should be at least recoffs + reclen * len0 bytes long.
<br>type - BufferDataSet.INT, BufferDataSet.DOUBLE, etc...

### Returns:
BufferDataSet of the given type.

<a href="https://github.com/autoplot/dev/search?q=makeDataSet&unscoped_q=makeDataSet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

makeDataSet( int rank, int reclen, int recoffs, int[] qube, java.nio.ByteBuffer buf, Object type ) &rarr; BufferDataSet<br>
***
<a name="makeDataSetBits"></a>
# makeDataSetBits
makeDataSetBits( int rank, int reclenbits, int recoffsbits, int len0, int len1, int len2, int len3, java.nio.ByteBuffer buf, Object type ) &rarr; BufferDataSet

support binary types that are not a multiple of 8 bits.  This was
 added to support Nybbles, and 12-bit ints.

### Parameters:
rank - an int
<br>reclenbits - number of bits per record
<br>recoffsbits - number of bits offset.  Note this must be a multiple of 8, for now.
<br>len0 - number of elements in the first index
<br>len1 - number of elements in the second index
<br>len2 - number of elements in the third index
<br>len3 - number of elements in the fourth index
<br>buf - ByteBuffer containing the data, which should be at least recoffsbits/8 + reclenbits/8 * len0 bytes long.
<br>type - BufferDataSet.NYBBLE, etc

### Returns:
BufferDataSet of the given type.

<a href="https://github.com/autoplot/dev/search?q=makeDataSetBits&unscoped_q=makeDataSetBits">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="maybeCopy"></a>
# maybeCopy
maybeCopy( QDataSet ds ) &rarr; BufferDataSet

Copy the dataset to an BufferDataSet only if the dataset is not already an BufferDataSet.

### Parameters:
ds - a QDataSet

### Returns:
a BufferDataSet.

<a href="https://github.com/autoplot/dev/search?q=maybeCopy&unscoped_q=maybeCopy">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rank"></a>
# rank
rank(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=rank&unscoped_q=rank">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFieldStride"></a>
# setFieldStride
setFieldStride( int bytes ) &rarr; void

allow clients to override the cadence of data.  By default, this is
 just the number of bytes in each field.

### Parameters:
bytes - number of bytes between field beginnings.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFieldStride&unscoped_q=setFieldStride">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLength"></a>
# setLength
setLength( int len0 ) &rarr; void

reset the number of records.

### Parameters:
len0 - the new number of records.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLength&unscoped_q=setLength">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLength1"></a>
# setLength1
setLength1( int len1 ) &rarr; void

reset the length (in fields) of each record of the rank 2 dataset.

### Parameters:
len1 - the length of each record of the rank 2 dataset.

### Returns:
void (returns nothing)

### See Also:
<a href='Ops.md#decimateBufferDataSet'>Ops#decimateBufferDataSet(org.das2.qds.buffer.BufferDataSet, int, int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setLength1&unscoped_q=setLength1">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRecordStride"></a>
# setRecordStride
setRecordStride( int bytes ) &rarr; void

allow clients to override the cadece of the records.  By default, this
 is the number of bytes in each record.

### Parameters:
bytes - number of bytes between record beginnings.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRecordStride&unscoped_q=setRecordStride">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="shouldAllocateDirect"></a>
# shouldAllocateDirect
shouldAllocateDirect(  ) &rarr; int

return 1 if direct allocate should be used, 0 if not.  
 Direct allocations are memory allocations outside of the JVM heap memory.
 (The internal variable has a -1 initial state, which is why this is
 not boolean.)  This looks for 32bit Javas, and if more than 1/2 Gig is 
 being used then it will allocate direct.  This is because 32bit Javas
 cannot access any memory outside of 1Gig.

### Returns:
1 or 0 if direct allocations should not be made.
### See Also:
<a href='https://sourceforge.net/p/autoplot/bugs/1395/'>https://sourceforge.net/p/autoplot/bugs/1395/</a> <br>
<a href='http://stackoverflow.com/questions/807263/how-do-i-detect-which-kind-of-jre-is-installed-32bit-vs-64bit'>http://stackoverflow.com/questions/807263/how-do-i-detect-which-kind-of-jre-is-installed-32bit-vs-64bit</a> <br>
<a href='http://stackoverflow.com/questions/3651737/why-the-odd-performance-curve-differential-between-bytebuffer-allocate-and-byt "How ByteBuffer works and why Direct '>http://stackoverflow.com/questions/3651737/why-the-odd-performance-curve-differential-between-bytebuffer-allocate-and-byt "How ByteBuffer works and why Direct (Byte)</a> "How ByteBuffer works and why Direct (Byte)Buffers are the only truly useful now"<br>

<a href="https://github.com/autoplot/dev/search?q=shouldAllocateDirect&unscoped_q=shouldAllocateDirect">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="slice"></a>
# slice
slice( int i ) &rarr; QDataSet



### Parameters:
i - an int

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=slice&unscoped_q=slice">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="trim"></a>
# trim
trim( int ist, int ien ) &rarr; QDataSet



### Parameters:
ist - an int
<br>ien - an int

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=trim&unscoped_q=trim">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="typeFor"></a>
# typeFor
typeFor( java.lang.Class c ) &rarr; Object

Return the type for the given class.  Note that there is a type for
 each native type (Byte,Short,Float,etc), but not a class for each type. 
 (E.g. UBYTE is unsigned byte.)

### Parameters:
c - java class

### Returns:
DOUBLE,FLOAT,etc.

<a href="https://github.com/autoplot/dev/search?q=typeFor&unscoped_q=typeFor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="value"></a>
# value
value(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

value( int i0 ) &rarr; double<br>
value( int i0, int i1 ) &rarr; double<br>
value( int i0, int i1, int i2 ) &rarr; double<br>
value( int i0, int i1, int i2, int i3 ) &rarr; double<br>
