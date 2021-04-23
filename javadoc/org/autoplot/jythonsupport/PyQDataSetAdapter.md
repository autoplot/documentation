# org.autoplot.jythonsupport.PyQDataSetAdapter

Adapt QDataSet results to PyQDataSet, which provides __getitem__
 and __setitem__.  (ds[0,0]=ds[0,0]+1)

# PyQDataSetAdapter( )


***
<a name="adapt"></a>
# adapt
adapt( Object arg0 ) &rarr; PyObject



### Parameters:
arg0 - an Object

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=adapt&unscoped_q=adapt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="adaptList"></a>
# adaptList
adaptList( PyList p ) &rarr; QDataSet

adapts list to QDataSet.  
 If this contains datums or rank 0 datasets with different units, then a bundle is returned.
 TODO: Consider: if element is a string, then enumeration units are used.

### Parameters:
p - a PyList

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=adaptList&unscoped_q=adaptList">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

adaptList( PyList p, Units u ) &rarr; QDataSet<br>
***
<a name="adaptTuple"></a>
# adaptTuple
adaptTuple( PyTuple p ) &rarr; QDataSet



### Parameters:
p - a PyTuple

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=adaptTuple&unscoped_q=adaptTuple">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

adaptTuple( PyTuple p, Units u ) &rarr; QDataSet<br>
***
<a name="canAdapt"></a>
# canAdapt
canAdapt( Object arg0 ) &rarr; boolean



### Parameters:
arg0 - an Object

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=canAdapt&unscoped_q=canAdapt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

