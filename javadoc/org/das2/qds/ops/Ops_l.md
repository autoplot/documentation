***
<a name="labels"></a>
# <del>labels</del>
Deprecated: use labelsDataset
labels( java.lang.String[] labels ) &rarr; QDataSet<br>
***
<a name="labelsDataset"></a>
# labelsDataset
labelsDataset( java.lang.String[] labels, String context ) &rarr; QDataSet

create a labels dataset for tagging rows of a dataset.  If the context
 has been used already, including "default", then the EnumerationUnit
 for the data will be preserved.  labelsDataset(['red','green','blue'],'default')
 will always return an equivalent (and comparable) result during a session.

 Example:
 <tt>dep1= labelsDataset( ['X','Y','Z'], 'GSM' )</tt>

### Parameters:
labels - array of string labels
<br>context - the namespace for the labels, to provide control over String&rarr;int mapping.

### Returns:
rank 1 QDataSet

<a href="https://github.com/autoplot/dev/search?q=labelsDataset&unscoped_q=labelsDataset">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

labelsDataset( java.lang.String[] labels ) &rarr; QDataSet<br>
labelsDataset( String label ) &rarr; QDataSet<br>
labelsDataset( String label, String context ) &rarr; QDataSet<br>
***
<a name="le"></a>
# le
le( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

element-wise function returns 1 where ds1&lt;=ds2.

### Parameters:
ds1 - a QDataSet
<br>ds2 - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=le&unscoped_q=le">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

le( Object ds1, Object ds2 ) &rarr; QDataSet<br>
***
<a name="lesserOf"></a>
# lesserOf
lesserOf( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

element-wise function returns the smaller of ds1 and ds2.
 If an element of ds1 or ds2 is fill, then the result is fill.

### Parameters:
ds1 - a QDataSet
<br>ds2 - a QDataSet

### Returns:
the smaller of the two, in the units of ds1.

<a href="https://github.com/autoplot/dev/search?q=lesserOf&unscoped_q=lesserOf">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

lesserOf( Object ds1, Object ds2 ) &rarr; QDataSet<br>
***
<a name="link"></a>
# link
link( QDataSet x, QDataSet y ) &rarr; QDataSet

link is the fundamental operator where we declare that one
 dataset is dependent on another.  For example link(x,y) creates
 a new dataset where y is the dependent variable of the independent
 variable x.  link is like the plot command, but doesn't plot.  For example
<blockquote><pre>
plot(X,Y) shows a plot of Y(X),
link(X,Y) returns the dataset Y(X).
</pre></blockquote>

### Parameters:
x - rank 1 dataset
<br>y - rank 1 or rank 2 bundle dataset

### Returns:
rank 1 dataset with DEPEND_0 set to x.

<a href="https://github.com/autoplot/dev/search?q=link&unscoped_q=link">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

link( QDataSet x, QDataSet y, QDataSet z ) &rarr; QDataSet<br>
link( QDataSet d0, QDataSet d1, QDataSet d2, QDataSet z ) &rarr; QDataSet<br>
link( QDataSet d0, QDataSet d1, QDataSet d2, QDataSet d3, QDataSet z ) &rarr; QDataSet<br>
link( Object x, Object y ) &rarr; QDataSet<br>
link( Object x, Object y, Object z ) &rarr; QDataSet<br>
link( Object d0, Object d1, Object d2, Object z ) &rarr; QDataSet<br>
***
<a name="linspace"></a>
# linspace
linspace( double min, double max, int len0 ) &rarr; QDataSet

return a rank 1 dataset with <tt>len0</tt> linearly-spaced values, the first
 is min and the last is max.

### Parameters:
min - double
<br>max - double
<br>len0 - number of elements in the result

### Returns:
rank 1 dataset of linearly spaced data.

<a href="https://github.com/autoplot/dev/search?q=linspace&unscoped_q=linspace">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

linspace( Object omin, Object omax, int len0 ) &rarr; QDataSet<br>
***
<a name="log"></a>
# log
log( QDataSet ds ) &rarr; QDataSet

element-wise natural logarithm.

### Parameters:
ds - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=log&unscoped_q=log">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

log( double ds1 ) &rarr; double<br>
log( Object ds1 ) &rarr; QDataSet<br>
***
<a name="log10"></a>
# log10
log10( QDataSet ds ) &rarr; QDataSet

element-wise base 10 logarithm.

### Parameters:
ds - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=log10&unscoped_q=log10">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

log10( double ds1 ) &rarr; double<br>
log10( Object ds1 ) &rarr; QDataSet<br>
***
<a name="logspace"></a>
# logspace
logspace( double min, double max, int len0 ) &rarr; QDataSet

return a rank 1 dataset with <tt>len0</tt> logarithmically-spaced values, the first
 is min and the last is max.

### Parameters:
min - double
<br>max - double
<br>len0 - number of elements in the result

### Returns:
rank 1 dataset of logarithmically spaced data.

<a href="https://github.com/autoplot/dev/search?q=logspace&unscoped_q=logspace">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

logspace( Object omin, Object omax, int len0 ) &rarr; QDataSet<br>
***
<a name="lonarr"></a>
# lonarr
lonarr( int len0 ) &rarr; QDataSet

create a dataset filled with zeros, stored in 8-byte longs, suitable for
 storing cdf_tt2000 times..

### Parameters:
len0 - the zeroth dimension length

### Returns:
rank 1 dataset filled with zeros.
### See Also:
<a href='Ops_z.md#zeros'>zeros(int)</a> <br>
<a href='Ops_d.md#dblarr'>dblarr(int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=lonarr&unscoped_q=lonarr">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

lonarr( int len0, int len1 ) &rarr; QDataSet<br>
***
<a name="lt"></a>
# lt
lt( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

element-wise function returns 1 where ds1&lt;ds2.

### Parameters:
ds1 - a QDataSet
<br>ds2 - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=lt&unscoped_q=lt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

lt( Object ds1, Object ds2 ) &rarr; QDataSet<br>
