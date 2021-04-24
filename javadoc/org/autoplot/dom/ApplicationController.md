# org.autoplot.dom.ApplicationController

The ApplicationController, one per dom, is in charge of managing the 
 application as a whole, for example, adding and deleting plots,
 managing bindings, and managing focus.

# ApplicationController( org.autoplot.ApplicationModel model, org.autoplot.dom.Application application )


***
<a name="VALUE_BLUR_FOCUS"></a>
# VALUE_BLUR_FOCUS

use this value to blur the focus.

***
<a name="PROP_STATUS"></a>
# PROP_STATUS



***
<a name="PROP_FOCUSURI"></a>
# PROP_FOCUSURI

property focusUri is the uri that has gained focus.  This can be the datasource uri, or the location of the .vap file.

***
<a name="PROP_PLOT_ELEMENT"></a>
# PROP_PLOT_ELEMENT



***
<a name="PROP_PLOT"></a>
# PROP_PLOT



***
<a name="PROP_CANVAS"></a>
# PROP_CANVAS



***
<a name="PROP_DATASOURCEFILTER"></a>
# PROP_DATASOURCEFILTER

focus dataSourceFilter.

***
<a name="PROP_PENDINGCHANGECOUNT"></a>
# PROP_PENDINGCHANGECOUNT



***
<a name="addActionListener"></a>
# addActionListener
addActionListener( java.awt.event.ActionListener list ) &rarr; void



### Parameters:
list - an ActionListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addActionListener&unscoped_q=addActionListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addAnnotation"></a>
# addAnnotation
addAnnotation( org.autoplot.dom.Annotation annotation ) &rarr; Annotation

experiment with Jython-friendly method where the annotation is 
 instantiated within the script.  This allows code like:

<blockquote><pre><small>
 ann= Annotation( text='Feature', pointAtX=datum(tt), pointAtY=datum('100nT'), showArrow=True )
</small></pre></blockquote>

### Parameters:
annotation - an Annotation

### Returns:
the annotation, configured.

<a href="https://github.com/autoplot/dev/search?q=addAnnotation&unscoped_q=addAnnotation">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addAnnotation( org.autoplot.dom.Plot p, String text ) &rarr; Annotation<br>
addAnnotation( org.autoplot.dom.Row row, org.autoplot.dom.Column column, String text ) &rarr; Annotation<br>
***
<a name="addCanvas"></a>
# addCanvas
addCanvas(  ) &rarr; DasCanvas

add a canvas to the application.  Currently, only one canvas is supported, so this
 will have unanticipated effects if called more than once.

 This must be public to provide access to org.autoplot.ApplicationModel

### Returns:
an org.das2.graph.DasCanvas


<a href="https://github.com/autoplot/dev/search?q=addCanvas&unscoped_q=addCanvas">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addConnector"></a>
# addConnector
addConnector( org.autoplot.dom.Plot upperPlot, org.autoplot.dom.Plot lowerPlot ) &rarr; void

adds a context overview plotId below the plotId.

### Parameters:
upperPlot - the upper plot
<br>lowerPlot - the lower plot

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addConnector&unscoped_q=addConnector">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addDas2PeerChangeListener"></a>
# addDas2PeerChangeListener
addDas2PeerChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void

kludgy way to decouple the context menus from the DOM tree.

### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addDas2PeerChangeListener&unscoped_q=addDas2PeerChangeListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addDataSourceFilter"></a>
# addDataSourceFilter
addDataSourceFilter(  ) &rarr; DataSourceFilter

add a DataSourceFilter to the dom.

### Returns:
the new DataSourceFilter

<a href="https://github.com/autoplot/dev/search?q=addDataSourceFilter&unscoped_q=addDataSourceFilter">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addPlot"></a>
# addPlot
addPlot( Object direction ) &rarr; Plot

add a plot to the canvas.  Direction is with respect to the current
 focus plot, and currently only LayoutConstants.ABOVE and LayoutConstants.BELOW
 are supported.

### Parameters:
direction - LayoutConstants.ABOVE, LayoutConstants.BELOW, or null.  
 Null indicates the layout will be done elsewhere, and the new plot will
 be on top of the old.

### Returns:
an org.autoplot.dom.Plot


<a href="https://github.com/autoplot/dev/search?q=addPlot&unscoped_q=addPlot">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addPlot( org.autoplot.dom.Plot focus, Object direction ) &rarr; Plot<br>
addPlot( org.autoplot.dom.Row row, org.autoplot.dom.Column column ) &rarr; Plot<br>
addPlot( String xpos, String ypos ) &rarr; Plot<br>
***
<a name="addPlotElement"></a>
# addPlotElement
addPlotElement( org.autoplot.dom.Plot domPlot, org.autoplot.dom.DataSourceFilter dsf ) &rarr; PlotElement

add a plotElement to the application, attaching it to the given Plot and DataSourceFilter.

### Parameters:
domPlot - if null, create a Plot, if non-null, add the plotElement to this plot.
<br>dsf - if null, create a DataSourceFilter.  If non-null, connect the plotElement to this data source.

### Returns:
an org.autoplot.dom.PlotElement


<a href="https://github.com/autoplot/dev/search?q=addPlotElement&unscoped_q=addPlotElement">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addPlotElement( org.autoplot.dom.Plot domPlot, org.autoplot.dom.PlotElement parent, org.autoplot.dom.DataSourceFilter dsf ) &rarr; PlotElement<br>
***
<a name="addPlots"></a>
# addPlots
addPlots( int nrow, int ncol, Object dir ) &rarr; List

adds a block of plots to the canvas below the focus plot.  A plotElement
 is added for each plot as well.

### Parameters:
nrow - number of rows
<br>ncol - number of columns
<br>dir - LayoutConstants.ABOVE or LayoutConstants.BELOW or null.  Null means use the current row.

### Returns:
a list of the newly added plots.

<a href="https://github.com/autoplot/dev/search?q=addPlots&unscoped_q=addPlots">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bind"></a>
# bind
bind( org.autoplot.dom.DomNode src, String srcProp, Object dst, String dstProp, Converter converter ) &rarr; void

binds two bean properties together.  Bindings are bidirectional, but
 the initial copy is from src to dst.  In MVC terms, src should be the model
 and dst should be a view.  The properties must fire property
 change events for the binding mechanism to work.  A converter object can be 
 provided that converts the object type between the two nodes.

 BeansBinding library is apparently not thread-safe.
 
 Example:
<blockquote><pre><small>
 model= getApplicationModel()
 bind( model.getPlotDefaults(), "title", model.getPlotDefaults().getXAxis(), "label" )
</small></pre></blockquote>

### Parameters:
src - java bean such as model.getPlotDefaults()
<br>srcProp - a property name such as "title"
<br>dst - java bean such as model.getPlotDefaults().getXAxis()
<br>dstProp - a property name such as "label"
<br>converter - a converter object for the binding.  (e.g. Color name to Color object)

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=bind&unscoped_q=bind">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

bind( org.autoplot.dom.DomNode src, String srcProp, Object dst, String dstProp ) &rarr; void<br>
***
<a name="cancelAllPendingTasks"></a>
# cancelAllPendingTasks
cancelAllPendingTasks(  ) &rarr; void

go through the monitors we keep track of, and cancel each one.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=cancelAllPendingTasks&unscoped_q=cancelAllPendingTasks">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="copyPlot"></a>
# copyPlot
copyPlot( org.autoplot.dom.Plot srcPlot, boolean bindx, boolean bindy, boolean addPlotElement ) &rarr; Plot

Copy the plot and its axis settings, optionally binding the axes. Whether
 the axes are bound or not, the duplicate plot is initially synchronized to
 the source plot.

### Parameters:
srcPlot - The plot to be copied
<br>bindx - If true, X axes are bound.  If the srcPlot x axis is bound to the
    application timerange, then bind to that instead (kludge--handle higher)
<br>bindy - If true, Y axes are bound
<br>addPlotElement - add a plotElement attached to the new plot as well.

### Returns:
The duplicate plot

<a href="https://github.com/autoplot/dev/search?q=copyPlot&unscoped_q=copyPlot">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="copyPlotAndPlotElements"></a>
# copyPlotAndPlotElements
copyPlotAndPlotElements( org.autoplot.dom.Plot domPlot, org.autoplot.dom.DataSourceFilter dsf, boolean bindx, boolean bindy ) &rarr; Plot

copy plot and plotElements into a new plot.

### Parameters:
domPlot - copy this plot.
<br>dsf - if non-null, then use this dataSourceFilter
<br>bindx - If true, X axes are bound.  If the srcPlot x axis is bound to the
    application timerange, then bind to that instead (kludge--handle higher)
<br>bindy - If true, Y axes are bound

### Returns:
the new plot

<a href="https://github.com/autoplot/dev/search?q=copyPlotAndPlotElements&unscoped_q=copyPlotAndPlotElements">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="delete"></a>
# delete
delete( String id ) &rarr; void

delete the named plot, plotElement, annotation, or dataSource

### Parameters:
id - node name like "plot_5", see dom.plots[0].id.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=delete&unscoped_q=delete">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

delete( org.autoplot.dom.DomNode n ) &rarr; void<br>
***
<a name="deleteAnnotation"></a>
# deleteAnnotation
deleteAnnotation( org.autoplot.dom.Annotation c ) &rarr; void

delete the annotation

### Parameters:
c - the annotation

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=deleteAnnotation&unscoped_q=deleteAnnotation">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="deleteBinding"></a>
# <del>deleteBinding</del>
Deprecated: see removeBinding(binding)
***
<a name="deleteConnector"></a>
# deleteConnector
deleteConnector( org.autoplot.dom.Connector connector ) &rarr; void

delete the connector between two plot X axes.

### Parameters:
connector - a Connector

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=deleteConnector&unscoped_q=deleteConnector">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="deleteDataSourceFilter"></a>
# deleteDataSourceFilter
deleteDataSourceFilter( org.autoplot.dom.DataSourceFilter dsf ) &rarr; void

delete the dsf and any parents that deleting it leaves orphaned. (??? maybe they should be called children...)

### Parameters:
dsf - a DataSourceFilter

### Returns:
void (returns nothing)

### See Also:
<a href='DomUtil.md#deleteDataSourceFilter'>DomUtil#deleteDataSourceFilter(org.autoplot.dom.Application, org.autoplot.dom.DataSourceFilter)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=deleteDataSourceFilter&unscoped_q=deleteDataSourceFilter">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="deletePlot"></a>
# deletePlot
deletePlot( org.autoplot.dom.Plot domPlot ) &rarr; void

delete the plot from the application.
 TODO: this should really call the plot.controller.deleteDasPeer()

### Parameters:
domPlot - a Plot

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=deletePlot&unscoped_q=deletePlot">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="deletePlotElement"></a>
# deletePlotElement
deletePlotElement( org.autoplot.dom.PlotElement pelement ) &rarr; void

delete the plot element completely, or if it is the last, then empty the data source.
 Earlier versions of this would throw an exception if the last plotElement was deleted.

### Parameters:
pelement - a PlotElement

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=deletePlotElement&unscoped_q=deletePlotElement">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="doplot"></a>
# doplot
doplot( org.autoplot.dom.Plot plot, org.autoplot.dom.PlotElement pele, String secondaryUri, String teriaryUri, String primaryUri ) &rarr; PlotElement



### Parameters:
plot - a Plot
<br>pele - a PlotElement
<br>secondaryUri - a String
<br>teriaryUri - a String
<br>primaryUri - a String

### Returns:
org.autoplot.dom.PlotElement


<a href="https://github.com/autoplot/dev/search?q=doplot&unscoped_q=doplot">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

doplot( org.autoplot.dom.Plot plot, org.autoplot.dom.PlotElement pele, String secondaryUri, String primaryUri ) &rarr; PlotElement<br>
doplot( org.autoplot.dom.Plot plot, org.autoplot.dom.PlotElement pele, String primaryUri ) &rarr; PlotElement<br>
***
<a name="fillEditPlotMenu"></a>
# fillEditPlotMenu
fillEditPlotMenu( javax.swing.JMenu editPlotMenu, org.autoplot.dom.Plot domPlot ) &rarr; void



### Parameters:
editPlotMenu - a JMenu
<br>domPlot - a Plot

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=fillEditPlotMenu&unscoped_q=fillEditPlotMenu">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="findBinding"></a>
# findBinding
findBinding( org.autoplot.dom.DomNode src, String srcProp, org.autoplot.dom.DomNode dst, String dstProp ) &rarr; BindingModel

Find the binding, if it exists.  All bindingImpls are symmetric, so the src and dst order is ignored in this
 search.

### Parameters:
src - the node (e.g. an Axis)
<br>srcProp - the property name (e.g. "range")
<br>dst - the other node
<br>dstProp - the other node's property name (e.g. "range")

### Returns:
the BindingModel or null if it doesn't exist.

<a href="https://github.com/autoplot/dev/search?q=findBinding&unscoped_q=findBinding">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="findBindings"></a>
# findBindings
findBindings( org.autoplot.dom.DomNode src, String srcProp ) &rarr; List

returns a list of bindings of the node for the property

### Parameters:
src - a DomNode
<br>srcProp - a String

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=findBindings&unscoped_q=findBindings">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

findBindings( org.autoplot.dom.DomNode src, String srcProp, org.autoplot.dom.DomNode dst, String dstProp ) &rarr; List<br>
***
<a name="getApplication"></a>
# getApplication
getApplication(  ) &rarr; Application



### Returns:
org.autoplot.dom.Application


<a href="https://github.com/autoplot/dev/search?q=getApplication&unscoped_q=getApplication">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getApplicationModel"></a>
# getApplicationModel
getApplicationModel(  ) &rarr; ApplicationModel



### Returns:
org.autoplot.ApplicationModel


<a href="https://github.com/autoplot/dev/search?q=getApplicationModel&unscoped_q=getApplicationModel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBindingsFor"></a>
# getBindingsFor
getBindingsFor( org.autoplot.dom.DomNode node ) &rarr; BindingModel



### Parameters:
node - a DomNode

### Returns:
org.autoplot.dom.BindingModel[]


<a href="https://github.com/autoplot/dev/search?q=getBindingsFor&unscoped_q=getBindingsFor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCanvas"></a>
# getCanvas
getCanvas(  ) &rarr; Canvas

focus canvas.  Note there is only one canvas allowed (for now).

### Returns:
the focus canvas.

<a href="https://github.com/autoplot/dev/search?q=getCanvas&unscoped_q=getCanvas">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getColumn"></a>
# getColumn
getColumn(  ) &rarr; DasColumn

get the DasColumn implementation for the marginRow.

### Returns:
the DasColumn implementation for the marginColumn.

<a href="https://github.com/autoplot/dev/search?q=getColumn&unscoped_q=getColumn">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDasCanvas"></a>
# getDasCanvas
getDasCanvas(  ) &rarr; DasCanvas

return the das canvas.

### Returns:
the das canvas.

<a href="https://github.com/autoplot/dev/search?q=getDasCanvas&unscoped_q=getDasCanvas">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSourceFilter"></a>
# getDataSourceFilter
getDataSourceFilter(  ) &rarr; DataSourceFilter

return focus dataSourceFilter.

### Returns:
the focus dataSourceFilter.

<a href="https://github.com/autoplot/dev/search?q=getDataSourceFilter&unscoped_q=getDataSourceFilter">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSourceFilterFor"></a>
# getDataSourceFilterFor
getDataSourceFilterFor( org.autoplot.dom.PlotElement element ) &rarr; DataSourceFilter

return the DataSourceFilter for the plotElement, or null if none exists.

### Parameters:
element - a PlotElement

### Returns:
the DataSourceFilter to which the plot element refers, or null.
### See Also:
<a href='#getFirstPlotFor'>getFirstPlotFor(org.autoplot.dom.DataSourceFilter)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getDataSourceFilterFor&unscoped_q=getDataSourceFilterFor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getElementById"></a>
# getElementById
getElementById( String id ) &rarr; DomNode

return the dom element (plot,axis,etc) with this id.

### Parameters:
id - a String

### Returns:
the DomNode with this id.

<a href="https://github.com/autoplot/dev/search?q=getElementById&unscoped_q=getElementById">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFirstPlotFor"></a>
# getFirstPlotFor
getFirstPlotFor( org.autoplot.dom.DataSourceFilter dsf ) &rarr; Plot

find the first plot that is connected to this data, following vap+internal
 links.  This is used, for example, to get a timerange to control the DSF.

### Parameters:
dsf - a DataSourceFilter

### Returns:
an org.autoplot.dom.Plot


<a href="https://github.com/autoplot/dev/search?q=getFirstPlotFor&unscoped_q=getFirstPlotFor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFocusUri"></a>
# getFocusUri
getFocusUri(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getFocusUri&unscoped_q=getFocusUri">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMonitorFactory"></a>
# getMonitorFactory
getMonitorFactory(  ) &rarr; MonitorFactory

return the source of monitors.

### Returns:
the source of monitors.

<a href="https://github.com/autoplot/dev/search?q=getMonitorFactory&unscoped_q=getMonitorFactory">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNextPlotHoriz"></a>
# getNextPlotHoriz
getNextPlotHoriz( org.autoplot.dom.Plot p, Object dir ) &rarr; Plot



### Parameters:
p - a Plot
<br>dir - an Object

### Returns:
org.autoplot.dom.Plot


<a href="https://github.com/autoplot/dev/search?q=getNextPlotHoriz&unscoped_q=getNextPlotHoriz">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPendingChangeCount"></a>
# getPendingChangeCount
getPendingChangeCount(  ) &rarr; int

get the number of pending changes.  0 means the application is idle.

### Returns:
get the number of pending changes.

<a href="https://github.com/autoplot/dev/search?q=getPendingChangeCount&unscoped_q=getPendingChangeCount">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlot"></a>
# getPlot
getPlot( org.autoplot.dom.Plot p, Object dir ) &rarr; Plot



### Parameters:
p - a Plot
<br>dir - an Object

### Returns:
org.autoplot.dom.Plot


<a href="https://github.com/autoplot/dev/search?q=getPlot&unscoped_q=getPlot">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getPlot(  ) &rarr; Plot<br>
***
<a name="getPlotAbove"></a>
# getPlotAbove
getPlotAbove( org.autoplot.dom.Plot p ) &rarr; Plot

return a plot that is immediately above the given plot.  This
 encapsulates the layout model, and implementation should change.

### Parameters:
p - a Plot

### Returns:
an org.autoplot.dom.Plot


<a href="https://github.com/autoplot/dev/search?q=getPlotAbove&unscoped_q=getPlotAbove">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlotBelow"></a>
# getPlotBelow
getPlotBelow( org.autoplot.dom.Plot p ) &rarr; Plot

return a plot that is immediately below the given plot.  This
 encapsulates the layout model, and implementation should change.

### Parameters:
p - a Plot

### Returns:
an org.autoplot.dom.Plot


<a href="https://github.com/autoplot/dev/search?q=getPlotBelow&unscoped_q=getPlotBelow">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlotElement"></a>
# getPlotElement
getPlotElement(  ) &rarr; PlotElement

return the focus plot element

### Returns:
the focus plot element

<a href="https://github.com/autoplot/dev/search?q=getPlotElement&unscoped_q=getPlotElement">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlotElementsFor"></a>
# getPlotElementsFor
getPlotElementsFor( org.autoplot.dom.Plot plot ) &rarr; List

return the PlotElements for the plot, if any.

### Parameters:
plot - a Plot

### Returns:
list of PlotElements.

<a href="https://github.com/autoplot/dev/search?q=getPlotElementsFor&unscoped_q=getPlotElementsFor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getPlotElementsFor( org.autoplot.dom.DataSourceFilter dsf ) &rarr; List<br>
***
<a name="getPlotFor"></a>
# getPlotFor
getPlotFor( java.awt.Component c ) &rarr; Plot

return the Plot corresponding to the das2 component.

### Parameters:
c - Das2 component such as DasPlot or DasAxis.

### Returns:
an org.autoplot.dom.Plot


<a href="https://github.com/autoplot/dev/search?q=getPlotFor&unscoped_q=getPlotFor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getPlotFor( org.autoplot.dom.PlotElement element ) &rarr; Plot<br>
***
<a name="getPlotsFor"></a>
# getPlotsFor
getPlotsFor( org.autoplot.dom.DataSourceFilter dsf ) &rarr; List

return the Plot using the DataSourceFilter, checking for ticksURI
 as well.  This does not
 return indirect (via vap+internal) references.

### Parameters:
dsf - the data source filter.

### Returns:
return the PlotElements for the data source filter, if any.

<a href="https://github.com/autoplot/dev/search?q=getPlotsFor&unscoped_q=getPlotsFor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRow"></a>
# getRow
getRow(  ) &rarr; DasRow

get the DasRow implementation for the marginRow.

### Returns:
the DasRow implementation for the marginRow.

<a href="https://github.com/autoplot/dev/search?q=getRow&unscoped_q=getRow">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getStatus"></a>
# getStatus
getStatus(  ) &rarr; String

clients can get status here.

### Returns:
the last status message.
### See Also:
<a href='#waitUntilIdle'>waitUntilIdle()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getStatus&unscoped_q=getStatus">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isHeadless"></a>
# isHeadless
isHeadless(  ) &rarr; boolean

true if running in headless environment

### Returns:
true if running in headless environment

<a href="https://github.com/autoplot/dev/search?q=isHeadless&unscoped_q=isHeadless">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isTimeSeriesBrowse"></a>
# isTimeSeriesBrowse
isTimeSeriesBrowse( org.autoplot.dom.Plot p ) &rarr; boolean

return true if the plot has the time series browse capability, meaning
 something will go off and load more data if the time range is changed.
 Note the TSB may be connected to the plot's context property, and 
 the x-axis is not a time axis.

### Parameters:
p - the plot.

### Returns:
true if the plot has the time series browse.

<a href="https://github.com/autoplot/dev/search?q=isTimeSeriesBrowse&unscoped_q=isTimeSeriesBrowse">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="maybeGetApplicatonGUI"></a>
# maybeGetApplicatonGUI
maybeGetApplicatonGUI(  ) &rarr; AutoplotUI

contain the logic which returns a reference to the AutoplotUI, so that 
 this nasty bit of code is contained.

### Returns:
null or the application

<a href="https://github.com/autoplot/dev/search?q=maybeGetApplicatonGUI&unscoped_q=maybeGetApplicatonGUI">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="peekBindingSupport"></a>
# peekBindingSupport
peekBindingSupport(  ) &rarr; BindingSupport

for debugging in scripts.

### Returns:
the BindingSupport object.

<a href="https://github.com/autoplot/dev/search?q=peekBindingSupport&unscoped_q=peekBindingSupport">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="plotUri"></a>
# plotUri
plotUri( String suri, boolean resetPlot ) &rarr; void

provide method for plotting a URI without any axis resetting.

### Parameters:
suri - the URI to plot
<br>resetPlot - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=plotUri&unscoped_q=plotUri">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeActionListener"></a>
# removeActionListener
removeActionListener( java.awt.event.ActionListener list ) &rarr; void



### Parameters:
list - an ActionListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeActionListener&unscoped_q=removeActionListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeBinding"></a>
# removeBinding
removeBinding( org.autoplot.dom.BindingModel binding ) &rarr; void

remove the binding and its implementation.

### Parameters:
binding - a BindingModel

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeBinding&unscoped_q=removeBinding">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reset"></a>
# reset
reset(  ) &rarr; void

resets the dom to the initial state by deleting added 
 plotElements, plots and data sources.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reset&unscoped_q=reset">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setCanvas"></a>
# setCanvas
setCanvas( org.autoplot.dom.Canvas canvas ) &rarr; void

set focus canvas, which must be the one of the canvas the application
 knows about.

### Parameters:
canvas - the new focus canvas.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCanvas&unscoped_q=setCanvas">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataSourceFilter"></a>
# setDataSourceFilter
setDataSourceFilter( org.autoplot.dom.DataSourceFilter dataSourceFilter ) &rarr; void

set the focus dataSourceFilter.

### Parameters:
dataSourceFilter - the focus dataSourceFilter.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSourceFilter&unscoped_q=setDataSourceFilter">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFocusUri"></a>
# setFocusUri
setFocusUri( String focusUri ) &rarr; void



### Parameters:
focusUri - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFocusUri&unscoped_q=setFocusUri">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPendingChangeCount"></a>
# setPendingChangeCount
setPendingChangeCount( int pendingChangeCount ) &rarr; void



### Parameters:
pendingChangeCount - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPendingChangeCount&unscoped_q=setPendingChangeCount">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPlot"></a>
# setPlot
setPlot( org.autoplot.dom.Plot plot ) &rarr; void

This can take a while and should not be called on the event thread.

### Parameters:
plot - a Plot

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPlot&unscoped_q=setPlot">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPlotElement"></a>
# setPlotElement
setPlotElement( org.autoplot.dom.PlotElement plotElement ) &rarr; void

set the focus plot element

### Parameters:
plotElement - the new focus plot element.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPlotElement&unscoped_q=setPlotElement">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setStatus"></a>
# setStatus
setStatus( String status ) &rarr; void

clients can send messages to here.  The message may be conventionally 
 prefixed with "busy:" "error:" or "warning:" (And these will be displayed
 as icons, for example, in the view.)

### Parameters:
status - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setStatus&unscoped_q=setStatus">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showBindings"></a>
# showBindings
showBindings(  ) &rarr; void

show the bindings, for debugging purposes.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showBindings&unscoped_q=showBindings">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="unbind"></a>
# unbind
unbind( org.autoplot.dom.DomNode src, String srcProp, Object dst, String dstProp ) &rarr; void

unbind the binding between a dom node and another object.

### Parameters:
src - a DomNode
<br>srcProp - the property name.
<br>dst - an Object
<br>dstProp - the property name.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=unbind&unscoped_q=unbind">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

unbind( org.autoplot.dom.DomNode src ) &rarr; void<br>
***
<a name="waitUntilIdle"></a>
# waitUntilIdle
waitUntilIdle(  ) &rarr; void

block the calling thread until the application is idle.

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/isPendingChanges/.md'>isPendingChanges.</a> <br>

<a href="https://github.com/autoplot/dev/search?q=waitUntilIdle&unscoped_q=waitUntilIdle">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

