# org.das2.qds.SubsetDataSetExtracts a subset of the source dataset by using a rank 1 subset of indeces on each index.
SubsetDataSet( QDataSet source )
create a subSetDataSet for the source, which is read for applyIndex calls
 which reduce each index.

***
<a name="applyIndex"></a>
# applyIndex
applyIndex( int idim, QDataSet idx ) &rarr; void

apply the subset indexes to a given dimension.  For example,
 if a=[10,20,30,40] then applyIndex( 0, [1,2] ) would result in [20,30].

### Parameters:
idim - an int
<br>idx - the rank 1 index list, for example from where on a rank 1 dataset.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=applyIndex&unscoped_q=applyIndex">[search for examples]</a>

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
length( int i, int j ) &rarr; int<br>
length( int i, int j, int k ) &rarr; int<br>
***
<a name="parseIndices"></a>
# parseIndices
parseIndices( String spec, int dimlen ) &rarr; int

parse the string spec into a list of indices.  The spec is a 
 comma-delineated list containing any combination of:<ul>
 <li>index, with negative indices relative to the end.
 <li>start:stop, with stop exclusive.
 <li>start:stop:stride, incrementing stride elements, including negative.
 <li>start-stopInclusive, where the trailing index is also included.
 </ul>
 If the spec starts with ~, then these indices are removed. For example:<ul>
 <li>~5, remove the 5th index.
 <li>~15:20, remove the 5 indices starting at 15.
 <li>~-1, remove the last index.
 </ul>
 Note if invert is present, then the indices cannot be reversed.

### Parameters:
spec - a String
<br>dimlen - an int

### Returns:
the list of integers.

<a href="https://github.com/autoplot/dev/search?q=parseIndices&unscoped_q=parseIndices">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="property"></a>
# property
property( String name, int i ) &rarr; Object



### Parameters:
name - a String
<br>i - an int

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=property&unscoped_q=property">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

property( String name ) &rarr; Object<br>
***
<a name="rank"></a>
# rank
rank(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=rank&unscoped_q=rank">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="value"></a>
# value
value(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

value( int i ) &rarr; double<br>
value( int i0, int i1 ) &rarr; double<br>
value( int i0, int i1, int i2 ) &rarr; double<br>
value( int i0, int i1, int i2, int i3 ) &rarr; double<br>
