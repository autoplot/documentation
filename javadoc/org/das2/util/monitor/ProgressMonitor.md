# org.das2.util.monitor.ProgressMonitor<code>ProgressMonitor</code> defines a set of methods that are useful for
 keeping track of the progress of an operation.  This interface also allows
 the operation being tracked to be notified if the user wishes to cancel the
 operation.  Code using this interface to track progress should call
 {@link #isCancelled()} prior to calling {@link #setTaskProgress(long)}.
 Implementations of this interface should throw an
 <code>IllegalArgumentException</code> when <code>setTaskProgress(int)</code>
 is called after the operation has been cancelled.
 <p>
 Code using the <code>ProgressMonitor</code> should call {@link #started()}
 before <code>setTaskProgress(long)</code> is called for the first time.
 <code>setTaskProgress()</code> should not be called after
 <code>cancel()</code> or <code>finished()</code> has been called.  Therefore,
 monitored processes should check isCancelled() before setTaskProgress(long)
 is called.  An
 implementation may throw an <code>IllegalArgumentException</code> if
 <code>setTaskProgress(int)</code> is called before <code>started()</code> or
 after <code>finished()</code> is called.  Note if isCancelled is not called
 by the process, then the cancel button will become disabled.

 <p>TODO: consider allowing the client to specify that an unchecked exception is 
 allowed, and he can then catch the exception.  
 1. The caller knows that the service provider's work can be ignored, and this would work.
 2. The service provider knows that the service must be cleaned up with a try/finally block.
 Should CancelledOperationException be a an unchecked exception?
 See https://bugs-pw.physics.uiowa.edu/mantis/view.php?id=457
 </p>
 
 <p>A client codes receiving a monitor must do one of two things.
 It should either call setTaskSize(long), started(), setTaskProgress(long) zero or more times, then
 finished(); or it should do nothing with the monitor, possibly passing the
 monitor to a subprocess.  This is to ensure that it's easy to see that
 the monitor lifecycle is properly performed. </p>
***
<a name="SIZE_INDETERMINATE"></a>
# SIZE_INDETERMINATE



***
<a name="canBeCancelled"></a>
# canBeCancelled
canBeCancelled(  ) &rarr; boolean

return true if the process appears to support cancel.  Many
 processes use a monitor to provide status feedback, but do not check
 if the human operator has pressed cancel.

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=canBeCancelled&unscoped_q=canBeCancelled">[search for examples]</a>

***
<a name="cancel"></a>
# cancel
cancel(  ) &rarr; void

Notifies the <code>ProgressMonitor</code> that the task
 being monitored should be canceled.  After this method is
 called, implementations should return <code>true</code> on
 any subsequent calls to {@link #isCancelled()} and should
 throw an IllegalStateException on any subsequent calls to
 {@link #setTaskProgress(long)}.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=cancel&unscoped_q=cancel">[search for examples]</a>

***
<a name="finished"></a>
# finished
finished(  ) &rarr; void

Notifies the <code>ProgressMonitor</code> that the task
 being monitored has finished.  This must only be called once, and note that isFinished() must return
 the state of this monitor.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=finished&unscoped_q=finished">[search for examples]</a>

***
<a name="getLabel"></a>
# getLabel
getLabel(  ) &rarr; String

Return the label string displayed, which is a concise string that 
 describes the task being performed.  This is primarily to aid in debugging,
 and this method need not return the string set by setLabel.

### Returns:
the label.

<a href="https://github.com/autoplot/dev/search?q=getLabel&unscoped_q=getLabel">[search for examples]</a>

***
<a name="getSubtaskMonitor"></a>
# getSubtaskMonitor
getSubtaskMonitor( int start, int end, String label ) &rarr; ProgressMonitor

return a monitor to use for a subtask.  This is provided mostly as
 a convenience.  setTaskProgress calls to the subtask monitor are mapped to
 this monitor.  A label can also be specified for the subtask to improve
 user experience.
 
 If the parent process is not supporting cancel, then subprocesses cannot support cancel.

### Parameters:
start - start position on this monitor.
<br>end - end position on this monitor (exclusive).
<br>label - a label for the subtask, often this is handled as progress message; or null.

### Returns:
a new progress monitor.  (generally type SubTaskMonitor)

<a href="https://github.com/autoplot/dev/search?q=getSubtaskMonitor&unscoped_q=getSubtaskMonitor">[search for examples]</a>

getSubtaskMonitor( String label ) &rarr; ProgressMonitor<br>
***
<a name="getTaskProgress"></a>
# getTaskProgress
getTaskProgress(  ) &rarr; long

Returns the current progress of the monitored task.

### Returns:
the current progress of the monitored task.

<a href="https://github.com/autoplot/dev/search?q=getTaskProgress&unscoped_q=getTaskProgress">[search for examples]</a>

***
<a name="getTaskSize"></a>
# getTaskSize
getTaskSize(  ) &rarr; long

Return the size of the task.  The units are arbitrary

### Returns:
the size of the task.

<a href="https://github.com/autoplot/dev/search?q=getTaskSize&unscoped_q=getTaskSize">[search for examples]</a>

***
<a name="isCancelled"></a>
# isCancelled
isCancelled(  ) &rarr; boolean

Returns <code>true</code> if the operation being tracked
 should be cancelled.  For example, the human operator has pressed
 the cancel button indicating that the process should be stopped.  Note
 that if the process is not checking the cancel status, the cancel button
 should be disabled.

### Returns:
<code>true</code> if the operation being tracked
 should be cancelled.

<a href="https://github.com/autoplot/dev/search?q=isCancelled&unscoped_q=isCancelled">[search for examples]</a>

***
<a name="isFinished"></a>
# isFinished
isFinished(  ) &rarr; boolean

true if the process has indicated that it is finished

### Returns:
true if the process has indicated that it is finished

<a href="https://github.com/autoplot/dev/search?q=isFinished&unscoped_q=isFinished">[search for examples]</a>

***
<a name="isStarted"></a>
# isStarted
isStarted(  ) &rarr; boolean

true if the process has indicated that it has started.

### Returns:
true if the process has indicated that it has started.

<a href="https://github.com/autoplot/dev/search?q=isStarted&unscoped_q=isStarted">[search for examples]</a>

***
<a name="setAdditionalInfo"></a>
# <del>setAdditionalInfo</del>
Deprecated: setProgressMessage should be used by the service provider 
    to indicate how the process is being implemented.
***
<a name="setLabel"></a>
# setLabel
setLabel( String label ) &rarr; void

Set a concise string that describes the task being performed.  Monitors
 don't necessarily need to display this label, and this request may be
 ignored.  It is only provided so a process can describe the task that
 is going on.  This is usually set by the client of the process to indicate
 what service we are waiting for.  e.g. "Loading Data"

### Parameters:
label - the label describing the task.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLabel&unscoped_q=setLabel">[search for examples]</a>

***
<a name="setProgressMessage"></a>
# setProgressMessage
setProgressMessage( String message ) &rarr; void

Provides additional feedback as to what's going on in the process. 
 This message should be set by the service provider, not the client,
 and refer to the implementation of the task.  e.g. "Reading file myData.dat"

### Parameters:
message - the message describing the state of progress.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setProgressMessage&unscoped_q=setProgressMessage">[search for examples]</a>

***
<a name="setTaskProgress"></a>
# setTaskProgress
setTaskProgress( long position ) &rarr; void

Notifies the ProgressMonitor of a change in the progress
 of the task.

### Parameters:
position - the current task position

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTaskProgress&unscoped_q=setTaskProgress">[search for examples]</a>

***
<a name="setTaskSize"></a>
# setTaskSize
setTaskSize( long taskSize ) &rarr; void

Sets the maximum value for the task progress of this
 <code>ProgressMonitor</code>.

### Parameters:
taskSize - maximum value for the task progress.  A taskSize of -1 indicates the taskSize is indeterminate.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTaskSize&unscoped_q=setTaskSize">[search for examples]</a>

***
<a name="started"></a>
# started
started(  ) &rarr; void

Notifies the <code>ProgressMonitor</code> that the task
 being monitored has started.  If the <code>ProgressMonitor</code>
 is in a cancelled state when this method is called, that <code>
 ProgressMonitor</code> should be 'uncancelled'.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=started&unscoped_q=started">[search for examples]</a>

