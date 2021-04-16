# org.autoplot.dom.PlotElementControllerUtil
PlotElementControllerUtil( )


***
<a name="getTimeRange"></a>
# getTimeRange
getTimeRange( org.autoplot.dom.Application dom, org.autoplot.dom.PlotElement pe ) &rarr; DatumRange

return the DatumRange for the plot element's data.  When there is a
 TimeSeriesBrowse, this is its timerange (the axis range or the loaded range
 when a time axis is not visible), otherwise it comes from
 the data.  If none is found, then null is returned.

### Parameters:
dom - the application
<br>pe - the plot element

### Returns:
the DatumRange or null.

<a href="https://github.com/autoplot/dev/search?q=getTimeRange&unscoped_q=getTimeRange">[search for examples]</a>

