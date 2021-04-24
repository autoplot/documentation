# org.das2.qds.LeafTrimDataSet

pull out a subset of the dataset by reducing the number of columns in the
 last dimension.  This does not reduce rank.  This assumes the dataset has no
 row with length&gt;end.

# LeafTrimDataSet( QDataSet source, int start, int end )


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
length( int i0, int i1, int i2 ) &rarr; int<br>
***
<a name="property"></a>
# property
property( String name ) &rarr; Object



### Parameters:
name - a String

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=property&unscoped_q=property">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

property( String name, int i ) &rarr; Object<br>
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
slice( int i ) &rarr; QDataSet

{@inheritDoc}
 This must also copy the dimension properties explicitly.

### Parameters:
i - an int

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=slice&unscoped_q=slice">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="trim"></a>
# trim
trim( int start, int end ) &rarr; QDataSet



### Parameters:
start - an int
<br>end - an int

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=trim&unscoped_q=trim">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="value"></a>
# value
value( int i ) &rarr; double



### Parameters:
i - an int

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

value( int i0, int i1 ) &rarr; double<br>
value( int i0, int i1, int i2 ) &rarr; double<br>
value( int i0, int i1, int i2, int i3 ) &rarr; double<br>
