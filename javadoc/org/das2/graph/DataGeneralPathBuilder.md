# org.das2.graph.DataGeneralPathBuilder

introduce class to handle the task of creating GeneralPaths from a
 series of data points.  We notice that creating the GeneralPath is 
 plenty fast, and it's rendering it that is slow, so this will allow for
 future optimizations.

# DataGeneralPathBuilder( org.das2.graph.DasAxis xaxis, org.das2.graph.DasAxis yaxis )


***
<a name="PROP_HISTOGRAM_MODE"></a>
# PROP_HISTOGRAM_MODE



***
<a name="addDataPoint"></a>
# addDataPoint
addDataPoint( boolean valid, Datum x, Datum y ) &rarr; void

add a data point to the curve.

### Parameters:
valid - if invalid, then break the line at this point.
<br>x - the x value
<br>y - the y value

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addDataPoint&unscoped_q=addDataPoint">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addDataPoint( boolean valid, double x, double y ) &rarr; void<br>
***
<a name="finishThought"></a>
# finishThought
finishThought(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=finishThought&unscoped_q=finishThought">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCadenceDouble"></a>
# getCadenceDouble
getCadenceDouble(  ) &rarr; double

return the x cadence used as a double.  This is should interpreted with
 the xaxis units and with isCadenceRatiometric.

### Returns:
the cadence as a double, or 1e38 if there is no cadence.

<a href="https://github.com/autoplot/dev/search?q=getCadenceDouble&unscoped_q=getCadenceDouble">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getGeneralPath"></a>
# getGeneralPath
getGeneralPath(  ) &rarr; GeneralPath

get the generalPath for drawing.  This may affect the
 path, when histogramMode is true.

### Returns:
the generalPath for drawing.

<a href="https://github.com/autoplot/dev/search?q=getGeneralPath&unscoped_q=getGeneralPath">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPathIterator"></a>
# getPathIterator
getPathIterator(  ) &rarr; PathIterator

get the path iterator.

### Returns:
the path iterator.

<a href="https://github.com/autoplot/dev/search?q=getPathIterator&unscoped_q=getPathIterator">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPenPosition"></a>
# getPenPosition
getPenPosition(  ) &rarr; Point2D

this is added so that the fill-to-zero code can add the returns.

### Returns:
a java.awt.geom.Point2D


<a href="https://github.com/autoplot/dev/search?q=getPenPosition&unscoped_q=getPenPosition">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getXUnits"></a>
# getXUnits
getXUnits(  ) &rarr; Units

return the units of the xaxis.

### Returns:
the units of the xaxis.

<a href="https://github.com/autoplot/dev/search?q=getXUnits&unscoped_q=getXUnits">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getYUnits"></a>
# getYUnits
getYUnits(  ) &rarr; Units

return the units of the yaxis.

### Returns:
the units of the yaxis.

<a href="https://github.com/autoplot/dev/search?q=getYUnits&unscoped_q=getYUnits">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="insertLineTo"></a>
# insertLineTo
insertLineTo( double x, double y ) &rarr; void

allow client to insert a point.  This is used when trying to implement the fill-to-zero.

### Parameters:
x - pixel position
<br>y - pixel position

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=insertLineTo&unscoped_q=insertLineTo">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isCadenceRatiometric"></a>
# isCadenceRatiometric
isCadenceRatiometric(  ) &rarr; boolean

return true if the spacing in x has been identified as ratiometric 
 (linearly spaced on a log axis).  Note this
 is for the data, which is not necessarily the x axis setting.

### Returns:
true if the data has been marked as ratiometric.

<a href="https://github.com/autoplot/dev/search?q=isCadenceRatiometric&unscoped_q=isCadenceRatiometric">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isHistogramMode"></a>
# isHistogramMode
isHistogramMode(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isHistogramMode&unscoped_q=isHistogramMode">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setCadence"></a>
# setCadence
setCadence( Datum sw ) &rarr; void

set the limit where two points are considered adjacent, or null
 if no check should be done.

### Parameters:
sw - a Datum

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCadence&unscoped_q=setCadence">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setHistogramFillFlag"></a>
# setHistogramFillFlag
setHistogramFillFlag(  ) &rarr; void

kludge to tell the builder to subtract a half cadence from the next point

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setHistogramFillFlag&unscoped_q=setHistogramFillFlag">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setHistogramMode"></a>
# setHistogramMode
setHistogramMode( boolean histogramMode ) &rarr; void



### Parameters:
histogramMode - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setHistogramMode&unscoped_q=setHistogramMode">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setName"></a>
# setName
setName( String name ) &rarr; void

set the name of this DataGeneralPathBuilder when logging.

### Parameters:
name - "" or the name of the general path object in log messages.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setName&unscoped_q=setName">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

