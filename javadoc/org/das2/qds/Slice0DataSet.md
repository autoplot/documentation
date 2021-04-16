# org.das2.qds.Slice0DataSetWraps a rank N dataset, slicing on an index of the first dimension to make a rank N-1 dataset.
 This is currently used to implement DataSetOps.slice0().
 
 Slicing a rank 1 dataset results in a rank 0 dataset.

 Supports rank 2 depend_1 datasets.  Supports CONTEXT_0, DELTA_PLUS, DELTA_MINUS

 Supports BINS_1, JOIN_0
Slice0DataSet( QDataSet ds, int index )


Slice0DataSet( QDataSet ds, int index, boolean addContext )


***
<a name="equals"></a>
# equals
equals( Object obj ) &rarr; boolean



### Parameters:
obj - an Object

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=equals&unscoped_q=equals">[search for examples]</a>

***
<a name="hashCode"></a>
# hashCode
hashCode(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=hashCode&unscoped_q=hashCode">[search for examples]</a>

***
<a name="length"></a>
# length
length(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=length&unscoped_q=length">[search for examples]</a>

length( int i0 ) &rarr; int<br>
length( int i0, int i1 ) &rarr; int<br>
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
value(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

value( int i ) &rarr; double<br>
value( int i0, int i1 ) &rarr; double<br>
value( int i0, int i1, int i2 ) &rarr; double<br>
