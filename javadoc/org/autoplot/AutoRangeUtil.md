# org.autoplot.AutoRangeUtil



# AutoRangeUtil( )


***
<a name="autoRange"></a>
# autoRange
autoRange( QDataSet hist, QDataSet ds, java.util.Map properties ) &rarr; AutoRangeDescriptor

this is a copy of the other autorange, lacking some of its hacks.  TODO: why?
 This is not used.

### Parameters:
hist - a QDataSet
<br>ds - a QDataSet
<br>properties - a java.util.Map

### Returns:
an org.autoplot.AutoRangeUtil.AutoRangeDescriptor

### See Also:
<a href='#autoRange'>autoRange(QDataSet, java.util.Map, boolean)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=autoRange&unscoped_q=autoRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

autoRange( QDataSet ds, java.util.Map properties ) &rarr; AutoRangeDescriptor<br>
autoRange( QDataSet ds, java.util.Map properties, boolean ignoreDsProps ) &rarr; AutoRangeDescriptor<br>
***
<a name="bounds"></a>
# bounds
bounds( QDataSet dataSet, org.autoplot.RenderType renderType ) &rarr; QDataSet

return the bounding qube for the given render type.  This was stolen from Test022.

### Parameters:
dataSet - a QDataSet
<br>renderType - a RenderType

### Returns:
bounding cube[3,2]

<a href="https://github.com/autoplot/dev/search?q=bounds&unscoped_q=bounds">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

