***
<a name="ne"></a>
# ne
ne( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

element-wise not equal test.  1.0 is returned where elements are not equal.
 Fill is returned where either measurement is invalid.

### Parameters:
ds1 - a QDataSet
<br>ds2 - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=ne&unscoped_q=ne">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

ne( Object ds1, Object ds2 ) &rarr; QDataSet<br>
***
<a name="negate"></a>
# negate
negate( QDataSet ds1 ) &rarr; QDataSet

return a dataset with each element negated.
 If units are specified, Units must be ratiometric units, like "5 km" 
 or dimensionless, and not ordinal or time location units.

### Parameters:
ds1 - a QDataSet

### Returns:
a QDataSet

### See Also:
<a href='Ops_c.md#copysign'>copysign</a> <br>
<a href='Ops_s.md#signum'>signum</a> <br>

<a href="https://github.com/autoplot/dev/search?q=negate&unscoped_q=negate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

negate( Object ds1 ) &rarr; QDataSet<br>
***
<a name="neighborFill"></a>
# neighborFill
neighborFill( QDataSet ds ) &rarr; QDataSet

fill in the missing values by copying nearest data points.  All data
 in the result will be copies of elements found in the result, but no
 regard is given to how far a point is shifted.  This was
 motivated by supporting fill in median.

### Parameters:
ds - a QDataSet

### Returns:
dataset that does not contain fill.

<a href="https://github.com/autoplot/dev/search?q=neighborFill&unscoped_q=neighborFill">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="normalize"></a>
# normalize
normalize( QDataSet ds ) &rarr; QDataSet

normalize the data so that the max is 1, where we normalize by the biggest

### Parameters:
ds - a QDataSet

### Returns:
dataset with the same geometry as ds.

<a href="https://github.com/autoplot/dev/search?q=normalize&unscoped_q=normalize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="not"></a>
# not
not( QDataSet ds1 ) &rarr; QDataSet

element-wise logical not function.  non-zero is true, zero is false.

### Parameters:
ds1 - a QDataSet

### Returns:
a QDataSet

### See Also:
<a href='Ops_b.md#bitwiseXor'>bitwiseXor(QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=not&unscoped_q=not">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

not( Object ds1 ) &rarr; QDataSet<br>
