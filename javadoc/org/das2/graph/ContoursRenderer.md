# org.das2.graph.ContoursRenderer

Renderer for making contour plots.

# ContoursRenderer( )


***
<a name="CONTROL_KEY_LEVELS"></a>
# CONTROL_KEY_LEVELS



***
<a name="CONTROL_KEY_LABELS"></a>
# CONTROL_KEY_LABELS



***
<a name="CONTROL_KEY_LABEL_CADENCE"></a>
# CONTROL_KEY_LABEL_CADENCE



***
<a name="CONTROL_KEY_FORMAT"></a>
# CONTROL_KEY_FORMAT



***
<a name="CONTROL_KEY_LABEL_ORIENT"></a>
# CONTROL_KEY_LABEL_ORIENT



***
<a name="PROP_FONTSIZE"></a>
# PROP_FONTSIZE



***
<a name="PROP_FORMAT"></a>
# PROP_FORMAT

format, empty string means use the default format.

***
<a name="PROP_LABELORIENT"></a>
# PROP_LABELORIENT



***
<a name="PROP_SIMPLIFYPATHS"></a>
# PROP_SIMPLIFYPATHS



***
<a name="PROP_LINETHICK"></a>
# PROP_LINETHICK

handle for the property lineThick.

***
<a name="PROP_LINESTYLE"></a>
# PROP_LINESTYLE



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
acceptsDataSet( QDataSet ds ) &rarr; boolean



### Parameters:
ds - a QDataSet

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=acceptsDataSet&unscoped_q=acceptsDataSet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="doAutorange"></a>
# doAutorange
doAutorange( QDataSet ds ) &rarr; QDataSet

autorange on the data, returning a rank 2 bounds for the dataset.

### Parameters:
ds - the dataset.

### Returns:
a bounding box
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/examples/Schemes.md#boundingBox'>org.das2.qds.examples.Schemes#boundingBox()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=doAutorange&unscoped_q=doAutorange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getColor"></a>
# getColor
getColor(  ) &rarr; Color

Get the color for contour lines

### Returns:
the color for contour lines

<a href="https://github.com/autoplot/dev/search?q=getColor&unscoped_q=getColor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getContours"></a>
# getContours
getContours(  ) &rarr; String

return the contour locations, a comma-separated list

### Returns:
the contour locations, a comma-separated list

<a href="https://github.com/autoplot/dev/search?q=getContours&unscoped_q=getContours">[search for examples]</a>
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
<a name="getFontSize"></a>
# getFontSize
getFontSize(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getFontSize&unscoped_q=getFontSize">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFormat"></a>
# getFormat
getFormat(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getFormat&unscoped_q=getFormat">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLabelCadence"></a>
# getLabelCadence
getLabelCadence(  ) &rarr; String

return the inter-label distance, in ems.

### Returns:
get the inter-label distance, in ems.

<a href="https://github.com/autoplot/dev/search?q=getLabelCadence&unscoped_q=getLabelCadence">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLabelOrient"></a>
# getLabelOrient
getLabelOrient(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getLabelOrient&unscoped_q=getLabelOrient">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLineStyle"></a>
# getLineStyle
getLineStyle(  ) &rarr; PsymConnector



### Returns:
org.das2.graph.PsymConnector


<a href="https://github.com/autoplot/dev/search?q=getLineStyle&unscoped_q=getLineStyle">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLineThick"></a>
# getLineThick
getLineThick(  ) &rarr; double

get the line thickness in pixels.

### Returns:
the line thickness in pixels.

<a href="https://github.com/autoplot/dev/search?q=getLineThick&unscoped_q=getLineThick">[search for examples]</a>
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
<a name="isDrawLabels"></a>
# isDrawLabels
isDrawLabels(  ) &rarr; boolean

true if labels should be drawn.

### Returns:
true if labels should be drawn.

<a href="https://github.com/autoplot/dev/search?q=isDrawLabels&unscoped_q=isDrawLabels">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isSimplifyPaths"></a>
# isSimplifyPaths
isSimplifyPaths(  ) &rarr; boolean

return true if we should reduce paths to remove features that fall within a pixel, etc.

### Returns:
true if we should reduce paths

<a href="https://github.com/autoplot/dev/search?q=isSimplifyPaths&unscoped_q=isSimplifyPaths">[search for examples]</a>
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

Set the color for contour lines

### Parameters:
color - the color for contour lines

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setColor&unscoped_q=setColor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setContours"></a>
# setContours
setContours( String contours ) &rarr; void

set the contour locations, a comma-separated list

### Parameters:
contours - the contour locations, a comma-separated list

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setContours&unscoped_q=setContours">[search for examples]</a>
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
<a name="setDrawLabels"></a>
# setDrawLabels
setDrawLabels( boolean drawLabels ) &rarr; void

true if labels should be drawn.

### Parameters:
drawLabels - true if labels should be drawn.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDrawLabels&unscoped_q=setDrawLabels">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFontSize"></a>
# setFontSize
setFontSize( String fontSize ) &rarr; void



### Parameters:
fontSize - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFontSize&unscoped_q=setFontSize">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFormat"></a>
# setFormat
setFormat( String value ) &rarr; void

explicitly set the format.
 format is found there.

### Parameters:
value - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFormat&unscoped_q=setFormat">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLabelCadence"></a>
# setLabelCadence
setLabelCadence( String labelCadence ) &rarr; void

set the inter-label distance, in ems.

### Parameters:
labelCadence - the inter-label distance, in ems.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLabelCadence&unscoped_q=setLabelCadence">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLabelOrient"></a>
# setLabelOrient
setLabelOrient( String labelOrient ) &rarr; void



### Parameters:
labelOrient - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLabelOrient&unscoped_q=setLabelOrient">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLineStyle"></a>
# setLineStyle
setLineStyle( org.das2.graph.PsymConnector lineStyle ) &rarr; void



### Parameters:
lineStyle - a PsymConnector

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLineStyle&unscoped_q=setLineStyle">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLineThick"></a>
# setLineThick
setLineThick( double newlineThick ) &rarr; void

set the line thickness in pixels.

### Parameters:
newlineThick - the line thickness in pixels.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLineThick&unscoped_q=setLineThick">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setParent"></a>
# setParent
setParent( org.das2.graph.DasPlot parent ) &rarr; void



### Parameters:
parent - a DasPlot

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setParent&unscoped_q=setParent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSimplifyPaths"></a>
# setSimplifyPaths
setSimplifyPaths( boolean newsimplifyPaths ) &rarr; void

set to true if we should reduce paths to remove features that fall within a pixel, etc.

### Parameters:
newsimplifyPaths - true if we should reduce paths

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSimplifyPaths&unscoped_q=setSimplifyPaths">[search for examples]</a>
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

