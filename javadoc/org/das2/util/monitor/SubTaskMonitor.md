# org.das2.util.monitor.SubTaskMonitorcreates a ProgressMonitor that maps its progress to a parent's progress.
 For example, if a process takes a progress monitor, but is implemented in
 two steps that each take a progress monitor, then two subtask monitors can
 be created to monitor each step, and the client who passed in the monitor 
 will see the whole deal as one process.

 Note we would often abuse monitors, handing them off to several processes
 that would each take the monitor through its lifecycle.  Now we require the
 lifecycle be performed once, so that machines can use the monitors to monitor
 processes.  In this case, SubTaskMonitors should be used, and getSubtaskMonitor
 was added.  Note too that this class should not be called directly, because
 getSubtaskMonitor allows the source class to return a monitor of its own design.
***
<a name="canBeCancelled"></a>
# canBeCancelled
canBeCancelled(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=canBeCancelled&unscoped_q=canBeCancelled">[search for examples]</a>

***
<a name="cancel"></a>
# cancel
cancel(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=cancel&unscoped_q=cancel">[search for examples]</a>

***
<a name="create"></a>
# create
create( ProgressMonitor parent, long min, long max ) &rarr; SubTaskMonitor

create the subtask monitor.

### Parameters:
parent - parent monitor
<br>min - minium
<br>max - maximum

### Returns:
SubTaskMonitor

<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

create( ProgressMonitor parent, long min, long max, boolean cancelChecked ) &rarr; SubTaskMonitor<br>
create( ProgressMonitor parent, boolean cancelChecked ) &rarr; SubTaskMonitor<br>
***
<a name="finished"></a>
# finished
finished(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=finished&unscoped_q=finished">[search for examples]</a>

***
<a name="getLabel"></a>
# getLabel
getLabel(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getLabel&unscoped_q=getLabel">[search for examples]</a>

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

getSubtaskMonitor( String label ) &rarr; ProgressMonitor<br>
***
<a name="getTaskProgress"></a>
# getTaskProgress
getTaskProgress(  ) &rarr; long



### Returns:
long


<a href="https://github.com/autoplot/dev/search?q=getTaskProgress&unscoped_q=getTaskProgress">[search for examples]</a>

***
<a name="getTaskSize"></a>
# getTaskSize
getTaskSize(  ) &rarr; long



### Returns:
long


<a href="https://github.com/autoplot/dev/search?q=getTaskSize&unscoped_q=getTaskSize">[search for examples]</a>

***
<a name="isCancelled"></a>
# isCancelled
isCancelled(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isCancelled&unscoped_q=isCancelled">[search for examples]</a>

***
<a name="isFinished"></a>
# isFinished
isFinished(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isFinished&unscoped_q=isFinished">[search for examples]</a>

***
<a name="isStarted"></a>
# isStarted
isStarted(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isStarted&unscoped_q=isStarted">[search for examples]</a>

***
<a name="setAdditionalInfo"></a>
# setAdditionalInfo
setAdditionalInfo( String s ) &rarr; void



### Parameters:
s - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAdditionalInfo&unscoped_q=setAdditionalInfo">[search for examples]</a>

***
<a name="setLabel"></a>
# setLabel
setLabel( String label ) &rarr; void



### Parameters:
label - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLabel&unscoped_q=setLabel">[search for examples]</a>

***
<a name="setProgressMessage"></a>
# setProgressMessage
setProgressMessage( String message ) &rarr; void

these messages are lost, unless doEchoToParent is set.

### Parameters:
message - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setProgressMessage&unscoped_q=setProgressMessage">[search for examples]</a>

***
<a name="setTaskProgress"></a>
# setTaskProgress
setTaskProgress( long position ) &rarr; void



### Parameters:
position - a long

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTaskProgress&unscoped_q=setTaskProgress">[search for examples]</a>

***
<a name="setTaskSize"></a>
# setTaskSize
setTaskSize( long taskSize ) &rarr; void



### Parameters:
taskSize - a long

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTaskSize&unscoped_q=setTaskSize">[search for examples]</a>

***
<a name="started"></a>
# started
started(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=started&unscoped_q=started">[search for examples]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

