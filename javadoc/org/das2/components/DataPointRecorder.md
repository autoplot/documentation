# org.das2.components.DataPointRecorder

DataPointRecorder is a GUI for storing data points selected by the user.  
 The columns are set dynamically as the data arrives (via addDataPoint).
 
 This replaces DataPointRecorderNew.  (DataPointRecorderNew replaced an older 
 DataPointerRecorder whose name has been reclaimed.)

# DataPointRecorder( )
create a DataPointRecorder which will collect data such that X
 values are sorted and unique.

# DataPointRecorder( boolean sorted )
create a DataPointRecorder.  When sorted is true, the data point recorder will only allow
 one point per X value, and the data will be sorted as it is collected.  When it is 
 false, the data will be stored in the order it arrives.

***
<a name="addAccessory"></a>
# addAccessory
addAccessory( javax.swing.JComponent c ) &rarr; void

add a small component to the lower-right portion of the DataPointRecorder.  It should be roughly the size of a
 button.

### Parameters:
c - the component.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addAccessory&unscoped_q=addAccessory">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addDataPoint"></a>
# addDataPoint
addDataPoint( QDataSet ds ) &rarr; void

add a record, which should be a rank 1 bundle.

### Parameters:
ds - a QDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addDataPoint&unscoped_q=addDataPoint">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addDataPoint( Datum x, Datum y ) &rarr; void<br>
addDataPoint( double x, double y ) &rarr; void<br>
addDataPoint( double x, double y, java.util.Map planes ) &rarr; void<br>
addDataPoint( Datum x, Datum y, Object meta ) &rarr; void<br>
addDataPoint( Datum x, Datum y, java.util.Map planes ) &rarr; void<br>
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
<a name="addDataPoints"></a>
# addDataPoints
addDataPoints( QDataSet ds ) &rarr; void

append the rank 2 data.  The data should be rank 2, without DEPEND_0.
 Note earlier versions of this code assumed there would be a DEPEND_0.

### Parameters:
ds - rank 2 bundle dataset.

### Returns:
void (returns nothing)

### See Also:
<a href='#addDataPoint'>addDataPoint(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=addDataPoints&unscoped_q=addDataPoints">[search for examples]</a>
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
# <del>appendDataSet</del>
Deprecated: see #addDataPoints, which does not use DEPEND_0.
appendDataSet( org.das2.dataset.VectorDataSet ds ) &rarr; void<br>
***
<a name="createFramed"></a>
# createFramed
createFramed(  ) &rarr; DataPointRecorder



### Returns:
org.das2.components.DataPointRecorder


<a href="https://github.com/autoplot/dev/search?q=createFramed&unscoped_q=createFramed">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="dataPointSelected"></a>
# dataPointSelected
dataPointSelected( org.das2.event.DataPointSelectionEvent e ) &rarr; void



### Parameters:
e - a DataPointSelectionEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dataPointSelected&unscoped_q=dataPointSelected">[search for examples]</a>
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
<a name="getBundleDataSet"></a>
# <del>getBundleDataSet</del>
Deprecated: use getDataPoints.
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
<a name="getDataPoints"></a>
# getDataPoints
getDataPoints(  ) &rarr; QDataSet

returns a entire set of data points as a rank 2 bundle.
 This is the same as getBundleDataSet, and just calls it.

### Returns:
rank 2 bundle
### See Also:
<a href='#getSelectedDataPoints'>getSelectedDataPoints()</a> which returns the selected records.<br>
<a href='#getBundleDataSet'>getBundleDataSet()</a> which is the old name for this routine.<br>

<a href="https://github.com/autoplot/dev/search?q=getDataPoints&unscoped_q=getDataPoints">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSet"></a>
# <del>getDataSet</del>
Deprecated: see #getDataPoints
***
<a name="getSelectedDataPoints"></a>
# getSelectedDataPoints
getSelectedDataPoints(  ) &rarr; QDataSet

return the subset of the data points which are selected, as a rank 2 bundle.

### Returns:
rank 2 dataset
### See Also:
<a href='#getSelectedDataSet'>getSelectedDataSet()</a> which returns the selection in a different form<br>
<a href='#getDataPoints'>getDataPoints()</a> which returns all points.<br>

<a href="https://github.com/autoplot/dev/search?q=getSelectedDataPoints&unscoped_q=getSelectedDataPoints">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSelectedDataSet"></a>
# <del>getSelectedDataSet</del>
Deprecated: getSelectedDataPoints returns data as a simple bundle of x,y,...
***
<a name="getTimeFormat"></a>
# getTimeFormat
getTimeFormat(  ) &rarr; String

Get the value of timeFormat

### Returns:
the value of timeFormat

<a href="https://github.com/autoplot/dev/search?q=getTimeFormat&unscoped_q=getTimeFormat">[search for examples]</a>
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

load the file into the digitizer.  Columns will be created for the 
 each column of the file.  This should be able to read files created by
 the DataPointRecorder.
 
 Here's an example of a file which works:
 <pre><code>
 # Generated by Autoplot on Tue Nov 24 14:53:25 CST 2020
 x(UTC), y(Hz), BMag(nT), Fce(nT), Fci(nT), Fpe(nT), Fpe_Fce, Fuhr(Hz), Flhr(nT), F_L0(Hz), F_R0(Hz), N_e(cm!a-3!n), markedType, visualFeature, qualityIndex, comment
 2017-03-27T09:30:22.378Z, 3466.8, 1.72870E5, 4.84030E6, 2636.3, 96486.0, 0.019934, 4.84120E6, 3466.8, 4558.9, 4.84220E6, 115.44, Flhr, peak, f, v20200213x
 2017-03-27T09:30:23.634Z, 3515.6, 1.72730E5, 4.83650E6, 2634.3, 99779.0, 0.02063, 4.83750E6, 3515.6, 4691.9, 4.83860E6, 123.46, Flhr, peak, f, v20200213x
 2017-03-27T09:30:24.889Z, 3515.6, 1.72620E5, 4.83340E6, 2632.5, 99862.0, 0.020661, 4.83440E6, 3515.6, 4694.9, 4.83540E6, 123.67, Flhr, peak, f, v20200213
 </code></pre>

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



### Parameters:
file - a File

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=saveToFile&unscoped_q=saveToFile">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="select"></a>
# select
select( DatumRange xrange, DatumRange yrange ) &rarr; int

Selects all the points in the GUI where the first column is within xrange and
 the second column is within yrange.  Returns the first of the selected 
 indices, or -1 if no elements are found.

### Parameters:
xrange - the range constraint (non-null).
<br>yrange - the range constraint  or null if no constraint.

### Returns:
the first of the selected indices, or -1 if no elements are found.
### See Also:
<a href='#getSelectedDataSet'>getSelectedDataSet()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=select&unscoped_q=select">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

select( DatumRange xrange, DatumRange yrange, boolean xOrY ) &rarr; int<br>
select( java.util.List selection ) &rarr; void<br>
***
<a name="setActive"></a>
# setActive
setActive( boolean active ) &rarr; void

active=true means fire off events on any change.  false= wait for update button.

### Parameters:
active - true means fire off events on any change

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
<a name="setTimeFormat"></a>
# setTimeFormat
setTimeFormat( String timeFormat ) &rarr; void

Set the value of timeFormat

### Parameters:
timeFormat - new value of timeFormat

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTimeFormat&unscoped_q=setTimeFormat">[search for examples]</a>
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

