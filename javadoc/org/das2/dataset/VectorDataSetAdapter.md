# org.das2.dataset.VectorDataSetAdapter



# VectorDataSetAdapter( QDataSet y, QDataSet x )
Creates a new instance of VectorDataSetAdapter

***
<a name="create"></a>
# create
create( QDataSet y ) &rarr; VectorDataSet



### Parameters:
y - a QDataSet

### Returns:
org.das2.dataset.VectorDataSet


<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createFromBundle"></a>
# createFromBundle
createFromBundle( QDataSet bds ) &rarr; VectorDataSet

In das2's dataset, Z(X,Y) where X and Y are rank 1, this is
 a dataset with Y(X) and Y has a plane for the Z values.
 Also we adapt a bundle with two columns to Y(X).

### Parameters:
bds - a dataset

### Returns:
an org.das2.dataset.VectorDataSet


<a href="https://github.com/autoplot/dev/search?q=createFromBundle&unscoped_q=createFromBundle">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDatum"></a>
# getDatum
getDatum( int i ) &rarr; Datum



### Parameters:
i - an int

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getDatum&unscoped_q=getDatum">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDouble"></a>
# getDouble
getDouble( int i, Units units ) &rarr; double



### Parameters:
i - an int
<br>units - an Units

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=getDouble&unscoped_q=getDouble">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInt"></a>
# getInt
getInt( int i, Units units ) &rarr; int



### Parameters:
i - an int
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



### Returns:
org.das2.datum.Units


<a href="https://github.com/autoplot/dev/search?q=getXUnits&unscoped_q=getXUnits">[search for examples]</a>
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
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

