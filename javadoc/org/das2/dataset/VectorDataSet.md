# org.das2.dataset.VectorDataSetInterface definition for datasets comprised of a y value
 for each x tag such that y(x).
***
<a name="getDatum"></a>
# getDatum
getDatum( int i ) &rarr; Datum

Returns the Y value for the given index into the x tags as a
 <code>Datum</code>.

### Parameters:
i - index of the x tag for the requested value.

### Returns:
the value at index location i as a <code>Datum</code>

<a href="https://github.com/autoplot/dev/search?q=getDatum&unscoped_q=getDatum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDouble"></a>
# getDouble
getDouble( int i, Units units ) &rarr; double

Returns the Y value for the given index into the x tags as a
 <code>double</code> with the given units.

### Parameters:
i - index of the x tag for the requested value.
<br>units - the units the returned value should be coverted to.

### Returns:
the value at index location i as a <code>double</code>.

<a href="https://github.com/autoplot/dev/search?q=getDouble&unscoped_q=getDouble">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInt"></a>
# getInt
getInt( int i, Units units ) &rarr; int

Returns the Y value for the given index into the x tags as a
 <code>int</code> with the given units.

### Parameters:
i - index of the x tag for the requested value.
<br>units - the units the returned value should be coverted to.

### Returns:
the value at index location i as a <code>int</code>.

<a href="https://github.com/autoplot/dev/search?q=getInt&unscoped_q=getInt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

