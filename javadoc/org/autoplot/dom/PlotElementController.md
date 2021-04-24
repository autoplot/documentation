# org.autoplot.dom.PlotElementController

PlotElementController manages the PlotElement, for example resolving the datasource and loading the dataset.
 Once the data is loaded, the listening PlotElementController receives the update and does the following:<ol>
  <li> resolve the plot type: spectrogram, lineplot, stack of lineplot, etc, using AutoplotUtil.guessRenderType(fillDs);
  <li> reset the plot element, setting the plot type and creating children if needed.  For example, a B-GSM (demo 5) is
      resolved by creating three children, and handing the components off to them.
  <li> if the component property is not empty, then we implement the component and display that.
  <li> adjusting the component slice index will not affect ranging when the index is changed.
 </ol>

# PlotElementController( org.autoplot.ApplicationModel model, org.autoplot.dom.Application dom, org.autoplot.dom.PlotElement plotElement )


***
<a name="SYMSIZE_DATAPOINT_COUNT"></a>
# SYMSIZE_DATAPOINT_COUNT

switch over between fine and course points.

***
<a name="LARGE_DATASET_COUNT"></a>
# LARGE_DATASET_COUNT



***
<a name="PROP_DATASET"></a>
# PROP_DATASET

the current dataset plotted, after operations (component property) has been applied.

***
<a name="PROP_RESETRANGES"></a>
# PROP_RESETRANGES

true indicates the controller should autorange next time the fillDataSet is changed.

***
<a name="PROP_RESETPLOTELEMENT"></a>
# PROP_RESETPLOTELEMENT

true indicates the controller should install a new renderer to implement the
 renderType selection.  This may mean that we introduce or remove child plotElements.
 This implies resetRenderType.

***
<a name="PROP_RESETCOMPONENT"></a>
# PROP_RESETCOMPONENT

true indicates that the component should be reset when the dataset arrives.  This
 is added as a controller property so that clients can clear this setting if
 they do not want the component to be reset.  This is only considered if resetPlotElement is
 set.

***
<a name="PROP_RESETRENDERTYPE"></a>
# PROP_RESETRENDERTYPE

true indicates the peer should be reset to the current renderType.

***
<a name="PROP_DSFRESET"></a>
# PROP_DSFRESET

when true, a change in the DataSourceFilter should reset the plotElement.

***
<a name="PROP_SLICEAUTORANGES"></a>
# PROP_SLICEAUTORANGES



***
<a name="bindToContoursRenderer"></a>
# bindToContoursRenderer
bindToContoursRenderer( org.das2.graph.Renderer renderer ) &rarr; void



### Parameters:
renderer - a Renderer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=bindToContoursRenderer&unscoped_q=bindToContoursRenderer">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bindToDigitalRenderer"></a>
# bindToDigitalRenderer
bindToDigitalRenderer( org.das2.graph.DigitalRenderer renderer ) &rarr; void



### Parameters:
renderer - a DigitalRenderer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=bindToDigitalRenderer&unscoped_q=bindToDigitalRenderer">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bindToEventsRenderer"></a>
# bindToEventsRenderer
bindToEventsRenderer( org.das2.graph.EventsRenderer renderer ) &rarr; void



### Parameters:
renderer - an EventsRenderer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=bindToEventsRenderer&unscoped_q=bindToEventsRenderer">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bindToImageVectorDataSetRenderer"></a>
# bindToImageVectorDataSetRenderer
bindToImageVectorDataSetRenderer( org.das2.graph.HugeScatterRenderer renderer ) &rarr; void



### Parameters:
renderer - a HugeScatterRenderer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=bindToImageVectorDataSetRenderer&unscoped_q=bindToImageVectorDataSetRenderer">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bindToPolarPlotRenderer"></a>
# bindToPolarPlotRenderer
bindToPolarPlotRenderer( org.das2.graph.PolarPlotRenderer renderer ) &rarr; void



### Parameters:
renderer - a PolarPlotRenderer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=bindToPolarPlotRenderer&unscoped_q=bindToPolarPlotRenderer">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bindToSeriesRenderer"></a>
# bindToSeriesRenderer
bindToSeriesRenderer( org.das2.graph.SeriesRenderer seriesRenderer ) &rarr; void



### Parameters:
seriesRenderer - a SeriesRenderer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=bindToSeriesRenderer&unscoped_q=bindToSeriesRenderer">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bindToSpectrogramRenderer"></a>
# bindToSpectrogramRenderer
bindToSpectrogramRenderer( org.das2.graph.SpectrogramRenderer spectrogramRenderer ) &rarr; void



### Parameters:
spectrogramRenderer - a SpectrogramRenderer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=bindToSpectrogramRenderer&unscoped_q=bindToSpectrogramRenderer">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bindToTickCurveRenderer"></a>
# bindToTickCurveRenderer
bindToTickCurveRenderer( org.das2.graph.TickCurveRenderer renderer ) &rarr; void



### Parameters:
renderer - a TickCurveRenderer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=bindToTickCurveRenderer&unscoped_q=bindToTickCurveRenderer">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="doAutoranging"></a>
# doAutoranging
doAutoranging( org.autoplot.dom.PlotElement peleCopy, java.util.Map props, QDataSet fillDs ) &rarr; void



### Parameters:
peleCopy - a PlotElement
<br>props - a java.util.Map
<br>fillDs - a QDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=doAutoranging&unscoped_q=doAutoranging">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

doAutoranging( org.autoplot.dom.PlotElement peleCopy, java.util.Map props, QDataSet fillDs, boolean ignoreDsProps ) &rarr; void<br>
***
<a name="doResetRenderType"></a>
# doResetRenderType
doResetRenderType( org.autoplot.RenderType renderType ) &rarr; void

used to explicitly set the rendering type.  This installs a das2 renderer
 into the plot to implement the render type.

 preconditions:
   renderer type has been identified.
 postconditions:
   das2 renderer peer is created and bindings made.

### Parameters:
renderType - a RenderType

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=doResetRenderType&unscoped_q=doResetRenderType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getApplication"></a>
# getApplication
getApplication(  ) &rarr; Application

return the application that the plotElement belongs to.

### Returns:
an org.autoplot.dom.Application


<a href="https://github.com/autoplot/dev/search?q=getApplication&unscoped_q=getApplication">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getChildPlotElements"></a>
# getChildPlotElements
getChildPlotElements(  ) &rarr; List

return child plotElements, which are plotElements that share a datasource but pull out
 a component of the data.

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=getChildPlotElements&unscoped_q=getChildPlotElements">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDasPlot"></a>
# getDasPlot
getDasPlot(  ) &rarr; DasPlot

return the plot containing this plotElement's renderer, or null.

### Returns:
the plot containing this plotElement's renderer, or null.

<a href="https://github.com/autoplot/dev/search?q=getDasPlot&unscoped_q=getDasPlot">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSet"></a>
# getDataSet
getDataSet(  ) &rarr; QDataSet

the current dataset plotted, after operations (component property) has been applied.

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSourceFilter"></a>
# getDataSourceFilter
getDataSourceFilter(  ) &rarr; DataSourceFilter

return the data source and filter for this plotElement.

### Returns:
an org.autoplot.dom.DataSourceFilter


<a href="https://github.com/autoplot/dev/search?q=getDataSourceFilter&unscoped_q=getDataSourceFilter">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getParentPlotElement"></a>
# getParentPlotElement
getParentPlotElement(  ) &rarr; PlotElement

return the parent plotElement, or null if the plotElement doesn't have a parent.

### Returns:
an org.autoplot.dom.PlotElement


<a href="https://github.com/autoplot/dev/search?q=getParentPlotElement&unscoped_q=getParentPlotElement">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlotElement"></a>
# getPlotElement
getPlotElement(  ) &rarr; PlotElement

return the plot element.

### Returns:
the plot element.

<a href="https://github.com/autoplot/dev/search?q=getPlotElement&unscoped_q=getPlotElement">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRenderer"></a>
# getRenderer
getRenderer(  ) &rarr; Renderer



### Returns:
org.das2.graph.Renderer


<a href="https://github.com/autoplot/dev/search?q=getRenderer&unscoped_q=getRenderer">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDsfReset"></a>
# isDsfReset
isDsfReset(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isDsfReset&unscoped_q=isDsfReset">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isPendingChanges"></a>
# isPendingChanges
isPendingChanges(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isPendingChanges&unscoped_q=isPendingChanges">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isResetComponent"></a>
# isResetComponent
isResetComponent(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isResetComponent&unscoped_q=isResetComponent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isResetPlotElement"></a>
# isResetPlotElement
isResetPlotElement(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isResetPlotElement&unscoped_q=isResetPlotElement">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isResetRanges"></a>
# isResetRanges
isResetRanges(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isResetRanges&unscoped_q=isResetRanges">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isResetRenderType"></a>
# isResetRenderType
isResetRenderType(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isResetRenderType&unscoped_q=isResetRenderType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isSliceAutoranges"></a>
# isSliceAutoranges
isSliceAutoranges(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isSliceAutoranges&unscoped_q=isSliceAutoranges">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="pendingChanges"></a>
# pendingChanges
pendingChanges( java.util.Map changes ) &rarr; void



### Parameters:
changes - a java.util.Map

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=pendingChanges&unscoped_q=pendingChanges">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resolveRenderType"></a>
# resolveRenderType
resolveRenderType( QDataSet fillds ) &rarr; String

Resolve the renderType and renderControl for the dataset.  This may be
 set explicitly by the dataset, in its RENDER_TYPE property, or resolved
 using the dataset scheme.

### Parameters:
fillds - a QDataSet

### Returns:
the render string with canonical types.  The result will always contain a greater than (&gt;).

<a href="https://github.com/autoplot/dev/search?q=resolveRenderType&unscoped_q=resolveRenderType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDsfReset"></a>
# setDsfReset
setDsfReset( boolean dsfReset ) &rarr; void



### Parameters:
dsfReset - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDsfReset&unscoped_q=setDsfReset">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRenderer"></a>
# setRenderer
setRenderer( org.das2.graph.Renderer renderer ) &rarr; void

set the renderer controlled by this PlotElement controller.  
 This should be used with caution.

### Parameters:
renderer - a Renderer

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/external/PlotCommand.md'>external.PlotCommand</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setRenderer&unscoped_q=setRenderer">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setResetComponent"></a>
# setResetComponent
setResetComponent( boolean resetComponent ) &rarr; void



### Parameters:
resetComponent - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setResetComponent&unscoped_q=setResetComponent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setResetPlotElement"></a>
# setResetPlotElement
setResetPlotElement( boolean resetPlotElement ) &rarr; void



### Parameters:
resetPlotElement - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setResetPlotElement&unscoped_q=setResetPlotElement">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setResetRanges"></a>
# setResetRanges
setResetRanges( boolean resetRanges ) &rarr; void



### Parameters:
resetRanges - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setResetRanges&unscoped_q=setResetRanges">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setResetRenderType"></a>
# setResetRenderType
setResetRenderType( boolean resetRenderType ) &rarr; void



### Parameters:
resetRenderType - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setResetRenderType&unscoped_q=setResetRenderType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSliceAutoranges"></a>
# setSliceAutoranges
setSliceAutoranges( boolean sliceAutoranges ) &rarr; void



### Parameters:
sliceAutoranges - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSliceAutoranges&unscoped_q=setSliceAutoranges">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

