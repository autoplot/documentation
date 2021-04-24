# org.das2.qds.Slice1DataSet

return a rank N-1 dataset from a rank N dataset by slicing on the second
 dimension.  (Rank 2, 3, and 4 supported.)
 
 plane datasets are sliced as well, when they have rank 2 or greater.
 bundle_1 handled.

 Note when DEPEND_1 has EnumerationUnits (like when it comes from labels() method,
 then this should be the same as the unbundle method.

# Slice1DataSet( QDataSet ds, int index )


# Slice1DataSet( QDataSet ds, int index, boolean unbundle )


***
<a name="equals"></a>
# equals
equals( Object obj ) &rarr; boolean



### Parameters:
obj - an Object

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=equals&unscoped_q=equals">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hashCode"></a>
# hashCode
hashCode(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=hashCode&unscoped_q=hashCode">[search for examples]</a>
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
***
<a name="property"></a>
# property
property( String name ) &rarr; Object



### Parameters:
name - a String

### Returns:
an Object


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
value( int i ) &rarr; double



### Parameters:
i - an int

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

value( int i0, int i1 ) &rarr; double<br>
value( int i0, int i1, int i2 ) &rarr; double<br>
