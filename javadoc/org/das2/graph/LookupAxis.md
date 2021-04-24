# org.das2.graph.LookupAxis

This is like a TCA, but is an axis which has ticks positioned by another axis.

# LookupAxis( org.das2.graph.DasAxis axis )


***
<a name="paintComponent"></a>
# paintComponent
paintComponent( java.awt.Graphics g ) &rarr; void



### Parameters:
g - a Graphics

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=paintComponent&unscoped_q=paintComponent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resize"></a>
# resize
resize(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resize&unscoped_q=resize">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAxis"></a>
# setAxis
setAxis( org.das2.graph.DasAxis axis ) &rarr; void

set the axis.  This must be in units convertible to xx.
 This must be a vertical axis with ticks on the left side, for now.

### Parameters:
axis - the axis.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAxis&unscoped_q=setAxis">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataSet"></a>
# setDataSet
setDataSet( QDataSet yy ) &rarr; void



### Parameters:
yy - a QDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSet&unscoped_q=setDataSet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

setDataSet( QDataSet xx, QDataSet yy ) &rarr; void<br>
***
<a name="updateTicks"></a>
# updateTicks
updateTicks(  ) &rarr; void

the axis has changed, so update the tick positions.
 preconditions: the axis ticks have changed.
 postconditions: new x values have been calculated in xpos and fpos

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=updateTicks&unscoped_q=updateTicks">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

