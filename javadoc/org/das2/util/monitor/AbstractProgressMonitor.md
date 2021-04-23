# org.das2.util.monitor.AbstractProgressMonitorThis is a progress monitor to use when we don't care about the progress,
 this doesn't provide a view of the progress to the client.

 Further, this can act as a base class for other monitor types.
AbstractProgressMonitor( )


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
<a name="finished"></a>
# finished
finished(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=finished&unscoped_q=finished">[search for examples]</a>

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
<a name="getProgressMessage"></a>
# getProgressMessage
getProgressMessage(  ) &rarr; String

provide access to the last progress message setting.

### Returns:
the last progress message setting.

<a href="https://github.com/autoplot/dev/search?q=getProgressMessage&unscoped_q=getProgressMessage">[search for examples]</a>

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
<a name="setLabel"></a>
# setLabel
setLabel( String s ) &rarr; void



### Parameters:
s - a String

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

return a human-readable representation of the monitor, which is
 currently position + "of" + taskSize.

### Returns:
return a human-readable representation of the monitor

<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

