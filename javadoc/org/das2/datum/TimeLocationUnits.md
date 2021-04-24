# org.das2.datum.TimeLocationUnits



# TimeLocationUnits( String id, String description, Units offsetUnits, org.das2.datum.Basis basis )


***
<a name="getDatumFormatterFactory"></a>
# getDatumFormatterFactory
getDatumFormatterFactory(  ) &rarr; DatumFormatterFactory



### Returns:
org.das2.datum.format.DatumFormatterFactory


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
<a name="getTimeZone"></a>
# getTimeZone
getTimeZone(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getTimeZone&unscoped_q=getTimeZone">[search for examples]</a>
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

***
<a name="isValid"></a>
# isValid
isValid( double value ) &rarr; boolean

test if the double represents a valid datum in the context of this unit.

### Parameters:
value - a double

### Returns:
true if the data is not fill.

<a href="https://github.com/autoplot/dev/search?q=isValid&unscoped_q=isValid">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parse"></a>
# parse
parse( String s ) &rarr; Datum



### Parameters:
s - a String

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=parse&unscoped_q=parse">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="validMax"></a>
# validMax
validMax(  ) &rarr; double

return the maximum valid value.  Any value greater than this value is invalid.

### Returns:
the maximum valid value.

<a href="https://github.com/autoplot/dev/search?q=validMax&unscoped_q=validMax">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="validMin"></a>
# validMin
validMin(  ) &rarr; double

return the minimum valid value.  Any value less than this value is invalid.

### Returns:
the minimum valid value

<a href="https://github.com/autoplot/dev/search?q=validMin&unscoped_q=validMin">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

