# org.das2.qds.util.TransposeRankNDataSetwrap a qube dataset to transpose the indeces.  This brute force implementation
 calculates the index mapping and is implemented without copying.  For rank 4
 datasets, order[0] must equal 0.
TransposeRankNDataSet( QDataSet source, int[] order )


***
<a name="length"></a>
# length
length(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=length&unscoped_q=length">[search for examples]</a>

length( int i ) &rarr; int<br>
length( int i, int j ) &rarr; int<br>
length( int i, int j, int k ) &rarr; int<br>
***
<a name="property"></a>
# property
property( String name ) &rarr; Object



### Parameters:
name - a String

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=property&unscoped_q=property">[search for examples]</a>

property( String name, int i ) &rarr; Object<br>
***
<a name="rank"></a>
# rank
rank(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=rank&unscoped_q=rank">[search for examples]</a>

***
<a name="value"></a>
# value
value( int i ) &rarr; double



### Parameters:
i - an int

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

value( int i0, int i1 ) &rarr; double<br>
value( int i1, int i2, int i3 ) &rarr; double<br>
value( int i0, int i1, int i2, int i3 ) &rarr; double<br>
