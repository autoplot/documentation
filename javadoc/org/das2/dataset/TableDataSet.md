# org.das2.dataset.TableDataSetA <code>DataSet</code> implementation for 3 dimensional z(x,y) data sets
 where the data is arranged in a sequence of tables.  Each table will have
 a set of monotonically increasing x tags and y tags.  The x tags for all
 the tables, when taken together in the order that the table are in, will
 be monotonically increasing over the whole data set.  The y tags are constant
 over the y scans of each table, but may change, either in number or value,
 from table to table.
***
<a name="getDatum"></a>
# getDatum
getDatum( int i, int j ) &rarr; Datum

Returns the Z value for the given indices into the x and y tags as a
 <code>Datum</code>.

### Parameters:
i - index of the x tag for the requested value.
<br>j - index of the y tag for the requested value.

### Returns:
the value at index location (i, j) as a <code>Datum</code>

<a href="https://github.com/autoplot/dev/search?q=getDatum&unscoped_q=getDatum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDouble"></a>
# getDouble
getDouble( int i, int j, Units units ) &rarr; double

Returns the Z value for the given indices into the x and y tags as a
 <code>double</code> with the given units.

### Parameters:
i - index of the y tag for the requested value.
<br>j - index of the x tag for the requested value.
<br>units - the units the returned value should be converted to.

### Returns:
the value at index location (i, j) as a <code>double</code>.

<a href="https://github.com/autoplot/dev/search?q=getDouble&unscoped_q=getDouble">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDoubleScan"></a>
# getDoubleScan
getDoubleScan( int i, Units units ) &rarr; double



### Parameters:
i - an int
<br>units - an Units

### Returns:
double[]


<a href="https://github.com/autoplot/dev/search?q=getDoubleScan&unscoped_q=getDoubleScan">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInt"></a>
# getInt
getInt( int i, int j, Units units ) &rarr; int

Returns the Z value for the given indices into the x and y tags as a
 <code>int</code> with the given units.

### Parameters:
i - index of the x tag for the requested value.
<br>j - index of the y tag for the requested value.
<br>units - the units the returned value should be converted to.

### Returns:
the value at index location (i, j) as a <code>int</code>.

<a href="https://github.com/autoplot/dev/search?q=getInt&unscoped_q=getInt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getProperty"></a>
# getProperty
getProperty( int table, String name ) &rarr; Object

Return the property value attached to the table.  This should 
 simply return DataSet.getProperty() if the table has no special
 value for the table.

### Parameters:
table - an int
<br>name - a String

### Returns:
an Object


<a href="https://github.com/autoplot/dev/search?q=getProperty&unscoped_q=getProperty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getScan"></a>
# getScan
getScan( int i ) &rarr; DatumVector



### Parameters:
i - an int

### Returns:
org.das2.datum.DatumVector


<a href="https://github.com/autoplot/dev/search?q=getScan&unscoped_q=getScan">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getXSlice"></a>
# getXSlice
getXSlice( int i ) &rarr; VectorDataSet

Returns a slice view of this data set for a specific x value

### Parameters:
i - an int

### Returns:
org.das2.dataset.VectorDataSet


<a href="https://github.com/autoplot/dev/search?q=getXSlice&unscoped_q=getXSlice">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getYLength"></a>
# getYLength
getYLength( int table ) &rarr; int

Returns the number of y tags in the specified table for this data set.
  YTags must be monotonically increasing with j.

### Parameters:
table - index of the table

### Returns:
the number of x tags in this data set.

<a href="https://github.com/autoplot/dev/search?q=getYLength&unscoped_q=getYLength">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getYSlice"></a>
# getYSlice
getYSlice( int j, int table ) &rarr; VectorDataSet

Returns a slice view of this data set for a specific y value

### Parameters:
j - an int
<br>table - an int

### Returns:
org.das2.dataset.VectorDataSet


<a href="https://github.com/autoplot/dev/search?q=getYSlice&unscoped_q=getYSlice">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getYTagDatum"></a>
# getYTagDatum
getYTagDatum( int table, int j ) &rarr; Datum

Returns the value of the y tag at the given index j as a
      <code>Datum</code>.

### Parameters:
table - the table number
<br>j - the index of the requested y tag

### Returns:
the value of the y tag at the given index j as a
      <code>Datum</code>.

<a href="https://github.com/autoplot/dev/search?q=getYTagDatum&unscoped_q=getYTagDatum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getYTagDouble"></a>
# getYTagDouble
getYTagDouble( int table, int j, Units units ) &rarr; double

Returns the value of the y tag at the given index j as a
      <code>double</code> in the given units.  YTags must be
      monotonically increasing with j.

### Parameters:
table - the table number
<br>j - the index of the requested y tag
<br>units - the units of the returned value

### Returns:
the value of the y tag at the given index j as a
      <code>double</code>.

<a href="https://github.com/autoplot/dev/search?q=getYTagDouble&unscoped_q=getYTagDouble">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getYTagInt"></a>
# getYTagInt
getYTagInt( int table, int j, Units units ) &rarr; int

Returns the value of the y tag at the given index j as an
      <code>int</code> in the given units.  YTags must be
      monotonically increasing with j.

### Parameters:
table - an int
<br>j - the index of the requested y tag
<br>units - the units of the returned value

### Returns:
the value of the y tag at the given index j as an
      <code>int</code>.

<a href="https://github.com/autoplot/dev/search?q=getYTagInt&unscoped_q=getYTagInt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getYTags"></a>
# getYTags
getYTags( int table ) &rarr; DatumVector

Returns the yTags for this data set as a <code>DatumVector</code>

### Parameters:
table - the table number

### Returns:
the yTags for this data set as a <code>DatumVector</code>

<a href="https://github.com/autoplot/dev/search?q=getYTags&unscoped_q=getYTags">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getZUnits"></a>
# getZUnits
getZUnits(  ) &rarr; Units

Returns the Units object representing the unit type of the y values for
 this data set.

### Returns:
the x units

<a href="https://github.com/autoplot/dev/search?q=getZUnits&unscoped_q=getZUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="tableCount"></a>
# tableCount
tableCount(  ) &rarr; int

Returns the number of tables in this data set

### Returns:
the number of tables in this data set

<a href="https://github.com/autoplot/dev/search?q=tableCount&unscoped_q=tableCount">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="tableEnd"></a>
# tableEnd
tableEnd( int table ) &rarr; int

Returns the index after the last x tag index of the specified table

### Parameters:
table - the index of the table

### Returns:
the index after the last x tag index of the specified table

<a href="https://github.com/autoplot/dev/search?q=tableEnd&unscoped_q=tableEnd">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="tableOfIndex"></a>
# tableOfIndex
tableOfIndex( int i ) &rarr; int

Returns the table number that the specified index is in.

### Parameters:
i - x tag index

### Returns:
the table number that the specified index is in

<a href="https://github.com/autoplot/dev/search?q=tableOfIndex&unscoped_q=tableOfIndex">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="tableStart"></a>
# tableStart
tableStart( int table ) &rarr; int

Returns the first x tag index of the specified table.

### Parameters:
table - the index of the table.

### Returns:
the first x tag index of the specified table

<a href="https://github.com/autoplot/dev/search?q=tableStart&unscoped_q=tableStart">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

