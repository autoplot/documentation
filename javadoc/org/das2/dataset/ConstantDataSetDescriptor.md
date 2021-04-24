# org.das2.dataset.ConstantDataSetDescriptor

This class wraps a DataSet to use where DataSetDescriptors are required.  This 
 trivially returns the wrapped DataSet regardless of the getDataSet parameters.
 Originally this class was used with Renderers, which needed a DataSetDescriptor 
 for their operation.  Now that they interact only with DataSets, and this
 class should not be used with them, use Renderer.setDataSet instead.

# ConstantDataSetDescriptor( org.das2.dataset.DataSet ds )
Creates a new instance of ConstantDataSetDescriptor

***
<a name="getDataSet"></a>
# getDataSet
getDataSet( Datum start, Datum end, Datum resolution, ProgressMonitor monitor ) &rarr; DataSet



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
<a name="getDataSetImpl"></a>
# getDataSetImpl
getDataSetImpl( Datum start, Datum end, Datum resolution, ProgressMonitor monitor ) &rarr; DataSet



### Parameters:
start - a Datum
<br>end - a Datum
<br>resolution - a Datum
<br>monitor - a ProgressMonitor

### Returns:
org.das2.dataset.DataSet


<a href="https://github.com/autoplot/dev/search?q=getDataSetImpl&unscoped_q=getDataSetImpl">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getXUnits"></a>
# getXUnits
getXUnits(  ) &rarr; Units



### Returns:
org.das2.datum.Units


<a href="https://github.com/autoplot/dev/search?q=getXUnits&unscoped_q=getXUnits">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="requestDataSet"></a>
# requestDataSet
requestDataSet( Datum start, Datum end, Datum resolution, ProgressMonitor monitor, Object lockObject ) &rarr; void



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

