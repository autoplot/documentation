# org.das2.graph.DasLabelAxis



# DasLabelAxis( org.das2.datum.DatumVector labels, int orientation )


# DasLabelAxis( QDataSet labels, int orientation )


***
<a name="createAttachedAxis"></a>
# createAttachedAxis
createAttachedAxis( org.das2.graph.DasRow row, org.das2.graph.DasColumn column ) &rarr; DasAxis



### Parameters:
row - a DasRow
<br>column - a DasColumn

### Returns:
org.das2.graph.DasAxis


<a href="https://github.com/autoplot/dev/search?q=createAttachedAxis&unscoped_q=createAttachedAxis">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

createAttachedAxis( int orientation ) &rarr; DasAxis<br>
***
<a name="findTick"></a>
# findTick
findTick( Datum xDatum, double direction, boolean minor ) &rarr; Datum



### Parameters:
xDatum - a Datum
<br>direction - a double
<br>minor - a boolean

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=findTick&unscoped_q=findTick">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getAffineTransform"></a>
# getAffineTransform
getAffineTransform( org.das2.graph.DasAxis.Memento memento, java.awt.geom.AffineTransform at ) &rarr; AffineTransform



### Parameters:
memento - a DasAxis.Memento
<br>at - an AffineTransform

### Returns:
java.awt.geom.AffineTransform


<a href="https://github.com/autoplot/dev/search?q=getAffineTransform&unscoped_q=getAffineTransform">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInterItemSpace"></a>
# getInterItemSpace
getInterItemSpace(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getInterItemSpace&unscoped_q=getInterItemSpace">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getItemMax"></a>
# getItemMax
getItemMax( Datum d ) &rarr; int

get the maximum pixel location  of the bin allocated to the Datum.

### Parameters:
d - a Datum

### Returns:
pixel location of the max.

<a href="https://github.com/autoplot/dev/search?q=getItemMax&unscoped_q=getItemMax">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getItemMin"></a>
# getItemMin
getItemMin( Datum d ) &rarr; int

get the minimum pixel location of the bin allocated to the Datum.

### Parameters:
d - a Datum

### Returns:
pixel location of the min.

<a href="https://github.com/autoplot/dev/search?q=getItemMin&unscoped_q=getItemMin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLabelPositions"></a>
# getLabelPositions
getLabelPositions(  ) &rarr; int



### Returns:
int[]


<a href="https://github.com/autoplot/dev/search?q=getLabelPositions&unscoped_q=getLabelPositions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getOutsidePadding"></a>
# getOutsidePadding
getOutsidePadding(  ) &rarr; int

Getter for property outsidePadding.

### Returns:
Value of property outsidePadding.

<a href="https://github.com/autoplot/dev/search?q=getOutsidePadding&unscoped_q=getOutsidePadding">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTickV"></a>
# getTickV
getTickV(  ) &rarr; TickVDescriptor



### Returns:
org.das2.graph.TickVDescriptor


<a href="https://github.com/autoplot/dev/search?q=getTickV&unscoped_q=getTickV">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="invTransform"></a>
# invTransform
invTransform( double d ) &rarr; Datum



### Parameters:
d - a double

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=invTransform&unscoped_q=invTransform">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isFloppyItemSpacing"></a>
# isFloppyItemSpacing
isFloppyItemSpacing(  ) &rarr; boolean

Getter for property floppyltemSpacing.

### Returns:
Value of property floppyltemSpacing.

<a href="https://github.com/autoplot/dev/search?q=isFloppyItemSpacing&unscoped_q=isFloppyItemSpacing">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFloppyItemSpacing"></a>
# setFloppyItemSpacing
setFloppyItemSpacing( boolean floppyItemSpacing ) &rarr; void

Setter for property floppyltemSpacing.

### Parameters:
floppyItemSpacing - New value of property floppyltemSpacing.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFloppyItemSpacing&unscoped_q=setFloppyItemSpacing">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLabelFormatter"></a>
# setLabelFormatter
setLabelFormatter( org.das2.datum.format.DatumFormatter df ) &rarr; void

vg1pws needed a way to explicitly set this.

### Parameters:
df - a DatumFormatter

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLabelFormatter&unscoped_q=setLabelFormatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setOutsidePadding"></a>
# setOutsidePadding
setOutsidePadding( int outsidePadding ) &rarr; void

Setter for property outsidePadding.

### Parameters:
outsidePadding - New value of property outsidePadding.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setOutsidePadding&unscoped_q=setOutsidePadding">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="transform"></a>
# transform
transform( double value, Units units ) &rarr; double



### Parameters:
value - a double
<br>units - an Units

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=transform&unscoped_q=transform">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="update"></a>
# update
update( org.das2.graph.event.DasUpdateEvent e ) &rarr; void



### Parameters:
e - a DasUpdateEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=update&unscoped_q=update">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="updateTickV"></a>
# updateTickV
updateTickV(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=updateTickV&unscoped_q=updateTickV">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

