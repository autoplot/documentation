# org.das2.components.HorizontalSpectrogramSlicer



***
<a name="addAction"></a>
# addAction
addAction( javax.swing.Action a ) &rarr; void

add a button

### Parameters:
a - the action for the button.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addAction&unscoped_q=addAction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="clear"></a>
# clear
clear( QDataSet tds ) &rarr; void

clear the current dataset to avoid units errors.  If the
 new dataset can be used, use it.

### Parameters:
tds - the new dataset

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=clear&unscoped_q=clear">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createSlicer"></a>
# createSlicer
createSlicer( org.das2.graph.DasPlot plot, org.das2.dataset.TableDataSetConsumer dataSetConsumer ) &rarr; HorizontalSpectrogramSlicer



### Parameters:
plot - a DasPlot
<br>dataSetConsumer - a TableDataSetConsumer

### Returns:
org.das2.components.HorizontalSpectrogramSlicer


<a href="https://github.com/autoplot/dev/search?q=createSlicer&unscoped_q=createSlicer">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="dataPointSelected"></a>
# dataPointSelected
dataPointSelected( org.das2.event.DataPointSelectionEvent e ) &rarr; void

show the slice at the data point selected.

### Parameters:
e - the selection event containing the data point.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dataPointSelected&unscoped_q=dataPointSelected">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="dispose"></a>
# dispose
dispose(  ) &rarr; void

dispose of the popup slicer.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dispose&unscoped_q=dispose">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSet"></a>
# getDataSet
getDataSet(  ) &rarr; QDataSet

provide access to the dataset

### Returns:
the dataset.

<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMarkColor"></a>
# getMarkColor
getMarkColor(  ) &rarr; Color

the color for the mark (vertical bar) indicating slice position

### Returns:
the mark color

<a href="https://github.com/autoplot/dev/search?q=getMarkColor&unscoped_q=getMarkColor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSliceY"></a>
# getSliceY
getSliceY(  ) &rarr; Datum

provide the Y position of the data.  Note this may be different 
 than where the user requested because the nearest channel is provided.

### Returns:
the slice position.

<a href="https://github.com/autoplot/dev/search?q=getSliceY&unscoped_q=getSliceY">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setMarkColor"></a>
# setMarkColor
setMarkColor( java.awt.Color markColor ) &rarr; void

set the color for the mark (vertical bar) indicating slice position
 Color(230,230,230) is the default.

### Parameters:
markColor - the color

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMarkColor&unscoped_q=setMarkColor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showPopup"></a>
# showPopup
showPopup(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showPopup&unscoped_q=showPopup">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

