# org.das2.qds.TrimStrideWrapper

Wraps rank N qube dataset to present a dataset with the same rank that is a subset of
 wrapped dataset.

 Note this was used before trim() was a native operator for datasets, and it
 should be used when the zeroth dimension is trimmed with stride==1.

# TrimStrideWrapper( QDataSet ds )
construct a wrapper with no trimming by default.  setTrim is
 called to trim a dimension.

***
<a name="length"></a>
# length
length( int i, int j, int k ) &rarr; int



### Parameters:
i - an int
<br>j - an int
<br>k - an int

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=length&unscoped_q=length">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

length( int i, int j ) &rarr; int<br>
length( int i ) &rarr; int<br>
length(  ) &rarr; int<br>
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

***
<a name="rank"></a>
# rank
rank(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=rank&unscoped_q=rank">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTrim"></a>
# setTrim
setTrim( int dim, Number start, Number stop, Number stride ) &rarr; void

trim the dimension.  Null indexes indicate the default should be 
 used.  Negative indeces are relative to the length of the dimension.

### Parameters:
dim - the index, between 0 and rank.
<br>start - index to start from, null for 0, or negative.
<br>stop - exclusive index to end from, null for qube[dim], or negative.
<br>stride - the step size, or null for 1.  TODO: I doubt this can be negative, but this needs verification.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTrim&unscoped_q=setTrim">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="value"></a>
# value
value( int i0, int i1, int i2, int i3 ) &rarr; double



### Parameters:
i0 - an int
<br>i1 - an int
<br>i2 - an int
<br>i3 - an int

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

value( int i0, int i1, int i2 ) &rarr; double<br>
value( int i0, int i1 ) &rarr; double<br>
value( int i0 ) &rarr; double<br>
