# org.das2.qds.WeightsDataSetProvide consistent valid logic to operators by providing a QDataSet
 with 1.0 where the data is valid, and 0.0 where the data is invalid.
 VALID_MIN, VALID_MAX and FILL_VALUE properties are used.
 
 Note, when FILL_VALUE is not specified, -1e31 is used.  This is to
 support legacy logic.
 
 The property FILL_VALUE is no longer set to the fill value used.  https://sourceforge.net/p/autoplot/bugs/1458/
 SUGGEST_FILL will be set in the properties.
***
<a name="PROP_SUGGEST_FILL"></a>
# PROP_SUGGEST_FILL

the fill value from the original dataset.  
 TODO: We really need a justification of this.  I suspect this was because
 you wouldn't know what values would "fit" into the result, for example,
 you don't want to suggest 1e38 if IDataSet is the implementation.  However,
 I think the fill value used really depends on a number of things and
 it's difficult to preserve the value safely.

***
<a name="applyRules"></a>
# applyRules
applyRules( QDataSet src, QDataSet v ) &rarr; QDataSet

applies the rules from src to dataset v, returning an array of 0 or non-zero.

### Parameters:
src - a QDataSet
<br>v - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=applyRules&unscoped_q=applyRules">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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
property( String name, int i0, int i1 ) &rarr; Object<br>
property( String name, int i0, int i1, int i2 ) &rarr; Object<br>
property( String name, int i0, int i1, int i2, int i3 ) &rarr; Object<br>
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



### Returns:
java.lang.String


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

value( int i ) &rarr; double<br>
value( int i0, int i1 ) &rarr; double<br>
value( int i0, int i1, int i2 ) &rarr; double<br>
value( int i0, int i1, int i2, int i3 ) &rarr; double<br>
