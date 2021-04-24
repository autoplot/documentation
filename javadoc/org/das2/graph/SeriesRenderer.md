# org.das2.graph.SeriesRenderer

SeriesRender is a high-performance replacement for the SymbolLineRenderer.
 The SymbolLineRenderer is limited to about 30,000 points, beyond which 
 contracts for speed start breaking, degrading usability.  The goal of the
 SeriesRenderer is to plot 1,000,000 points without breaking the contracts.
 
 It should be said that five years after its introduction that it's still quite limited.
 
 The SeriesRenderer has a few additional features, such as error bars and 
 fill-to-reference.  These are implemented as "render elements" so that work 
 is encapsulated.

# SeriesRenderer( )


***
<a name="PROP_SHOWLIMITS"></a>
# PROP_SHOWLIMITS



***
<a name="PROP_ADDITIONALCLIP"></a>
# PROP_ADDITIONALCLIP



***
<a name="PROP_DRAWERROR"></a>
# PROP_DRAWERROR



***
<a name="PROP_BACKGROUNDWIDTH"></a>
# PROP_BACKGROUNDWIDTH



***
<a name="PROP_FILLDIRECTION"></a>
# PROP_FILLDIRECTION



***
<a name="PROP_ERRORBARTYPE"></a>
# PROP_ERRORBARTYPE



***
<a name="PROP_STAMPPSYMS"></a>
# PROP_STAMPPSYMS



***
<a name="PROP_UPDATESPOINTSPERMILLISECOND"></a>
# PROP_UPDATESPOINTSPERMILLISECOND



***
<a name="PROP_RENDERPOINTSPERMILLISECOND"></a>
# PROP_RENDERPOINTSPERMILLISECOND



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
<a name="acceptsDataSet"></a>
# acceptsDataSet
acceptsDataSet( QDataSet dataSet ) &rarr; boolean



### Parameters:
dataSet - a QDataSet

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=acceptsDataSet&unscoped_q=acceptsDataSet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="drawListIcon"></a>
# drawListIcon
drawListIcon( java.awt.Graphics2D g1, int x, int y ) &rarr; void



### Parameters:
g1 - a Graphics2D
<br>x - an int
<br>y - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=drawListIcon&unscoped_q=drawListIcon">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBackgroundThick"></a>
# getBackgroundThick
getBackgroundThick(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getBackgroundThick&unscoped_q=getBackgroundThick">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getColor"></a>
# getColor
getColor(  ) &rarr; Color

Getter for property color.

### Returns:
Value of property color.

<a href="https://github.com/autoplot/dev/search?q=getColor&unscoped_q=getColor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getColorByDataSetId"></a>
# getColorByDataSetId
getColorByDataSetId(  ) &rarr; String

Getter for property colorByDataSetId.

### Returns:
Value of property colorByDataSetId.

<a href="https://github.com/autoplot/dev/search?q=getColorByDataSetId&unscoped_q=getColorByDataSetId">[search for examples]</a>
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
<a name="getDOMElement"></a>
# getDOMElement
getDOMElement( org.w3c.dom.Document document ) &rarr; Element



### Parameters:
document - a Document

### Returns:
org.w3c.dom.Element


<a href="https://github.com/autoplot/dev/search?q=getDOMElement&unscoped_q=getDOMElement">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSetSizeLimit"></a>
# getDataSetSizeLimit
getDataSetSizeLimit(  ) &rarr; int

Getter for property dataSetSizeLimit.

### Returns:
Value of property dataSetSizeLimit.

<a href="https://github.com/autoplot/dev/search?q=getDataSetSizeLimit&unscoped_q=getDataSetSizeLimit">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getErrorBarType"></a>
# getErrorBarType
getErrorBarType(  ) &rarr; ErrorBarType



### Returns:
org.das2.graph.ErrorBarType


<a href="https://github.com/autoplot/dev/search?q=getErrorBarType&unscoped_q=getErrorBarType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFillColor"></a>
# getFillColor
getFillColor(  ) &rarr; Color

Getter for property fillReference.

### Returns:
Value of property fillReference.

<a href="https://github.com/autoplot/dev/search?q=getFillColor&unscoped_q=getFillColor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFillDirection"></a>
# getFillDirection
getFillDirection(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getFillDirection&unscoped_q=getFillDirection">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFillStyle"></a>
# getFillStyle
getFillStyle(  ) &rarr; FillStyle

how each plot symbol is filled.

### Returns:
an org.das2.graph.FillStyle


<a href="https://github.com/autoplot/dev/search?q=getFillStyle&unscoped_q=getFillStyle">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFirstIndex"></a>
# getFirstIndex
getFirstIndex(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getFirstIndex&unscoped_q=getFirstIndex">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLastIndex"></a>
# getLastIndex
getLastIndex(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getLastIndex&unscoped_q=getLastIndex">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLineWidth"></a>
# getLineWidth
getLineWidth(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=getLineWidth&unscoped_q=getLineWidth">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getListIcon"></a>
# getListIcon
getListIcon(  ) &rarr; Icon

get an Icon representing the trace.  This will be an ImageIcon.
 TODO: cache the result to support use in legend.

### Returns:
a javax.swing.Icon


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
<a name="getPsym"></a>
# getPsym
getPsym(  ) &rarr; PlotSymbol

Getter for property psym.

### Returns:
Value of property psym.

<a href="https://github.com/autoplot/dev/search?q=getPsym&unscoped_q=getPsym">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPsymConnector"></a>
# getPsymConnector
getPsymConnector(  ) &rarr; PsymConnector



### Returns:
org.das2.graph.PsymConnector


<a href="https://github.com/autoplot/dev/search?q=getPsymConnector&unscoped_q=getPsymConnector">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getReference"></a>
# getReference
getReference(  ) &rarr; Datum

Getter for property reference.

### Returns:
Value of property reference.

<a href="https://github.com/autoplot/dev/search?q=getReference&unscoped_q=getReference">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRenderPointsPerMillisecond"></a>
# getRenderPointsPerMillisecond
getRenderPointsPerMillisecond(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=getRenderPointsPerMillisecond&unscoped_q=getRenderPointsPerMillisecond">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSymSize"></a>
# getSymSize
getSymSize(  ) &rarr; double

Getter for property symsize.

### Returns:
Value of property symsize.

<a href="https://github.com/autoplot/dev/search?q=getSymSize&unscoped_q=getSymSize">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getUpdatesPointsPerMillisecond"></a>
# getUpdatesPointsPerMillisecond
getUpdatesPointsPerMillisecond(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=getUpdatesPointsPerMillisecond&unscoped_q=getUpdatesPointsPerMillisecond">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isAdditionalClip"></a>
# isAdditionalClip
isAdditionalClip(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isAdditionalClip&unscoped_q=isAdditionalClip">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isAntiAliased"></a>
# isAntiAliased
isAntiAliased(  ) &rarr; boolean

Getter for property antiAliased.

### Returns:
Value of property antiAliased.

<a href="https://github.com/autoplot/dev/search?q=isAntiAliased&unscoped_q=isAntiAliased">[search for examples]</a>
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
<a name="isDrawError"></a>
# isDrawError
isDrawError(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isDrawError&unscoped_q=isDrawError">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isFillToReference"></a>
# isFillToReference
isFillToReference(  ) &rarr; boolean

Getter for property fillToReference.

### Returns:
Value of property fillToReference.

<a href="https://github.com/autoplot/dev/search?q=isFillToReference&unscoped_q=isFillToReference">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isHistogram"></a>
# isHistogram
isHistogram(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isHistogram&unscoped_q=isHistogram">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isResetDebugCounters"></a>
# isResetDebugCounters
isResetDebugCounters(  ) &rarr; boolean

Getter for property resetDebugCounters.

### Returns:
Value of property resetDebugCounters.

<a href="https://github.com/autoplot/dev/search?q=isResetDebugCounters&unscoped_q=isResetDebugCounters">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isShowLimits"></a>
# isShowLimits
isShowLimits(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isShowLimits&unscoped_q=isShowLimits">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isSimplifyPaths"></a>
# isSimplifyPaths
isSimplifyPaths(  ) &rarr; boolean

Getter for property simplifyPaths.

### Returns:
Value of property simplifyPaths.

<a href="https://github.com/autoplot/dev/search?q=isSimplifyPaths&unscoped_q=isSimplifyPaths">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isStampPsyms"></a>
# isStampPsyms
isStampPsyms(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isStampPsyms&unscoped_q=isStampPsyms">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="render"></a>
# render
render( java.awt.Graphics2D g, org.das2.graph.DasAxis xAxis, org.das2.graph.DasAxis yAxis ) &rarr; void

render the dataset by delegating to internal components such as the symbol connector and error bars.

### Parameters:
g - the graphics context.
<br>xAxis - the x axis
<br>yAxis - the y axis

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=render&unscoped_q=render">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="selectionArea"></a>
# selectionArea
selectionArea(  ) &rarr; Shape

like accept context, but provides a shape to indicate selection.  This
 should be roughly the same as the locus of points where acceptContext is
 true.

### Returns:
a java.awt.Shape


<a href="https://github.com/autoplot/dev/search?q=selectionArea&unscoped_q=selectionArea">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setActive"></a>
# setActive
setActive( boolean active ) &rarr; void



### Parameters:
active - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setActive&unscoped_q=setActive">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAdditionalClip"></a>
# setAdditionalClip
setAdditionalClip( boolean additionalClip ) &rarr; void



### Parameters:
additionalClip - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAdditionalClip&unscoped_q=setAdditionalClip">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAntiAliased"></a>
# setAntiAliased
setAntiAliased( boolean antiAliased ) &rarr; void

Setter for property antiAliased.

### Parameters:
antiAliased - New value of property antiAliased.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAntiAliased&unscoped_q=setAntiAliased">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setBackgroundThick"></a>
# setBackgroundThick
setBackgroundThick( String backgroundThick ) &rarr; void

set the width of background lines, for example "2em" is twice the 
 thickness of the line.

### Parameters:
backgroundThick - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setBackgroundThick&unscoped_q=setBackgroundThick">[search for examples]</a>
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
<a name="setColor"></a>
# setColor
setColor( java.awt.Color color ) &rarr; void

Setter for property color.

### Parameters:
color - New value of property color.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setColor&unscoped_q=setColor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setColorBar"></a>
# setColorBar
setColorBar( org.das2.graph.DasColorBar cb ) &rarr; void

Setter for property colorBar.

### Parameters:
cb - New value of property colorBar.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setColorBar&unscoped_q=setColorBar">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setColorByDataSetId"></a>
# setColorByDataSetId
setColorByDataSetId( String colorByDataSetId ) &rarr; void

The dataset plane to use to get colors.  If this is null or "", then
 no coloring is done. (Note the default plane cannot be used to color.)

### Parameters:
colorByDataSetId - New value of property colorByDataSetId.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setColorByDataSetId&unscoped_q=setColorByDataSetId">[search for examples]</a>
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
<a name="setDataSetSizeLimit"></a>
# setDataSetSizeLimit
setDataSetSizeLimit( int dataSetSizeLimit ) &rarr; void

Setter for property dataSetSizeLimit.

### Parameters:
dataSetSizeLimit - New value of property dataSetSizeLimit.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSetSizeLimit&unscoped_q=setDataSetSizeLimit">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDrawError"></a>
# setDrawError
setDrawError( boolean drawError ) &rarr; void



### Parameters:
drawError - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDrawError&unscoped_q=setDrawError">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setErrorBarType"></a>
# setErrorBarType
setErrorBarType( org.das2.graph.ErrorBarType errorBarType ) &rarr; void



### Parameters:
errorBarType - an ErrorBarType

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setErrorBarType&unscoped_q=setErrorBarType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFillColor"></a>
# setFillColor
setFillColor( java.awt.Color color ) &rarr; void

Setter for property fillReference.

### Parameters:
color - the color

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFillColor&unscoped_q=setFillColor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFillDirection"></a>
# setFillDirection
setFillDirection( String fillDirection ) &rarr; void



### Parameters:
fillDirection - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFillDirection&unscoped_q=setFillDirection">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFillStyle"></a>
# setFillStyle
setFillStyle( org.das2.graph.FillStyle fillStyle ) &rarr; void

how each plot symbol is filled.

### Parameters:
fillStyle - a FillStyle

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFillStyle&unscoped_q=setFillStyle">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFillToReference"></a>
# setFillToReference
setFillToReference( boolean fillToReference ) &rarr; void

Setter for property fillToReference.

### Parameters:
fillToReference - New value of property fillToReference.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFillToReference&unscoped_q=setFillToReference">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setHistogram"></a>
# setHistogram
setHistogram( boolean b ) &rarr; void



### Parameters:
b - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setHistogram&unscoped_q=setHistogram">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLineWidth"></a>
# setLineWidth
setLineWidth( double f ) &rarr; void

set the width of the connecting lines.

### Parameters:
f - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLineWidth&unscoped_q=setLineWidth">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setListIconSymSize"></a>
# setListIconSymSize
setListIconSymSize( float newSize ) &rarr; void



### Parameters:
newSize - a float

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setListIconSymSize&unscoped_q=setListIconSymSize">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPsym"></a>
# setPsym
setPsym( org.das2.graph.PlotSymbol psym ) &rarr; void

Setter for property psym.

### Parameters:
psym - New value of property psym.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPsym&unscoped_q=setPsym">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPsymConnector"></a>
# setPsymConnector
setPsymConnector( org.das2.graph.PsymConnector p ) &rarr; void



### Parameters:
p - a PsymConnector

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPsymConnector&unscoped_q=setPsymConnector">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setReference"></a>
# setReference
setReference( Datum reference ) &rarr; void

Setter for property reference.

### Parameters:
reference - New value of property reference.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setReference&unscoped_q=setReference">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRenderPointsPerMillisecond"></a>
# setRenderPointsPerMillisecond
setRenderPointsPerMillisecond( double newrenderPointsPerMillisecond ) &rarr; void



### Parameters:
newrenderPointsPerMillisecond - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRenderPointsPerMillisecond&unscoped_q=setRenderPointsPerMillisecond">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setResetDebugCounters"></a>
# setResetDebugCounters
setResetDebugCounters( boolean resetDebugCounters ) &rarr; void

Setter for property resetDebugCounters.

### Parameters:
resetDebugCounters - New value of property resetDebugCounters.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setResetDebugCounters&unscoped_q=setResetDebugCounters">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setShowLimits"></a>
# setShowLimits
setShowLimits( boolean showLimits ) &rarr; void

if the dataset contains metadata describing nominal and warning ranges, display them.  Currently
 this is found in CDF metadata, but should become part of QDataSet.

### Parameters:
showLimits - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setShowLimits&unscoped_q=setShowLimits">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSimplifyPaths"></a>
# setSimplifyPaths
setSimplifyPaths( boolean simplifyPaths ) &rarr; void

Setter for property simplifyPaths.

### Parameters:
simplifyPaths - New value of property simplifyPaths.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSimplifyPaths&unscoped_q=setSimplifyPaths">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setStampPsyms"></a>
# setStampPsyms
setStampPsyms( boolean newstampPsyms ) &rarr; void



### Parameters:
newstampPsyms - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setStampPsyms&unscoped_q=setStampPsyms">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSymSize"></a>
# setSymSize
setSymSize( double symSize ) &rarr; void

Setter for property symsize.

### Parameters:
symSize - New value of property symsize.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSymSize&unscoped_q=setSymSize">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setUpdatesPointsPerMillisecond"></a>
# setUpdatesPointsPerMillisecond
setUpdatesPointsPerMillisecond( double newupdatesPointsPerMillisecond ) &rarr; void



### Parameters:
newupdatesPointsPerMillisecond - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUpdatesPointsPerMillisecond&unscoped_q=setUpdatesPointsPerMillisecond">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="updatePlotImage"></a>
# updatePlotImage
updatePlotImage( org.das2.graph.DasAxis xAxis, org.das2.graph.DasAxis yAxis, ProgressMonitor monitor ) &rarr; void

Do the same as updatePlotImage, but use AffineTransform to implement axis transform.  This is the
 main updatePlotImage method, which will delegate to internal components of the plot, such as connector
 and error bar elements.

### Parameters:
xAxis - the x axis
<br>yAxis - the y axis
<br>monitor - progress monitor is used to provide feedback

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=updatePlotImage&unscoped_q=updatePlotImage">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

