# org.das2.dataset.DataRequestThread



# DataRequestThread( )
Creates a new instance of DataRequestThread

***
<a name="cancelCurrentRequest"></a>
# cancelCurrentRequest
cancelCurrentRequest(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=cancelCurrentRequest&unscoped_q=cancelCurrentRequest">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="request"></a>
# request
request( org.das2.dataset.DataSetDescriptor dsd, Datum start, Datum end, Datum resolution, org.das2.dataset.DataRequestor requestor, ProgressMonitor monitor ) &rarr; void

Begins a data reqest operation that will be executed
 in a separate thread and pass the resulting DataSet to the
 org.das2.event.DataRequestListener#finished(org.das2.event.DataRequestEvent)
 finished() method of the <code>DataRequestor</code>
 specified.

### Parameters:
dsd - the <code>DataSetDescriptor</code> used to obtain
      the <code>DataSet</code>
<br>start - the start of the requested time interval
<br>end - the end of the requested time interval
<br>resolution - the requested resolution of the data set
<br>requestor - <code>DataRequestor</code> that is notified
      when the data loading operation is complete.
<br>monitor - a ProgressMonitor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=request&unscoped_q=request">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="requestAndWait"></a>
# requestAndWait
requestAndWait( org.das2.dataset.DataSetDescriptor dsd, Object params, Datum start, Datum end, Datum resolution, org.das2.dataset.DataRequestor requestor, ProgressMonitor monitor ) &rarr; void

Begins a data reqest operation that will be executed
 in a separate thread and pass the resulting DataSet to the
 org.das2.event.DataRequestListener#finished(org.das2.event.DataRequestEvent)
 finished() method of the <code>DataRequestor</code>
 specified.

 This method does not return until after the data loading is complete
 or the request had been canceled.

### Parameters:
dsd - the <code>DataSetDescriptor</code> used to obtain
      the <code>DataSet</code>
<br>params - extra parameters passed to the 
      DataSetDescriptor#getDataSet(org.das2.util.Datum,org.das2.util.Datum,org.das2.util.Datum,org.das2.util.monitor.ProgressMonitor)
      getDataSet() method.  (TODO: these are ignored)
<br>start - the start of the requested time interval
<br>end - the end of the requested time interval
<br>resolution - the requested resolution of the data set
<br>requestor - <code>DataRequestor</code> that is notified
      when the data loading operation is complete.
<br>monitor - a ProgressMonitor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=requestAndWait&unscoped_q=requestAndWait">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="run"></a>
# run
run(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=run&unscoped_q=run">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

