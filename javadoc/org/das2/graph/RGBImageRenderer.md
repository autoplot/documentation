# org.das2.graph.RGBImageRendererRenders RBG images stored in a QDataSet[m,n,3], etc.
RGBImageRenderer( )


***
<a name="PROP_NEARESTNEIGHBORINTERPOLATION"></a>
# PROP_NEARESTNEIGHBORINTERPOLATION



***
<a name="acceptContext"></a>
# acceptContext
acceptContext( int x, int y ) &rarr; boolean



### Parameters:
x - an int
<br>y - an int

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=acceptContext&unscoped_q=acceptContext">[search for examples]</a>

***
<a name="acceptsData"></a>
# acceptsData
acceptsData( QDataSet ds ) &rarr; boolean

accepts either rank2 data with grey scale 0-255, or rank3 (w,h,3 or 4)

### Parameters:
ds - the dataset

### Returns:
true if the dataset is useful.

<a href="https://github.com/autoplot/dev/search?q=acceptsData&unscoped_q=acceptsData">[search for examples]</a>

***
<a name="doAutorange"></a>
# doAutorange
doAutorange( QDataSet ds ) &rarr; QDataSet

autorange on the data, returning a rank 2 bounds for the dataset.

### Parameters:
ds - the dataset

### Returns:
a bounding box
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/examples/Schemes.md#boundingBox'>org.das2.qds.examples.Schemes#boundingBox()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=doAutorange&unscoped_q=doAutorange">[search for examples]</a>

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
<a name="isNearestNeighborInterpolation"></a>
# isNearestNeighborInterpolation
isNearestNeighborInterpolation(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isNearestNeighborInterpolation&unscoped_q=isNearestNeighborInterpolation">[search for examples]</a>

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
<a name="selectionArea"></a>
# selectionArea
selectionArea(  ) &rarr; Shape



### Returns:
java.awt.Shape


<a href="https://github.com/autoplot/dev/search?q=selectionArea&unscoped_q=selectionArea">[search for examples]</a>

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
<a name="setDataSet"></a>
# setDataSet
setDataSet( QDataSet ds ) &rarr; void



### Parameters:
ds - a QDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSet&unscoped_q=setDataSet">[search for examples]</a>

***
<a name="setNearestNeighborInterpolation"></a>
# setNearestNeighborInterpolation
setNearestNeighborInterpolation( boolean nearestNeighborInterpolation ) &rarr; void



### Parameters:
nearestNeighborInterpolation - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setNearestNeighborInterpolation&unscoped_q=setNearestNeighborInterpolation">[search for examples]</a>

***
<a name="updatePlotImage"></a>
# updatePlotImage
updatePlotImage( org.das2.graph.DasAxis xAxis, org.das2.graph.DasAxis yAxis, ProgressMonitor monitor ) &rarr; void

this actually can take a little while, I discovered when playing with the wave-at-cassini image.

### Parameters:
xAxis - a DasAxis
<br>yAxis - a DasAxis
<br>monitor - a ProgressMonitor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=updatePlotImage&unscoped_q=updatePlotImage">[search for examples]</a>

