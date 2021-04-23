# org.das2.qds.OldDataSetIterator

Iterator that provides access to each dataset point, hiding rank when
 when it is not needed.
 
 TODO: Rank2 and Rank3 have problems with zero length indeces.

***
<a name="create"></a>
# create
create( QDataSet ds ) &rarr; OldDataSetIterator



### Parameters:
ds - a QDataSet

### Returns:
org.das2.qds.OldDataSetIterator


<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getIndex"></a>
# getIndex
getIndex( int idim ) &rarr; int

returns the idimth index0 that the cursor is pointing at, after 
 the next() was called.

### Parameters:
idim - an int

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=getIndex&unscoped_q=getIndex">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasNext"></a>
# hasNext
hasNext(  ) &rarr; boolean

true if more data is available.

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=hasNext&unscoped_q=hasNext">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="next"></a>
# next
next(  ) &rarr; double

return the next point.

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=next&unscoped_q=next">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putValue"></a>
# putValue
putValue( org.das2.qds.WritableDataSet ds, org.das2.qds.OldDataSetIterator it, double v ) &rarr; void



### Parameters:
ds - a WritableDataSet
<br>it - an OldDataSetIterator
<br>v - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putValue&unscoped_q=putValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

