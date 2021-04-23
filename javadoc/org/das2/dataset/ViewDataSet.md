# org.das2.dataset.ViewDataSetA DataSet implementation that share properties, yUnits and
 yUnits with the instance of AbstractDataSet it is associated with.
 This class is provided so that sub-classes of AbstractDataSet can
 extend this class when creating views of their data without having
 to copy the immutable data AbstractDataSet contains.
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

Returns the value of the property that <code>name</code> represents

### Parameters:
name - String name of the property requested

### Returns:
the value of the property that <code>name</code> represents

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

Returns the Units object representing the unit type of the x tags
 for this data set.

### Returns:
the x units

<a href="https://github.com/autoplot/dev/search?q=getXUnits&unscoped_q=getXUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getYUnits"></a>
# getYUnits
getYUnits(  ) &rarr; Units

Returns the Units object representing the unit type of the y tags
 or y values for this data set.

### Returns:
the y units

<a href="https://github.com/autoplot/dev/search?q=getYUnits&unscoped_q=getYUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

