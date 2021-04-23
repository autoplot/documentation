# org.das2.datum.format.ExponentialDatumFormatter

Formats Datums forcing a given exponent and number of decimal places.
 This is useful for axes where each of the labels should have the same
 exponent.  Zero is treated specially, just "0" is returned.  This helps
 one to quickly identify zero on the axis.

# ExponentialDatumFormatter( int digits, int exponent )


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
grannyFormat( Datum datum, Units units ) &rarr; String



### Parameters:
datum - a Datum
<br>units - an Units

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=grannyFormat&unscoped_q=grannyFormat">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

grannyFormat( Datum datum ) &rarr; String<br>
***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

