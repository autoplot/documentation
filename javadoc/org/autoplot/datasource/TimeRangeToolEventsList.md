# org.autoplot.datasource.TimeRangeToolEventsList

The EventsList tool makes it easy to browse around a list of events.  It
 takes a URI for a dataset which can be represented as an events list, 
 and fires off timeRangeSelection events when an event is selected.

# TimeRangeToolEventsList( )
Creates new form TimeRangeToolEventsList

***
<a name="addDataRangeSelectionListener"></a>
# addDataRangeSelectionListener
addDataRangeSelectionListener( org.das2.event.DataRangeSelectionListener listener ) &rarr; void

Registers DataRangeSelectionListener to receive events.

### Parameters:
listener - The listener to register.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addDataRangeSelectionListener&unscoped_q=addDataRangeSelectionListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSetSelector"></a>
# getDataSetSelector
getDataSetSelector(  ) &rarr; DataSetSelector

return the dataSetSelector, so that for example a button for bookmarks 
 can be added by clients that know about bookmarks.

### Returns:
the DataSetSelector component.

<a href="https://github.com/autoplot/dev/search?q=getDataSetSelector&unscoped_q=getDataSetSelector">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="makeCanonical"></a>
# makeCanonical
makeCanonical( QDataSet vds ) &rarr; QDataSet

make canonical rank 2 bundle dataset of min,max,color,text

### Parameters:
vds - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=makeCanonical&unscoped_q=makeCanonical">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeDataRangeSelectionListener"></a>
# removeDataRangeSelectionListener
removeDataRangeSelectionListener( org.das2.event.DataRangeSelectionListener listener ) &rarr; void

Removes DataRangeSelectionListener from the list of listeners.

### Parameters:
listener - The listener to remove.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeDataRangeSelectionListener&unscoped_q=removeDataRangeSelectionListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

