# org.das2.dataset.SimpleTableDataSet

optimized TableDataSet where only 1-table data set is supported,
 and is backed by a 1-D array.  This is to house the result of the rebin method 
 used for spectrograms.

# SimpleTableDataSet( double[] x, double[] y, double[] z, Units xunits, Units yunits, Units zunits )


# SimpleTableDataSet( double[] x, double[] y, double[] z, Units xunits, Units yunits, Units zunits, String planeName, org.das2.dataset.TableDataSet planeData )


***
<a name="getDatum"></a>
# getDatum
getDatum( int i, int j ) &rarr; Datum



### Parameters:
i - an int
<br>j - an int

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getDatum&unscoped_q=getDatum">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDouble"></a>
# getDouble
getDouble( int i, int j, Units units ) &rarr; double



### Parameters:
i - an int
<br>j - an int
<br>units - an Units

### Returns:
double


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



### Parameters:
i - an int
<br>j - an int
<br>units - an Units

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getInt&unscoped_q=getInt">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlanarView"></a>
# getPlanarView
getPlanarView( String planeID ) &rarr; DataSet



### Parameters:
planeID - a String

### Returns:
org.das2.dataset.DataSet


<a href="https://github.com/autoplot/dev/search?q=getPlanarView&unscoped_q=getPlanarView">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlaneIds"></a>
# getPlaneIds
getPlaneIds(  ) &rarr; String



### Returns:
java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=getPlaneIds&unscoped_q=getPlaneIds">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getProperties"></a>
# getProperties
getProperties(  ) &rarr; Map



### Returns:
java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getProperties&unscoped_q=getProperties">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getProperty"></a>
# getProperty
getProperty( String name ) &rarr; Object



### Parameters:
name - a String

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=getProperty&unscoped_q=getProperty">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getProperty( int table, String name ) &rarr; Object<br>
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
<a name="getXLength"></a>
# getXLength
getXLength(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getXLength&unscoped_q=getXLength">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getXSlice"></a>
# getXSlice
getXSlice( int i ) &rarr; VectorDataSet



### Parameters:
i - an int

### Returns:
org.das2.dataset.VectorDataSet


<a href="https://github.com/autoplot/dev/search?q=getXSlice&unscoped_q=getXSlice">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getXTagDatum"></a>
# getXTagDatum
getXTagDatum( int i ) &rarr; Datum



### Parameters:
i - an int

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getXTagDatum&unscoped_q=getXTagDatum">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getXTagDouble"></a>
# getXTagDouble
getXTagDouble( int i, Units units ) &rarr; double



### Parameters:
i - an int
<br>units - an Units

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=getXTagDouble&unscoped_q=getXTagDouble">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getXTagInt"></a>
# getXTagInt
getXTagInt( int i, Units units ) &rarr; int



### Parameters:
i - an int
<br>units - an Units

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getXTagInt&unscoped_q=getXTagInt">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getXUnits"></a>
# getXUnits
getXUnits(  ) &rarr; Units



### Returns:
org.das2.datum.Units


<a href="https://github.com/autoplot/dev/search?q=getXUnits&unscoped_q=getXUnits">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getYLength"></a>
# getYLength
getYLength( int table ) &rarr; int



### Parameters:
table - an int

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getYLength&unscoped_q=getYLength">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getYSlice"></a>
# getYSlice
getYSlice( int j, int table ) &rarr; VectorDataSet



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



### Parameters:
table - an int
<br>j - an int

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getYTagDatum&unscoped_q=getYTagDatum">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getYTagDouble"></a>
# getYTagDouble
getYTagDouble( int table, int j, Units units ) &rarr; double



### Parameters:
table - an int
<br>j - an int
<br>units - an Units

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=getYTagDouble&unscoped_q=getYTagDouble">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getYTagInt"></a>
# getYTagInt
getYTagInt( int table, int j, Units units ) &rarr; int



### Parameters:
table - an int
<br>j - an int
<br>units - an Units

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getYTagInt&unscoped_q=getYTagInt">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getYTags"></a>
# getYTags
getYTags( int table ) &rarr; DatumVector



### Parameters:
table - an int

### Returns:
org.das2.datum.DatumVector


<a href="https://github.com/autoplot/dev/search?q=getYTags&unscoped_q=getYTags">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getYUnits"></a>
# getYUnits
getYUnits(  ) &rarr; Units



### Returns:
org.das2.datum.Units


<a href="https://github.com/autoplot/dev/search?q=getYUnits&unscoped_q=getYUnits">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getZUnits"></a>
# getZUnits
getZUnits(  ) &rarr; Units



### Returns:
org.das2.datum.Units


<a href="https://github.com/autoplot/dev/search?q=getZUnits&unscoped_q=getZUnits">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setYTagDouble"></a>
# setYTagDouble
setYTagDouble( int table, int j, double yvalue, Units units ) &rarr; void



### Parameters:
table - an int
<br>j - an int
<br>yvalue - a double
<br>units - an Units

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setYTagDouble&unscoped_q=setYTagDouble">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="tableCount"></a>
# tableCount
tableCount(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=tableCount&unscoped_q=tableCount">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="tableEnd"></a>
# tableEnd
tableEnd( int table ) &rarr; int



### Parameters:
table - an int

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=tableEnd&unscoped_q=tableEnd">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="tableOfIndex"></a>
# tableOfIndex
tableOfIndex( int i ) &rarr; int



### Parameters:
i - an int

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=tableOfIndex&unscoped_q=tableOfIndex">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="tableStart"></a>
# tableStart
tableStart( int table ) &rarr; int



### Parameters:
table - an int

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=tableStart&unscoped_q=tableStart">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

