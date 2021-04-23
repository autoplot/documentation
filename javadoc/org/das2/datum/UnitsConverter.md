# org.das2.datum.UnitsConverterUnits Converter object performs scale/offset conversions, but can
 also be used any double-to-double conversion, and contains an
 implementation to chain multiple conversions together.
***
<a name="IDENTITY"></a>
# IDENTITY

No conversion, where convert trivially returns the value.

***
<a name="LOOSE_IDENTITY"></a>
# LOOSE_IDENTITY

Allow conversion, but this is a flag that indicates the result 
 should be dimensionless because the Ratiometric units were
 not convertible.

***
<a name="TERA"></a>
# TERA



***
<a name="GIGA"></a>
# GIGA



***
<a name="MEGA"></a>
# MEGA



***
<a name="KILO"></a>
# KILO



***
<a name="MILLI"></a>
# MILLI



***
<a name="CENTI"></a>
# CENTI



***
<a name="MICRO"></a>
# MICRO



***
<a name="NANO"></a>
# NANO



***
<a name="PICO"></a>
# PICO



***
<a name="append"></a>
# append
append( org.das2.datum.UnitsConverter that ) &rarr; UnitsConverter



### Parameters:
that - an UnitsConverter

### Returns:
org.das2.datum.UnitsConverter


<a href="https://github.com/autoplot/dev/search?q=append&unscoped_q=append">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="convert"></a>
# convert
convert( double value ) &rarr; double

convert the value in the source units to the target units.

### Parameters:
value - value in source units.

### Returns:
value in target units.

<a href="https://github.com/autoplot/dev/search?q=convert&unscoped_q=convert">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

convert( Number number ) &rarr; Number<br>
***
<a name="getConverter"></a>
# getConverter
getConverter( Units fromUnits, Units toUnits ) &rarr; UnitsConverter

lookup the UnitsConverter object that takes numbers from fromUnits to toUnits.
 This will chain together UnitsConverters registered via units.registerConverter.

### Parameters:
fromUnits - an Units
<br>toUnits - an Units

### Returns:
UnitsConverter object

<a href="https://github.com/autoplot/dev/search?q=getConverter&unscoped_q=getConverter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInverse"></a>
# getInverse
getInverse(  ) &rarr; UnitsConverter



### Returns:
org.das2.datum.UnitsConverter


<a href="https://github.com/autoplot/dev/search?q=getInverse&unscoped_q=getInverse">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

