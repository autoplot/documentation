# org.das2.qds.IndexListDataSetIterator

Iterator that uses a rank 2 list of indeces.  For example,
 to iterate over 10 points of a rank 2 dataset, this would be constructed
 with a dataset[10,2].

# IndexListDataSetIterator( QDataSet indeces )
Create the iterator

***
<a name="createEmptyDs"></a>
# createEmptyDs
createEmptyDs(  ) &rarr; DDataSet



### Returns:
org.das2.qds.DDataSet


<a href="https://github.com/autoplot/dev/search?q=createEmptyDs&unscoped_q=createEmptyDs">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getValue"></a>
# getValue
getValue( QDataSet ds ) &rarr; double

get the value from ds at the current iterator position.

### Parameters:
ds - a dataset with compatible geometry as the iterator's geometry.

### Returns:
the value of ds at the current iterator position.

<a href="https://github.com/autoplot/dev/search?q=getValue&unscoped_q=getValue">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasNext"></a>
# hasNext
hasNext(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=hasNext&unscoped_q=hasNext">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="index"></a>
# index
index( int dim ) &rarr; int



### Parameters:
dim - an int

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=index&unscoped_q=index">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="length"></a>
# length
length( int dim ) &rarr; int



### Parameters:
dim - an int

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=length&unscoped_q=length">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="next"></a>
# next
next(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=next&unscoped_q=next">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putValue"></a>
# putValue
putValue( org.das2.qds.WritableDataSet ds, double v ) &rarr; void

replace the value in ds at the current iterator position.

### Parameters:
ds - a writable dataset with compatible geometry as the iterator's geometry.
<br>v - the value to insert.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putValue&unscoped_q=putValue">[search for examples]</a>
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
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

