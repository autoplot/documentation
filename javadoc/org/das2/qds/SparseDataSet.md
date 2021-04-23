# org.das2.qds.SparseDataSetDataSet for storing sparse data.  This is used initially to describe bundles.
 This returns 0 where no data has been set.  For example,
<blockquote><pre>
sp= SparseDataSet.createQube([2,4])
sp[2,2]= 1
print sp[0,0]
</pre></blockquote>
***
<a name="createQube"></a>
# createQube
createQube( int[] qube ) &rarr; SparseDataSet

create the qube dataset with the given dimensions.  This
 was introduced because setQube cannot be called from Jython scripts.

### Parameters:
qube - the index dimensions.

### Returns:
SparseDataSet with the given rank and dimensions based on qube.

<a href="https://github.com/autoplot/dev/search?q=createQube&unscoped_q=createQube">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRank"></a>
# createRank
createRank( int rank ) &rarr; SparseDataSet

create the dataset with the given rank.  The length of any dimension is explicitly set with the setLength
 method or implicitly by the highest index assigned a value.  Note Jython scripts are unable to call the setLength method.

### Parameters:
rank - number of indeces

### Returns:
a dataset that is empty.
### See Also:
<a href='#createRankLen'>createRankLen(int, int)</a> <br>
<a href='#createQube'>createQube(int[])</a> <br>

<a href="https://github.com/autoplot/dev/search?q=createRank&unscoped_q=createRank">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createRankLen"></a>
# createRankLen
createRankLen( int rank, int len0 ) &rarr; SparseDataSet

create the dataset with the given rank and initial length.  This
 was introduced because setLength cannot be called from Jython scripts.
 Each record will have length(i) based on the highest index assigned.

### Parameters:
rank - the result's rank.
<br>len0 - the number of records in the result.

### Returns:
SparseDataSet with the given rank.
### See Also:
<a href='#createQube'>createQube(int[])</a> <br>

<a href="https://github.com/autoplot/dev/search?q=createRankLen&unscoped_q=createRankLen">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="length"></a>
# length
length(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=length&unscoped_q=length">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

length( int i ) &rarr; int<br>
length( int i0, int i1 ) &rarr; int<br>
length( int i0, int i1, int i2 ) &rarr; int<br>
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
<a name="rank"></a>
# rank
rank(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=rank&unscoped_q=rank">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLength"></a>
# setLength
setLength( int length ) &rarr; void

set the length of the zeroth dimension.  Other dimensions have length set implicitly by the highest value set.
 If this is not set explicitly, then it will be implicit as well.

### Parameters:
length - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLength&unscoped_q=setLength">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setQube"></a>
# setQube
setQube( int[] qube ) &rarr; void

make this a qube dataset, where all the lengths are the same.

### Parameters:
qube - an int[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setQube&unscoped_q=setQube">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="value"></a>
# value
value(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

value( int i0 ) &rarr; double<br>
value( int i0, int i1 ) &rarr; double<br>
value( int i0, int i1, int i2 ) &rarr; double<br>
value( int i0, int i1, int i2, int i3 ) &rarr; double<br>
