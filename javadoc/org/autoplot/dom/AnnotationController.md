# org.autoplot.dom.AnnotationController

implements the annotation

# AnnotationController( org.autoplot.dom.Application dom, org.autoplot.dom.Annotation annotation, org.das2.graph.DasAnnotation dasAnnotation )


***
<a name="getCanvas"></a>
# getCanvas
getCanvas(  ) &rarr; Canvas

return the canvas where this annotation lives.

### Returns:
an org.autoplot.dom.Canvas


<a href="https://github.com/autoplot/dev/search?q=getCanvas&unscoped_q=getCanvas">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDasAnnotation"></a>
# getDasAnnotation
getDasAnnotation(  ) &rarr; DasAnnotation

provide direct access to the annotation

### Returns:
the implementing das2 annotation

<a href="https://github.com/autoplot/dev/search?q=getDasAnnotation&unscoped_q=getDasAnnotation">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFontConverter"></a>
# getFontConverter
getFontConverter( org.das2.graph.DasCanvasComponent dcc ) &rarr; Converter

converts forward from relative font spec to point size, used by
 the annotation and axis nodes.

### Parameters:
dcc - the canvas component.

### Returns:
the converter that converts between strings like "1em" and the font.

<a href="https://github.com/autoplot/dev/search?q=getFontConverter&unscoped_q=getFontConverter">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

