# org.das2.datum.LocationUnitsUnits for describing locations, Stevens' Interval Scale.
LocationUnits( String id, String description, Units offsetUnits, org.das2.datum.Basis basis )
Creates a new instance of LocationUnit

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

***
<a name="getBasis"></a>
# getBasis
getBasis(  ) &rarr; Basis

return the basis for the unit, such as "since 2000-01-01T00:00Z" or "north of Earth's equator"

### Returns:
an org.das2.datum.Basis


<a href="https://github.com/autoplot/dev/search?q=getBasis&unscoped_q=getBasis">[search for examples]</a>

***
<a name="getOffsetUnits"></a>
# getOffsetUnits
getOffsetUnits(  ) &rarr; Units

return the physical units of the basis vector, such as "microseconds" or "degrees"

### Returns:
an Units


<a href="https://github.com/autoplot/dev/search?q=getOffsetUnits&unscoped_q=getOffsetUnits">[search for examples]</a>

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

