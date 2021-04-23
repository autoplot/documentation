# org.das2.dataset.DataSetDescriptorDataSetDescriptors are a source from where datasets are produced.  These uniquely identify a data set
 that is parameteric.  Typically, the parameter is time, so for example, there might be a DataSetDescriptor
 for "discharge of the Iowa River measured at Iowa City."  Clients of the class get
 DataSets from the DataSetDescriptor via the getDataSet( Start, End, Resolution ) method.  So for
 example, you might ask what is the discharge from June 1 to August 31st, 2005, at a resolution of
 1 day.  Presently, it's implicit that this means to give bin averages of the data.

 <p>DataSetDescriptors are identified with a URL-like string:
 {@code http://www-pw.physics.uiowa.edu/das/das2Server?das2_1/cluster/wbd/r_wbd_dsn_cfd&spacecraft%3Dc1%26antenna%3DEy}
 </p>

 <p>The protocol of the string indicates how the DataSetDescriptor is to be constructed, and presently
 there are:
<pre>
   http     a das2Server provides the specification of the datasetdescriptor.
   class    refers to a loadable java class that is an instanceof DataSetDescriptor and
            has the method newDataSetDescriptor( Map params ) throws DasException
</pre>
***
<a name="addDataSetUpdateListener"></a>
# addDataSetUpdateListener
addDataSetUpdateListener( org.das2.dataset.DataSetUpdateListener listener ) &rarr; void



### Parameters:
listener - a DataSetUpdateListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addDataSetUpdateListener&unscoped_q=addDataSetUpdateListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="create"></a>
# create
create( String dataSetID ) &rarr; DataSetDescriptor

creates a DataSetDescriptor for the given identification string.  The identification
 string is a URL-like string, for example 
  http://www-pw.physics.uiowa.edu/das/das2Server?das2_1/cluster/wbd/r_wbd_dsn_cfd&spacecraft%3Dc1%26antenna%3DEy
 The protocol of the string indicates how the DataSetDescriptor is to be constructed, and presently
 there are:
<pre>
   http     a das2Server provides the specification of the DataSetDescriptor, and a
            StreamDataSetDescriptor is created.
   class    refers to a loadable java class that is an instanceof DataSetDescriptor and
            has the method newDataSetDescriptor( Map params )
</pre>
 Note that DataSetDescriptors are stateless, the same DataSetDescriptor object
 may be returned to multiple clients.

### Parameters:
dataSetID - the URL-like identifier.

### Returns:
the DataSetDescriptor for the id.

<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="drawListIcon"></a>
# drawListIcon
drawListIcon( java.awt.Graphics2D g, int x, int y ) &rarr; void



### Parameters:
g - a Graphics2D
<br>x - an int
<br>y - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=drawListIcon&unscoped_q=drawListIcon">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSet"></a>
# getDataSet
getDataSet( Datum start, Datum end, Datum resolution, ProgressMonitor monitor ) &rarr; DataSet

Retrieve the dataset for this interval and resolution.  The contract for this function is that
 identical start,end,resolution parameters will yield an identical dataSet, except for when an
 DataSetUpdate has been fired in the meantime.

 null for the data resolution indicates that the data should be returned at its "intrinsic resolution"
 if such a resolution exists.

### Parameters:
start - a Datum
<br>end - a Datum
<br>resolution - a Datum
<br>monitor - a ProgressMonitor

### Returns:
org.das2.dataset.DataSet


<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSetCache"></a>
# getDataSetCache
getDataSetCache(  ) &rarr; DataSetCache



### Returns:
the DataSetCache object used to store cached copies of the
 DataSets created by this object.

<a href="https://github.com/autoplot/dev/search?q=getDataSetCache&unscoped_q=getDataSetCache">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSetID"></a>
# getDataSetID
getDataSetID(  ) &rarr; String



### Returns:
the string that uniquely identifies this dataset.

<a href="https://github.com/autoplot/dev/search?q=getDataSetID&unscoped_q=getDataSetID">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getListIcon"></a>
# getListIcon
getListIcon(  ) &rarr; Icon



### Returns:
javax.swing.Icon


<a href="https://github.com/autoplot/dev/search?q=getListIcon&unscoped_q=getListIcon">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getListLabel"></a>
# getListLabel
getListLabel(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getListLabel&unscoped_q=getListLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getProperty"></a>
# getProperty
getProperty( String name ) &rarr; Object

Returns the value of the property with the specified name

### Parameters:
name - The name of the property requested

### Returns:
The value of the requested property as an Object

<a href="https://github.com/autoplot/dev/search?q=getProperty&unscoped_q=getProperty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getXUnits"></a>
# getXUnits
getXUnits(  ) &rarr; Units



### Returns:
the x units of the DataSetDescriptor that parameterize the data.  This is used to identify dataSet requests.

<a href="https://github.com/autoplot/dev/search?q=getXUnits&unscoped_q=getXUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeDataSetUpdateListener"></a>
# removeDataSetUpdateListener
removeDataSetUpdateListener( org.das2.dataset.DataSetUpdateListener listener ) &rarr; void



### Parameters:
listener - a DataSetUpdateListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeDataSetUpdateListener&unscoped_q=removeDataSetUpdateListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="requestDataSet"></a>
# requestDataSet
requestDataSet( Datum start, Datum end, Datum resolution, ProgressMonitor monitor, Object lockObject ) &rarr; void

Requests that a dataSet be loaded, and that the dataSet be returned via a DataSetUpdate event.
 The @param lockObject is an object that is dependent on the load, for example, the DasCanvas,
 and will be passed in to the request processor.  If the dataSet is available in interactive time,
 then the dataSetUpdate may be fired on the same thread as the request is made.

### Parameters:
start - a Datum
<br>end - a Datum
<br>resolution - a Datum
<br>monitor - a ProgressMonitor
<br>lockObject - an Object

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=requestDataSet&unscoped_q=requestDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

requestDataSet( Datum start, Datum end, Datum resolution, ProgressMonitor monitor, Object lockObject, org.das2.dataset.DataSetUpdateListener listener ) &rarr; void<br>
***
<a name="reset"></a>
# reset
reset(  ) &rarr; void

clear any state that's developed, in particular any data caches.  Note
 this currently deletes all cached datasets, regardless of the DataSetDescriptor
 that produced them.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reset&unscoped_q=reset">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDefaultCaching"></a>
# setDefaultCaching
setDefaultCaching( boolean value ) &rarr; void

defaultCaching means that the abstract DataSetDescriptor is allowed to handle
 repeat getDataSet calls by returning a cached dataset.  If a dataSetUpdate event
 is thrown, the defaultCache is reset.

 Use caution when using this.  Note that caching may only be turned off
 with this call.

### Parameters:
value - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDefaultCaching&unscoped_q=setDefaultCaching">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

