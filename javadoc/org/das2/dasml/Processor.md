# org.das2.dasml.ProcessorIntroduced to factor out all the dasml stuff from the graph package.
Processor( )


***
<a name="refPattern"></a>
# refPattern



***
<a name="intPattern"></a>
# intPattern



***
<a name="floatPattern"></a>
# floatPattern



***
<a name="createFormCanvas"></a>
# createFormCanvas
createFormCanvas( String name, int width, int height ) &rarr; DasCanvas



### Parameters:
name - a String
<br>width - an int
<br>height - an int

### Returns:
DasCanvas with a name.

<a href="https://github.com/autoplot/dev/search?q=createFormCanvas&unscoped_q=createFormCanvas">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createNamedAxis"></a>
# createNamedAxis
createNamedAxis( String name ) &rarr; DasAxis

TODO

### Parameters:
name - a String

### Returns:
an org.das2.graph.DasAxis


<a href="https://github.com/autoplot/dev/search?q=createNamedAxis&unscoped_q=createNamedAxis">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createNamedColorBar"></a>
# createNamedColorBar
createNamedColorBar( String name ) &rarr; DasColorBar



### Parameters:
name - a String

### Returns:
org.das2.graph.DasColorBar


<a href="https://github.com/autoplot/dev/search?q=createNamedColorBar&unscoped_q=createNamedColorBar">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createNamedPlot"></a>
# createNamedPlot
createNamedPlot( String name ) &rarr; DasPlot



### Parameters:
name - a String

### Returns:
org.das2.graph.DasPlot


<a href="https://github.com/autoplot/dev/search?q=createNamedPlot&unscoped_q=createNamedPlot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="deregisterComponent"></a>
# deregisterComponent
deregisterComponent( org.das2.graph.DasCanvas canvas ) &rarr; void



### Parameters:
canvas - a DasCanvas

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=deregisterComponent&unscoped_q=deregisterComponent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDOMElement"></a>
# getDOMElement
getDOMElement( org.das2.graph.DasAxis axis, org.w3c.dom.Document document ) &rarr; Element

TODO

### Parameters:
axis - a DasAxis
<br>document - a Document

### Returns:
an org.w3c.dom.Element


<a href="https://github.com/autoplot/dev/search?q=getDOMElement&unscoped_q=getDOMElement">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getDOMElement( org.das2.graph.DasCanvas canvas, org.w3c.dom.Document document ) &rarr; Element<br>
getDOMElement( org.das2.graph.DasRow row, org.w3c.dom.Document document ) &rarr; Element<br>
getDOMElement( org.das2.graph.DasColumn column, org.w3c.dom.Document document ) &rarr; Element<br>
getDOMElement( org.das2.graph.DasColorBar colorbar, org.w3c.dom.Document document ) &rarr; Element<br>
getDOMElement( org.das2.graph.DasPlot plot, org.w3c.dom.Document document ) &rarr; Element<br>
getDOMElement( org.das2.graph.Renderer r, org.w3c.dom.Document doc ) &rarr; Element<br>
***
<a name="getForm"></a>
# getForm
getForm( org.das2.graph.DasCanvas canvas ) &rarr; FormBase

TODO

### Parameters:
canvas - a DasCanvas

### Returns:
an org.das2.dasml.FormBase


<a href="https://github.com/autoplot/dev/search?q=getForm&unscoped_q=getForm">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parseValue"></a>
# parseValue
parseValue( org.das2.NameContext nameContext, String valueString, java.lang.Class type ) &rarr; Object

Parses the given <code>String</code> object in an attempt to
 produce the an object of the given type.

### Parameters:
nameContext - a NameContext
<br>valueString - the given <code>String</code>
<br>type - the given type

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=parseValue&unscoped_q=parseValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="processCanvasElement"></a>
# processCanvasElement
processCanvasElement( org.w3c.dom.Element element, org.das2.dasml.FormBase form ) &rarr; DasCanvas

Process a <code>&lt;canvas&gt;</code> element.

### Parameters:
element - The DOM tree node that represents the element
<br>form - a FormBase

### Returns:
an org.das2.graph.DasCanvas


<a href="https://github.com/autoplot/dev/search?q=processCanvasElement&unscoped_q=processCanvasElement">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="processLinePlotElement"></a>
# processLinePlotElement
processLinePlotElement( org.w3c.dom.Element element, org.das2.graph.DasPlot parent, org.das2.dasml.FormBase form ) &rarr; SeriesRenderer



### Parameters:
element - an Element
<br>parent - a DasPlot
<br>form - a FormBase

### Returns:
org.das2.graph.SeriesRenderer


<a href="https://github.com/autoplot/dev/search?q=processLinePlotElement&unscoped_q=processLinePlotElement">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="processPlotElement"></a>
# processPlotElement
processPlotElement( org.w3c.dom.Element element, org.das2.dasml.FormBase form ) &rarr; DasPlot



### Parameters:
element - an Element
<br>form - a FormBase

### Returns:
org.das2.graph.DasPlot


<a href="https://github.com/autoplot/dev/search?q=processPlotElement&unscoped_q=processPlotElement">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="processSpectrogramElement"></a>
# processSpectrogramElement
processSpectrogramElement( org.w3c.dom.Element element, org.das2.graph.DasPlot parent, org.das2.dasml.FormBase form ) &rarr; SpectrogramRenderer



### Parameters:
element - an Element
<br>parent - a DasPlot
<br>form - a FormBase

### Returns:
org.das2.graph.SpectrogramRenderer


<a href="https://github.com/autoplot/dev/search?q=processSpectrogramElement&unscoped_q=processSpectrogramElement">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="processStackedHistogramElement"></a>
# processStackedHistogramElement
processStackedHistogramElement( org.w3c.dom.Element element, org.das2.graph.DasPlot parent, org.das2.dasml.FormBase form ) &rarr; Renderer



### Parameters:
element - an Element
<br>parent - a DasPlot
<br>form - a FormBase

### Returns:
org.das2.graph.Renderer


<a href="https://github.com/autoplot/dev/search?q=processStackedHistogramElement&unscoped_q=processStackedHistogramElement">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="registerComponent"></a>
# registerComponent
registerComponent( org.das2.graph.DasCanvas canvas ) &rarr; void



### Parameters:
canvas - a DasCanvas

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=registerComponent&unscoped_q=registerComponent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

