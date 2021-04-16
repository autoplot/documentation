# org.das2.util.monitor.AlertNullProgressMonitorLike the NullProgressMonitor, but print to stderr when the task is
 taking a non-trivial amount of time.  The NullProgressMonitor is used
 when the developer thinks that a task is trivial, so this should be used
 to verify.  After one second, this will start dumping messages to 
 stderr.
AlertNullProgressMonitor( )
create a monitor.

AlertNullProgressMonitor( String label )
create a monitor with the label.

***
<a name="setTaskProgress"></a>
# setTaskProgress
setTaskProgress( long position ) &rarr; void



### Parameters:
position - a long

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTaskProgress&unscoped_q=setTaskProgress">[search for examples]</a>

