# org.das2.qds.LengthsDataSet

DataSet that is the lengths of another dataset.  The total of all the leaves
 is the total number of elements in the dataset.  The rank is one less than
 that of the wrapped dataset, and the values are the lengths of the last dimension
 of the wrapped dataset.

 It's expected that this will be generally useful and a handy way to make
 a QUBE dataset implementation such as DDataSet support non-qube datasets.

# LengthsDataSet( QDataSet ds )


***
<a name="length"></a>
# length
length(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=length&unscoped_q=length">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

length( int i ) &rarr; int<br>
length( int i, int j ) &rarr; int<br>
length( int i, int j, int k ) &rarr; int<br>
***
<a name="rank"></a>
# rank
rank(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=rank&unscoped_q=rank">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="value"></a>
# value
value(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

value( int i ) &rarr; double<br>
value( int i0, int i1 ) &rarr; double<br>
value( int i0, int i1, int i2 ) &rarr; double<br>
