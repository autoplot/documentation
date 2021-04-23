# org.autoplot.dom.PlotControllerManages a Plot node, for example listening for autoRange updates 
 and layout changes.
PlotController( org.autoplot.dom.Application dom, org.autoplot.dom.Plot domPlot, org.das2.graph.DasPlot dasPlot, org.das2.graph.DasColorBar colorbar )


PlotController( org.autoplot.dom.Application dom, org.autoplot.dom.Plot plot )


***
<a name="pdListen"></a>
# pdListen

the plot elements we listen to for autoranging.

***
<a name="rowColListener"></a>
# rowColListener



***
<a name="PROP_AUTOBINDING"></a>
# PROP_AUTOBINDING

true indicates that the controller is allowed to automatically add
 bindings to the plot axes.

***
<a name="PROP_PLOTELEMENTPROPSMENUITEM"></a>
# PROP_PLOTELEMENTPROPSMENUITEM



***
<a name="contextOverview"></a>
# contextOverview
contextOverview(  ) &rarr; Plot

add a context overview.  This uses controllers, and should be rewritten
 so that it doesn't.

### Returns:
the new plot which is the overview.

<a href="https://github.com/autoplot/dev/search?q=contextOverview&unscoped_q=contextOverview">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="doHints"></a>
# doHints
doHints( org.autoplot.dom.Axis axis, String hintsString ) &rarr; void

implement hints like width=40&amp;includeZero=T.  
 <blockquote><pre>
 includeZero   T or F     make sure that zero is within the result.
 width         30nT       use this width.  This is a formatted datum which 
                          is parsed with the units of the axis, or with the number of cycles for log.
 log           T or F     force log or linear axis
 widths        30nT,300nT,3000nT   use one of these widths
 center        0          constrain the center to be this location
 (not yet) reluctant     T or F     use the old range if it is acceptable.
 </pre></blockquote>

### Parameters:
axis - the axis to which we are applying the hints.
<br>hintsString - the string, ampersand-delimited; or null when no hints should be applied.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=doHints&unscoped_q=doHints">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getApplication"></a>
# getApplication
getApplication(  ) &rarr; Application



### Returns:
org.autoplot.dom.Application


<a href="https://github.com/autoplot/dev/search?q=getApplication&unscoped_q=getApplication">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBindings"></a>
# getBindings
getBindings(  ) &rarr; BindingModel



### Returns:
org.autoplot.dom.BindingModel[]


<a href="https://github.com/autoplot/dev/search?q=getBindings&unscoped_q=getBindings">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getBindings( int index ) &rarr; BindingModel<br>
***
<a name="getColumn"></a>
# getColumn
getColumn(  ) &rarr; Column

return the row for this plot.  This just calls dom.canvases.get(0).getController().getRowFor(this.plot);

### Returns:
an org.autoplot.dom.Column


<a href="https://github.com/autoplot/dev/search?q=getColumn&unscoped_q=getColumn">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDasColorBar"></a>
# getDasColorBar
getDasColorBar(  ) &rarr; DasColorBar



### Returns:
org.das2.graph.DasColorBar


<a href="https://github.com/autoplot/dev/search?q=getDasColorBar&unscoped_q=getDasColorBar">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDasPlot"></a>
# getDasPlot
getDasPlot(  ) &rarr; DasPlot



### Returns:
org.das2.graph.DasPlot


<a href="https://github.com/autoplot/dev/search?q=getDasPlot&unscoped_q=getDasPlot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getExpertMenuItems"></a>
# getExpertMenuItems
getExpertMenuItems(  ) &rarr; JMenuItem



### Returns:
javax.swing.JMenuItem[]


<a href="https://github.com/autoplot/dev/search?q=getExpertMenuItems&unscoped_q=getExpertMenuItems">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlot"></a>
# getPlot
getPlot(  ) &rarr; Plot



### Returns:
org.autoplot.dom.Plot


<a href="https://github.com/autoplot/dev/search?q=getPlot&unscoped_q=getPlot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlotElement"></a>
# getPlotElement
getPlotElement(  ) &rarr; PlotElement

return the plotElement we are listening to.

### Returns:
an org.autoplot.dom.PlotElement


<a href="https://github.com/autoplot/dev/search?q=getPlotElement&unscoped_q=getPlotElement">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlotElementPropsMenuItem"></a>
# getPlotElementPropsMenuItem
getPlotElementPropsMenuItem(  ) &rarr; JMenuItem



### Returns:
javax.swing.JMenuItem


<a href="https://github.com/autoplot/dev/search?q=getPlotElementPropsMenuItem&unscoped_q=getPlotElementPropsMenuItem">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRow"></a>
# getRow
getRow(  ) &rarr; Row

return the row for this plot.  This just calls dom.canvases.get(0).getController().getRowFor(this.plot);

### Returns:
an org.autoplot.dom.Row


<a href="https://github.com/autoplot/dev/search?q=getRow&unscoped_q=getRow">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isAutoBinding"></a>
# isAutoBinding
isAutoBinding(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isAutoBinding&unscoped_q=isAutoBinding">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resetZoom"></a>
# resetZoom
resetZoom( boolean x, boolean y, boolean z ) &rarr; void

set the zoom so that all of the plotElements' data is visible.  This means finding
 the "union" of the plotElements' plotDefault ranges.  If any plotElement's default log
 is false, then the new setting will be false.

### Parameters:
x - reset zoom in the x dimension.
<br>y - reset zoom in the y dimension.
<br>z - reset zoom in the z dimension.

### Returns:
void (returns nothing)

### See Also:
<a href='AutoplotUtil.md#resetZoomX'>AutoplotUtil#resetZoomX(org.autoplot.dom.Application, org.autoplot.dom.Plot)</a> <br>
<a href='AutoplotUtil.md#resetZoomY'>AutoplotUtil#resetZoomY(org.autoplot.dom.Application, org.autoplot.dom.Plot)</a> <br>
<a href='AutoplotUtil.md#resetZoomZ'>AutoplotUtil#resetZoomZ(org.autoplot.dom.Application, org.autoplot.dom.Plot)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=resetZoom&unscoped_q=resetZoom">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAutoBinding"></a>
# setAutoBinding
setAutoBinding( boolean autoBinding ) &rarr; void



### Parameters:
autoBinding - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAutoBinding&unscoped_q=setAutoBinding">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setExpertMenuItems"></a>
# setExpertMenuItems
setExpertMenuItems( javax.swing.JMenuItem[] items ) &rarr; void

provide spot to locate the menu items that are hidden in basic mode.

### Parameters:
items - a javax.swing.JMenuItem[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setExpertMenuItems&unscoped_q=setExpertMenuItems">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setExpertMode"></a>
# setExpertMode
setExpertMode( boolean expert ) &rarr; void



### Parameters:
expert - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setExpertMode&unscoped_q=setExpertMode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPlotElementPropsMenuItem"></a>
# setPlotElementPropsMenuItem
setPlotElementPropsMenuItem( javax.swing.JMenuItem pelePropsMenuItem ) &rarr; void



### Parameters:
pelePropsMenuItem - a JMenuItem

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPlotElementPropsMenuItem&unscoped_q=setPlotElementPropsMenuItem">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTitleAutomatically"></a>
# setTitleAutomatically
setTitleAutomatically( String title ) &rarr; void

set the title, leaving autoLabel true.

### Parameters:
title - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTitleAutomatically&unscoped_q=setTitleAutomatically">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toBottom"></a>
# toBottom
toBottom( org.autoplot.dom.PlotElement p ) &rarr; void

move the plot element to the bottom.

### Parameters:
p - a PlotElement

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=toBottom&unscoped_q=toBottom">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toTop"></a>
# toTop
toTop( org.autoplot.dom.PlotElement p ) &rarr; void

move the plot element to the top.

### Parameters:
p - the plot element

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=toTop&unscoped_q=toTop">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

