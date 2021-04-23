# org.das2.graph.DigitalRenderer



# DigitalRenderer( )


***
<a name="PROP_COLOR"></a>
# PROP_COLOR



***
<a name="PROP_ALIGN"></a>
# PROP_ALIGN



***
<a name="PROP_PLOTSYMBOL"></a>
# PROP_PLOTSYMBOL



***
<a name="PROP_FORMAT"></a>
# PROP_FORMAT

format, empty string means use either dataset's format, or %.2f

***
<a name="PROP_SIZE"></a>
# PROP_SIZE

font size, 0 indicates the plot font should be used.
 TODO: this should be relativeSize.  Add a property for this as well.

***
<a name="PROP_FONTSIZE"></a>
# PROP_FONTSIZE

font size, expressed as relative string like "1em" or "6pt"

***
<a name="PROP_FILLLABEL"></a>
# PROP_FILLLABEL



***
<a name="PROP_DATASETSIZELIMIT"></a>
# PROP_DATASETSIZELIMIT



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

autorange on the data, returning a rank 2 bounds for the dataset.

### Parameters:
ds - the dataset

### Returns:
a bounding box
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/examples/Schemes.md#boundingBox'>org.das2.qds.examples.Schemes#boundingBox()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=doAutorange&unscoped_q=doAutorange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="formatDatum"></a>
# formatDatum
formatDatum( String form, Datum d, char type ) &rarr; String

format the datum into a string, using the format and the 
 pre-calculated type.

### Parameters:
form - the format, such as %.2f or "x=%d cc"
<br>d - a Datum
<br>type - 'x' 'X' 'd' 'o' 'c' 'C' or 'f'

### Returns:
the string

<a href="https://github.com/autoplot/dev/search?q=formatDatum&unscoped_q=formatDatum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getAlign"></a>
# getAlign
getAlign(  ) &rarr; Align



### Returns:
org.das2.graph.DigitalRenderer.Align


<a href="https://github.com/autoplot/dev/search?q=getAlign&unscoped_q=getAlign">[search for examples]</a>

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
<a name="getControl"></a>
# getControl
getControl(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getControl&unscoped_q=getControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSetSizeLimit"></a>
# getDataSetSizeLimit
getDataSetSizeLimit(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getDataSetSizeLimit&unscoped_q=getDataSetSizeLimit">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFillLabel"></a>
# getFillLabel
getFillLabel(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getFillLabel&unscoped_q=getFillLabel">[search for examples]</a>

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
<a name="getPlotSymbol"></a>
# getPlotSymbol
getPlotSymbol(  ) &rarr; PlotSymbol



### Returns:
org.das2.graph.PlotSymbol


<a href="https://github.com/autoplot/dev/search?q=getPlotSymbol&unscoped_q=getPlotSymbol">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSize"></a>
# getSize
getSize(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=getSize&unscoped_q=getSize">[search for examples]</a>

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

like accept context, but provides a shape to indicate selection.  This
 should be roughly the same as the locus of points where acceptContext is
 true.

### Returns:
a java.awt.Shape


<a href="https://github.com/autoplot/dev/search?q=selectionArea&unscoped_q=selectionArea">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAlign"></a>
# setAlign
setAlign( org.das2.graph.DigitalRenderer.Align align ) &rarr; void

For the box containing the digital number, which corner is anchored 
 to the data.  Note this is consistent with the anchorPosition property of
 annotations.

### Parameters:
align - a DigitalRenderer.Align

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAlign&unscoped_q=setAlign">[search for examples]</a>

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
<a name="setDataSetSizeLimit"></a>
# setDataSetSizeLimit
setDataSetSizeLimit( int dataSetSizeLimit ) &rarr; void



### Parameters:
dataSetSizeLimit - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSetSizeLimit&unscoped_q=setDataSetSizeLimit">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFillLabel"></a>
# setFillLabel
setFillLabel( String fillLabel ) &rarr; void

the label printed where fill data (invalid data placeholder) is found.

### Parameters:
fillLabel - the label such as "fill" or "" for nothing.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFillLabel&unscoped_q=setFillLabel">[search for examples]</a>

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

note the dataset's format will be used if this is "", and "%.2f" if no
 format is found there.

### Parameters:
value - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFormat&unscoped_q=setFormat">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPlotSymbol"></a>
# setPlotSymbol
setPlotSymbol( org.das2.graph.PlotSymbol plotSymbol ) &rarr; void



### Parameters:
plotSymbol - a PlotSymbol

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPlotSymbol&unscoped_q=setPlotSymbol">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSize"></a>
# setSize
setSize( double size ) &rarr; void



### Parameters:
size - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSize&unscoped_q=setSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="typeForFormat"></a>
# typeForFormat
typeForFormat( String form ) &rarr; char

return the data type needed for the format.  For example, %d needs integers, %f needs floats.

### Parameters:
form - a String

### Returns:
'x' 'X' 'd' 'o' 'c' 'C' or 'f'

<a href="https://github.com/autoplot/dev/search?q=typeForFormat&unscoped_q=typeForFormat">[search for examples]</a>

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

