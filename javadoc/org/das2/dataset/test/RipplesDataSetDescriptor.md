# org.das2.dataset.test.RipplesDataSetDescriptor
RipplesDataSetDescriptor( )


RipplesDataSetDescriptor( double x1, double y1, double p1, double x2, double y2, double p2, int nx, int ny )
creates a DataSetDescriptor (note the range and resolution is ignored--an unneccessary use
 since Render now has setDataSet method) that is the sum of two ripples.

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

***
<a name="getXUnits"></a>
# getXUnits
getXUnits(  ) &rarr; Units



### Returns:
org.das2.datum.Units


<a href="https://github.com/autoplot/dev/search?q=getXUnits&unscoped_q=getXUnits">[search for examples]</a>

***
<a name="getYUnits"></a>
# getYUnits
getYUnits(  ) &rarr; Units



### Returns:
org.das2.datum.Units


<a href="https://github.com/autoplot/dev/search?q=getYUnits&unscoped_q=getYUnits">[search for examples]</a>

***
<a name="getZUnits"></a>
# getZUnits
getZUnits(  ) &rarr; Units



### Returns:
org.das2.datum.Units


<a href="https://github.com/autoplot/dev/search?q=getZUnits&unscoped_q=getZUnits">[search for examples]</a>

