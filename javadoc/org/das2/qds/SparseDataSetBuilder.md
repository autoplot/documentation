# org.das2.qds.SparseDataSetBuilder

Builder for SparseDataSets.  This was introduced to fix the problem where
 we wish to calculate the SparseDataSet in one pass, but we can't do this because
 PyQDataSets obscure the type and there was no way to set the length.
 
 This is also useful for building the BundleDescriptor datasets that describe how to 
 unpack rank 2 datasets with the BUNDLE_1 property.

# SparseDataSetBuilder( int rank )


***
<a name="getDataSet"></a>
# getDataSet
getDataSet(  ) &rarr; SparseDataSet



### Returns:
org.das2.qds.SparseDataSet


<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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
<a name="setLength"></a>
# setLength
setLength( int i0 ) &rarr; void

set the length of the zeroth dimension.  Other dimensions have length set implicitly by the highest value set.
 If this is not set explicitly, then it will be implicit as well.

### Parameters:
i0 - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLength&unscoped_q=setLength">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setQube"></a>
# setQube
setQube( int[] qube ) &rarr; void

make this a qube dataset, where all the lengths are the same.
 implicitly this calls setLength(qube[0]).

### Parameters:
qube - an int[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setQube&unscoped_q=setQube">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

