# org.das2.datum.Units

Class for indicating physical units, and other random units.

***
<a name="dimensionless"></a>
# dimensionless



***
<a name="radians"></a>
# radians



***
<a name="degrees"></a>
# degrees



***
<a name="deg"></a>
# deg



***
<a name="degrees2"></a>
# degrees2



***
<a name="rgbColor"></a>
# rgbColor



***
<a name="celciusDegrees"></a>
# celciusDegrees



***
<a name="fahrenheitDegrees"></a>
# fahrenheitDegrees



***
<a name="years"></a>
# years



***
<a name="days"></a>
# days



***
<a name="hours"></a>
# hours



***
<a name="minutes"></a>
# minutes



***
<a name="seconds"></a>
# seconds



***
<a name="seconds2"></a>
# seconds2



***
<a name="milliseconds"></a>
# milliseconds



***
<a name="milliseconds2"></a>
# milliseconds2



***
<a name="microseconds"></a>
# microseconds



***
<a name="microseconds2"></a>
# microseconds2



***
<a name="microseconds3"></a>
# microseconds3



***
<a name="nanoseconds"></a>
# nanoseconds



***
<a name="ns"></a>
# ns



***
<a name="picoseconds"></a>
# picoseconds



***
<a name="bytesPerSecond"></a>
# bytesPerSecond



***
<a name="kiloBytesPerSecond"></a>
# kiloBytesPerSecond



***
<a name="bytes"></a>
# bytes



***
<a name="kiloBytes"></a>
# kiloBytes



***
<a name="hertz"></a>
# hertz



***
<a name="kiloHertz"></a>
# kiloHertz



***
<a name="megaHertz"></a>
# megaHertz



***
<a name="gigaHertz"></a>
# gigaHertz



***
<a name="eV"></a>
# eV



***
<a name="ev"></a>
# ev



***
<a name="keV"></a>
# keV



***
<a name="MeV"></a>
# MeV



***
<a name="pcm3"></a>
# pcm3

1 / cm<sup>3</sup>

***
<a name="kelvin"></a>
# kelvin



***
<a name="cm_2s_1keV_1"></a>
# cm_2s_1keV_1



***
<a name="cm_2s_1MeV_1"></a>
# cm_2s_1MeV_1



***
<a name="v2pm2Hz"></a>
# v2pm2Hz

Volts <sup>2</sup> m<sup>-2</sup> Hz<sup>-1</sup>

***
<a name="wpm2"></a>
# wpm2

Watts / m<sup>2</sup>

***
<a name="meters"></a>
# meters



***
<a name="millimeters"></a>
# millimeters



***
<a name="centimeters"></a>
# centimeters



***
<a name="kiloMeters"></a>
# kiloMeters



***
<a name="inches"></a>
# inches



***
<a name="typographicPoints"></a>
# typographicPoints



***
<a name="nT"></a>
# nT



***
<a name="cmps"></a>
# cmps



***
<a name="mps"></a>
# mps



***
<a name="centigrade"></a>
# centigrade

begin of LocationUnits.  These must be defined after the physical units to support Basis.

***
<a name="fahrenheitScale"></a>
# fahrenheitScale



***
<a name="dollars"></a>
# dollars

currencies for demonstration purposes.

***
<a name="euros"></a>
# euros



***
<a name="yen"></a>
# yen



***
<a name="rupee"></a>
# rupee



***
<a name="us2000"></a>
# us2000

Microseconds since midnight Jan 1, 2000, excluding those within a leap second.  Differences across leap
 second boundaries do not represent the number of microseconds elapsed.

***
<a name="us1980"></a>
# us1980

Microseconds since midnight Jan 1, 1980, excluding those within a leap second.

***
<a name="t2010"></a>
# t2010

Seconds since midnight Jan 1, 2010, excluding leap seconds.

***
<a name="t2000"></a>
# t2000

Seconds since midnight Jan 1, 2000, excluding leap seconds.

***
<a name="t1970"></a>
# t1970

seconds since midnight Jan 1, 1970, excluding leap seconds.

***
<a name="ms1970"></a>
# ms1970

milliseconds since midnight Jan 1, 1970, excluding leap seconds.

***
<a name="mj1958"></a>
# mj1958

roughly days since on midnight on 1958-01-01, Julian - 2436204.5 to be more precise.

***
<a name="mjd"></a>
# mjd

The Modified Julian Day (MJD) is the number of days (with decimal fraction of the day) that have elapsed since midnight at the beginning of Wednesday November 17, 1858. 
 Julian - 2400000.5

***
<a name="julianDay"></a>
# julianDay

The Julian Day (MJD) is the number of days (with decimal fraction of the day) that have elapsed since noon on January 1, 4713 BCE.  
 Julian - 2400000.5

***
<a name="cdfEpoch"></a>
# cdfEpoch

cdf epoch milliseconds since midnight, 01-Jan-0000, excluding those with a leap second.  There must be skipped days, because this doesn't yield 01-Jan-0000 for 0.,
 but works fine at 1-1-2000., excluding those within a leap second

***
<a name="cdfTT2000"></a>
# cdfTT2000

the number of nanoseconds since 01-Jan-2000T12:00, roughly.  This includes leap seconds, so conversion is more than a scale,offset.

***
<a name="decimalYear"></a>
# decimalYear

the year plus the fraction into the current year, ((doy-1)/365) for non-leap years.

***
<a name="percent"></a>
# percent

ratiometric units

***
<a name="dB"></a>
# dB

Define a set of units to describe ratiometric (logarithmic) spacing.  Note that Units.percent
 is no longer the defacto ratiometric spacing, and Units.percentIncrease takes its place.  
 Note the log10Ratio is the preferred method for expressing spacing, but all are convertible
 See logERatio, log10Ratio and google for "fold change."

***
<a name="ampRatio"></a>
# ampRatio



***
<a name="percentIncrease"></a>
# percentIncrease



***
<a name="log10Ratio"></a>
# log10Ratio



***
<a name="logERatio"></a>
# logERatio



***
<a name="add"></a>
# add
add( Number a, Number b, Units bUnits ) &rarr; Datum



### Parameters:
a - a Number
<br>b - a Number
<br>bUnits - an Units

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=add&unscoped_q=add">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="convertDoubleTo"></a>
# convertDoubleTo
convertDoubleTo( Units toUnits, double value ) &rarr; double

convert the double in this units' space to toUnits' space.

### Parameters:
toUnits - the units.
<br>value - the value in toUnits.

### Returns:
the double in the new units system.

<a href="https://github.com/autoplot/dev/search?q=convertDoubleTo&unscoped_q=convertDoubleTo">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createDatum"></a>
# createDatum
createDatum( double value ) &rarr; Datum



### Parameters:
value - a double

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=createDatum&unscoped_q=createDatum">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

createDatum( int value ) &rarr; Datum<br>
createDatum( long value ) &rarr; Datum<br>
createDatum( Number value ) &rarr; Datum<br>
createDatum( Datum value ) &rarr; Datum<br>
createDatum( double value, double resolution ) &rarr; Datum<br>
***
<a name="divide"></a>
# divide
divide( Number a, Number b, Units bUnits ) &rarr; Datum



### Parameters:
a - a Number
<br>b - a Number
<br>bUnits - an Units

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=divide&unscoped_q=divide">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="format"></a>
# format
format( Datum datum ) &rarr; String

format the Datum.

### Parameters:
datum - the Datum

### Returns:
the Datum formatted as a string.

<a href="https://github.com/autoplot/dev/search?q=format&unscoped_q=format">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getAllUnits"></a>
# getAllUnits
getAllUnits(  ) &rarr; List

return all the known units.

### Returns:
list of all the known units.

<a href="https://github.com/autoplot/dev/search?q=getAllUnits&unscoped_q=getAllUnits">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBasis"></a>
# getBasis
getBasis(  ) &rarr; Basis

return the Basis which defines the meaning of zero and the direction of positive values, such as 
 "since midnight, Jan 1, 1970"

### Returns:
the Basis object, which simply identifies a basis.

<a href="https://github.com/autoplot/dev/search?q=getBasis&unscoped_q=getBasis">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getByName"></a>
# getByName
getByName( String s ) &rarr; Units

returns a Units object with the given string representation that is stored in the unitsMap.
 Unlike lookupUnits, this will not allocate new units but will throw an IllegalArgumentException
 if the string is not recognized.

### Parameters:
s - units identifier

### Returns:
units object
### See Also:
<a href='#lookupUnits'>lookupUnits(java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getByName&unscoped_q=getByName">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCanonicalUnit"></a>
# getCanonicalUnit
getCanonicalUnit( Units units ) &rarr; Units

return the preferred unit to use when there are multiple representations
 of the same unit (having conversion UnitsConverter.IDENTITY.

### Parameters:
units - an Units

### Returns:
the preferred unit

<a href="https://github.com/autoplot/dev/search?q=getCanonicalUnit&unscoped_q=getCanonicalUnit">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getConvertableUnits"></a>
# <del>getConvertableUnits</del>
Deprecated: use getConvertibleUnits, which is spelled correctly.
***
<a name="getConverter"></a>
# getConverter
getConverter( Units fromUnits, Units toUnits ) &rarr; UnitsConverter

lookup the UnitsConverter object that takes numbers from fromUnits to toUnits.  
 This will chain together UnitsConverters registered via units.registerConverter.

### Parameters:
fromUnits - units instance that is the source units.
<br>toUnits - units instance that is the target units.

### Returns:
UnitsConverter object

<a href="https://github.com/autoplot/dev/search?q=getConverter&unscoped_q=getConverter">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getConverter( Units toUnits ) &rarr; UnitsConverter<br>
***
<a name="getConvertibleUnits"></a>
# getConvertibleUnits
getConvertibleUnits(  ) &rarr; Units

return the units to which this unit is convertible.

### Returns:
the units to which this unit is convertible.

<a href="https://github.com/autoplot/dev/search?q=getConvertibleUnits&unscoped_q=getConvertibleUnits">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDatumFormatterFactory"></a>
# getDatumFormatterFactory
getDatumFormatterFactory(  ) &rarr; DatumFormatterFactory

return the formatter factor for this Datum.

### Returns:
an org.das2.datum.format.DatumFormatterFactory


<a href="https://github.com/autoplot/dev/search?q=getDatumFormatterFactory&unscoped_q=getDatumFormatterFactory">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFillDatum"></a>
# getFillDatum
getFillDatum(  ) &rarr; Datum



### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getFillDatum&unscoped_q=getFillDatum">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFillDouble"></a>
# getFillDouble
getFillDouble(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=getFillDouble&unscoped_q=getFillDouble">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getId"></a>
# getId
getId(  ) &rarr; String

get the id uniquely identifying the units.  Note the id may contain
 special tokens, like "since" for time locations.

### Returns:
the id.

<a href="https://github.com/autoplot/dev/search?q=getId&unscoped_q=getId">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getOffsetUnits"></a>
# getOffsetUnits
getOffsetUnits(  ) &rarr; Units

return the units from the Basis for the unit, such as "seconds" in
 "seconds since midnight, Jan 1, 1970"

### Returns:
this units offsets.

<a href="https://github.com/autoplot/dev/search?q=getOffsetUnits&unscoped_q=getOffsetUnits">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="grannyFormat"></a>
# grannyFormat
grannyFormat( Datum datum ) &rarr; String

format the Datum, allowing use of subscripts and superscripts interpretted by GrannyTextRenderer.

### Parameters:
datum - the Datum

### Returns:
the Datum formatted as a string, possibly containing control sequences like !A and !n, etc.

<a href="https://github.com/autoplot/dev/search?q=grannyFormat&unscoped_q=grannyFormat">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isConvertableTo"></a>
# <del>isConvertableTo</del>
Deprecated: use isConvertibleTo (which does not contain spelling error)
***
<a name="isConvertibleTo"></a>
# isConvertibleTo
isConvertibleTo( Units toUnits ) &rarr; boolean

return true if the unit can be converted to toUnits.

### Parameters:
toUnits - Units object.

### Returns:
true if the unit can be converted to toUnits.

<a href="https://github.com/autoplot/dev/search?q=isConvertibleTo&unscoped_q=isConvertibleTo">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isFill"></a>
# isFill
isFill( double value ) &rarr; boolean



### Parameters:
value - a double

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isFill&unscoped_q=isFill">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

isFill( Number value ) &rarr; boolean<br>
***
<a name="isValid"></a>
# isValid
isValid( double value ) &rarr; boolean

test if the double represents a valid datum in the context of this unit.
 Note slight differences in implementation may cause isFill and isValid 
 to produce inconsistent results.  For example, this code checks for NaNs
 whereas isFill does not.

### Parameters:
value - the value to check.

### Returns:
true if the data is not fill and not NaN.

<a href="https://github.com/autoplot/dev/search?q=isValid&unscoped_q=isValid">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="lookupTimeLengthUnit"></a>
# lookupTimeLengthUnit
lookupTimeLengthUnit( String s ) &rarr; Units

return canonical das2 unit for colloquial time.

### Parameters:
s - string containing time unit like s, sec, millisec, etc.

### Returns:
an Units


<a href="https://github.com/autoplot/dev/search?q=lookupTimeLengthUnit&unscoped_q=lookupTimeLengthUnit">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="lookupTimeUnits"></a>
# lookupTimeUnits
lookupTimeUnits( Datum base, Units offsetUnits ) &rarr; Units

lookupUnits canonical units object, or allocate one.  If one is
 allocated, then parse for "&lt;unit&gt; since &lt;datum&gt;" and add conversion to
 "microseconds since 2000-001T00:00."  Note leap seconds are ignored!

### Parameters:
base - the base time, for example 2000-001T00:00.
<br>offsetUnits - the offset units for example microseconds.  Positive values of the units will be since the base time.

### Returns:
the unit.

<a href="https://github.com/autoplot/dev/search?q=lookupTimeUnits&unscoped_q=lookupTimeUnits">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

lookupTimeUnits( String units ) &rarr; Units<br>
***
<a name="lookupUnits"></a>
# lookupUnits
lookupUnits( String sunits ) &rarr; Units

lookupUnits canonical units object, or allocate one if the 
 unit has not been used already.
 Examples include:
   "nT" where it's already allocated,
   "apples" where it allocates a new one, and
   "seconds since 2011-12-21T00:00" where it uses lookupTimeUnits.

### Parameters:
sunits - string identifier.

### Returns:
canonical units object.
### See Also:
<a href='#getByName'>getByName(java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=lookupUnits&unscoped_q=lookupUnits">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="multiply"></a>
# multiply
multiply( Number a, Number b, Units bUnits ) &rarr; Datum



### Parameters:
a - a Number
<br>b - a Number
<br>bUnits - an Units

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=multiply&unscoped_q=multiply">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="nominal"></a>
# nominal
nominal(  ) &rarr; EnumerationUnits

return unit for identifying nominal data.  Strings are enumerated using
 this unit using the result's create(string) method, which returns a datum
 representing the string.  This method allocates
 a number for the string if one hasn't already been allocated, and the 
 name is unique within the namespace "default".

### Returns:
an EnumerationUnit with the namespace "default"

<a href="https://github.com/autoplot/dev/search?q=nominal&unscoped_q=nominal">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

nominal( String nameSpace ) &rarr; EnumerationUnits<br>
***
<a name="parse"></a>
# parse
parse( String s ) &rarr; Datum

parse the string in the context of these units.  The unit may
 throw a parse exception if it cannot be parsed, or may return
 a

### Parameters:
s - a String

### Returns:
a Datum


<a href="https://github.com/autoplot/dev/search?q=parse&unscoped_q=parse">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="registerConverter"></a>
# registerConverter
registerConverter( Units toUnits, org.das2.datum.UnitsConverter converter ) &rarr; void

register a converter between the units.  Note these converters can be 
 changed together to derive conversions. (A to B, B to C defines A to C.)

### Parameters:
toUnits - the target units
<br>converter - the converter that goes from this unit to target units.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=registerConverter&unscoped_q=registerConverter">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="subtract"></a>
# subtract
subtract( Number a, Number b, Units bUnits ) &rarr; Datum



### Parameters:
a - a Number
<br>b - a Number
<br>bUnits - an Units

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=subtract&unscoped_q=subtract">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

