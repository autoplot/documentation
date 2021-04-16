# org.das2.dataset.DefaultVectorDataSet
DefaultVectorDataSet( double[] xTags, Units xUnits, double[] yValues, Units yUnits, java.util.Map properties )
Creates a new instance of DefaultVectorDataSet

DefaultVectorDataSet( double[] xTags, Units xUnits, double[] yValues, Units yUnits, java.util.Map yValuesMap, java.util.Map yUnitsMap, java.util.Map properties )
Creates a new instance of DefaultVectorDataSet
 The keys for the properties, yValuesMap, and unitsMap parameter must
 consist solely of String values.  If any of these key sets contain
 non-string values an IllegalArgumentException will be thrown.
 The key set of the yUnitsMap parameter must match exactly the key set
 of the yValuesMap.  If their key sets do not exactly match, an
 IllegalArgumentException will be thrown.

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

***
<a name="getPlanarView"></a>
# getPlanarView
getPlanarView( String planeID ) &rarr; DataSet

Returns a <code>DataSet</code> with the specified view as the primary
 view.

### Parameters:
planeID - the <code>String</code> id of the requested plane.

### Returns:
the specified view, as a <code>DataSet</code>

<a href="https://github.com/autoplot/dev/search?q=getPlanarView&unscoped_q=getPlanarView">[search for examples]</a>

***
<a name="getPlaneIds"></a>
# getPlaneIds
getPlaneIds(  ) &rarr; String



### Returns:
java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=getPlaneIds&unscoped_q=getPlaneIds">[search for examples]</a>

