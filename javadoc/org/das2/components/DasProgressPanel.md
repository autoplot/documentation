# org.das2.components.DasProgressPanel

ProgressMonitor component used throughout das2.

 Here's an Autoplot script demoing its operation:
<blockquote><pre>{@code
monitor.setTaskSize( 100 )
monitor.started()

for i in range(100):
  if ( i>50 and monitor.isCancelled() ):
    raise Exception('cancel pressed')
  print i
  java.lang.Thread.sleep(100)
  monitor.setTaskProgress(i)

monitor.finished()
}</pre></blockquote>

***
<a name="MSG_CANCEL_TASK"></a>
# MSG_CANCEL_TASK



***
<a name="MSG_TASK_CANNOT_BE_CANCELED"></a>
# MSG_TASK_CANNOT_BE_CANCELED



***
<a name="PROP_STARTED"></a>
# PROP_STARTED



***
<a name="PROP_FINISHED"></a>
# PROP_FINISHED



***
<a name="PROP_CANCELLED"></a>
# PROP_CANCELLED

true if the task is cancelled.  Note cancelled will be set
 before finished.

***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addPropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="canBeCancelled"></a>
# canBeCancelled
canBeCancelled(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=canBeCancelled&unscoped_q=canBeCancelled">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="cancel"></a>
# cancel
cancel(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=cancel&unscoped_q=cancel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createComponent"></a>
# createComponent
createComponent( String label ) &rarr; DasProgressPanel

return a progress panel which can be embedded within a GUI.  Use 
 getComponent() to return the component which should be embedded.

### Parameters:
label - string label for the label.

### Returns:
a new DasProgressPanel
### See Also:
<a href='#getComponent'>getComponent()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=createComponent&unscoped_q=createComponent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createComponentPanel"></a>
# createComponentPanel
createComponentPanel( org.das2.graph.DasCanvasComponent component, String initialMessage ) &rarr; DasProgressPanel

return a new progress panel with component indicating status for the component.

### Parameters:
component - the canvas component providing a context for the progress, for example a DasPlot which will load some data.
<br>initialMessage - initial message for the monitor

### Returns:
the new component

<a href="https://github.com/autoplot/dev/search?q=createComponentPanel&unscoped_q=createComponentPanel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

createComponentPanel( org.das2.graph.DasCanvas canvas, String initialMessage ) &rarr; DasProgressPanel<br>
***
<a name="createFramed"></a>
# createFramed
createFramed( String label ) &rarr; DasProgressPanel

this may be called from off the event thread, but it does assume that the
 event thread is free.

### Parameters:
label - label describing the task.

### Returns:
a DasProgressPanel.

<a href="https://github.com/autoplot/dev/search?q=createFramed&unscoped_q=createFramed">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

createFramed( java.awt.Window parent, String label ) &rarr; DasProgressPanel<br>
***
<a name="finished"></a>
# finished
finished(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=finished&unscoped_q=finished">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getComponent"></a>
# getComponent
getComponent(  ) &rarr; Component

returns the JPanel component.

### Returns:
the JPanel component.

<a href="https://github.com/autoplot/dev/search?q=getComponent&unscoped_q=getComponent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getConsumer"></a>
# getConsumer
getConsumer(  ) &rarr; Exception



### Returns:
java.lang.Exception


<a href="https://github.com/autoplot/dev/search?q=getConsumer&unscoped_q=getConsumer">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLabel"></a>
# getLabel
getLabel(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getLabel&unscoped_q=getLabel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSource"></a>
# getSource
getSource(  ) &rarr; Exception



### Returns:
java.lang.Exception


<a href="https://github.com/autoplot/dev/search?q=getSource&unscoped_q=getSource">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSubtaskMonitor"></a>
# getSubtaskMonitor
getSubtaskMonitor( int start, int end, String label ) &rarr; ProgressMonitor



### Parameters:
start - an int
<br>end - an int
<br>label - a String

### Returns:
org.das2.util.monitor.ProgressMonitor


<a href="https://github.com/autoplot/dev/search?q=getSubtaskMonitor&unscoped_q=getSubtaskMonitor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getSubtaskMonitor( String label ) &rarr; ProgressMonitor<br>
***
<a name="getTaskProgress"></a>
# getTaskProgress
getTaskProgress(  ) &rarr; long



### Returns:
long


<a href="https://github.com/autoplot/dev/search?q=getTaskProgress&unscoped_q=getTaskProgress">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTaskSize"></a>
# getTaskSize
getTaskSize(  ) &rarr; long



### Returns:
long


<a href="https://github.com/autoplot/dev/search?q=getTaskSize&unscoped_q=getTaskSize">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isCancelled"></a>
# isCancelled
isCancelled(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isCancelled&unscoped_q=isCancelled">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isFinished"></a>
# isFinished
isFinished(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isFinished&unscoped_q=isFinished">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isStarted"></a>
# isStarted
isStarted(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isStarted&unscoped_q=isStarted">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isValidateRoot"></a>
# isValidateRoot
isValidateRoot(  ) &rarr; boolean

Returning true here keeps the progress bar from forcing the whole canvas
 to repaint when the label of the progress bar changes.

### Returns:
this always returns true

<a href="https://github.com/autoplot/dev/search?q=isValidateRoot&unscoped_q=isValidateRoot">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isVisible"></a>
# isVisible
isVisible(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isVisible&unscoped_q=isVisible">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="maybeCenter"></a>
# maybeCenter
maybeCenter( ProgressMonitor mon, java.awt.Component window ) &rarr; void

provide convenient code which will center DasProgressMonitors on window.

### Parameters:
mon - the monitor, which may be a DasProgressPanel.
<br>window - the component about which to center the monitor.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=maybeCenter&unscoped_q=maybeCenter">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

removePropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="setAdditionalInfo"></a>
# setAdditionalInfo
setAdditionalInfo( String s ) &rarr; void



### Parameters:
s - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAdditionalInfo&unscoped_q=setAdditionalInfo">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setContextComponent"></a>
# setContextComponent
setContextComponent( java.awt.Component window ) &rarr; void

set the component where this progress monitor is understood.  This
 is typically the DasCanvas.

### Parameters:
window - a Component

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setContextComponent&unscoped_q=setContextComponent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLabel"></a>
# setLabel
setLabel( String label ) &rarr; void



### Parameters:
label - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLabel&unscoped_q=setLabel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setProgressMessage"></a>
# setProgressMessage
setProgressMessage( String message ) &rarr; void



### Parameters:
message - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setProgressMessage&unscoped_q=setProgressMessage">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setShowProgressRate"></a>
# setShowProgressRate
setShowProgressRate( boolean showProgressRate ) &rarr; void

Setter for property showProgressRate.

### Parameters:
showProgressRate - New value of property showProgressRate.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setShowProgressRate&unscoped_q=setShowProgressRate">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTaskProgress"></a>
# setTaskProgress
setTaskProgress( long position ) &rarr; void



### Parameters:
position - a long

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTaskProgress&unscoped_q=setTaskProgress">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTaskSize"></a>
# setTaskSize
setTaskSize( long taskSize ) &rarr; void



### Parameters:
taskSize - a long

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTaskSize&unscoped_q=setTaskSize">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setVisible"></a>
# setVisible
setVisible( boolean visible ) &rarr; void

make the progressPanel visible or hide it.  This

### Parameters:
visible - true if the progressPanel should be visible.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setVisible&unscoped_q=setVisible">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="started"></a>
# started
started(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=started&unscoped_q=started">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

