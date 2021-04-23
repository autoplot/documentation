# org.das2.dataset.DefaultTableDataSet



# DefaultTableDataSet( double[] xTags, Units xUnits, double[][] yTags, Units yUnits, double[][][] zValues, Units zUnits, java.util.Map zValuesMap, java.util.Map zUnitsMap, java.util.Map properties )
Creates a new instance of DefaultTableDataSet for tables where the
 table geometry changes, and the DataSet contains multiple planes.

# DefaultTableDataSet( double[] xTags, Units xUnits, double[] yTags, Units yUnits, double[][] zValues, Units zUnits, java.util.Map properties )
Creates a DefaultTableDataSet when the table geometry changes.

***
<a name="createSimple"></a>
# createSimple
createSimple( double[] xTags, double[] yTags, double[][] zValues ) &rarr; DefaultTableDataSet



### Parameters:
xTags - a double[]
<br>yTags - a double[]
<br>zValues - a double[][]

### Returns:
org.das2.dataset.DefaultTableDataSet


<a href="https://github.com/autoplot/dev/search?q=createSimple&unscoped_q=createSimple">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="dump"></a>
# dump
dump( java.io.PrintStream out ) &rarr; void



### Parameters:
out - a PrintStream

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dump&unscoped_q=dump">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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
<a name="printDebugInfo"></a>
# printDebugInfo
printDebugInfo( java.io.PrintStream out ) &rarr; void



### Parameters:
out - a PrintStream

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=printDebugInfo&unscoped_q=printDebugInfo">[search for examples]</a>

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

***
<a name="toQDataSet"></a>
# toQDataSet
toQDataSet(  ) &rarr; AbstractDataSet

this is a highly-interleaved table, and if we sort it out and create a 
 optimal QDataSet, it's better.

### Returns:
a QDataSet version of the data

<a href="https://github.com/autoplot/dev/search?q=toQDataSet&unscoped_q=toQDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

