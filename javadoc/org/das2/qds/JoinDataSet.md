# org.das2.qds.JoinDataSet

Create a higher rank dataset with dim 0 being a JOIN dimension.  Join implies
 that the joined datasets occupy the same physical dimension, and this can
 be thought of as the "array of" index.  Note DEPEND_0 is treated as a
 special case of join.
 Note this dataset is mutable, and clients should not mutate it once the reference is made public.

# JoinDataSet( int rank )
Creates a new instance of JoinDataSet

# JoinDataSet( QDataSet ds1 )
create a new JoinDataSet, and join the first dataset.
<blockquote><pre>
ds1= Ops.rand(30);
jds= new JoinDataSet( ds1 );
assert( ds1.rank()==1 );
assert( jds.rank()==2 );
assert( jds.slice(0).equals(ds1) );
</pre></blockquote>

***
<a name="copy"></a>
# copy
copy( org.das2.qds.JoinDataSet joinDataSet ) &rarr; JoinDataSet

copy the JoinDataSet without copying each dataset it contains.

### Parameters:
joinDataSet - another JoinDataSet

### Returns:
a copy of the dataset.

<a href="https://github.com/autoplot/dev/search?q=copy&unscoped_q=copy">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="deepCopy"></a>
# <del>deepCopy</del>
Deprecated: see WritableJoinDataSet
***
<a name="join"></a>
# join
join( QDataSet ds ) &rarr; void

add the dataset to this set of joined datasets.

### Parameters:
ds - rank N-1 dataset where N is the rank of this JoinDataSet.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=join&unscoped_q=join">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

join( int index, QDataSet ds ) &rarr; void<br>
***
<a name="joinAll"></a>
# joinAll
joinAll( org.das2.qds.JoinDataSet ds1 ) &rarr; void

copy all the records into this JoinDataSet.  Note this is
 a shallow copy, and changes to one of the element datasets is visible
 in both JoinDataSets.
 TODO: this is probably under implemented, for example element properties.

### Parameters:
ds1 - a JoinDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=joinAll&unscoped_q=joinAll">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="length"></a>
# length
length(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=length&unscoped_q=length">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

length( int i0 ) &rarr; int<br>
length( int i0, int i1 ) &rarr; int<br>
length( int i0, int i1, int i2 ) &rarr; int<br>
***
<a name="property"></a>
# property
property( String name, int i0 ) &rarr; Object



### Parameters:
name - a String
<br>i0 - an int

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=property&unscoped_q=property">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

property( String name ) &rarr; Object<br>
***
<a name="putProperty"></a>
# putProperty
putProperty( String name, Object value ) &rarr; void

We override putProperty here because we remove the JOIN_0 if DEPEND_0 is set.

### Parameters:
name - a String
<br>value - an Object

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putProperty&unscoped_q=putProperty">[search for examples]</a>

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
<a name="slice"></a>
# slice
slice( int idx ) &rarr; QDataSet

slice the dataset by returning the joined dataset at this index.  If the
 dataset is a MutablePropertiesDataSet, then add the properties of this
 join dataset to it.  The result is made a mutable properties dataset if it 
 is not already, the danger here is that we may mutate the original data.
 Capabilities will fix this.

### Parameters:
idx - the index for the slice

### Returns:
the rank N-1 slice at the position.

<a href="https://github.com/autoplot/dev/search?q=slice&unscoped_q=slice">[search for examples]</a>

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
<a name="trim"></a>
# trim
trim( int imin, int imax ) &rarr; JoinDataSet



### Parameters:
imin - an int
<br>imax - an int

### Returns:
org.das2.qds.JoinDataSet


<a href="https://github.com/autoplot/dev/search?q=trim&unscoped_q=trim">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="value"></a>
# value
value( int i0 ) &rarr; double



### Parameters:
i0 - an int

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

value( int i0, int i1 ) &rarr; double<br>
value( int i0, int i1, int i2 ) &rarr; double<br>
value( int i0, int i1, int i2, int i3 ) &rarr; double<br>
