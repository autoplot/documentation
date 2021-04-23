# org.das2.qds.GridDataSetgrids a bundle of (X,Y,Z) data into a table Z(X,Y).
GridDataSet( )
creates the dataset, initially length is zero.

***
<a name="add"></a>
# add
add( QDataSet slice ) &rarr; void

add either rank 1 slice ( x,y,z ) or
 add rank 2 dataset ( *,3 )

### Parameters:
slice - rank 1 or rank 2 bundle

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=add&unscoped_q=add">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

add( double x, double y, double z ) &rarr; void<br>
***
<a name="length"></a>
# length
length(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=length&unscoped_q=length">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

length( int i ) &rarr; int<br>
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
value( int i0, int i1 ) &rarr; double



### Parameters:
i0 - an int
<br>i1 - an int

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

