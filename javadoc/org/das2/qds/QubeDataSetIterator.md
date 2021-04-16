# org.das2.qds.QubeDataSetIteratorDataSetIterator implementation that can be used for all dataset (not just qubes).  
 Originally this only worked for QDataSets that were qubes, or datasets that 
 had the same dataset geometry for each slice.  At some point this was 
 modified to work with any dataset but the name remains.
 
 DataSetIterators are intended to work with multiple datasets at once.  For example,
 if we want to add the data from two datasets together, we would create one 
 iterator that would be used to access both datasets.  One dataset is provided
 to the constructor, but any dataset of the same geometry can be passed to the
 getValue method.
 
 TODO: This does not work for Rank 0 datasets.  See
 sftp://klunk.physics.uiowa.edu/home/jbf/project/autoplot/script/demos/jeremy/qubeDataSetIteratorForNonQubes.jy
QubeDataSetIterator( QDataSet ds )
dataset iterator to help in implementing the complex indexing
 types of python.  Each of the dimensions is set to iterate over all
 indeces (e.g ds[:,:,:])
 
 Client codes should create a new iterator, set the index iterator factories, then iterate.

***
<a name="checkValidIndexList"></a>
# checkValidIndexList
checkValidIndexList( QDataSet ds, int indexSize ) &rarr; void



### Parameters:
ds - a QDataSet
<br>indexSize - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=checkValidIndexList&unscoped_q=checkValidIndexList">[search for examples]</a>

***
<a name="createEmptyDs"></a>
# createEmptyDs
createEmptyDs(  ) &rarr; DDataSet

return a dataset that will have the same geometry at the
 dataset implied by each dimension iterator.  This is
 introduced to encapsulate this dangerous code to here where it could
 be done correctly.  Right now this assumes QUBES.

 Do not pass the result of this into the putValue of this iterator,
 the result should have its own iterator.

 20101006 jbf: copy dimensional metadata DEPEND_0, etc where possible
 20120718 jbf: bugfix with ds[7,16,4,:]. Support BINS.

### Returns:
empty dataset with structural properties set.

<a href="https://github.com/autoplot/dev/search?q=createEmptyDs&unscoped_q=createEmptyDs">[search for examples]</a>

***
<a name="currentJythonLine"></a>
# currentJythonLine
currentJythonLine(  ) &rarr; String

return the current line in the Jython script as &lt;filename&gt;:&lt;linenum&gt;
 or ??? if this cannot be done.  Note calls to this will collect a stack
 trace and will affect performance.

### Returns:
the current line or ???
### See Also:
<a href='JythonOps.md#currentLine'>JythonOps#currentLine()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=currentJythonLine&unscoped_q=currentJythonLine">[search for examples]</a>

***
<a name="getValue"></a>
# getValue
getValue( QDataSet ds ) &rarr; double



### Parameters:
ds - a QDataSet

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=getValue&unscoped_q=getValue">[search for examples]</a>

***
<a name="hasNext"></a>
# hasNext
hasNext(  ) &rarr; boolean

true if there are more values.

### Returns:
true if there are more values.

<a href="https://github.com/autoplot/dev/search?q=hasNext&unscoped_q=hasNext">[search for examples]</a>

***
<a name="index"></a>
# index
index( int dim ) &rarr; int



### Parameters:
dim - an int

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=index&unscoped_q=index">[search for examples]</a>

***
<a name="length"></a>
# length
length( int dim ) &rarr; int



### Parameters:
dim - an int

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=length&unscoped_q=length">[search for examples]</a>

***
<a name="next"></a>
# next
next(  ) &rarr; void

advance to the next index.  getValue(ds) will return the value of the
 dataset at this index.

### Returns:
void (returns nothing)

### See Also:
<a href='#getValue'>getValue(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=next&unscoped_q=next">[search for examples]</a>

***
<a name="putValue"></a>
# putValue
putValue( org.das2.qds.WritableDataSet ds, double v ) &rarr; void



### Parameters:
ds - a WritableDataSet
<br>v - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putValue&unscoped_q=putValue">[search for examples]</a>

***
<a name="rank"></a>
# rank
rank(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=rank&unscoped_q=rank">[search for examples]</a>

***
<a name="setIndexIteratorFactory"></a>
# setIndexIteratorFactory
setIndexIteratorFactory( int dim, org.das2.qds.QubeDataSetIterator.DimensionIteratorFactory fit ) &rarr; void

reinitializes the iterator.

### Parameters:
dim - the dimension index (0,...,rank-1)
<br>fit - the iterator factory to use for the index.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setIndexIteratorFactory&unscoped_q=setIndexIteratorFactory">[search for examples]</a>

***
<a name="setMonitor"></a>
# setMonitor
setMonitor( ProgressMonitor mon ) &rarr; void

convenient method for monitoring long processes, this allows
 clients to let the iterator manage the monitor.  setTaskSize, 
 started, setTaskProgress, and finished are called automatically.  
 The monitor will reflect the zeroth index.

### Parameters:
mon - the monitor, or null.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMonitor&unscoped_q=setMonitor">[search for examples]</a>

***
<a name="sliceIterator"></a>
# sliceIterator
sliceIterator( QDataSet ds, int sliceIndex ) &rarr; QubeDataSetIterator

return an iterator for the slice of a dataset (on the 0th index).  
 This is introduced to improve performance by reducing the number of 
 bounds checks, etc from the general case.  Note slice is a native
 operation for most datasets now, so this is probably obsolete.

### Parameters:
ds - the dataset.
<br>sliceIndex - the index of the slice.

### Returns:
an iterator for the slice.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/QDataSet.md#slice'>QDataSet#slice(int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=sliceIterator&unscoped_q=sliceIterator">[search for examples]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

