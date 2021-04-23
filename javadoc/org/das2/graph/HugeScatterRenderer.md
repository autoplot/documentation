# org.das2.graph.HugeScatterRendererHugeScatterRenderer

 This renderer can handle vector data sets with hundreds of thousands of points
 by histogramming the points and then creating a greyscale spectrogram of
 the histogram.  The property "saturationHitCount" defines the number of pixel
 hits that will make the pixel black.  
 
 This has been modified a lot over the years:<ul>
 <li> connecting lines when the data is of timeseries, 
 <li> alternate modes are used when we zoom in closely,
 <li> support for QDataSets and waveform scheme data,
 <li> lone pixels are highlighted.
 </ul>
 
 Created on April 14, 2005, 8:45 PM
HugeScatterRenderer( org.das2.dataset.DataSetDescriptor dsd )


***
<a name="PROP_ENVELOPE"></a>
# PROP_ENVELOPE



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

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="doAutorange"></a>
# doAutorange
doAutorange( QDataSet ds ) &rarr; QDataSet



### Parameters:
ds - a QDataSet

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=doAutorange&unscoped_q=doAutorange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getColor"></a>
# getColor
getColor(  ) &rarr; Color



### Returns:
java.awt.Color


<a href="https://github.com/autoplot/dev/search?q=getColor&unscoped_q=getColor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getEnvelope"></a>
# getEnvelope
getEnvelope(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getEnvelope&unscoped_q=getEnvelope">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getListIcon"></a>
# getListIcon
getListIcon(  ) &rarr; Icon



### Returns:
javax.swing.Icon


<a href="https://github.com/autoplot/dev/search?q=getListIcon&unscoped_q=getListIcon">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSaturationHitCount"></a>
# getSaturationHitCount
getSaturationHitCount(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getSaturationHitCount&unscoped_q=getSaturationHitCount">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isPrint300dpi"></a>
# isPrint300dpi
isPrint300dpi(  ) &rarr; boolean

Getter for property draw300dpi.

### Returns:
Value of property draw300dpi.

<a href="https://github.com/autoplot/dev/search?q=isPrint300dpi&unscoped_q=isPrint300dpi">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="render"></a>
# render
render( java.awt.Graphics2D g1, org.das2.graph.DasAxis xAxis, org.das2.graph.DasAxis yAxis ) &rarr; void



### Parameters:
g1 - a Graphics2D
<br>xAxis - a DasAxis
<br>yAxis - a DasAxis

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=render&unscoped_q=render">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="selectionArea"></a>
# selectionArea
selectionArea(  ) &rarr; Shape

return a Shape object showing where the data lie and focus should be accepted.

### Returns:
a java.awt.Shape


<a href="https://github.com/autoplot/dev/search?q=selectionArea&unscoped_q=selectionArea">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setColor"></a>
# setColor
setColor( java.awt.Color color ) &rarr; void



### Parameters:
color - a Color

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setColor&unscoped_q=setColor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataSet"></a>
# setDataSet
setDataSet( QDataSet ds ) &rarr; void



### Parameters:
ds - a QDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSet&unscoped_q=setDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setEnvelope"></a>
# setEnvelope
setEnvelope( int envelope ) &rarr; void

0=none. 1=faint envelope with points on top.  2=only envelope

### Parameters:
envelope - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setEnvelope&unscoped_q=setEnvelope">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPrint300dpi"></a>
# setPrint300dpi
setPrint300dpi( boolean print300dpi ) &rarr; void

Setter for property draw300dpi.

### Parameters:
print300dpi - New value of property draw300dpi.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPrint300dpi&unscoped_q=setPrint300dpi">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSaturationHitCount"></a>
# setSaturationHitCount
setSaturationHitCount( int d ) &rarr; void



### Parameters:
d - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSaturationHitCount&unscoped_q=setSaturationHitCount">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="updatePlotImage"></a>
# updatePlotImage
updatePlotImage( org.das2.graph.DasAxis xAxis, org.das2.graph.DasAxis yAxis, ProgressMonitor monitor ) &rarr; void



### Parameters:
xAxis - a DasAxis
<br>yAxis - a DasAxis
<br>monitor - a ProgressMonitor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=updatePlotImage&unscoped_q=updatePlotImage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

