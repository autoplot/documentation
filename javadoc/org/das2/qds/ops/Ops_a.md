# org.das2.qds.ops.Ops

A fairly complete set of operations for QDataSets, including binary operations
 like "add" and "subtract", but also more abstract (and complex) operations like
 smooth and fftPower.  Most operations check data units and validity, but
 consult the documentation for each function.
 
 These operations are all available in Jython scripts, and some, like add, are
 connected to operator symbols like +.

***
<a name="PI"></a>
# PI

closest double to &pi; or TAU/2

***
<a name="TAU"></a>
# TAU

closest double to &tau; or 2*PI

***
<a name="E"></a>
# E

the closest double to e, the base of natural logarithms.

***
<a name="abs"></a>
# abs
abs( QDataSet ds1 ) &rarr; QDataSet

element-wise abs.  For vectors, this returns the length of each element.
 Note Jython conflict needs to be resolved.  Note the result of this
 will have dimensionless units, and see magnitude for the more abstract
 operator.  
 For ratio-type units (Stevens) like "kms", the unit is preserved.

### Parameters:
ds1 - the dataset

### Returns:
dataset with the same geometry
### See Also:
<a href='Ops_m.md#magnitude'>Ops#magnitude(QDataSet)</a> magnitude(ds), which preserves the sign.<br>

<a href="https://github.com/autoplot/dev/search?q=abs&unscoped_q=abs">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

abs( long x ) &rarr; long<br>
abs( double v ) &rarr; double<br>
abs( Object ds1 ) &rarr; QDataSet<br>
***
<a name="accum"></a>
# accum
accum( QDataSet accumDs, QDataSet ds ) &rarr; QDataSet

return an array that is the running sum of each element in the array,
 starting with the value accum.
 Result[i]= accum + total( ds[0:i+1] )

### Parameters:
accumDs - the initial value of the running sum.  Last value of Rank 0 or Rank 1 dataset is used, or may be null.
<br>ds - each element is added to the running sum

### Returns:
the running of each element in the array.
### See Also:
<a href='Ops_d.md#diff'>diff(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=accum&unscoped_q=accum">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

accum( Object accumDs, Object ds ) &rarr; QDataSet<br>
accum( QDataSet ds ) &rarr; QDataSet<br>
accum( Object ds ) &rarr; QDataSet<br>
***
<a name="acos"></a>
# acos
acos( QDataSet ds ) &rarr; QDataSet

element-wise arccos.

### Parameters:
ds - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=acos&unscoped_q=acos">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

acos( double ds ) &rarr; double<br>
acos( Object ds ) &rarr; QDataSet<br>
***
<a name="add"></a>
# add
add( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

add the two datasets which have the compatible geometry and units.  For example,
<blockquote><pre>
ds1=timegen('2014-10-15T07:23','60s',300)
ds2=dataset('30s')
print add(ds1,ds2)
</pre></blockquote>
 The units handling is quite simple, and this will soon change.
 Note that the Jython operator + is overloaded to this method.

### Parameters:
ds1 - a rank N dataset
<br>ds2 - a rank M dataset with compatible geometry

### Returns:
the element-wise sum of the two datasets.
### See Also:
<a href='Ops_a.md#addGen'>addGen(QDataSet, QDataSet, java.util.Map)</a> addGen, which shows how units are resolved.<br>

<a href="https://github.com/autoplot/dev/search?q=add&unscoped_q=add">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

add( Object ds1, Object ds2 ) &rarr; QDataSet<br>
***
<a name="and"></a>
# and
and( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

element-wise logical and function.  non-zero is true, zero is false.

### Parameters:
ds1 - a QDataSet
<br>ds2 - a QDataSet

### Returns:
a QDataSet

### See Also:
<a href='Ops_b.md#bitwiseAnd'>bitwiseAnd(QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=and&unscoped_q=and">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

and( Object ds1, Object ds2 ) &rarr; QDataSet<br>
***
<a name="append"></a>
# append
append( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

append two datasets that are QUBEs.  DEPEND_0 and other metadata is
 handled as well.  So for example: 
<blockquote><pre>
ds1= findgen(10)
ds2= findgen(12)
print append(ds1,ds2)  ; dataSet[22] (dimensionless)
</pre></blockquote>     
 If both datasets are ArrayDataSets and of the same component type, then
 the result will have this type as well.  Otherwise DDataSet is returned.

### Parameters:
ds1 - null or rank N dataset
<br>ds2 - rank N dataset with compatible geometry.

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=append&unscoped_q=append">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="appendEvents"></a>
# appendEvents
appendEvents( QDataSet ev1, QDataSet ev2 ) &rarr; QDataSet

provide explicit method for appending two events scheme datasets.  This will probably be 
 deprecated, and this was added at 17:30 for a particular need.

### Parameters:
ev1 - a QDataSet
<br>ev2 - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=appendEvents&unscoped_q=appendEvents">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="applyBinaryOp"></a>
# applyBinaryOp
applyBinaryOp( QDataSet ds1, QDataSet ds2, org.das2.qds.ops.Ops.BinaryOp op ) &rarr; MutablePropertyDataSet

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

applyBinaryOp( Object ds1, Object ds2, org.das2.qds.ops.Ops.BinaryOp op ) &rarr; MutablePropertyDataSet<br>
***
<a name="applyIndex"></a>
# applyIndex
applyIndex( QDataSet vv, QDataSet ds, Number fillValue ) &rarr; WritableDataSet

apply the indeces, checking for out-of-bounds values.

### Parameters:
vv - values to return, a rank 1, N-element dataset.
<br>ds - the indeces.
<br>fillValue - the value to use when the index is out-of-bounds.

### Returns:
data a dataset with the geometry of ds and the units of values.
### See Also:
<a href='Ops_s.md#subset'>subset(QDataSet, QDataSet)</a> subset, which does the same thing.<br>
<a href='Ops_a.md#applyIndex'>applyIndex(QDataSet, int, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=applyIndex&unscoped_q=applyIndex">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

applyIndex( QDataSet ds, QDataSet r ) &rarr; WritableDataSet<br>
applyIndex( Object dso, QDataSet r ) &rarr; WritableDataSet<br>
applyIndex( QDataSet ds, int dimension, QDataSet indices ) &rarr; MutablePropertyDataSet<br>
***
<a name="applyUnaryOp"></a>
# applyUnaryOp
applyUnaryOp( QDataSet ds1, org.das2.qds.ops.Ops.UnaryOp op ) &rarr; MutablePropertyDataSet

apply the unary operation (such as "cos") to the dataset, propagating
 DEPEND_0 through DEPEND_3 are propagated.  TODO: This should be reviewed
 for speed (iterator is known to be slow) and other metadata that can 
 be preserved.

### Parameters:
ds1 - the argument
<br>op - the operation for each element.

### Returns:
the result the the same geometry.

<a href="https://github.com/autoplot/dev/search?q=applyUnaryOp&unscoped_q=applyUnaryOp">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

applyUnaryOp( Object ds1, org.das2.qds.ops.Ops.UnaryOp op ) &rarr; MutablePropertyDataSet<br>
***
<a name="asin"></a>
# asin
asin( QDataSet ds ) &rarr; QDataSet

element-wise arcsin.

### Parameters:
ds - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=asin&unscoped_q=asin">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

asin( double ds ) &rarr; double<br>
asin( Object ds ) &rarr; QDataSet<br>
***
<a name="atan"></a>
# atan
atan( QDataSet ds ) &rarr; QDataSet

element-wise atan.

### Parameters:
ds - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=atan&unscoped_q=atan">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

atan( double ds ) &rarr; double<br>
atan( Object ds ) &rarr; QDataSet<br>
***
<a name="atan2"></a>
# atan2
atan2( QDataSet y, QDataSet x ) &rarr; QDataSet

element-wise atan2, 4-quadrant atan.  From the Java atan2 documentation:
 "Returns the angle <i>theta</i> from the conversion of rectangular 
 coordinates ( x,&nbsp; y) to polar coordinates 
 (r,&nbsp;<i>theta</i>).  This method computes the phase <i>theta</i> 
 by computing an arc tangent of  y/x in the range of 
 -<i>pi</i> to <i>pi</i>."
 <p>Note different languages have different 
 argument order.  Microsoft Office uses atan2(x,y); IDL uses atan(y,x);  
 Matlab uses atan2(y,x); and NumPy uses arctan2(y,x).</p>

### Parameters:
y - the y values
<br>x - the x values

### Returns:
angles between -PI and PI
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/java/lang/Math_a.md#atan2'>java.lang.Math#atan2(double, double)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=atan2&unscoped_q=atan2">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

atan2( double y, double x ) &rarr; double<br>
atan2( Object dsy, Object dsx ) &rarr; QDataSet<br>
***
<a name="autoHistogram"></a>
# autoHistogram
autoHistogram( QDataSet ds ) &rarr; QDataSet

AutoHistogram is a one-pass self-scaling histogram, useful in autoranging data.  
 The data is fed into the routine, and bins will grow as more and more data is added,
 to result in about 100 bins.  For example, if the initial binsize is 1.0 unit, and the data extent
 is 0-200, then bins are combined so that the new binsize is 2.0 units and 100 bins are used.

### Parameters:
ds - rank N dataset (all ranks are supported).

### Returns:
rank 1 dataset

<a href="https://github.com/autoplot/dev/search?q=autoHistogram&unscoped_q=autoHistogram">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

