# org.das2.components.BatchMasterBatchMaster is a object that runs through a batch file, controlling a time axis to produce a series of images.
BatchMaster( org.das2.graph.DasCanvas canvas )
Creates a new instance of BatchMaster

***
<a name="timer"></a>
# timer



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

***
<a name="createPngs"></a>
# createPngs
createPngs( org.das2.graph.DasCanvas canvas, java.io.File specFile, String pngFilenameTemplate ) &rarr; BatchMaster

create the pngwalk using the class.

### Parameters:
canvas - the source for images
<br>specFile - flat text file containing one parsable time range per line. (For example, "1990-01-01T00:00 1990-01-02T00:00" or "1990-01-01")
<br>pngFilenameTemplate - (For example, "BEGIN_END.png")

### Returns:
BatchMaster object.

<a href="https://github.com/autoplot/dev/search?q=createPngs&unscoped_q=createPngs">[search for examples]</a>

***
<a name="createPngsTaskOutputDescriptor"></a>
# createPngsTaskOutputDescriptor
createPngsTaskOutputDescriptor( String pngFilenameTemplate ) &rarr; TaskOutputDescriptor



### Parameters:
pngFilenameTemplate - BEGIN,END,RANGE substituted to form name

### Returns:
TaskOutputDescriptor describing the task.

<a href="https://github.com/autoplot/dev/search?q=createPngsTaskOutputDescriptor&unscoped_q=createPngsTaskOutputDescriptor">[search for examples]</a>

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

***
<a name="start"></a>
# start
start(  ) &rarr; void

Starts the batch process.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=start&unscoped_q=start">[search for examples]</a>

