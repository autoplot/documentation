# org.das2.datum.DatumUtil



***
<a name="asOrderOneUnits"></a>
# asOrderOneUnits
asOrderOneUnits( Datum d ) &rarr; Datum

This method takes the input datum and gets it as close to order one as
 possible by trying all possible conversions.

### Parameters:
d - A datum that needs to have its units changed to order one units.

### Returns:
The order-one-ified Datum.

<a href="https://github.com/autoplot/dev/search?q=asOrderOneUnits&unscoped_q=asOrderOneUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bestFormatter"></a>
# bestFormatter
bestFormatter( org.das2.datum.DatumVector datums ) &rarr; DatumFormatter



### Parameters:
datums - a DatumVector

### Returns:
org.das2.datum.format.DatumFormatter


<a href="https://github.com/autoplot/dev/search?q=bestFormatter&unscoped_q=bestFormatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

bestFormatter( Datum minimum, Datum maximum, int nsteps ) &rarr; DatumFormatter<br>
***
<a name="bestTimeFormatter"></a>
# bestTimeFormatter
bestTimeFormatter( Datum minimum, Datum maximum, int nsteps ) &rarr; DatumFormatter



### Parameters:
minimum - a Datum
<br>maximum - a Datum
<br>nsteps - an int

### Returns:
org.das2.datum.format.DatumFormatter


<a href="https://github.com/autoplot/dev/search?q=bestTimeFormatter&unscoped_q=bestTimeFormatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createValid"></a>
# createValid
createValid( String s ) &rarr; Datum

create a dimensionless datum by parsing the string.
 See TimeUtil.createValid( String stime ).

### Parameters:
s - a String

### Returns:
a Datum


<a href="https://github.com/autoplot/dev/search?q=createValid&unscoped_q=createValid">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="datumStringSplit"></a>
# datumStringSplit
datumStringSplit( String s ) &rarr; String

splits the datum into a magnitude part and a unit part.  When times
 are detected, "UTC" will be the units part.
 Here is a list to test against, and the motivation:
 <ul>
 <li> 2014-05-29T00:00 ISO8601 times, cannot contain spaces.
 <li> 5.e4 Hz          registered known units
 <li> 5.6 foos         units from the wild
 <li> 5.7 bytes/sec    mix of MKS and units from the wild.
 <li> 5.7Hz            no space
 <li> 5.7T             no space, contains T.
 <li> +5.7E+2Hz        more challenging double.
 <li> $57              unit before number
 </ul>
 Note: units cannot start with E or e then a number or plus or minus.
 Datums cannot contain commas, semicolons, or quotes.
 NaN is Double.NaN.
 
 TODO: only $ is supported as a prefix.  Others should be considered for
 completeness.

### Parameters:
s - the string-formatted datum

### Returns:
the magnitude and the units, or [null,s] when it is not parseable.

<a href="https://github.com/autoplot/dev/search?q=datumStringSplit&unscoped_q=datumStringSplit">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="divp"></a>
# divp
divp( Datum amount, Datum delta ) &rarr; Datum

this is the divide that rounds down to the next integer, so divp("-25hr","24hr") is -2.
 Note that the result must be dimensionless, other forms are not supported.
 TODO: study inconsistencies with QDataset Ops divp

### Parameters:
amount - a Datum
<br>delta - a Datum

### Returns:
the dimensionless amount.

<a href="https://github.com/autoplot/dev/search?q=divp&unscoped_q=divp">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="doubleValues"></a>
# doubleValues
doubleValues( org.das2.datum.Datum[] datums, Units units ) &rarr; double



### Parameters:
datums - an org.das2.datum.Datum[]
<br>units - an Units

### Returns:
double[]


<a href="https://github.com/autoplot/dev/search?q=doubleValues&unscoped_q=doubleValues">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

doubleValues( org.das2.datum.Datum[] datums, org.das2.datum.Units[] unitsArray ) &rarr; double<br>
***
<a name="fractionalDigits"></a>
# fractionalDigits
fractionalDigits( Datum resolution ) &rarr; int



### Parameters:
resolution - a Datum

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=fractionalDigits&unscoped_q=fractionalDigits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="limitLogResolutionFormatter"></a>
# limitLogResolutionFormatter
limitLogResolutionFormatter( Datum minimum, Datum maximum, int nsteps ) &rarr; DatumFormatter



### Parameters:
minimum - a Datum
<br>maximum - a Datum
<br>nsteps - an int

### Returns:
org.das2.datum.format.DatumFormatter


<a href="https://github.com/autoplot/dev/search?q=limitLogResolutionFormatter&unscoped_q=limitLogResolutionFormatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="limitResolutionFormatter"></a>
# limitResolutionFormatter
limitResolutionFormatter( Datum minimum, Datum maximum, int nsteps ) &rarr; DatumFormatter



### Parameters:
minimum - a Datum
<br>maximum - a Datum
<br>nsteps - an int

### Returns:
org.das2.datum.format.DatumFormatter


<a href="https://github.com/autoplot/dev/search?q=limitResolutionFormatter&unscoped_q=limitResolutionFormatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="lookupDatum"></a>
# lookupDatum
lookupDatum( String s ) &rarr; Datum

Attempts to resolve strings commonly encountered.  This was introduced to create a standard 
 method for resolving Strings in ASCII files to a Datum.
 This follows the rules that:
 <ul>
 <li> Things that appear to be times are parsed to a TimeLocationUnit.
 <li> a double followed by whitespace then a unit is parsed as lookupUnit then parse(double)
 </ul>
 Here is a list to test against, and the motivation:
 <ul>
 <li> 2014-05-29T00:00 ISO8601 times, cannot contain spaces.
 <li> 5.e4 Hz          registered known units
 <li> 5.6 foos         units from the wild
 <li> 5.7 bytes/sec    mix of MKS and units from the wild.
 <li> 5.7Hz            no space
 <li> 5.7T             no space, (contains T which is also in ISO8601 times)
 <li> 5.7eggs          e could be mistaken for exponent.
 <li> +5.7E+2Hz        more challenging double.
 <li> $57              unit before number
 </ul>

### Parameters:
s - a String

### Returns:
a Datum containing the value.
### See Also:
<a href='Units.md#parse'>Units#parse(java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=lookupDatum&unscoped_q=lookupDatum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="modp"></a>
# modp
modp( Datum amount, Datum delta ) &rarr; Datum

return the modulo within the delta.  The result will always
 be a positive number.  For example:
 <table><tr><td>modp('-3days','7days')</td><td>4days</td></tr>
 <tr><td>modp('10days','7days')</td><td>3days</td></tr>
 </table>
 A typical use might be:
 <pre>%{code
 t= t + modp(t-phaseStart,span)
 }</pre>
 TODO: study inconsistencies with QDataset Ops modp.

### Parameters:
amount - a Datum
<br>delta - a Datum

### Returns:
the amount.

<a href="https://github.com/autoplot/dev/search?q=modp&unscoped_q=modp">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="numericalResolutionLimit"></a>
# numericalResolutionLimit
numericalResolutionLimit( Datum datum ) &rarr; Datum

return the numeric resolution of the Datum.  Note some Datum implementations
 have additional information which allows the measurement resolution
 to be reflected as well, and this should be much smaller.

### Parameters:
datum - a datum

### Returns:
a datum in the offset units.

<a href="https://github.com/autoplot/dev/search?q=numericalResolutionLimit&unscoped_q=numericalResolutionLimit">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parse"></a>
# parse
parse( String s ) &rarr; Datum

attempt to parse the string as a datum.  Note that if the
 units aren't specified, then of course the Datum will be
 assumed to be dimensionless.  This also requires the the
 unit be registered already, and lookup should be used if
 the unit should be registered automatically.  
 Strings containing the unit UTC are parsed as times.  
 Strings containing an ISO8601 string like $Y-$m-$dT$H:$M are parsed as strings.

### Parameters:
s - the string representing the Datum, e.g. "5 Hz" (but not 5Hz).

### Returns:
the Datum

<a href="https://github.com/autoplot/dev/search?q=parse&unscoped_q=parse">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parseValid"></a>
# parseValid
parseValid( String s ) &rarr; Datum

parse the string which contains a valid representation of a
 a Datum.  A runtime exception is thrown when the string 
 cannot be parsed.

### Parameters:
s - the string representing the Datum, e.g. "5 Hz"

### Returns:
the Datum

<a href="https://github.com/autoplot/dev/search?q=parseValid&unscoped_q=parseValid">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="splitDatumString"></a>
# splitDatumString
splitDatumString( String s ) &rarr; String

Split the string to separate magnitude component from units component.
 "5" &rarr; [ "5", "" ]
 "5 m" &rarr; [ "5", "m" ]
 "5m" &rarr; [ "5", "m" ]
 "4.5m^2" &rarr; [ "4.5", "m^2" ] 
 "4.5e6m^2" &rarr; [ "4.5e6", "m^2" ]
 "-1" &rarr; [ "-1", "" ]
 "-1s" &rarr; [ "-1", "s" ]
 "-1.0e-6s" &rarr; [ "-1e-6", "s" ]
 "5 Deg N" &rarr;  [ "5", "Deg N" ]
 " 10 days" &rarr; [ "10", "days" ]
 See http://jfaden.net:8080/hudson/job/autoplot-test037/ws/splitDatumString.jy

### Parameters:
s - the string to break up

### Returns:
two element array

<a href="https://github.com/autoplot/dev/search?q=splitDatumString&unscoped_q=splitDatumString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="zeros"></a>
# zeros
zeros( int count ) &rarr; String

return "0" for 0, "0.0" for 1, "0.00" for 2, and so on.  This can be used
 in factory.newFormatter(formatString).

### Parameters:
count - number of decimal places following the decimal.

### Returns:
string for newFormatter.
### See Also:
<a href='DatumFormatterFactory.md#newFormatter'>DatumFormatterFactory#newFormatter(java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=zeros&unscoped_q=zeros">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

