# org.das2.qds.ops.OpsParl



***
<a name="applyBinaryOp"></a>
# applyBinaryOp
applyBinaryOp( QDataSet ds1, QDataSet ds2, org.das2.qds.ops.OpsParl.BinaryOp op ) &rarr; MutablePropertyDataSet

apply the binary operator element-for-element of the two datasets, minding
 dataset geometry, fill values, etc.  The two datasets are coerced to
 compatible geometry, if possible (e.g.Temperature[Time]+2deg), using 
 CoerceUtil.coerce.  Structural metadata such as DEPEND_0 are preserved 
 where this is reasonable, and dimensional metadata such as UNITS are
 dropped.

### Parameters:
ds1 - the first argument
<br>ds2 - the second argument
<br>op - binary operation for each pair of elements

### Returns:
the result with the same geometry as the pair.

<a href="https://github.com/autoplot/dev/search?q=applyBinaryOp&unscoped_q=applyBinaryOp">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="applyBinaryOpNoIter"></a>
# applyBinaryOpNoIter
applyBinaryOpNoIter( QDataSet ds1, QDataSet ds2, org.das2.qds.ops.OpsParl.BinaryOp op ) &rarr; MutablePropertyDataSet

apply the binary operator element-for-element of the two datasets, minding
 dataset geometry, fill values, etc.  The two datasets are coerced to
 compatible geometry, if possible (e.g.Temperature[Time]+2deg), using 
 CoerceUtil.coerce.  Structural metadata such as DEPEND_0 are preserved 
 where this is reasonable, and dimensional metadata such as UNITS are
 dropped.
 
 This implementation avoids the use of DataSetIterators, which have been
 shown to be slow.  (But it's not known why.)

### Parameters:
ds1 - the first argument
<br>ds2 - the second argument
<br>op - binary operation for each pair of elements

### Returns:
the result with the same geometry as the pair.

<a href="https://github.com/autoplot/dev/search?q=applyBinaryOpNoIter&unscoped_q=applyBinaryOpNoIter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="applyBinaryOpParl"></a>
# applyBinaryOpParl
applyBinaryOpParl( QDataSet ds1, QDataSet ds2, org.das2.qds.ops.OpsParl.BinaryOp op ) &rarr; MutablePropertyDataSet

apply the binary operator element-for-element of the two datasets, minding
 dataset geometry, fill values, etc.  The two datasets are coerced to
 compatible geometry, if possible (e.g.Temperature[Time]+2deg), using 
 CoerceUtil.coerce.  Structural metadata such as DEPEND_0 are preserved 
 where this is reasonable, and dimensional metadata such as UNITS are
 dropped.
 
 This implementation runs the trivially parallelizable task on separate 
 threads.

### Parameters:
ds1 - the first argument
<br>ds2 - the second argument
<br>op - binary operation for each pair of elements

### Returns:
the result with the same geometry as the pair.

<a href="https://github.com/autoplot/dev/search?q=applyBinaryOpParl&unscoped_q=applyBinaryOpParl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="eq"></a>
# eq
eq( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

element-wise equality test.  1.0 is returned where the two datasets are
 equal.  Fill is returned where either measurement is invalid.

### Parameters:
ds1 - rank n dataset
<br>ds2 - rank m dataset with compatible geometry.

### Returns:
rank n or m dataset.

<a href="https://github.com/autoplot/dev/search?q=eq&unscoped_q=eq">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="eq_noiter"></a>
# eq_noiter
eq_noiter( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

element-wise equality test.  1.0 is returned where the two datasets are
 equal.  Fill is returned where either measurement is invalid.

### Parameters:
ds1 - rank n dataset
<br>ds2 - rank m dataset with compatible geometry.

### Returns:
rank n or m dataset.

<a href="https://github.com/autoplot/dev/search?q=eq_noiter&unscoped_q=eq_noiter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="eq_parl"></a>
# eq_parl
eq_parl( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

element-wise equality test.  1.0 is returned where the two datasets are
 equal.  Fill is returned where either measurement is invalid.

### Parameters:
ds1 - rank n dataset
<br>ds2 - rank m dataset with compatible geometry.

### Returns:
rank n or m dataset.

<a href="https://github.com/autoplot/dev/search?q=eq_parl&unscoped_q=eq_parl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

