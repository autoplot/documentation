# org.autoplot.datasource.capability.Streaming

allows the records to be read in as they are available.  Note
 when the Iterator hasNext method may block until more records are 
 available.

***
<a name="streamDataSet"></a>
# streamDataSet
streamDataSet( ProgressMonitor mon ) &rarr; Iterator

provide an iterator that will provide access to each slice of the data
 set.  It should be understood that each record returned should be
 join-able to the previous records.

### Parameters:
mon - the monitor.  assert monitor.finished()==(!result.hasNext())

### Returns:
a dataset iterator.

<a href="https://github.com/autoplot/dev/search?q=streamDataSet&unscoped_q=streamDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

