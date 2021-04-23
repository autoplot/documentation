# org.autoplot.RenderType
***
<a name="spectrogram"></a>
# spectrogram



***
<a name="nnSpectrogram"></a>
# nnSpectrogram



***
<a name="hugeScatter"></a>
# hugeScatter



***
<a name="series"></a>
# series



***
<a name="scatter"></a>
# scatter



***
<a name="colorScatter"></a>
# colorScatter



***
<a name="stairSteps"></a>
# stairSteps



***
<a name="fillToZero"></a>
# fillToZero



***
<a name="digital"></a>
# digital



***
<a name="image"></a>
# image



***
<a name="pitchAngleDistribution"></a>
# pitchAngleDistribution



***
<a name="polar"></a>
# polar



***
<a name="eventsBar"></a>
# eventsBar



***
<a name="stackedHistogram"></a>
# stackedHistogram



***
<a name="vectorPlot"></a>
# vectorPlot



***
<a name="bounds"></a>
# bounds



***
<a name="internal"></a>
# internal



***
<a name="orbitPlot"></a>
# orbitPlot



***
<a name="contour"></a>
# contour



***
<a name="acceptsData"></a>
# acceptsData
acceptsData( org.autoplot.RenderType rt, QDataSet ds ) &rarr; boolean

return true if the render type can make a reasonable rendering of the data.
 If the render type is not recognized, just return true.  This was introduced to
 constrain the options of the user to valid entries.

 Note this is called on the event thread and must be implemented so that 
 evaluation takes a trivial amount of time.

### Parameters:
rt - a RenderType
<br>ds - a QDataSet

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=acceptsData&unscoped_q=acceptsData">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="valueOf"></a>
# valueOf
valueOf( String name ) &rarr; RenderType



### Parameters:
name - a String

### Returns:
org.autoplot.RenderType


<a href="https://github.com/autoplot/dev/search?q=valueOf&unscoped_q=valueOf">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="values"></a>
# values
values(  ) &rarr; RenderType



### Returns:
org.autoplot.RenderType[]


<a href="https://github.com/autoplot/dev/search?q=values&unscoped_q=values">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

