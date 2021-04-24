# org.autoplot.dom.DomOps

Many operations are defined within the DOM object controllers that needn't
 be.  This class is a place for operations that are performed on the DOM
 independent of the controllers.  For example, the operation to swap the
 position of two plots is easily implemented by changing the rowid and columnid
 properties of the two plots.

# DomOps( )


***
<a name="aggregateAll"></a>
# aggregateAll
aggregateAll( org.autoplot.dom.Application dom ) &rarr; void

aggregate all the URIs within the dom.

### Parameters:
dom - an Application

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=aggregateAll&unscoped_q=aggregateAll">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bottomAndTopMostPlot"></a>
# bottomAndTopMostPlot
bottomAndTopMostPlot( org.autoplot.dom.Application dom, java.util.List plots ) &rarr; Plot

return the bottom and top most plot of a list of plots.  
 This does use controllers.

### Parameters:
dom - an Application
<br>plots - a java.util.List

### Returns:
an org.autoplot.dom.Plot[]


<a href="https://github.com/autoplot/dev/search?q=bottomAndTopMostPlot&unscoped_q=bottomAndTopMostPlot">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="copyPlot"></a>
# copyPlot
copyPlot( org.autoplot.dom.Plot srcPlot, boolean bindx, boolean bindy, Object direction ) &rarr; Plot

Copy the plot and its axis settings, optionally binding the axes. Whether
 the axes are bound or not, the duplicate plot is initially synchronized to
 the source plot.
 See {@link org.autoplot.dom.ApplicationController#copyPlot(org.autoplot.dom.Plot, boolean, boolean, boolean) copyPlot}

### Parameters:
srcPlot - a Plot
<br>bindx - a boolean
<br>bindy - a boolean
<br>direction - an Object

### Returns:
the new plot

<a href="https://github.com/autoplot/dev/search?q=copyPlot&unscoped_q=copyPlot">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="copyPlotAndPlotElements"></a>
# copyPlotAndPlotElements
copyPlotAndPlotElements( org.autoplot.dom.Plot srcPlot, boolean copyPlotElements, boolean bindx, boolean bindy, Object direction ) &rarr; Plot

copyPlotAndPlotElements.  This does not appear to be used.
 See {@link org.autoplot.dom.ApplicationController#copyPlotAndPlotElements(org.autoplot.dom.Plot, org.autoplot.dom.DataSourceFilter, boolean, boolean) copyPlotAndPlotElements}

### Parameters:
srcPlot - a Plot
<br>copyPlotElements - a boolean
<br>bindx - a boolean
<br>bindy - a boolean
<br>direction - an Object

### Returns:
an org.autoplot.dom.Plot


<a href="https://github.com/autoplot/dev/search?q=copyPlotAndPlotElements&unscoped_q=copyPlotAndPlotElements">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="copyPlotElements"></a>
# copyPlotElements
copyPlotElements( org.autoplot.dom.Plot srcPlot, org.autoplot.dom.Plot dstPlot ) &rarr; List

copy the plot elements from srcPlot to dstPlot.  This does not appear
 to be used.
 See {@link org.autoplot.dom.ApplicationController#copyPlotElement(org.autoplot.dom.PlotElement, org.autoplot.dom.Plot, org.autoplot.dom.DataSourceFilter) copyPlotElement}

### Parameters:
srcPlot - plot containing zero or more plotElements.
<br>dstPlot - destination for the plotElements.

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=copyPlotElements&unscoped_q=copyPlotElements">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="fixLayout"></a>
# fixLayout
fixLayout( org.autoplot.dom.Application dom ) &rarr; void

New layout mechanism which fixes a number of shortcomings of the old layout mechanism, 
 newCanvasLayout.  This one:<ul>
 <li> Removes extra whitespace
 <li> Preserves relative size weights.
 <li> Preserves em heights, to support components which should not be rescaled. (Not yet supported.)
 <li> Preserves space taken by strange objects, to support future canvas components.
 <li> Renormalizes the margin row, so it is nice. (Not yet supported.  This should consider font size, where large fonts don't need so much space.)
 </ul>
 This should also be idempotent, where calling this a second time should have no effect.

### Parameters:
dom - an application state, with controller nodes. TODO: remove dependence on controller nodes.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=fixLayout&unscoped_q=fixLayout">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getOrCreateSelectedColumn"></a>
# getOrCreateSelectedColumn
getOrCreateSelectedColumn( org.autoplot.dom.Application dom, java.util.List selectedPlots, boolean create ) &rarr; Column

Used in the LayoutPanel's add hidden plot, get the column of 
 the selected plot or create a new column if several plots are
 selected.

### Parameters:
dom - the application.
<br>selectedPlots - the selected plots.
<br>create - allow a new column to be created.

### Returns:
an org.autoplot.dom.Column


<a href="https://github.com/autoplot/dev/search?q=getOrCreateSelectedColumn&unscoped_q=getOrCreateSelectedColumn">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getOrCreateSelectedRow"></a>
# getOrCreateSelectedRow
getOrCreateSelectedRow( org.autoplot.dom.Application dom, java.util.List selectedPlots, boolean create ) &rarr; Row

Used in the LayoutPanel's add hidden plot, get the row of 
 the selected plot or create a new row if several plots are
 selected.

### Parameters:
dom - the application.
<br>selectedPlots - the selected plots.
<br>create - allow a new column to be created.

### Returns:
an org.autoplot.dom.Row


<a href="https://github.com/autoplot/dev/search?q=getOrCreateSelectedRow&unscoped_q=getOrCreateSelectedRow">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlotsFor"></a>
# getPlotsFor
getPlotsFor( org.autoplot.dom.Application dom, org.autoplot.dom.Row row, boolean visible ) &rarr; List

return a list of the plots using the given row.
 This does not use controllers.

### Parameters:
dom - a dom
<br>row - the row to search for.
<br>visible - if true, then the plot must also be visible.  (Note its colorbar visible is ignored.)

### Returns:
a list of plots.

<a href="https://github.com/autoplot/dev/search?q=getPlotsFor&unscoped_q=getPlotsFor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="newCanvasLayout"></a>
# newCanvasLayout
newCanvasLayout( org.autoplot.dom.Application dom ) &rarr; void

play with new canvas layout.  This started as a Jython Script, but it's faster to implement here.
 See http://autoplot.org/developer.autolayout#Algorithm

### Parameters:
dom - an Application

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=newCanvasLayout&unscoped_q=newCanvasLayout">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="swapPosition"></a>
# swapPosition
swapPosition( org.autoplot.dom.Plot a, org.autoplot.dom.Plot b ) &rarr; void

swap the position of the two plots.  If one plot has its tick labels hidden,
 then this is swapped as well.

### Parameters:
a - a Plot
<br>b - a Plot

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=swapPosition&unscoped_q=swapPosition">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

