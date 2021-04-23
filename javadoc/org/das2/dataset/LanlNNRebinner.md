# org.das2.dataset.LanlNNRebinner

DataSetRebinner for explicitly doing NN rebinning.  The AverageTableRebinner had been used for the purpose, and
 there were numerous problems.  Also, this looks for BIN_PLUS, BIN_MINUS, BIN_MAX, and BIN_MIN properties in the dataset.

# LanlNNRebinner( )


***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rebin"></a>
# rebin
rebin( QDataSet ds, org.das2.dataset.RebinDescriptor ddX, org.das2.dataset.RebinDescriptor ddY, org.das2.dataset.RebinDescriptor ddZ ) &rarr; QDataSet

rebin the data, using the interpolate control to define the interpolation between measurements.  Data that fall into the
 same pixel are always averaged in the linear space, regardless of interpolation method.

### Parameters:
ds - rank 2 table or rank 3 join of tables.
<br>ddX - a RebinDescriptor
<br>ddY - a RebinDescriptor
<br>ddZ - a RebinDescriptor

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=rebin&unscoped_q=rebin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

