# org.das2.qds.math.matrix.CompositeMatrixAll of the elementary row and column operations are applied to both
 underlying matrices.  Reads are done from the first matrix.  Writes
 are not allowed (except those that are side effects of elementary
 matrix operations).
CompositeMatrix( org.das2.qds.math.matrix.Matrix m1, org.das2.qds.math.matrix.Matrix m2 )


***
<a name="get"></a>
# get
get( int row, int col ) &rarr; double



### Parameters:
row - an int
<br>col - an int

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=get&unscoped_q=get">[search for examples]</a>

***
<a name="rowTimes"></a>
# rowTimes
rowTimes( int row, double s ) &rarr; void



### Parameters:
row - an int
<br>s - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=rowTimes&unscoped_q=rowTimes">[search for examples]</a>

***
<a name="rowTimesAddTo"></a>
# rowTimesAddTo
rowTimesAddTo( int srcRow, double s, int dstRow ) &rarr; void



### Parameters:
srcRow - an int
<br>s - a double
<br>dstRow - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=rowTimesAddTo&unscoped_q=rowTimesAddTo">[search for examples]</a>

***
<a name="set"></a>
# set
set( int row, int col, double d ) &rarr; void



### Parameters:
row - an int
<br>col - an int
<br>d - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=set&unscoped_q=set">[search for examples]</a>

***
<a name="swapRows"></a>
# swapRows
swapRows( int row1, int row2 ) &rarr; void



### Parameters:
row1 - an int
<br>row2 - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=swapRows&unscoped_q=swapRows">[search for examples]</a>

