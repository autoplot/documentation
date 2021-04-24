# org.das2.qds.buffer.FloatDataSet



# FloatDataSet( int rank, int reclen, int recoffs, int len0, int len1, int len2, int len3, java.nio.ByteBuffer back )


***
<a name="capability"></a>
# capability
capability( java.lang.Class clazz ) &rarr; Object

Clients should use this instead of casting the class to the 
 capability class.

### Parameters:
clazz - the class, such as WritableDataSet.class

### Returns:
null or the capability if exists, such as WritableDataSet

<a href="https://github.com/autoplot/dev/search?q=capability&unscoped_q=capability">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putProperty"></a>
# putProperty
putProperty( String name, Object value ) &rarr; void

check for fill as well, since often numerical noise will corrupt 
 the fill values.

### Parameters:
name - the property name
<br>value - the property value

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putProperty&unscoped_q=putProperty">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putValue"></a>
# putValue
putValue( double d ) &rarr; void



### Parameters:
d - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putValue&unscoped_q=putValue">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

putValue( int i0, double d ) &rarr; void<br>
putValue( int i0, int i1, double d ) &rarr; void<br>
putValue( int i0, int i1, int i2, double d ) &rarr; void<br>
putValue( int i0, int i1, int i2, int i3, double d ) &rarr; void<br>
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
