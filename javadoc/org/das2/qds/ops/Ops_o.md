***
<a name="ones"></a>
# ones
ones( int len0 ) &rarr; QDataSet

return new dataset filled with ones.

### Parameters:
len0 - the length of the first index.

### Returns:
dataset filled with ones.

<a href="https://github.com/autoplot/dev/search?q=ones&unscoped_q=ones">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

ones( int len0, int len1 ) &rarr; QDataSet<br>
ones( int len0, int len1, int len2 ) &rarr; QDataSet<br>
ones( int len0, int len1, int len2, int len3 ) &rarr; QDataSet<br>
***
<a name="or"></a>
# or
or( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

element-wise logical or function.  
 returns 1 where ds1 is non-zero or ds2 is non-zero.

### Parameters:
ds1 - a QDataSet
<br>ds2 - a QDataSet

### Returns:
a QDataSet

### See Also:
<a href='Ops_b.md#bitwiseOr'>bitwiseOr(QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=or&unscoped_q=or">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

or( Object ds1, Object ds2 ) &rarr; QDataSet<br>
***
<a name="outerProduct"></a>
# outerProduct
outerProduct( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

returns outerProduct of two rank 1 datasets, a rank 2 dataset with 
 elements R[i,j]= ds1[i] * ds2[j].

### Parameters:
ds1 - rank 1 dataset length m.
<br>ds2 - rank 1 dataset of length n.

### Returns:
rank 2 dataset that is m by n.

<a href="https://github.com/autoplot/dev/search?q=outerProduct&unscoped_q=outerProduct">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

outerProduct( Object ds1, Object ds2 ) &rarr; QDataSet<br>
***
<a name="outerSum"></a>
# outerSum
outerSum( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

returns outerSum of two rank 1 datasets, a rank 2 dataset with
 elements R[i,j]= ds1[i] + ds2[j].

### Parameters:
ds1 - a rank 1 dataset of length m
<br>ds2 - a rank 1 dataset of length n

### Returns:
a rank 2 dataset[m,n]

<a href="https://github.com/autoplot/dev/search?q=outerSum&unscoped_q=outerSum">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

outerSum( Object ds1, Object ds2 ) &rarr; QDataSet<br>
