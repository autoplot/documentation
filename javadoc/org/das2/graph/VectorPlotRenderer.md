# org.das2.graph.VectorPlotRenderer

Draw vectors as arrows, from a dataset[:,4] where
 dataset[0,:] is x,y,dx,dy.

# VectorPlotRenderer( )


***
<a name="PROP_SCALE"></a>
# PROP_SCALE

property name for the scale.

***
<a name="acceptsData"></a>
# acceptsData
acceptsData( QDataSet ds ) &rarr; boolean

return true if the renderer accepts data in this form.  This
 renderer needs rank 2 data with 4 columns,

### Parameters:
ds - a QDataSet

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=acceptsData&unscoped_q=acceptsData">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="doAutorange"></a>
# doAutorange
doAutorange( QDataSet ds ) &rarr; QDataSet

autorange on the data, returning a rank 2 bounds for the dataset.

### Parameters:
ds - the dataset to autorange.

### Returns:
a bounds dataset, where result[0,:] is the xrange and result[1,:] is the yrange.

<a href="https://github.com/autoplot/dev/search?q=doAutorange&unscoped_q=doAutorange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getScale"></a>
# getScale
getScale(  ) &rarr; double

get the scale relating the length of the vector (dx and dy, the last two 
 columns) to the positions of the vector (in the first two columns).

### Returns:
the scale

<a href="https://github.com/autoplot/dev/search?q=getScale&unscoped_q=getScale">[search for examples]</a>

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
<a name="setScale"></a>
# setScale
setScale( double scale ) &rarr; void

set the scale relating the length of the vector (dx and dy, the last two 
 columns) to the positions of the vector (in the first two columns).
 Default is 1.

### Parameters:
scale - the new scale

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setScale&unscoped_q=setScale">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

