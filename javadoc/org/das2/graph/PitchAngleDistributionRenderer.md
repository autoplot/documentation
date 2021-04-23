# org.das2.graph.PitchAngleDistributionRenderer

Draws a pitch angle distribution, which is a spectrogram wrapped around an origin.  Datasets must
 be of the form Z[Angle,Radius].  The dataset Angle must be in radians (Units.radians or dimensionless), or 
 have units Units.degrees.  Note, at one time it would guess the angles dimension, but this was unreliable and was
 removed.

# PitchAngleDistributionRenderer( org.das2.graph.DasColorBar cb )


***
<a name="PROP_ORIGINNORTH"></a>
# PROP_ORIGINNORTH

if true, then angle=0 is in the positive Y direction, otherwise
 it is in the positive x direction

***
<a name="PROP_CLOCKWISE"></a>
# PROP_CLOCKWISE



***
<a name="PROP_ORIGIN"></a>
# PROP_ORIGIN

One of "", "N", "S", "E", "W"

***
<a name="PROP_DRAWPOLARAXES"></a>
# PROP_DRAWPOLARAXES



***
<a name="PROP_MIRROR"></a>
# PROP_MIRROR



***
<a name="acceptsData"></a>
# acceptsData
acceptsData( QDataSet ds ) &rarr; boolean

accepts data that is rank 2 and not a timeseries.  Angles
 may be in radians or in Units.degrees.  
 ds[Energy,Pitch] or ds[Pitch,Energy] where Pitch is in:
   Units.degrees, Units.radians, or dimensionless and -2*PI to 2*PI.

### Parameters:
ds - a QDataSet

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=acceptsData&unscoped_q=acceptsData">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="doAutorange"></a>
# doAutorange
doAutorange( QDataSet tds ) &rarr; QDataSet



### Parameters:
tds - a QDataSet

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=doAutorange&unscoped_q=doAutorange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getControl"></a>
# getControl
getControl(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getControl&unscoped_q=getControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getListIcon"></a>
# getListIcon
getListIcon(  ) &rarr; Icon



### Returns:
javax.swing.Icon


<a href="https://github.com/autoplot/dev/search?q=getListIcon&unscoped_q=getListIcon">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getOrigin"></a>
# getOrigin
getOrigin(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getOrigin&unscoped_q=getOrigin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isClockwise"></a>
# isClockwise
isClockwise(  ) &rarr; boolean

true if increasing angle corresponds to clockwise when not mirror.

### Returns:
true if increasing angle corresponds to clockwise

<a href="https://github.com/autoplot/dev/search?q=isClockwise&unscoped_q=isClockwise">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDrawPolarAxes"></a>
# isDrawPolarAxes
isDrawPolarAxes(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isDrawPolarAxes&unscoped_q=isDrawPolarAxes">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isMirror"></a>
# isMirror
isMirror(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isMirror&unscoped_q=isMirror">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isOriginNorth"></a>
# isOriginNorth
isOriginNorth(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isOriginNorth&unscoped_q=isOriginNorth">[search for examples]</a>

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
<a name="setClockwise"></a>
# setClockwise
setClockwise( boolean clockwise ) &rarr; void

true if increasing angle corresponds to clockwise when not mirror.

### Parameters:
clockwise - true if increasing angle corresponds to clockwise

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setClockwise&unscoped_q=setClockwise">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setColorBar"></a>
# setColorBar
setColorBar( org.das2.graph.DasColorBar colorBar ) &rarr; void



### Parameters:
colorBar - a DasColorBar

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setColorBar&unscoped_q=setColorBar">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setControl"></a>
# setControl
setControl( String s ) &rarr; void



### Parameters:
s - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setControl&unscoped_q=setControl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDrawPolarAxes"></a>
# setDrawPolarAxes
setDrawPolarAxes( boolean drawPolarAxes ) &rarr; void



### Parameters:
drawPolarAxes - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDrawPolarAxes&unscoped_q=setDrawPolarAxes">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setMirror"></a>
# setMirror
setMirror( boolean mirror ) &rarr; void



### Parameters:
mirror - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMirror&unscoped_q=setMirror">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setOrigin"></a>
# setOrigin
setOrigin( String origin ) &rarr; void



### Parameters:
origin - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setOrigin&unscoped_q=setOrigin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setOriginNorth"></a>
# setOriginNorth
setOriginNorth( boolean originNorth ) &rarr; void



### Parameters:
originNorth - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setOriginNorth&unscoped_q=setOriginNorth">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

