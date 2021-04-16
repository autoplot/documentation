# org.das2.dataset.AverageNoInterpolateTableRebinnerThis rebinner will bin average elements that fall on the same bin, and will enlarge cells that
 cover multiple bins.  This is done efficiently, and also does not introduce half-pixel aliasing because
 input cells covering multiple output cells are averaged weighting by overlap.
AverageNoInterpolateTableRebinner( )


***
<a name="isNearestNeighbor"></a>
# isNearestNeighbor
isNearestNeighbor(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isNearestNeighbor&unscoped_q=isNearestNeighbor">[search for examples]</a>

***
<a name="rebin"></a>
# rebin
rebin( org.das2.dataset.DataSet ds, org.das2.dataset.RebinDescriptor ddx, org.das2.dataset.RebinDescriptor ddy ) &rarr; DataSet



### Parameters:
ds - a DataSet
<br>ddx - a RebinDescriptor
<br>ddy - a RebinDescriptor

### Returns:
org.das2.dataset.DataSet


<a href="https://github.com/autoplot/dev/search?q=rebin&unscoped_q=rebin">[search for examples]</a>

***
<a name="setNearestNeighbor"></a>
# setNearestNeighbor
setNearestNeighbor( boolean v ) &rarr; void



### Parameters:
v - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setNearestNeighbor&unscoped_q=setNearestNeighbor">[search for examples]</a>

