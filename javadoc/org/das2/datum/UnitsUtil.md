# org.das2.datum.UnitsUtilUseful operations for units, and tests for Steven's Levels of Measurement.
***
<a name="divide"></a>
# divide
divide( Datum aDatum, Datum bDatum ) &rarr; Datum

attempt to perform the division of two Datums by looking for
 convertible units or dimensionless.

### Parameters:
aDatum - the numerator
<br>bDatum - the denominator

### Returns:
the result

<a href="https://github.com/autoplot/dev/search?q=divide&unscoped_q=divide">[search for examples]</a>

***
<a name="divideToString"></a>
# divideToString
divideToString( Datum aDatum, Datum bDatum ) &rarr; String

Special division operation that either does the Datum division if
 possible, or returns the division of the magnitude parts of the
 Datums plus the unit names "A/B", suitable for human consumption.

### Parameters:
aDatum - the numerator
<br>bDatum - the denominator

### Returns:
String for the result, or "A/B"

<a href="https://github.com/autoplot/dev/search?q=divideToString&unscoped_q=divideToString">[search for examples]</a>

***
<a name="getInverseUnit"></a>
# getInverseUnit
getInverseUnit( Units unit ) &rarr; Units

returns the unit whose product with the parameter unit is unity.
 (Presently this is only supports time units like Hz&rarr;seconds).

### Parameters:
unit - the unit

### Returns:
the inverse unit, or throws exception if one is not known.

<a href="https://github.com/autoplot/dev/search?q=getInverseUnit&unscoped_q=getInverseUnit">[search for examples]</a>

***
<a name="isIntervalMeasurement"></a>
# isIntervalMeasurement
isIntervalMeasurement( Units unit ) &rarr; boolean

returns true if the unit is a interval measurement, meaning the choice of
 zero is arbitrary.  Subtraction and comparison are allowed, but addition, 
 multiplication and division are invalid operators.  
 Examples include "2008-04-09T14:27:00Z" and 15 deg W Longitude.

### Parameters:
unit - an Units

### Returns:
a boolean

### See Also:
<a href='http://en.wikipedia.org/wiki/Level_of_measurement'>http://en.wikipedia.org/wiki/Level_of_measurement</a> <br>
<a href='http://www.statisticssolutions.com/data-levels-of-measurement/'>http://www.statisticssolutions.com/data-levels-of-measurement/</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isIntervalMeasurement&unscoped_q=isIntervalMeasurement">[search for examples]</a>

***
<a name="isIntervalOrRatioMeasurement"></a>
# isIntervalOrRatioMeasurement
isIntervalOrRatioMeasurement( Units unit ) &rarr; boolean

returns true if the unit is a interval measurement or is a ratio measurement,
 and not a nominal or ordinal measurement.  These are things that are plotted
 by showing a location on an axis.
 See http://en.wikipedia.org/wiki/Level_of_measurement
 Examples include "2008-04-09T14:27:00Z" and "5 km"

### Parameters:
unit - an Units

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isIntervalOrRatioMeasurement&unscoped_q=isIntervalOrRatioMeasurement">[search for examples]</a>

***
<a name="isNominalMeasurement"></a>
# isNominalMeasurement
isNominalMeasurement( Units unit ) &rarr; boolean

returns true if the unit is nominal, meaning that Datums with this unit
 can only be equal or not equal.  Currently all nominal data is stored
 as ordinal data, so this always returns false.  
 Examples include "Iowa City", and "Voyager 1".
 See http://en.wikipedia.org/wiki/Level_of_measurement

### Parameters:
unit - the unit

### Returns:
true if the unit is nominal.

<a href="https://github.com/autoplot/dev/search?q=isNominalMeasurement&unscoped_q=isNominalMeasurement">[search for examples]</a>

***
<a name="isOrdinalMeasurement"></a>
# isOrdinalMeasurement
isOrdinalMeasurement( Units unit ) &rarr; boolean

returns true if the unit is ordinal, meaning that Datums with this unit
 can only be equal or not equal, or compared.  subtract, add, multiply,
 divide are invalid.
 Examples include energy bin labels and quality measures.
 See http://en.wikipedia.org/wiki/Level_of_measurement

### Parameters:
unit - an Units

### Returns:
true if the unit is ordinal.

<a href="https://github.com/autoplot/dev/search?q=isOrdinalMeasurement&unscoped_q=isOrdinalMeasurement">[search for examples]</a>

***
<a name="isRatioMeasurement"></a>
# isRatioMeasurement
isRatioMeasurement( Units unit ) &rarr; boolean

returns true if the unit is a ratio measurement, meaning there is a physical zero
 and you can make meaningful ratios between arbitrary numbers.  All operations
 like add, multiply and divide are allowed.  
 Examples include "5 km" or "0.2/cc" and "15 counts"

### Parameters:
unit - an Units

### Returns:
a boolean

### See Also:
<a href='http://en.wikipedia.org/wiki/Level_of_measurement'>http://en.wikipedia.org/wiki/Level_of_measurement</a> <br>
<a href='http://www.statisticssolutions.com/data-levels-of-measurement/'>http://www.statisticssolutions.com/data-levels-of-measurement/</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isRatioMeasurement&unscoped_q=isRatioMeasurement">[search for examples]</a>

***
<a name="isRatiometric"></a>
# isRatiometric
isRatiometric( Units unit ) &rarr; boolean

returns true if the unit is used to measure distance in a logarithmic
 space, such as decibels or percent increase.  Note Units.dimensionless
 are not considered ratiometric.  (Of course, all ratiometic
 units are dimensionless...)

 Do not confuse this with isRatioMeasurement.  "5kg" is ratio measurement.
 "105%" is ratiometric.

### Parameters:
unit - the unit

### Returns:
true if the unit is used to measure distance in a logarithmic space

<a href="https://github.com/autoplot/dev/search?q=isRatiometric&unscoped_q=isRatiometric">[search for examples]</a>

***
<a name="isTimeLocation"></a>
# isTimeLocation
isTimeLocation( Units unit ) &rarr; boolean

returns true if the unit describes a location in time, as in us2000.

### Parameters:
unit - an Units

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isTimeLocation&unscoped_q=isTimeLocation">[search for examples]</a>

