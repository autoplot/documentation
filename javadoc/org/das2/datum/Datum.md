# org.das2.datum.Datum

<p>A Datum is a number in the context of a Unit, for example "15 microseconds."
   A Datum object has methods for formatting itself as a String, representing 
  itself as a double in the context of another Unit, and mathematical
 operators that allow simple calculations to be made at the physical quantities.
 Also a Datum's precision can be limited to improve formatting.</p>
 <p>

***
<a name="abs"></a>
# abs
abs(  ) &rarr; Datum

return the absolute value (magnitude) of this Datum.  If this
 datum is fill then the result is fill.  This will have the same
 units as the datum.

### Returns:
a Datum

### See Also:
<a href='#value'>value()</a> which returns the double value.<br>

<a href="https://github.com/autoplot/dev/search?q=abs&unscoped_q=abs">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="add"></a>
# add
add( Datum datum ) &rarr; Datum

returns a Datum whose value is the sum of <tt>this</tt> and <tt>datum</tt>, in <tt>this.getUnits()</tt>.

### Parameters:
datum - Datum to add, that is convertible to this.getUnits().

### Returns:
a Datum that is the sum of the two values in this Datum's units.

<a href="https://github.com/autoplot/dev/search?q=add&unscoped_q=add">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

add( Number value, Units units ) &rarr; Datum<br>
add( double d, Units units ) &rarr; Datum<br>
***
<a name="compareTo"></a>
# compareTo
compareTo( Object a ) &rarr; int

compare the datum to the object.

### Parameters:
a - the Object to compare this datum to.

### Returns:
an int &lt; 0 if this comes before Datum a in this Datum's units space, 0 if they are equal, and &gt; 0 otherwise.

<a href="https://github.com/autoplot/dev/search?q=compareTo&unscoped_q=compareTo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

compareTo( Datum a ) &rarr; int<br>
***
<a name="convertTo"></a>
# convertTo
convertTo( Units units ) &rarr; Datum

creates an equivalent datum using a different unit.  For example,<code>
  x= Datum.create( 5, Units.seconds );
  System.err.println( x.convertTo( Units.seconds ) );
 </code>

### Parameters:
units - the new Datum's units

### Returns:
a datum with the new units, that is equal to the original datum.

<a href="https://github.com/autoplot/dev/search?q=convertTo&unscoped_q=convertTo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="create"></a>
# create
create( double value ) &rarr; Datum

convenient method for creating a dimensionless Datum with the given value.

### Parameters:
value - the magnitude of the datum.

### Returns:
a dimensionless Datum with the given value.

<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

create( double value, Units units ) &rarr; Datum<br>
create( double value, Units units, org.das2.datum.format.DatumFormatter formatter ) &rarr; Datum<br>
create( double value, Units units, double resolution ) &rarr; Datum<br>
create( double value, Units units, double resolution, org.das2.datum.format.DatumFormatter formatter ) &rarr; Datum<br>
create( int value ) &rarr; Datum<br>
create( int value, Units units ) &rarr; Datum<br>
***
<a name="div"></a>
# div
div( Datum datum ) &rarr; Datum

Groovy scripting language uses this for overloading.

### Parameters:
datum - Datum to divide, that is convertible to this.getUnits().

### Returns:
a Datum that is the divide of the two values in this Datum's units.

<a href="https://github.com/autoplot/dev/search?q=div&unscoped_q=div">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="divide"></a>
# divide
divide( Datum a ) &rarr; Datum

divide this by the datum <tt>a</tt>.  Currently, only division is only supported:<pre>
   between convertable units, resulting in a Units.dimensionless quantity, or
   by a Units.dimensionless quantity, and a datum with this datum's units is returned.</pre>
 This may change, as a generic SI units class is planned.

### Parameters:
a - the datum divisor.

### Returns:
the quotient.

<a href="https://github.com/autoplot/dev/search?q=divide&unscoped_q=divide">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

divide( Number a, Units units ) &rarr; Datum<br>
divide( double d ) &rarr; Datum<br>
***
<a name="doubleValue"></a>
# doubleValue
doubleValue( Units units ) &rarr; double

returns a double representing the datum in the context of <code>units</code>.

### Parameters:
units - the Units in which the double should be returned

### Returns:
a double in the context of the provided units.

<a href="https://github.com/autoplot/dev/search?q=doubleValue&unscoped_q=doubleValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="equals"></a>
# equals
equals( Object a ) &rarr; boolean

returns true if the two datums are equal.  That is, their double values are equal when converted to the same units.

### Parameters:
a - the Object to compare to.

### Returns:
true if the datums are equal.

<a href="https://github.com/autoplot/dev/search?q=equals&unscoped_q=equals">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

equals( Datum a ) &rarr; boolean<br>
***
<a name="exp10"></a>
# exp10
exp10(  ) &rarr; Datum

return Math.pow(10,v)

### Returns:
Math.pow(10,v)

<a href="https://github.com/autoplot/dev/search?q=exp10&unscoped_q=exp10">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="ge"></a>
# ge
ge( Datum a ) &rarr; boolean

returns true if this is greater than or equal to <tt>a</tt>.

### Parameters:
a - a datum convertible to this Datum's units.

### Returns:
true if this is greater than or equal to <tt>a</tt>.

<a href="https://github.com/autoplot/dev/search?q=ge&unscoped_q=ge">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFormatter"></a>
# getFormatter
getFormatter(  ) &rarr; DatumFormatter

returns a formatter suitable for formatting this datum as a string.

### Returns:
a formatter to be used to format this Datum into a String.

<a href="https://github.com/autoplot/dev/search?q=getFormatter&unscoped_q=getFormatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getResolution"></a>
# getResolution
getResolution( Units units ) &rarr; double

returns the resolution (or precision) of the datum.  This is metadata for the datum, used
 primarily to limit the number of decimal places displayed in a string representation,
 but operators like add and multiply will propagate errors through the calculation.

### Parameters:
units - the Units in which the double resolution should be returned.  Note
   the units must be convertible to this.getUnits().getOffsetUnits().

### Returns:
the double resolution of the datum in the context of units.

<a href="https://github.com/autoplot/dev/search?q=getResolution&unscoped_q=getResolution">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getUnits"></a>
# getUnits
getUnits(  ) &rarr; Units

returns the datum's units.  For example, UT times might have the units
 Units.us2000.

### Returns:
the datum's units.

<a href="https://github.com/autoplot/dev/search?q=getUnits&unscoped_q=getUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="gt"></a>
# gt
gt( Datum a ) &rarr; boolean

returns true if this is greater than <tt>a</tt>.

### Parameters:
a - a datum convertible to this Datum's units.

### Returns:
true if this is greater than <tt>a</tt>.

<a href="https://github.com/autoplot/dev/search?q=gt&unscoped_q=gt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hashCode"></a>
# hashCode
hashCode(  ) &rarr; int

returns a hashcode that is a function of the value and the units.

### Returns:
a hashcode for the datum

<a href="https://github.com/autoplot/dev/search?q=hashCode&unscoped_q=hashCode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="intValue"></a>
# intValue
intValue( Units units ) &rarr; int

returns a int representing the datum in the context of <code>units</code>.

### Parameters:
units - the Units in which the int should be returned

### Returns:
a double in the context of the provided units.

<a href="https://github.com/autoplot/dev/search?q=intValue&unscoped_q=intValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isFill"></a>
# isFill
isFill(  ) &rarr; boolean

convenience method for checking to see if a datum is a fill datum.

### Returns:
true if the value is fill as defined by the Datum's units.

<a href="https://github.com/autoplot/dev/search?q=isFill&unscoped_q=isFill">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isFinite"></a>
# isFinite
isFinite(  ) &rarr; boolean

returns true if the value is finite, that is not INFINITY or NaN.

### Returns:
true if the value is finite, that is not INFINITY or NaN.

<a href="https://github.com/autoplot/dev/search?q=isFinite&unscoped_q=isFinite">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="le"></a>
# le
le( Datum a ) &rarr; boolean

returns true if this is less than or equal to <tt>a</tt>.

### Parameters:
a - a datum convertible to this Datum's units.

### Returns:
true if this is less than or equal to <tt>a</tt>.

<a href="https://github.com/autoplot/dev/search?q=le&unscoped_q=le">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="log10"></a>
# log10
log10(  ) &rarr; Datum

return log10 of this datum.

### Returns:
log10 of this datum.

<a href="https://github.com/autoplot/dev/search?q=log10&unscoped_q=log10">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="lt"></a>
# lt
lt( Datum a ) &rarr; boolean

returns true if this is less than <tt>a</tt>.

### Parameters:
a - a datum convertible to this Datum's units.

### Returns:
true if this is less than <tt>a</tt>.

<a href="https://github.com/autoplot/dev/search?q=lt&unscoped_q=lt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="minus"></a>
# minus
minus( Datum datum ) &rarr; Datum

Groovy scripting language uses this for overloading.

### Parameters:
datum - Datum to subtract, that is convertible to this.getUnits().

### Returns:
a Datum that is the sum of the two values in this Datum's units.

<a href="https://github.com/autoplot/dev/search?q=minus&unscoped_q=minus">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="multiply"></a>
# multiply
multiply( Datum a ) &rarr; Datum

multiply this by the datum <tt>a</tt>.  Currently, only multiplication is only supported
   by a dimensionless datum, or when this is dimensionless.
 This may change, as a generic SI units class is planned.

 This should also throw an IllegalArgumentException if the units are LocationUnits (e.g. UT time), but doesn't.  This may
 change.

### Parameters:
a - the datum to multiply

### Returns:
the product.

<a href="https://github.com/autoplot/dev/search?q=multiply&unscoped_q=multiply">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

multiply( Number a, Units units ) &rarr; Datum<br>
multiply( double d ) &rarr; Datum<br>
***
<a name="negative"></a>
# negative
negative(  ) &rarr; Datum

Groovy scripting language uses this negation operator.

### Returns:
a Datum such that it plus this is 0.

<a href="https://github.com/autoplot/dev/search?q=negative&unscoped_q=negative">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="plus"></a>
# plus
plus( Datum datum ) &rarr; Datum

Groovy scripting language uses this for overloading.

### Parameters:
datum - Datum to add, that is convertible to this.getUnits().

### Returns:
a Datum that is the sum of the two values in this Datum's units.

<a href="https://github.com/autoplot/dev/search?q=plus&unscoped_q=plus">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="positive"></a>
# positive
positive(  ) &rarr; Datum

Groovy scripting language uses this positive operator.

### Returns:
this datum.

<a href="https://github.com/autoplot/dev/search?q=positive&unscoped_q=positive">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="power"></a>
# power
power( double b ) &rarr; Datum

Groovy scripting language uses this for overloading a**b.

### Parameters:
b - double to exponentiate, that is dimensionless.

### Returns:
a Datum that is the exponentiate of the two values in this Datum's units.

<a href="https://github.com/autoplot/dev/search?q=power&unscoped_q=power">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

power( Datum datum ) &rarr; Datum<br>
***
<a name="subtract"></a>
# subtract
subtract( Datum datum ) &rarr; Datum

returns a Datum whose value is the difference of <tt>this</tt> and <tt>value</tt>.
 The returned Datum will have units according to the type of units subtracted.
 For example, "1979-01-02T00:00" - "1979-01-01T00:00" = "24 hours" (this datum's unit's offset units),
 while "1979-01-02T00:00" - "1 hour" = "1979-01-01T23:00" (this datum's units.)

 Note also the resolution of the result is calculated.

### Parameters:
datum - Datum to add, that is convertible to this.getUnits() or offset units.

### Returns:
a Datum that is the sum of the two values in this Datum's units.

<a href="https://github.com/autoplot/dev/search?q=subtract&unscoped_q=subtract">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

subtract( Number a, Units units ) &rarr; Datum<br>
subtract( double d, Units units ) &rarr; Datum<br>
***
<a name="toString"></a>
# toString
toString(  ) &rarr; String

returns a human readable String representation of the Datum, which should also be parseable with
 Units.parse()

### Returns:
a human readable String representation of the Datum, which should also be parseable with
 Units.parse()

<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="value"></a>
# value
value(  ) &rarr; double

returns the double value without the unit, as long as the Units indicate this is a ratio measurement, and there is a meaningful 0.
 For example "5 Kg" &rarr; 5, but "2012-02-16T00:00" would throw an IllegalArgumentException.  Note this was introduced because often we just need
 to check to see if a value is zero.

### Returns:
a double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

