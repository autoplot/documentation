# org.das2.graph.StackedHistogramRenderer
StackedHistogramRenderer( org.das2.graph.DasAxis zAxis )


StackedHistogramRenderer( org.das2.graph.DasPlot parent, org.das2.dataset.DataSetDescriptor dsd, org.das2.graph.DasAxis zAxis, org.das2.graph.DasAxis yAxis )


***
<a name="getControl"></a>
# getControl
getControl(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getControl&unscoped_q=getControl">[search for examples]</a>

***
<a name="getListIcon"></a>
# getListIcon
getListIcon(  ) &rarr; Icon



### Returns:
javax.swing.Icon


<a href="https://github.com/autoplot/dev/search?q=getListIcon&unscoped_q=getListIcon">[search for examples]</a>

***
<a name="getListLabel"></a>
# getListLabel
getListLabel(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getListLabel&unscoped_q=getListLabel">[search for examples]</a>

***
<a name="getPeaksIndicator"></a>
# getPeaksIndicator
getPeaksIndicator(  ) &rarr; PeaksIndicator

Getter for property peaksIndicator.

### Returns:
Value of property peaksIndicator.

<a href="https://github.com/autoplot/dev/search?q=getPeaksIndicator&unscoped_q=getPeaksIndicator">[search for examples]</a>

***
<a name="getZAxis"></a>
# getZAxis
getZAxis(  ) &rarr; DasAxis



### Returns:
org.das2.graph.DasAxis


<a href="https://github.com/autoplot/dev/search?q=getZAxis&unscoped_q=getZAxis">[search for examples]</a>

***
<a name="isSliceRebinnedData"></a>
# isSliceRebinnedData
isSliceRebinnedData(  ) &rarr; boolean

Getter for property sliceRebinnedData.

### Returns:
Value of property sliceRebinnedData.

<a href="https://github.com/autoplot/dev/search?q=isSliceRebinnedData&unscoped_q=isSliceRebinnedData">[search for examples]</a>

***
<a name="propertyChange"></a>
# propertyChange
propertyChange( java.beans.PropertyChangeEvent e ) &rarr; void



### Parameters:
e - a PropertyChangeEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=propertyChange&unscoped_q=propertyChange">[search for examples]</a>

***
<a name="render"></a>
# render
render( java.awt.Graphics2D g, org.das2.graph.DasAxis xAxis, org.das2.graph.DasAxis yAxis ) &rarr; void



### Parameters:
g - a Graphics2D
<br>xAxis - a DasAxis
<br>yAxis - a DasAxis

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=render&unscoped_q=render">[search for examples]</a>

***
<a name="setControl"></a>
# setControl
setControl( String s ) &rarr; void



### Parameters:
s - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setControl&unscoped_q=setControl">[search for examples]</a>

***
<a name="setPeaksIndicator"></a>
# setPeaksIndicator
setPeaksIndicator( org.das2.graph.StackedHistogramRenderer.PeaksIndicator peaksIndicator ) &rarr; void

Setter for property peaksIndicator.

### Parameters:
peaksIndicator - New value of property peaksIndicator.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPeaksIndicator&unscoped_q=setPeaksIndicator">[search for examples]</a>

***
<a name="setSliceRebinnedData"></a>
# setSliceRebinnedData
setSliceRebinnedData( boolean sliceRebinnedData ) &rarr; void

Setter for property sliceRebinnedData.

### Parameters:
sliceRebinnedData - New value of property sliceRebinnedData.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSliceRebinnedData&unscoped_q=setSliceRebinnedData">[search for examples]</a>

***
<a name="setYAxis"></a>
# setYAxis
setYAxis( org.das2.graph.DasAxis yAxis ) &rarr; void

This sets the yAxis and adds itself to the axis property change listener.
 TODO: why must this Renderer be special and have a separate set y axis?

### Parameters:
yAxis - the new yAxis

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setYAxis&unscoped_q=setYAxis">[search for examples]</a>

***
<a name="setZAxis"></a>
# setZAxis
setZAxis( org.das2.graph.DasAxis zAxis ) &rarr; void



### Parameters:
zAxis - a DasAxis

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setZAxis&unscoped_q=setZAxis">[search for examples]</a>

***
<a name="setZTitle"></a>
# setZTitle
setZTitle( String title ) &rarr; void



### Parameters:
title - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setZTitle&unscoped_q=setZTitle">[search for examples]</a>

***
<a name="updatePlotImage"></a>
# updatePlotImage
updatePlotImage( org.das2.graph.DasAxis xAxis, org.das2.graph.DasAxis yAxis_1, ProgressMonitor monitor ) &rarr; void



### Parameters:
xAxis - a DasAxis
<br>yAxis_1 - a DasAxis
<br>monitor - a ProgressMonitor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=updatePlotImage&unscoped_q=updatePlotImage">[search for examples]</a>

