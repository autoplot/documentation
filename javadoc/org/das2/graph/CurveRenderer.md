# org.das2.graph.CurveRenderer

Old renderer that really doesn't do anything that the SeriesRenderer can't do,
 but is much easier to understand.

# CurveRenderer( org.das2.dataset.DataSetDescriptor dsd, String xplane, String yplane )
The dataset descriptor should return a rank 2 QDataSet with time for
 and a bundle descriptor for BUNDLE_1.  DataSetOps.unbundle is used
 to extract the xplane and yplane components.

# CurveRenderer( )
Constructor for renderer which takes a dataset which is Y(DEPEND_0=X)

***
<a name="PROP_LINE_WIDTH"></a>
# PROP_LINE_WIDTH



***
<a name="PROP_COLOR"></a>
# PROP_COLOR



***
<a name="PROP_SYM_SIZE"></a>
# PROP_SYM_SIZE



***
<a name="PROP_SYM_CONNECTOR"></a>
# PROP_SYM_CONNECTOR



***
<a name="PROP_PSYM"></a>
# PROP_PSYM



***
<a name="getColor"></a>
# getColor
getColor(  ) &rarr; Color



### Returns:
java.awt.Color


<a href="https://github.com/autoplot/dev/search?q=getColor&unscoped_q=getColor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLineWidth"></a>
# getLineWidth
getLineWidth(  ) &rarr; double

Getter for property lineWidth.

### Returns:
Value of property lineWidth.

<a href="https://github.com/autoplot/dev/search?q=getLineWidth&unscoped_q=getLineWidth">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPsym"></a>
# getPsym
getPsym(  ) &rarr; Psym

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
<a name="getSymSize"></a>
# getSymSize
getSymSize(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=getSymSize&unscoped_q=getSymSize">[search for examples]</a>

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
<a name="setColor"></a>
# setColor
setColor( java.awt.Color color ) &rarr; void

setter for the property color.

### Parameters:
color - a Color

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setColor&unscoped_q=setColor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLineWidth"></a>
# setLineWidth
setLineWidth( double lineWidth ) &rarr; void

Setter for property lineWidth.

### Parameters:
lineWidth - New value of property lineWidth.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLineWidth&unscoped_q=setLineWidth">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPsym"></a>
# setPsym
setPsym( org.das2.graph.Psym psym ) &rarr; void

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

set the type of line connecting plot symbols (e.g. solid, none, dotted).

### Parameters:
p - a PsymConnector

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPsymConnector&unscoped_q=setPsymConnector">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSymSize"></a>
# setSymSize
setSymSize( double symSize ) &rarr; void

set the symbol size in pixels (ems)

### Parameters:
symSize - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSymSize&unscoped_q=setSymSize">[search for examples]</a>

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

