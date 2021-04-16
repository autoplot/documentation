# org.das2.qds.TailBundleDataSetcreate a high rank dataset the last dimension being the bundle.  Each
 dataset must have the same length.

 Modification History:
   2015-10-30: copied from BundleDataSet
   See https://sourceforge.net/p/autoplot/feature-requests/267/
TailBundleDataSet( int rank )
Creates a new instance of BundleDataSet with the given rank.  Rank 1
 datasets can bundle rank 0 datasets, while rank 2 can only bundle
 rank 1 datasets with the same depend_0.

TailBundleDataSet( QDataSet ds )
create a bundle with the first dataset.  The result will have 
 rank N+1 where ds has rank N.

***
<a name="bundle"></a>
# bundle
bundle( QDataSet ds ) &rarr; void

add the dataset to the bundle of datasets.  Currently this implementation only supports rank N-1 datasets (N is this
 dataset's rank), but the QDataSet spec allows for qube datasets of any rank&gt;1 to be bundled.  This limitation will be removed
 in a future version.  (Note QDataSet changes http://autoplot.org/QDataSet#2011-Apr-13)

### Parameters:
ds - a QDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=bundle&unscoped_q=bundle">[search for examples]</a>

***
<a name="length"></a>
# length
length(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=length&unscoped_q=length">[search for examples]</a>

length( int i0 ) &rarr; int<br>
length( int i0, int i1 ) &rarr; int<br>
length( int i0, int i1, int i2 ) &rarr; int<br>
***
<a name="property"></a>
# property
property( String name, int i0 ) &rarr; Object



### Parameters:
name - a String
<br>i0 - an int

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=property&unscoped_q=property">[search for examples]</a>

***
<a name="rank"></a>
# rank
rank(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=rank&unscoped_q=rank">[search for examples]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

***
<a name="unbundle"></a>
# unbundle
unbundle( int i ) &rarr; QDataSet

allow to simply unbundle the dataset.

### Parameters:
i - the index.

### Returns:
the dataset at i.

<a href="https://github.com/autoplot/dev/search?q=unbundle&unscoped_q=unbundle">[search for examples]</a>

***
<a name="value"></a>
# value
value( int i0 ) &rarr; double



### Parameters:
i0 - an int

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

value( int i0, int i1 ) &rarr; double<br>
value( int i0, int i1, int i2 ) &rarr; double<br>
value( int i0, int i1, int i2, int i3 ) &rarr; double<br>
