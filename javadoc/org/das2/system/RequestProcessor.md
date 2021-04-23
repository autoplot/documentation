# org.das2.system.RequestProcessor

Utility class for synchronous execution.
 This class maintains a pool of threads that are used to execute arbitrary
 code.  This class also serves as a central place to catch and handle
 unchecked exceptions.

 The {@link #invokeLater(java.lang.Runnable)} method is similar to the
 SwingUtilities {@link javax.swing.SwingUtilities#invokeLater(java.lang.Runnable)}
 method, except that the request is not executed on the event thread.

 The {@link #invokeLater(java.lang.Runnable, java.lang.Object)},
 the {@link #invokeAfter(java.lang.Runnable, java.lang.Object)},
 and the {@link #waitFor(java.lang.Object)} methods are designed to work
 together.  Both of the first two methods execute code asynchronously with
 respect to the calling thread.  Multiple requests made with a call to
 invokeLater that specified the same lock can execute at the same time,
 but not while a request made with the invokeAfter with the same lock
 is processing.  Any requests made before an invokeAfter request with the
 same lock will finish before that invokeAfter request begins. An
 invokeAfter request will finish before any requests with the same lock made
 after that invokeAfter request begins.  The {@link #waitFor(java.lang.Object)}
 method will cause the calling thread to block until all requests with the
 specified lock finish.

***
<a name="invokeAfter"></a>
# invokeAfter
invokeAfter( java.lang.Runnable run, Object lock ) &rarr; void

Executes run.run() asynchronously on a thread from the thread pool.
 The task will not be executed until after all requests made with
 {@link #invokeAfter(java.lang.Runnable, java.lang.Object)} or
 {@link #invokeLater(java.lang.Runnable, java.lang.Object)} with the same
 lock have finished.

### Parameters:
run - the task to be executed.
<br>lock - associates run with other tasks.

### Returns:
void (returns nothing)

### See Also:
<a href='#waitFor'>waitFor(java.lang.Object)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=invokeAfter&unscoped_q=invokeAfter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="invokeLater"></a>
# invokeLater
invokeLater( java.lang.Runnable run ) &rarr; void

Executes run.run() asynchronously on a thread from the thread pool.

### Parameters:
run - the task to be executed.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=invokeLater&unscoped_q=invokeLater">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

invokeLater( java.lang.Runnable run, Object lock ) &rarr; void<br>
***
<a name="printStatus"></a>
# printStatus
printStatus(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=printStatus&unscoped_q=printStatus">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setThreadCount"></a>
# setThreadCount
setThreadCount( int t ) &rarr; void

reset the maximum number of threads used.  If there are more threads 
 existing already, than the extra threads will be shut down as they finish
 their current jobs.

### Parameters:
t - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setThreadCount&unscoped_q=setThreadCount">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="shutdown"></a>
# shutdown
shutdown(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=shutdown&unscoped_q=shutdown">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="waitFor"></a>
# waitFor
waitFor( Object lock ) &rarr; void

Blocks until all tasks with the same lock have finished.

### Parameters:
lock - an Object

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=waitFor&unscoped_q=waitFor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

