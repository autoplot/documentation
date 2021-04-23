# org.das2.qds.util.DataSetBuilder

allows dataset of unknown length to be built. Presently, this only builds QUBES, but should allow for geometry changes.
 TODO: consider using WritableDataSet interface.
 The guessRecCount parameter is the initial number of allocated records, and is also the extension when this number of
 records is passed.  The final physical dataset size is not affected by this, because the data is copied.

# DataSetBuilder( int rank )
Create a new builder for a rank 0 dataset.

# DataSetBuilder( int rank, int guessRecCount )
Create a new builder for a rank 1 dataset.
 guessRecCount is the guess of dim0 size.  Bad guesses will simply result in an extra array copy.

# DataSetBuilder( int rank, int guessRecCount, int dim1 )
Create a new builder for a rank 2 dataset.
 guessRecCount is the guess of dim0 size.  Bad guesses will simply result in an extra array copy.

# DataSetBuilder( int rank, int guessRecCount, int dim1, int dim2 )
Create a new builder for a rank 3 dataset.
 guessRecCount is the guess of dim0 size.  Bad guesses will simply result in an extra array copy.

# DataSetBuilder( int rank, int guessRecCount, int dim1, int dim2, int dim3 )
Create a new builder for a rank 4 dataset.
 guessRecCount is the guess of dim0 size.  Bad guesses will simply result in an extra array copy.

***
<a name="UNRESOLVED_PROP_QDATASET"></a>
# UNRESOLVED_PROP_QDATASET



***
<a name="PROP_VALIDMIN"></a>
# PROP_VALIDMIN



***
<a name="PROP_VALIDMAX"></a>
# PROP_VALIDMAX



***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void

Adds a PropertyChangeListener to the listener list.

### Parameters:
l - The listener to add.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSet"></a>
# getDataSet
getDataSet(  ) &rarr; DDataSet

returns the result dataset, concatenating all the datasets it has built thus far.

### Returns:
the result dataset

<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFillValue"></a>
# getFillValue
getFillValue(  ) &rarr; double

Getter for property fillValue.

### Returns:
Value of property fillValue.

<a href="https://github.com/autoplot/dev/search?q=getFillValue&unscoped_q=getFillValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLength"></a>
# getLength
getLength(  ) &rarr; int

return the number of records added to the builder.

### Returns:
the number of records added to the builder.

<a href="https://github.com/autoplot/dev/search?q=getLength&unscoped_q=getLength">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getProperties"></a>
# getProperties
getProperties(  ) &rarr; Map

get a map of all the properties set thus far.

### Returns:
a java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getProperties&unscoped_q=getProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRecordElements"></a>
# getRecordElements
getRecordElements(  ) &rarr; int

return the number of elements in each record.

### Returns:
the number of elements in each record.

<a href="https://github.com/autoplot/dev/search?q=getRecordElements&unscoped_q=getRecordElements">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getUnits"></a>
# getUnits
getUnits( int i ) &rarr; Units

get the units for the column.

### Parameters:
i - an int

### Returns:
the units or null.

<a href="https://github.com/autoplot/dev/search?q=getUnits&unscoped_q=getUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getValidMax"></a>
# getValidMax
getValidMax(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=getValidMax&unscoped_q=getValidMax">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getValidMin"></a>
# getValidMin
getValidMin(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=getValidMin&unscoped_q=getValidMin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getValue"></a>
# getValue
getValue( int index0 ) &rarr; double

for index0==-1, return the last value entered into the rank 1 dataset.

### Parameters:
index0 - an int

### Returns:
a double


<a href="https://github.com/autoplot/dev/search?q=getValue&unscoped_q=getValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="nextRecord"></a>
# nextRecord
nextRecord(  ) &rarr; void

This must be called each time a record is complete.  Note this
 currently advances to the next record and at this point the next record
 exists.  In other words, the last call to nextRecord is not required.
 This logic may change, so that any fields written would be dropped unless 
 nextRecord is called to commit the record.
 When -1 is used for the indexes of the streaming dimension, then this
 will increment the internal counter.
 TODO: Check for unspecified entries.

### Returns:
void (returns nothing)

### See Also:
<a href='#nextRecord'>nextRecord(java.lang.Object...)</a> which inserts all values at once.<br>

<a href="https://github.com/autoplot/dev/search?q=nextRecord&unscoped_q=nextRecord">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

nextRecord( double[] values ) &rarr; void<br>
nextRecord( java.lang.Object[] values ) &rarr; void<br>
nextRecord( org.das2.datum.DatumVector v ) &rarr; void<br>
nextRecord( QDataSet v ) &rarr; void<br>
nextRecord( double v ) &rarr; void<br>
nextRecord( String s ) &rarr; void<br>
nextRecord( Datum v ) &rarr; void<br>
***
<a name="nextRecords"></a>
# nextRecords
nextRecords( QDataSet ds ) &rarr; void

add each of the records of ds to the builder.  This is somewhat equivalent to:
 <pre>
 
 for d in ds: dsb.nextRecord(d)
 
 </pre>
 (Note the above only works when ds is rank 1.)
 Though this is equivalent, this is provided because a future implementation may peek 
 at the dataset to transfer data more efficiently.

### Parameters:
ds - dataset with rank N, where N is the rank of this builder.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=nextRecords&unscoped_q=nextRecords">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putProperty"></a>
# putProperty
putProperty( String string, Object o ) &rarr; void

add the property to the dataset

### Parameters:
string - name like QDataSet.UNITS
<br>o - the value

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putProperty&unscoped_q=putProperty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putUnresolvedProperty"></a>
# putUnresolvedProperty
putUnresolvedProperty( String type, String pname, String svalue ) &rarr; void

mark the property as unresolved, for reference later.  This was
 added for the QStream reader, which doesn't resolve

### Parameters:
type - the property type, if qdataset this is resolved with dataSetResolver.
<br>pname - the property name ("gain")
<br>svalue - the arbitrary reference ("gain_04")

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putUnresolvedProperty&unscoped_q=putUnresolvedProperty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putValue"></a>
# putValue
putValue( int index0, double d ) &rarr; void

insert a value into the builder.

### Parameters:
index0 - The index to insert the data, or if -1, ignore and nextRecord() should be used.
<br>d - the value to insert.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putValue&unscoped_q=putValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

putValue( int index0, int index1, double d ) &rarr; void<br>
putValue( int index0, int index1, int index2, double d ) &rarr; void<br>
putValue( int index0, int index1, int index2, int index3, double d ) &rarr; void<br>
putValue( int index0, Datum d ) &rarr; void<br>
putValue( int index0, int index1, Datum d ) &rarr; void<br>
putValue( int index0, int index1, int index2, Datum d ) &rarr; void<br>
putValue( int index0, int index1, int index2, int index3, Datum d ) &rarr; void<br>
putValue( int index0, QDataSet d ) &rarr; void<br>
putValue( int index0, int index1, QDataSet d ) &rarr; void<br>
putValue( int index0, int index1, int index2, QDataSet d ) &rarr; void<br>
putValue( int index0, int index1, int index2, int index3, QDataSet d ) &rarr; void<br>
putValue( int index0, String s ) &rarr; void<br>
putValue( int index0, int index1, String s ) &rarr; void<br>
***
<a name="putValues"></a>
# putValues
putValues( int index0, QDataSet values, int count ) &rarr; void

copy the elements from one DDataSet into the builder (which can be done with
 a system call), ignoring dataset geometry.  TODO: since the element count
 allows for putting multiple records in at once, an index out of bounds may 
 occur after the last record of current is written.
 This should only be used to insert one record (with multiple values) at a time.
 Note this does not increment the current index, and nextRecord must be called to move to the next index.

### Parameters:
index0 - The index to put the values, or -1 for the current position.
<br>values - rank 1 dataset.
<br>count - the number of elements to copy

### Returns:
void (returns nothing)

### See Also:
<a href='#nextRecords'>nextRecords(QDataSet)</a> to insert multiple records at once.<br>

<a href="https://github.com/autoplot/dev/search?q=putValues&unscoped_q=putValues">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rank"></a>
# rank
rank(  ) &rarr; int

return the rank of the dataset we are building.

### Returns:
the rank of the dataset we are building

<a href="https://github.com/autoplot/dev/search?q=rank&unscoped_q=rank">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void

Removes a PropertyChangeListener from the listener list.

### Parameters:
l - The listener to remove.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resolveProperty"></a>
# resolveProperty
resolveProperty( String svalue, Object value ) &rarr; void

we now know the value, so resolve any unresolved properties containing the
 string representation.  Note
 the entry is left in the unresolved properties.

### Parameters:
svalue - the string reference
<br>value - the object value

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resolveProperty&unscoped_q=resolveProperty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataSetResolver"></a>
# setDataSetResolver
setDataSetResolver( org.das2.qds.util.DataSetBuilder.DataSetResolver dataSetResolver ) &rarr; void

add dataset resolved.

### Parameters:
dataSetResolver - a DataSetBuilder.DataSetResolver

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSetResolver&unscoped_q=setDataSetResolver">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFillValue"></a>
# setFillValue
setFillValue( double fillValue ) &rarr; void

Setter for property fillValue.

### Parameters:
fillValue - New value of property fillValue.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFillValue&unscoped_q=setFillValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLabel"></a>
# setLabel
setLabel( int i, String label ) &rarr; void

set the label (short, descriptive label for human consumption) 
 for the column, for rank 2 bundle datasets.

### Parameters:
i - the column number
<br>label - the label for the column

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLabel&unscoped_q=setLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setName"></a>
# setName
setName( int i, String name ) &rarr; void

set the name (valid Jython identifier) for the column.

### Parameters:
i - the column number
<br>name - the name (valid Jython identifier) for the column.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setName&unscoped_q=setName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setUnits"></a>
# setUnits
setUnits( Units u ) &rarr; void

set the units for the dataset.

### Parameters:
u - an Units

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUnits&unscoped_q=setUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

setUnits( int i, Units u ) &rarr; void<br>
***
<a name="setValidMax"></a>
# setValidMax
setValidMax( double validMax ) &rarr; void

set the valid max property.

### Parameters:
validMax - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setValidMax&unscoped_q=setValidMax">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setValidMin"></a>
# setValidMin
setValidMin( double validMin ) &rarr; void



### Parameters:
validMin - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setValidMin&unscoped_q=setValidMin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

