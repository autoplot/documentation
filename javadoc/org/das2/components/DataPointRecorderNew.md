# org.das2.components.DataPointRecorderNew

DataPointRecorderNew is a GUI for storing data points selected by the user.  
 This is the old recorder but:
 1. uses QDataSet to handle the data.  No more strange internal object.
 2. allows the columns to be declared explicitly by code, and data is merged in by name.

# DataPointRecorderNew( )
Creates a new instance of DataPointRecorder

***
<a name="addDataPoint"></a>
# addDataPoint
addDataPoint( Datum x, Datum y ) &rarr; void

add just the x and y values.

### Parameters:
x - the x position
<br>y - the y position

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addDataPoint&unscoped_q=addDataPoint">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addDataPoint( Datum x, Datum y, Object meta ) &rarr; void<br>
addDataPoint( Datum x, Datum y, java.util.Map planes ) &rarr; void<br>
addDataPoint( QDataSet rec ) &rarr; void<br>
***
<a name="addDataPointSelectionListener"></a>
# addDataPointSelectionListener
addDataPointSelectionListener( org.das2.event.DataPointSelectionListener listener ) &rarr; void

Registers DataPointSelectionListener to receive events.

### Parameters:
listener - The listener to register.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addDataPointSelectionListener&unscoped_q=addDataPointSelectionListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addDataSetUpdateListener"></a>
# addDataSetUpdateListener
addDataSetUpdateListener( org.das2.dataset.DataSetUpdateListener listener ) &rarr; void



### Parameters:
listener - a DataSetUpdateListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addDataSetUpdateListener&unscoped_q=addDataSetUpdateListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addSelectedDataSetUpdateListener"></a>
# addSelectedDataSetUpdateListener
addSelectedDataSetUpdateListener( org.das2.dataset.DataSetUpdateListener listener ) &rarr; void



### Parameters:
listener - a DataSetUpdateListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addSelectedDataSetUpdateListener&unscoped_q=addSelectedDataSetUpdateListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="appendDataSet"></a>
# appendDataSet
appendDataSet( org.das2.dataset.VectorDataSet ds ) &rarr; void



### Parameters:
ds - a VectorDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=appendDataSet&unscoped_q=appendDataSet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createFramed"></a>
# createFramed
createFramed(  ) &rarr; DataPointRecorderNew



### Returns:
org.das2.components.DataPointRecorderNew


<a href="https://github.com/autoplot/dev/search?q=createFramed&unscoped_q=createFramed">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="deleteInterval"></a>
# deleteInterval
deleteInterval( DatumRange range ) &rarr; void

delete all the points within the interval.  This was introduced to support the
 case where we are going to reprocess an interval, as with the  
 RBSP digitizer.

### Parameters:
range - range to delete, end time is exclusive.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=deleteInterval&unscoped_q=deleteInterval">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="deleteRow"></a>
# deleteRow
deleteRow( int row ) &rarr; void

delete the specified row.

### Parameters:
row - the row, where zero is the first element.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=deleteRow&unscoped_q=deleteRow">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="deleteRows"></a>
# deleteRows
deleteRows( int[] selectedRows ) &rarr; void

delete the specified rows.

### Parameters:
selectedRows - the rows, where zero is the first element..

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=deleteRows&unscoped_q=deleteRows">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getAppendDataSetUpListener"></a>
# getAppendDataSetUpListener
getAppendDataSetUpListener(  ) &rarr; DataSetUpdateListener

this adds all the points in the DataSet to the list.  This will also check the dataset for the special
 property "comment" and add it as a comment.

### Returns:
the listener to receive data set updates
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/dataset/DataSetUpdateEvent.md'>org.das2.dataset.DataSetUpdateEvent</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getAppendDataSetUpListener&unscoped_q=getAppendDataSetUpListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCurrentFile"></a>
# getCurrentFile
getCurrentFile(  ) &rarr; File

shows the current name for the file.

### Returns:
the current name for the file.

<a href="https://github.com/autoplot/dev/search?q=getCurrentFile&unscoped_q=getCurrentFile">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSet"></a>
# getDataSet
getDataSet(  ) &rarr; QDataSet

returns a data set of the table data.

### Returns:
a data set of the table data.

<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSelectedDataSet"></a>
# getSelectedDataSet
getSelectedDataSet(  ) &rarr; QDataSet

returns a data set of the selected table data.  Warning: this used to
 return a bundle dataset with Y,plane1,plane2,etc that had DEPEND_0 for X.
 This now returns a bundle ds[n,m] where m is the number of columns and
 n is the number of records.

### Returns:
a data set of the selected table data.
### See Also:
<a href='#select'>select(org.das2.datum.DatumRange, org.das2.datum.DatumRange)</a> which selects part of the dataset.<br>

<a href="https://github.com/autoplot/dev/search?q=getSelectedDataSet&unscoped_q=getSelectedDataSet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getXTagWidth"></a>
# getXTagWidth
getXTagWidth(  ) &rarr; Datum

Getter for property xTagWidth.  When xTagWidth is zero,
 this implies there is no binning.

### Returns:
Value of property xTagWidth.

<a href="https://github.com/autoplot/dev/search?q=getXTagWidth&unscoped_q=getXTagWidth">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isModified"></a>
# isModified
isModified(  ) &rarr; boolean

return true when the data point recorder has been modified.

### Returns:
true when the data point recorder has been modified.

<a href="https://github.com/autoplot/dev/search?q=isModified&unscoped_q=isModified">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isSnapToGrid"></a>
# isSnapToGrid
isSnapToGrid(  ) &rarr; boolean

Getter for property snapToGrid.

### Returns:
Value of property snapToGrid.

<a href="https://github.com/autoplot/dev/search?q=isSnapToGrid&unscoped_q=isSnapToGrid">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isSorted"></a>
# isSorted
isSorted(  ) &rarr; boolean

Getter for property sorted.

### Returns:
Value of property sorted.

<a href="https://github.com/autoplot/dev/search?q=isSorted&unscoped_q=isSorted">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="loadFromFile"></a>
# loadFromFile
loadFromFile( java.io.File file ) &rarr; void

load the dataset from the file.  
 TODO: this should be redone.

### Parameters:
file - a File

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=loadFromFile&unscoped_q=loadFromFile">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeDataPointSelectionListener"></a>
# removeDataPointSelectionListener
removeDataPointSelectionListener( org.das2.event.DataPointSelectionListener listener ) &rarr; void

Removes DataPointSelectionListener from the list of listeners.

### Parameters:
listener - The listener to remove.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeDataPointSelectionListener&unscoped_q=removeDataPointSelectionListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeDataSetUpdateListener"></a>
# removeDataSetUpdateListener
removeDataSetUpdateListener( org.das2.dataset.DataSetUpdateListener listener ) &rarr; void



### Parameters:
listener - a DataSetUpdateListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeDataSetUpdateListener&unscoped_q=removeDataSetUpdateListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeSelectedDataSetUpdateListener"></a>
# removeSelectedDataSetUpdateListener
removeSelectedDataSetUpdateListener( org.das2.dataset.DataSetUpdateListener listener ) &rarr; void



### Parameters:
listener - a DataSetUpdateListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeSelectedDataSetUpdateListener&unscoped_q=removeSelectedDataSetUpdateListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="save"></a>
# save
save(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=save&unscoped_q=save">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="saveAs"></a>
# saveAs
saveAs(  ) &rarr; boolean

return true if the file was saved, false if cancel

### Returns:
true if the file was saved, false if cancel

<a href="https://github.com/autoplot/dev/search?q=saveAs&unscoped_q=saveAs">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="saveBeforeExit"></a>
# saveBeforeExit
saveBeforeExit(  ) &rarr; boolean

return true if the file was saved or "don't save" was pressed by the user.

### Returns:
true if the file was saved or "don't save" was pressed by the user.

<a href="https://github.com/autoplot/dev/search?q=saveBeforeExit&unscoped_q=saveBeforeExit">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="saveToFile"></a>
# saveToFile
saveToFile( java.io.File file ) &rarr; void

This should be called off the event thread.

### Parameters:
file - a File

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=saveToFile&unscoped_q=saveToFile">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="select"></a>
# select
select( DatumRange xrange, DatumRange yrange ) &rarr; void

Selects all the points where the first column is within xrange and
 the second column is within yrange.

### Parameters:
xrange - the range constraint (non-null).
<br>yrange - the range constraint (non-null).
 return the selected index, or -1 if no elements are found.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=select&unscoped_q=select">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setActive"></a>
# setActive
setActive( boolean active ) &rarr; void

active=true means fire off events on any change.  false= wait for update button.

### Parameters:
active - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setActive&unscoped_q=setActive">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setColumn"></a>
# setColumn
setColumn( int i, String name, Units units, Datum deft ) &rarr; void

identify the name and unit for each column.

### Parameters:
i - the column number
<br>name - a Java identifier for the column, e.g. "StartTime"
<br>units - units for the column, or null for dimensionless.
<br>deft - default value to use when data is not provided.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setColumn&unscoped_q=setColumn">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

setColumn( int i, String name, Units units, String deft ) &rarr; void<br>
setColumn( int i, String name, Units units, double deft ) &rarr; void<br>
***
<a name="setColumnCount"></a>
# setColumnCount
setColumnCount( int count ) &rarr; void

explicitly declare the number of columns.  Call this and then 
 setColumn to define each column.

### Parameters:
count - the number of columns.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setColumnCount&unscoped_q=setColumnCount">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSnapToGrid"></a>
# setSnapToGrid
setSnapToGrid( boolean snapToGrid ) &rarr; void

Setter for property snapToGrid.  true indicates the xtag will be reset
 so that the tags are equally spaced, each xTagWidth apart.

### Parameters:
snapToGrid - New value of property snapToGrid.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSnapToGrid&unscoped_q=setSnapToGrid">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSorted"></a>
# setSorted
setSorted( boolean sorted ) &rarr; void

Setter for property sorted.

### Parameters:
sorted - New value of property sorted.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSorted&unscoped_q=setSorted">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setXTagWidth"></a>
# setXTagWidth
setXTagWidth( Datum xTagWidth ) &rarr; void

bins for the data, when xTagWidth is non-zero.

### Parameters:
xTagWidth - New value of property xTagWidth.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setXTagWidth&unscoped_q=setXTagWidth">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="update"></a>
# update
update(  ) &rarr; void

Notify listeners that the dataset has updated.  Pressing the "Update" 
 button calls this.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=update&unscoped_q=update">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

