# org.das2.qds.SortDataSetwraps QDataSet, rearranging the elements of the first index as specified
 by a rank 1 data set of indeces
SortDataSet( QDataSet source, QDataSet sort )
creates the SortDataSet

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

TODO: this is dangerous code, because as new properties are added to QDataSet, 
 they may not be handled properly here. (e.g. BIN_PLUS).
 Note the properties are intended to mask the things that have changed!

### Parameters:
name - a String

### Returns:
an Object


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
value( int i0, int i1, int i2 ) &rarr; double<br>
value( int i0, int i1, int i2, int i3 ) &rarr; double<br>
