# org.das2.qds.WritableJoinDataSetJoin of WritableDataSets where each dataset is writable.  Note type checking is
 only done when the constructor that accepts a dataset, otherwise type checking
 is not done until the data is accessed.  This was introduced to properly
 support Ops.copy.
WritableJoinDataSet( int rank )


WritableJoinDataSet( QDataSet ds )


***
<a name="copy"></a>
# copy
copy( QDataSet src ) &rarr; WritableDataSet

create a copy of the dataset src, which can be a join of qubes.
 Note this assumes that each slice is a qube, which was not asserted until now.

### Parameters:
src - a QDataSet

### Returns:
an org.das2.qds.WritableDataSet


<a href="https://github.com/autoplot/dev/search?q=copy&unscoped_q=copy">[search for examples]</a>

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
