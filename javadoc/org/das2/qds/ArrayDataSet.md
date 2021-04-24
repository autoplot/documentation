# org.das2.qds.ArrayDataSet

ArrayDataSet is the abstract base class for QDataSets which are backed by
 Java arrays  For example, DDataSet is a QDataSet which uses a double array
 to store its data.  Data is stored in 1-D Java arrays for performance, 
 inspired by https://www.cs.cmu.edu/~artigas/papers/cacm01.pdf.  Note for 
 modern versions of Java, Arrays of Arrays are implemented with no performance
 cost.
 
 A number of static methods were initially defined in DDataSet, then
 copied into FDataSet and others when they were made.  This super implementation
 will parent all such datasets and provide common methods.

***
<a name="about"></a>
# about
about(  ) &rarr; void

print some info about this ArrayDataSet.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=about&unscoped_q=about">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="append"></a>
# append
append( org.das2.qds.ArrayDataSet ds ) &rarr; void

append the dataset with the same geometry but different number of records (zeroth dim)
 to this.  An IllegalArgumentException is thrown when there is not enough room.  
 See grow(newRecCount).
 Not thread safe--we need to go through and make it so...

### Parameters:
ds - an ArrayDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=append&unscoped_q=append">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

append( org.das2.qds.ArrayDataSet ds1, org.das2.qds.ArrayDataSet ds2 ) &rarr; ArrayDataSet<br>
***
<a name="canAppend"></a>
# canAppend
canAppend( org.das2.qds.ArrayDataSet ds ) &rarr; boolean

return true if the dataset can be appended.  Note this assumes that the
 same length, etc.  This just checks that we have the number of spare records
 in the backing store.

### Parameters:
ds - the dataset to test

### Returns:
true if the dataset can be appended.

<a href="https://github.com/autoplot/dev/search?q=canAppend&unscoped_q=canAppend">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="copy"></a>
# copy
copy( java.lang.Class c, QDataSet ds ) &rarr; ArrayDataSet

Copy to array of specific type.  For example, copy( double.class, ds ) 
 would return a copy in a DDataSet.

### Parameters:
c - the primitive type to use (e.g. double.class, float.class, int.class).
<br>ds - the data to copy.

### Returns:
ArrayDataSet of specific type.

<a href="https://github.com/autoplot/dev/search?q=copy&unscoped_q=copy">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

copy( QDataSet ds ) &rarr; ArrayDataSet<br>
***
<a name="create"></a>
# create
create( java.lang.Class c, int[] qube ) &rarr; ArrayDataSet

create a dataset with the backing type and the dimensions given.
 The following component types are supported: double.class, float.class,
 long.class, int.class, short.class, and byte.class.

### Parameters:
c - the backing type, such as double.class, float.class, etc.
<br>qube - dimensions of the dataset

### Returns:
the dataset
### See Also:
<a href='#getComponentType'>getComponentType()</a> <br>
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/BufferDataSet which also supports unsigned types/.md'>BufferDataSet which also supports unsigned types.</a> which also supports unsigned types.<br>

<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRank0"></a>
# createRank0
createRank0( java.lang.Class c ) &rarr; ArrayDataSet

create a rank 0 dataset of the class, which can be 
 double.class, float.class, long.class, int.class, short.class and byte.class

### Parameters:
c - the primitive class of each element.

### Returns:
the ArrayDataSet

<a href="https://github.com/autoplot/dev/search?q=createRank0&unscoped_q=createRank0">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRank1"></a>
# createRank1
createRank1( java.lang.Class c, int len0 ) &rarr; ArrayDataSet

create a rank 1 dataset of the class, which can be 
 double.class, float.class, long.class, int.class, short.class and byte.class

### Parameters:
c - the primitive class of each element.
<br>len0 - the length of the dimension

### Returns:
the ArrayDataSet

<a href="https://github.com/autoplot/dev/search?q=createRank1&unscoped_q=createRank1">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRank2"></a>
# createRank2
createRank2( java.lang.Class c, int len0, int len1 ) &rarr; ArrayDataSet

create a rank 2 dataset of the class, which can be 
 double.class, float.class, long.class, int.class, short.class and byte.class

### Parameters:
c - the primitive class of each element.
<br>len0 - the length of the dimension
<br>len1 - the length of the dimension

### Returns:
the ArrayDataSet

<a href="https://github.com/autoplot/dev/search?q=createRank2&unscoped_q=createRank2">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRank3"></a>
# createRank3
createRank3( java.lang.Class c, int len0, int len1, int len2 ) &rarr; ArrayDataSet

create a rank 3 dataset of the class, which can be 
 double.class, float.class, long.class, int.class, short.class and byte.class

### Parameters:
c - the primitive class of each element.
<br>len0 - the length of the dimension
<br>len1 - the length of the dimension
<br>len2 - the length of the dimension

### Returns:
the ArrayDataSet

<a href="https://github.com/autoplot/dev/search?q=createRank3&unscoped_q=createRank3">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRank4"></a>
# createRank4
createRank4( java.lang.Class c, int len0, int len1, int len2, int len3 ) &rarr; ArrayDataSet

create a rank 4 dataset of the class, which can be 
 double.class, float.class, long.class, int.class, short.class and byte.class

### Parameters:
c - the primitive class of each element.
<br>len0 - the length of the dimension
<br>len1 - the length of the dimension
<br>len2 - the length of the dimension
<br>len3 - the length of the dimension

### Returns:
the ArrayDataSet

<a href="https://github.com/autoplot/dev/search?q=createRank4&unscoped_q=createRank4">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="flattenArray"></a>
# flattenArray
flattenArray( Object array, int[] qube ) &rarr; Object



### Parameters:
array - an Object
<br>qube - an int[]

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=flattenArray&unscoped_q=flattenArray">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getComponentType"></a>
# getComponentType
getComponentType(  ) &rarr; Class

return the component type of the backing array, such as double.class.

### Returns:
the component type of the backing array.
### See Also:
<a href='#create'>create(java.lang.Class, int[])</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getComponentType&unscoped_q=getComponentType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="grow"></a>
# grow
grow( int newRecCount ) &rarr; void

grow the internal store so that append may be used to resize the dataset.

### Parameters:
newRecCount - new number of records, which includes the old records.

### Returns:
void (returns nothing)

### See Also:
<a href='#putLength'>putLength(int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=grow&unscoped_q=grow">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="guessBackingStore"></a>
# guessBackingStore
guessBackingStore( QDataSet ds ) &rarr; Class

guess the type of the backing store, returning double.class
 if it cannot be determined.  TODO: Why not long.class?

### Parameters:
ds - the dataset

### Returns:
the backing store class, one of double.class, float.class, int.class, short.class, or byte.class.
### See Also:
<a href='#copy'>copy(QDataSet)</a> copy<br>

<a href="https://github.com/autoplot/dev/search?q=guessBackingStore&unscoped_q=guessBackingStore">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="jvmMemory"></a>
# jvmMemory
jvmMemory(  ) &rarr; int

returns the size of the dataset in bytes.

### Returns:
the size of the dataset in bytes.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/buffer/BufferDataSet which stores data outside of the JVM/.md'>org.das2.qds.buffer.BufferDataSet which stores data outside of the JVM.</a> which stores data outside of the JVM.<br>

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
<a name="maybeCopy"></a>
# maybeCopy
maybeCopy( QDataSet ds ) &rarr; ArrayDataSet

Copy the dataset to an ArrayDataSet only if the dataset is not 
 already an ArrayDataSet that is mutable.

### Parameters:
ds - the dataset to copy, which may be an ArrayDataSet

### Returns:
an ArrayDataSet.

<a href="https://github.com/autoplot/dev/search?q=maybeCopy&unscoped_q=maybeCopy">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

maybeCopy( java.lang.Class c, QDataSet ds ) &rarr; ArrayDataSet<br>
***
<a name="monotonicSubset"></a>
# monotonicSubset
monotonicSubset( org.das2.qds.ArrayDataSet ds ) &rarr; ArrayDataSet

ensure that there are no non-monotonic or repeat records, by removing
 the first N-1 records of N repeated records.

### Parameters:
ds - ArrayDataSet, which must be writable.

### Returns:
dataset, possibly with records removed.

<a href="https://github.com/autoplot/dev/search?q=monotonicSubset&unscoped_q=monotonicSubset">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="monotonicSubset2"></a>
# monotonicSubset2
monotonicSubset2( org.das2.qds.ArrayDataSet ds ) &rarr; ArrayDataSet

ensure that there are no non-monotonic or repeat records, by starting at the middle
 of the dataset and finding the monotonic subsection.  The input need not be writable.

### Parameters:
ds - ArrayDataSet, which must be writable.

### Returns:
dataset, possibly with records removed.

<a href="https://github.com/autoplot/dev/search?q=monotonicSubset2&unscoped_q=monotonicSubset2">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putLength"></a>
# putLength
putLength( int len ) &rarr; void

Shorten the dataset by changing it's dim 0 length parameter.  
 The same backing array is used, so the element that remain will be the same.
 This can only be used to shorten datasets, see grow to lengthen.

### Parameters:
len - new number of records

### Returns:
void (returns nothing)

### See Also:
<a href='#grow'>grow(int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=putLength&unscoped_q=putLength">[search for examples]</a>
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
<a name="setUnits"></a>
# setUnits
setUnits( Units units ) &rarr; QDataSet

set the units for this dataset.  This is a convenience method
 intended to encourage setting the data units.  For example in Jython:
<blockquote><pre>
ds= linspace(0.,10.,100).setUnits( Units.seconds )
</pre></blockquote>

### Parameters:
units - units object, like Units.seconds

### Returns:
this dataset.

<a href="https://github.com/autoplot/dev/search?q=setUnits&unscoped_q=setUnits">[search for examples]</a>
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
<a name="wrap"></a>
# wrap
wrap( Object array, int[] qube, boolean copy ) &rarr; ArrayDataSet

return the array as ArrayDataSet  The array must be a 1-D array and the
 dimensions of the result are provided in qube.

### Parameters:
array - 1-D array
<br>qube - dimensions of the dataset
<br>copy - copy the data so that original data is not modified with putValue

### Returns:
ArrayDataSet
### See Also:
<a href='#create'>create(java.lang.Class, int[])</a> <br>

<a href="https://github.com/autoplot/dev/search?q=wrap&unscoped_q=wrap">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

