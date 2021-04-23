# org.das2.datum.format.DatumFormatterFormats Datum objects for printing and parses strings to Datum objects.
***
<a name="axisFormat"></a>
# axisFormat
axisFormat( org.das2.datum.DatumVector datums, DatumRange context ) &rarr; String

format the set of Datums using a consistent and optimized format.
 First introduced to support DasAxis, where tighter coupling between
 the two is required to efficiently provide context.

### Parameters:
datums - a DatumVector
<br>context - visible range, context should be provided.

### Returns:
a java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=axisFormat&unscoped_q=axisFormat">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="format"></a>
# format
format( Datum datum ) &rarr; String



### Parameters:
datum - a Datum

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=format&unscoped_q=format">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

format( Datum datum, Units units ) &rarr; String<br>
***
<a name="grannyFormat"></a>
# grannyFormat
grannyFormat( Datum datum ) &rarr; String

Returns the datum formatted as a String with special formatting
 characters.  As with format, this should be out-of-context and should
 be tagged with the Units. 

 The default implementation just returns the result of
 {@link #format(org.das2.datum.Datum)}

### Parameters:
datum - a Datum

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=grannyFormat&unscoped_q=grannyFormat">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

grannyFormat( Datum datum, Units units ) &rarr; String<br>
