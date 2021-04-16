# org.das2.event.CutoffMouseModule
CutoffMouseModule( org.das2.graph.DasPlot parent, org.das2.dataset.DataSetConsumer consumer )


***
<a name="addDataSetUpdateListener"></a>
# addDataSetUpdateListener
addDataSetUpdateListener( org.das2.dataset.DataSetUpdateListener listener ) &rarr; void



### Parameters:
listener - a DataSetUpdateListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addDataSetUpdateListener&unscoped_q=addDataSetUpdateListener">[search for examples]</a>

***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void

Registers PropertyChangeListener to receive events.

### Parameters:
listener - The listener to register.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

***
<a name="cutoff"></a>
# cutoff
cutoff( QDataSet ds, Datum slopeMin, int nave, int mult, Datum levelMin ) &rarr; int

slopeMin in the y units of ds.
 levelMin in the y units of ds.
 mult=-1 high cutoff, =1 low cutoff

### Parameters:
ds - a QDataSet
<br>slopeMin - a Datum
<br>nave - an int
<br>mult - an int
<br>levelMin - a Datum

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=cutoff&unscoped_q=cutoff">[search for examples]</a>

***
<a name="getLevelMin"></a>
# getLevelMin
getLevelMin(  ) &rarr; Datum

Getter for property levelMin.

### Returns:
Value of property levelMin.

<a href="https://github.com/autoplot/dev/search?q=getLevelMin&unscoped_q=getLevelMin">[search for examples]</a>

***
<a name="getNave"></a>
# getNave
getNave(  ) &rarr; int

Getter for property nave.

### Returns:
Value of property nave.

<a href="https://github.com/autoplot/dev/search?q=getNave&unscoped_q=getNave">[search for examples]</a>

***
<a name="getSlicer"></a>
# getSlicer
getSlicer( org.das2.graph.DasPlot plot, org.das2.dataset.TableDataSetConsumer consumer ) &rarr; DataPointSelectionListener



### Parameters:
plot - a DasPlot
<br>consumer - a TableDataSetConsumer

### Returns:
org.das2.event.DataPointSelectionListener


<a href="https://github.com/autoplot/dev/search?q=getSlicer&unscoped_q=getSlicer">[search for examples]</a>

***
<a name="getSlopeMin"></a>
# getSlopeMin
getSlopeMin(  ) &rarr; Datum

Getter for property slopeMin.

### Returns:
Value of property slopeMin.

<a href="https://github.com/autoplot/dev/search?q=getSlopeMin&unscoped_q=getSlopeMin">[search for examples]</a>

***
<a name="getXResolution"></a>
# getXResolution
getXResolution(  ) &rarr; Datum



### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getXResolution&unscoped_q=getXResolution">[search for examples]</a>

***
<a name="isLowCutoff"></a>
# isLowCutoff
isLowCutoff(  ) &rarr; boolean

Getter for property lowCutoff.

### Returns:
Value of property lowCutoff.

<a href="https://github.com/autoplot/dev/search?q=isLowCutoff&unscoped_q=isLowCutoff">[search for examples]</a>

***
<a name="removeDataSetUpdateListener"></a>
# removeDataSetUpdateListener
removeDataSetUpdateListener( org.das2.dataset.DataSetUpdateListener listener ) &rarr; void



### Parameters:
listener - a DataSetUpdateListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeDataSetUpdateListener&unscoped_q=removeDataSetUpdateListener">[search for examples]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void

Removes PropertyChangeListener from the list of listeners.

### Parameters:
listener - The listener to remove.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

***
<a name="setLevelMin"></a>
# setLevelMin
setLevelMin( Datum levelMin ) &rarr; void

Setter for property levelMin.

### Parameters:
levelMin - New value of property levelMin.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLevelMin&unscoped_q=setLevelMin">[search for examples]</a>

***
<a name="setLowCutoff"></a>
# setLowCutoff
setLowCutoff( boolean lowCutoff ) &rarr; void

Setter for property lowCutoff.

### Parameters:
lowCutoff - New value of property lowCutoff.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLowCutoff&unscoped_q=setLowCutoff">[search for examples]</a>

***
<a name="setNave"></a>
# setNave
setNave( int nave ) &rarr; void

Setter for property nave.

### Parameters:
nave - New value of property nave.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setNave&unscoped_q=setNave">[search for examples]</a>

***
<a name="setSlopeMin"></a>
# setSlopeMin
setSlopeMin( Datum slopeMin ) &rarr; void

Setter for property slopeMin.

### Parameters:
slopeMin - New value of property slopeMin.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSlopeMin&unscoped_q=setSlopeMin">[search for examples]</a>

***
<a name="setXResolution"></a>
# setXResolution
setXResolution( Datum xResolution ) &rarr; void



### Parameters:
xResolution - a Datum

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setXResolution&unscoped_q=setXResolution">[search for examples]</a>

