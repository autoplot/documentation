# org.das2.qds.AbstractDataSet

Abstract class to simplify defining datasets.  This handles the
 properties for implementations, and they
 need only implement rank, and override the corresponding value and length
 methods.

# AbstractDataSet( )


***
<a name="capability"></a>
# capability
capability( java.lang.Class clazz ) &rarr; Object



### Parameters:
clazz - a java.lang.Class

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=capability&unscoped_q=capability">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isImmutable"></a>
# isImmutable
isImmutable(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isImmutable&unscoped_q=isImmutable">[search for examples]</a>
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
<a name="makeImmutable"></a>
# makeImmutable
makeImmutable(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=makeImmutable&unscoped_q=makeImmutable">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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
<a name="putProperty"></a>
# putProperty
putProperty( String name, Object value ) &rarr; void



### Parameters:
name - a String
<br>value - an Object

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putProperty&unscoped_q=putProperty">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

putProperty( String name, int index, Object value ) &rarr; void<br>
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



### Parameters:
i - an int

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=slice&unscoped_q=slice">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="svalue"></a>
# svalue
svalue(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=svalue&unscoped_q=svalue">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String

return a human-readable string representation of this QDataSet.

### Returns:
a human-readable string representation of this QDataSet.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/DataSetUtil.md#toString'>org.das2.qds.DataSetUtil#toString(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
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
value(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

value( int i0 ) &rarr; double<br>
value( int i0, int i1 ) &rarr; double<br>
value( int i0, int i1, int i2 ) &rarr; double<br>
value( int i0, int i1, int i2, int i3 ) &rarr; double<br>
