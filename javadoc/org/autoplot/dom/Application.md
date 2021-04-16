# org.autoplot.dom.ApplicationRepresents a state of the application as a whole, with its one canvas and
 multiple plots, axes, and bindings.
Application( )


***
<a name="DEFAULT_TIME_RANGE"></a>
# DEFAULT_TIME_RANGE

default time range indicates when the range is not being used.  This should never been seen by the user.

***
<a name="PROP_DATASOURCEFILTERS"></a>
# PROP_DATASOURCEFILTERS



***
<a name="PROP_PLOT_ELEMENTS"></a>
# PROP_PLOT_ELEMENTS



***
<a name="PROP_PLOTS"></a>
# PROP_PLOTS



***
<a name="PROP_CANVASES"></a>
# PROP_CANVASES



***
<a name="PROP_ANNOTATIONS"></a>
# PROP_ANNOTATIONS



***
<a name="PROP_TIMERANGE"></a>
# PROP_TIMERANGE

all time axes should hang off of this.

***
<a name="PROP_EVENTSLISTURI"></a>
# PROP_EVENTSLISTURI



***
<a name="PROP_BINDINGS"></a>
# PROP_BINDINGS



***
<a name="PROP_CONNECTORS"></a>
# PROP_CONNECTORS



***
<a name="childNodes"></a>
# childNodes
childNodes(  ) &rarr; List



### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=childNodes&unscoped_q=childNodes">[search for examples]</a>

***
<a name="copy"></a>
# copy
copy(  ) &rarr; DomNode

return a copy of this application state.

### Returns:
a copy of this application state.

<a href="https://github.com/autoplot/dev/search?q=copy&unscoped_q=copy">[search for examples]</a>

***
<a name="diffs"></a>
# diffs
diffs( org.autoplot.dom.DomNode node ) &rarr; List

List the differences between the two nodes.
 These should always be from this to that.
 TODO: somehow this ends up working, although PlotElement and Style don't follow this rule.

### Parameters:
node - a DomNode

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=diffs&unscoped_q=diffs">[search for examples]</a>

***
<a name="getAnnotations"></a>
# getAnnotations
getAnnotations(  ) &rarr; Annotation



### Returns:
org.autoplot.dom.Annotation[]


<a href="https://github.com/autoplot/dev/search?q=getAnnotations&unscoped_q=getAnnotations">[search for examples]</a>

getAnnotations( int index ) &rarr; Annotation<br>
***
<a name="getBindings"></a>
# getBindings
getBindings(  ) &rarr; BindingModel



### Returns:
org.autoplot.dom.BindingModel[]


<a href="https://github.com/autoplot/dev/search?q=getBindings&unscoped_q=getBindings">[search for examples]</a>

getBindings( int index ) &rarr; BindingModel<br>
***
<a name="getCanvases"></a>
# getCanvases
getCanvases(  ) &rarr; Canvas



### Returns:
org.autoplot.dom.Canvas[]


<a href="https://github.com/autoplot/dev/search?q=getCanvases&unscoped_q=getCanvases">[search for examples]</a>

getCanvases( int index ) &rarr; Canvas<br>
***
<a name="getConnectors"></a>
# getConnectors
getConnectors(  ) &rarr; Connector



### Returns:
org.autoplot.dom.Connector[]


<a href="https://github.com/autoplot/dev/search?q=getConnectors&unscoped_q=getConnectors">[search for examples]</a>

getConnectors( int index ) &rarr; Connector<br>
***
<a name="getController"></a>
# getController
getController(  ) &rarr; ApplicationController



### Returns:
org.autoplot.dom.ApplicationController


<a href="https://github.com/autoplot/dev/search?q=getController&unscoped_q=getController">[search for examples]</a>

***
<a name="getDataSourceFilters"></a>
# getDataSourceFilters
getDataSourceFilters(  ) &rarr; DataSourceFilter



### Returns:
org.autoplot.dom.DataSourceFilter[]


<a href="https://github.com/autoplot/dev/search?q=getDataSourceFilters&unscoped_q=getDataSourceFilters">[search for examples]</a>

getDataSourceFilters( int index ) &rarr; DataSourceFilter<br>
***
<a name="getElementById"></a>
# getElementById
getElementById( String id ) &rarr; DomNode

return the DomNode referenced by id.  This was introduced because
 it is often difficult to identify the index of a plot in the plots array
 but its id is known, and this avoids the import of DomUtil.

### Parameters:
id - an id, such as "plot_2"

### Returns:
the node
### See Also:
<a href='DomUtil.md#getElementById'>DomUtil#getElementById(org.autoplot.dom.DomNode, java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getElementById&unscoped_q=getElementById">[search for examples]</a>

***
<a name="getEventsListUri"></a>
# getEventsListUri
getEventsListUri(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getEventsListUri&unscoped_q=getEventsListUri">[search for examples]</a>

***
<a name="getOptions"></a>
# getOptions
getOptions(  ) &rarr; Options



### Returns:
org.autoplot.dom.Options


<a href="https://github.com/autoplot/dev/search?q=getOptions&unscoped_q=getOptions">[search for examples]</a>

***
<a name="getPlotElements"></a>
# getPlotElements
getPlotElements(  ) &rarr; PlotElement



### Returns:
org.autoplot.dom.PlotElement[]


<a href="https://github.com/autoplot/dev/search?q=getPlotElements&unscoped_q=getPlotElements">[search for examples]</a>

getPlotElements( int index ) &rarr; PlotElement<br>
***
<a name="getPlots"></a>
# getPlots
getPlots(  ) &rarr; Plot



### Returns:
org.autoplot.dom.Plot[]


<a href="https://github.com/autoplot/dev/search?q=getPlots&unscoped_q=getPlots">[search for examples]</a>

getPlots( int index ) &rarr; Plot<br>
***
<a name="getTimeRange"></a>
# getTimeRange
getTimeRange(  ) &rarr; DatumRange



### Returns:
org.das2.datum.DatumRange


<a href="https://github.com/autoplot/dev/search?q=getTimeRange&unscoped_q=getTimeRange">[search for examples]</a>

***
<a name="setAnnotations"></a>
# setAnnotations
setAnnotations( org.autoplot.dom.Annotation[] annotations ) &rarr; void



### Parameters:
annotations - an org.autoplot.dom.Annotation[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAnnotations&unscoped_q=setAnnotations">[search for examples]</a>

setAnnotations( int index, org.autoplot.dom.Annotation annotation ) &rarr; void<br>
***
<a name="setBindings"></a>
# setBindings
setBindings( org.autoplot.dom.BindingModel[] bindings ) &rarr; void



### Parameters:
bindings - an org.autoplot.dom.BindingModel[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setBindings&unscoped_q=setBindings">[search for examples]</a>

setBindings( int index, org.autoplot.dom.BindingModel newBinding ) &rarr; void<br>
***
<a name="setCanvases"></a>
# setCanvases
setCanvases( org.autoplot.dom.Canvas[] canvases ) &rarr; void



### Parameters:
canvases - an org.autoplot.dom.Canvas[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCanvases&unscoped_q=setCanvases">[search for examples]</a>

setCanvases( int index, org.autoplot.dom.Canvas newCanvas ) &rarr; void<br>
***
<a name="setConnectors"></a>
# setConnectors
setConnectors( org.autoplot.dom.Connector[] connectors ) &rarr; void



### Parameters:
connectors - an org.autoplot.dom.Connector[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setConnectors&unscoped_q=setConnectors">[search for examples]</a>

setConnectors( int index, org.autoplot.dom.Connector newConnector ) &rarr; void<br>
***
<a name="setDataSourceFilters"></a>
# setDataSourceFilters
setDataSourceFilters( org.autoplot.dom.DataSourceFilter[] dataSourceFilters ) &rarr; void



### Parameters:
dataSourceFilters - an org.autoplot.dom.DataSourceFilter[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSourceFilters&unscoped_q=setDataSourceFilters">[search for examples]</a>

setDataSourceFilters( int index, org.autoplot.dom.DataSourceFilter newDataSourceFilter ) &rarr; void<br>
***
<a name="setEventsListUri"></a>
# setEventsListUri
setEventsListUri( String eventsListUri ) &rarr; void



### Parameters:
eventsListUri - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setEventsListUri&unscoped_q=setEventsListUri">[search for examples]</a>

***
<a name="setOptions"></a>
# setOptions
setOptions( org.autoplot.dom.Options options ) &rarr; void



### Parameters:
options - an Options

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setOptions&unscoped_q=setOptions">[search for examples]</a>

***
<a name="setPlotElements"></a>
# setPlotElements
setPlotElements( org.autoplot.dom.PlotElement[] pele ) &rarr; void



### Parameters:
pele - an org.autoplot.dom.PlotElement[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPlotElements&unscoped_q=setPlotElements">[search for examples]</a>

setPlotElements( int index, org.autoplot.dom.PlotElement pele ) &rarr; void<br>
***
<a name="setPlots"></a>
# setPlots
setPlots( org.autoplot.dom.Plot[] plots ) &rarr; void



### Parameters:
plots - an org.autoplot.dom.Plot[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPlots&unscoped_q=setPlots">[search for examples]</a>

setPlots( int index, org.autoplot.dom.Plot newPlots ) &rarr; void<br>
***
<a name="setTimeRange"></a>
# setTimeRange
setTimeRange( DatumRange timeRange ) &rarr; void



### Parameters:
timeRange - a DatumRange

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTimeRange&unscoped_q=setTimeRange">[search for examples]</a>

***
<a name="syncTo"></a>
# syncTo
syncTo( org.autoplot.dom.DomNode n ) &rarr; void



### Parameters:
n - a DomNode

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=syncTo&unscoped_q=syncTo">[search for examples]</a>

syncTo( org.autoplot.dom.DomNode n, java.util.List exclude ) &rarr; void<br>
