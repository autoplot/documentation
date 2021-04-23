# org.das2.dataset.TableDataSetBuilder

Handles 1-N planes of table data.

 Update Note:  Historically by default there was an un-named plane, that was always
               present in the builder.  I removed that so that all planes could have a
               name, it probably breaks lots of stuff so extensive tests are needed
               before this change is committed. -cwp 2014-09-22

# TableDataSetBuilder( Units xUnits, Units yUnits, Units zUnits )
Creates a new instance of TableDataSetBuilder with a default plane
 A single plane with the empty string as it's name is defined.

# TableDataSetBuilder( Units xUnits, Units yUnits, Units zUnits, String name )
Creates a new instance of TableDataSetBuilder with a named default plane

***
<a name="addPlane"></a>
# addPlane
addPlane( String name, Units zUnits ) &rarr; void



### Parameters:
name - a String
<br>zUnits - an Units

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPlane&unscoped_q=addPlane">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addPlane( String name, Units zUnits, java.util.Map properties ) &rarr; void<br>
***
<a name="addProperties"></a>
# addProperties
addProperties( java.util.Map map ) &rarr; void



### Parameters:
map - a java.util.Map

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addProperties&unscoped_q=addProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="append"></a>
# append
append( org.das2.dataset.TableDataSet tds ) &rarr; void



### Parameters:
tds - a TableDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=append&unscoped_q=append">[search for examples]</a>

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

***
<a name="getXLength"></a>
# getXLength
getXLength(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getXLength&unscoped_q=getXLength">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getXTag"></a>
# getXTag
getXTag( int i ) &rarr; double



### Parameters:
i - an int

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=getXTag&unscoped_q=getXTag">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="insertYScan"></a>
# insertYScan
insertYScan( Datum x, org.das2.datum.DatumVector y, org.das2.datum.DatumVector z ) &rarr; void



### Parameters:
x - a Datum
<br>y - a DatumVector
<br>z - a DatumVector

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=insertYScan&unscoped_q=insertYScan">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

insertYScan( Datum x, org.das2.datum.DatumVector y, org.das2.datum.DatumVector z, String planeId ) &rarr; void<br>
insertYScan( Datum xTag, org.das2.datum.DatumVector yTags, org.das2.datum.DatumVector[] scans, java.lang.String[] planeIDs ) &rarr; void<br>
***
<a name="setPlaneProperties"></a>
# setPlaneProperties
setPlaneProperties( int table, java.util.Map properties ) &rarr; void



### Parameters:
table - an int
<br>properties - a java.util.Map

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPlaneProperties&unscoped_q=setPlaneProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setProperty"></a>
# setProperty
setProperty( String name, Object value ) &rarr; void



### Parameters:
name - a String
<br>value - an Object

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setProperty&unscoped_q=setProperty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

setProperty( int table, String name, Object value ) &rarr; void<br>
***
<a name="setXUnits"></a>
# setXUnits
setXUnits( Units units ) &rarr; void



### Parameters:
units - an Units

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setXUnits&unscoped_q=setXUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setYUnits"></a>
# setYUnits
setYUnits( Units units ) &rarr; void



### Parameters:
units - an Units

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setYUnits&unscoped_q=setYUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setZUnits"></a>
# setZUnits
setZUnits( Units units ) &rarr; void



### Parameters:
units - an Units

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setZUnits&unscoped_q=setZUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

setZUnits( Units units, String planeID ) &rarr; void<br>
***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toTableDataSet"></a>
# toTableDataSet
toTableDataSet(  ) &rarr; TableDataSet



### Returns:
org.das2.dataset.TableDataSet


<a href="https://github.com/autoplot/dev/search?q=toTableDataSet&unscoped_q=toTableDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

