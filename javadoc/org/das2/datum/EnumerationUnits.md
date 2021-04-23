# org.das2.datum.EnumerationUnits

Units class for mapping arbitrary objects to Datums.  Nothing about the contract
 for a Datum requires that they correspond to physical quantities, and we can
 assign a mapping from numbers to objects using this class.  This allows 
 information such as "Cluster 1" or "Spin Flip" to be encoded.
 
 This is used to model ordinal or nominal data, as described in
 http://en.wikipedia.org/wiki/Level_of_measurement

# EnumerationUnits( String id )


# EnumerationUnits( String id, String description )


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



### Parameters:
toUnits - an Units
<br>value - a double

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=convertDoubleTo&unscoped_q=convertDoubleTo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="create"></a>
# create
create( Object o ) &rarr; EnumerationUnits

create the enumeration unit with the given context.

### Parameters:
o - an Object

### Returns:
an org.das2.datum.EnumerationUnits


<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createDatum"></a>
# createDatum
createDatum( int ival, Object sval, int color ) &rarr; Datum

creates the datum, explicitly setting the ordinal.  Use with caution.

### Parameters:
ival - the integer value of the datum
<br>sval - the object to associate.  This can be an object for legacy reasons, but should be a String.
<br>color - RGB color to associate with this value.

### Returns:
the Datum, which may have been created already.

<a href="https://github.com/autoplot/dev/search?q=createDatum&unscoped_q=createDatum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

createDatum( int ival, Object sval ) &rarr; Datum<br>
createDatum( Object object ) &rarr; Datum<br>
createDatum( int value ) &rarr; Datum<br>
createDatum( long value ) &rarr; Datum<br>
createDatum( Number value ) &rarr; Datum<br>
createDatum( double d ) &rarr; Datum<br>
createDatum( double d, double resolution ) &rarr; Datum<br>
createDatum( Datum value ) &rarr; Datum<br>
***
<a name="createDatumAndUnits"></a>
# createDatumAndUnits
createDatumAndUnits( Object object ) &rarr; Datum



### Parameters:
object - an Object

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=createDatumAndUnits&unscoped_q=createDatumAndUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createDatumVector"></a>
# createDatumVector
createDatumVector( java.lang.Object[] objects ) &rarr; DatumVector



### Parameters:
objects - a java.lang.Object[]

### Returns:
org.das2.datum.DatumVector


<a href="https://github.com/autoplot/dev/search?q=createDatumVector&unscoped_q=createDatumVector">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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
<a name="getColor"></a>
# getColor
getColor( Datum d ) &rarr; int

return color suggestion for this value.  Note this color is not always used.

### Parameters:
d - the datum

### Returns:
the color suggestions

<a href="https://github.com/autoplot/dev/search?q=getColor&unscoped_q=getColor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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

return the datum for ""

### Returns:
a Datum


<a href="https://github.com/autoplot/dev/search?q=getFillDatum&unscoped_q=getFillDatum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFillDouble"></a>
# getFillDouble
getFillDouble(  ) &rarr; double

return the double for ""

### Returns:
a double


<a href="https://github.com/autoplot/dev/search?q=getFillDouble&unscoped_q=getFillDouble">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getHighestOrdinal"></a>
# getHighestOrdinal
getHighestOrdinal(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getHighestOrdinal&unscoped_q=getHighestOrdinal">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getObject"></a>
# getObject
getObject( Datum datum ) &rarr; Object

return the object (typically a string) associated with this Datum

### Parameters:
datum - a Datum

### Returns:
the object associated with the Datum.

<a href="https://github.com/autoplot/dev/search?q=getObject&unscoped_q=getObject">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getValues"></a>
# getValues
getValues(  ) &rarr; Map

provides access to map of all values.

### Returns:
all the values

<a href="https://github.com/autoplot/dev/search?q=getValues&unscoped_q=getValues">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasFillDatum"></a>
# hasFillDatum
hasFillDatum(  ) &rarr; boolean

true if fill has been defined, which is the empty string or all spaces.

### Returns:
true if fill has been defined.

<a href="https://github.com/autoplot/dev/search?q=hasFillDatum&unscoped_q=hasFillDatum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isFill"></a>
# isFill
isFill( Number value ) &rarr; boolean



### Parameters:
value - a Number

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isFill&unscoped_q=isFill">[search for examples]</a>

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

