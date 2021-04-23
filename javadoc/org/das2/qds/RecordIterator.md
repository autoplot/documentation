# org.das2.qds.RecordIterator

Make any QDataSet into a table, then iterate over the records.  This
 was introduced to support the first Autoplot HAPI server, but will be
 useful elsewhere.

# RecordIterator( QDataSet src )
set up the iterator.  If the src is rank 1 with a DEPEND_0, then
 the two are bundled together.

***
<a name="TIME_STAMP"></a>
# TIME_STAMP



***
<a name="constrainDepend0"></a>
# constrainDepend0
constrainDepend0( DatumRange dr ) &rarr; void

limit the data returned such that only data within the datum range
 provided are returned.

### Parameters:
dr - a DatumRange

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=constrainDepend0&unscoped_q=constrainDepend0">[search for examples]</a>

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
<a name="next"></a>
# next
next(  ) &rarr; QDataSet



### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=next&unscoped_q=next">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="remove"></a>
# remove
remove(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=remove&unscoped_q=remove">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

