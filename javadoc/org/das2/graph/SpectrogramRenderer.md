# org.das2.graph.SpectrogramRenderer

Renderer for spectrograms.  A setting for rebinning data controls how data is binned into pixel space,
 for example by nearest neighbor or interpolation.

# SpectrogramRenderer( org.das2.dataset.DataSetDescriptor dsd, org.das2.graph.DasColorBar colorBar )


***
<a name="CONTROL_KEY_REBIN"></a>
# CONTROL_KEY_REBIN



***
<a name="PROP_REBINNER"></a>
# PROP_REBINNER



***
<a name="PROP_CADENCECHECK"></a>
# PROP_CADENCECHECK



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
<a name="getConsumedDataSet"></a>
# getConsumedDataSet
getConsumedDataSet(  ) &rarr; QDataSet



### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=getConsumedDataSet&unscoped_q=getConsumedDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getControl"></a>
# getControl
getControl(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getControl&unscoped_q=getControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFillColor"></a>
# getFillColor
getFillColor(  ) &rarr; Color

Getter for property fillColor.

### Returns:
Value of property fillColor.

<a href="https://github.com/autoplot/dev/search?q=getFillColor&unscoped_q=getFillColor">[search for examples]</a>

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
<a name="getListLabel"></a>
# getListLabel
getListLabel(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getListLabel&unscoped_q=getListLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRebinner"></a>
# getRebinner
getRebinner(  ) &rarr; RebinnerEnum

Getter for property rebinner.

### Returns:
Value of property rebinner.

<a href="https://github.com/autoplot/dev/search?q=getRebinner&unscoped_q=getRebinner">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getZAxis"></a>
# getZAxis
getZAxis(  ) &rarr; DasAxis



### Returns:
org.das2.graph.DasAxis


<a href="https://github.com/autoplot/dev/search?q=getZAxis&unscoped_q=getZAxis">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isCadenceCheck"></a>
# isCadenceCheck
isCadenceCheck(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isCadenceCheck&unscoped_q=isCadenceCheck">[search for examples]</a>

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
<a name="isSliceRebinnedData"></a>
# isSliceRebinnedData
isSliceRebinnedData(  ) &rarr; boolean

Getter for property sliceRebinnedData.

### Returns:
Value of property sliceRebinnedData.

<a href="https://github.com/autoplot/dev/search?q=isSliceRebinnedData&unscoped_q=isSliceRebinnedData">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="selectionArea"></a>
# selectionArea
selectionArea(  ) &rarr; Shape

return the shape or null.

### Returns:
a java.awt.Shape


<a href="https://github.com/autoplot/dev/search?q=selectionArea&unscoped_q=selectionArea">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setCadenceCheck"></a>
# setCadenceCheck
setCadenceCheck( boolean cadenceCheck ) &rarr; void

If true, then use a cadence estimate to determine and indicate data gaps.

### Parameters:
cadenceCheck - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCadenceCheck&unscoped_q=setCadenceCheck">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setColorBar"></a>
# setColorBar
setColorBar( org.das2.graph.DasColorBar cb ) &rarr; void



### Parameters:
cb - a DasColorBar

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setColorBar&unscoped_q=setColorBar">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setControl"></a>
# setControl
setControl( String s ) &rarr; void



### Parameters:
s - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setControl&unscoped_q=setControl">[search for examples]</a>

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
<a name="setFillColor"></a>
# setFillColor
setFillColor( java.awt.Color fillColor ) &rarr; void

Setter for property fillColor.

### Parameters:
fillColor - New value of property fillColor.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFillColor&unscoped_q=setFillColor">[search for examples]</a>

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
<a name="setRebinner"></a>
# setRebinner
setRebinner( org.das2.graph.SpectrogramRenderer.RebinnerEnum rebinnerEnum ) &rarr; void

Setter for property rebinner.

### Parameters:
rebinnerEnum - New value of property rebinner.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRebinner&unscoped_q=setRebinner">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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

