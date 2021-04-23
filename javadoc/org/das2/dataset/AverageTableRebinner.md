# org.das2.dataset.AverageTableRebinner

DataSetRebinner implementing either bilinear interpolation in blocks of 4 points, or nearest neighbor interpolation by
 grabbing close points, or no interpolation at all..  Points the land on the same pixel are averaged together.

# AverageTableRebinner( )
Creates a new instance of TableAverageRebinner

***
<a name="PROP_CADENCECHECK"></a>
# PROP_CADENCECHECK



***
<a name="PROP_INTERPOLATETYPE"></a>
# PROP_INTERPOLATETYPE



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
<a name="getInterpolateType"></a>
# getInterpolateType
getInterpolateType(  ) &rarr; Interpolate



### Returns:
org.das2.dataset.AverageTableRebinner.Interpolate


<a href="https://github.com/autoplot/dev/search?q=getInterpolateType&unscoped_q=getInterpolateType">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isCadenceCheck"></a>
# isCadenceCheck
isCadenceCheck(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isCadenceCheck&unscoped_q=isCadenceCheck">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isEnlargePixels"></a>
# isEnlargePixels
isEnlargePixels(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isEnlargePixels&unscoped_q=isEnlargePixels">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isInterpolate"></a>
# isInterpolate
isInterpolate(  ) &rarr; boolean

"Interpolate" here simply means connecting the data points.

### Returns:
true indicates we should connect the data points.

<a href="https://github.com/autoplot/dev/search?q=isInterpolate&unscoped_q=isInterpolate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isInterpolateXThenY"></a>
# isInterpolateXThenY
isInterpolateXThenY(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isInterpolateXThenY&unscoped_q=isInterpolateXThenY">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rebin"></a>
# rebin
rebin( QDataSet ds, org.das2.dataset.RebinDescriptor ddX, org.das2.dataset.RebinDescriptor ddY, org.das2.dataset.RebinDescriptor ddZ ) &rarr; QDataSet

rebin the data, using the interpolate control to define the interpolation between measurements.  Data that fall into the
 same pixel are always averaged in the linear space, regardless of interpolation method.

### Parameters:
ds - rank 2 table or rank 3 join of tables.  New: rank 2 bundle of (X,Y,Z)
<br>ddX - a RebinDescriptor
<br>ddY - a RebinDescriptor
<br>ddZ - a RebinDescriptor

### Returns:
rank 2 table with one row/column per screen pixel.

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

***
<a name="setCadenceCheck"></a>
# setCadenceCheck
setCadenceCheck( boolean cadenceCheck ) &rarr; void



### Parameters:
cadenceCheck - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCadenceCheck&unscoped_q=setCadenceCheck">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setEnlargePixels"></a>
# setEnlargePixels
setEnlargePixels( boolean enlargePixels ) &rarr; void



### Parameters:
enlargePixels - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setEnlargePixels&unscoped_q=setEnlargePixels">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setInterpolate"></a>
# setInterpolate
setInterpolate( boolean interpolate ) &rarr; void

"Interpolate" here simply means connecting the data points.

### Parameters:
interpolate - true indicates we should connect the data points.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setInterpolate&unscoped_q=setInterpolate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setInterpolateType"></a>
# setInterpolateType
setInterpolateType( org.das2.dataset.AverageTableRebinner.Interpolate interpolateType ) &rarr; void



### Parameters:
interpolateType - an AverageTableRebinner.Interpolate

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setInterpolateType&unscoped_q=setInterpolateType">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setInterpolateXThenY"></a>
# setInterpolateXThenY
setInterpolateXThenY( boolean interpolateXThenY ) &rarr; void

first interpolate over gaps in X then gaps in Y.

### Parameters:
interpolateXThenY - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setInterpolateXThenY&unscoped_q=setInterpolateXThenY">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

