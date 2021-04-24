# org.das2.qds.ops.CoerceUtil

Utility class for reconciling the geometries of two datasets.  For example,
 a rank 1 dataset's values can be repeated to make it rank 2.

 TODO: dataset geometry is increased by keeping a reference to a dataset with
 the target geometry.  This might result in keeping data in memory that would
 otherwise be released, so a future implementation of this should probably
 use a non-qube dataset to store each index's length:
<blockquote><pre>
 public int length() {
    return lengths.length()
 }
 public int length(int i0) {
    return lengths.value(i0);
 }
</pre></blockquote>

# CoerceUtil( )


***
<a name="coerce"></a>
# coerce
coerce( QDataSet ds1, QDataSet ds2, boolean createResult, org.das2.qds.QDataSet[] operands ) &rarr; WritableDataSet

increase rank of datasets so that element-wise operations can be performed.  For example,
 if a rank 1 and a rank 2 dataset are to be combined and both have equal dim 0 length, then the
 rank 1 is promoted to rank 2 by repeating its values.  This implements the rule that dimensions
 in QDataSet have nested context.  The second dimension elements are to be understood in the context of
 the first dimension element. (Except for qubes, where the order is arbitrary.)

### Parameters:
ds1 - the first operand
<br>ds2 - the second operand
<br>createResult - if true, then a dataset is created where the result can be installed.
<br>operands - the array in which the promoted operands are inserted.

### Returns:
an empty dataset where the results can be inserted, or null if createResult is false.

<a href="https://github.com/autoplot/dev/search?q=coerce&unscoped_q=coerce">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="equalGeom"></a>
# equalGeom
equalGeom( QDataSet ds1, QDataSet ds2 ) &rarr; boolean

returns true if two datasets have the same number of elements in each dimension.

### Parameters:
ds1 - a QDataSet
<br>ds2 - a QDataSet

### Returns:
returns true if two datasets have the same number of elements in each dimension.

<a href="https://github.com/autoplot/dev/search?q=equalGeom&unscoped_q=equalGeom">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="increaseRank0"></a>
# increaseRank0
increaseRank0( QDataSet ds, QDataSet ds2 ) &rarr; QDataSet

increase the rank of a rank zero dataset by adding join dimensions that repeat the lower rank elements.

### Parameters:
ds - a rank 0 dataset
<br>ds2 - dataset to provide rank and lengths.

### Returns:
a dataset with the same geometry as ds2.

<a href="https://github.com/autoplot/dev/search?q=increaseRank0&unscoped_q=increaseRank0">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="increaseRank1"></a>
# increaseRank1
increaseRank1( QDataSet ds, QDataSet ds2 ) &rarr; QDataSet

increase the rank of a rank one dataset by adding join dimensions that repeat the lower rank elements.

### Parameters:
ds - a rank 1 dataset to provide values and properties
<br>ds2 - dataset to provide rank and lengths.

### Returns:
a dataset with the same geometry as ds2.

<a href="https://github.com/autoplot/dev/search?q=increaseRank1&unscoped_q=increaseRank1">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="increaseRank2"></a>
# increaseRank2
increaseRank2( QDataSet ds, QDataSet ds2 ) &rarr; QDataSet

increase the rank of a rank two dataset by adding join dimensions that repeat the lower rank elements.

### Parameters:
ds - a rank 2 dataset to provide values and properties
<br>ds2 - dataset to provide rank and lengths.

### Returns:
a dataset with the same geometry as ds2.

<a href="https://github.com/autoplot/dev/search?q=increaseRank2&unscoped_q=increaseRank2">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

