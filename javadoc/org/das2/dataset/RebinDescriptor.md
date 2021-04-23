# org.das2.dataset.RebinDescriptorThe RebinDescriptor will quickly look up which 1-D bin a Datum is
 in.  This is not thread-safe, and must be used by only one thread during its
 lifetime.
RebinDescriptor( double start, double end, Units units, int nBin, boolean isLog )


RebinDescriptor( Datum start, Datum end, int nBin, boolean isLog )


***
<a name="FIRSTORLAST"></a>
# FIRSTORLAST



***
<a name="MINUSONE"></a>
# MINUSONE



***
<a name="EXTRAPOLATE"></a>
# EXTRAPOLATE



***
<a name="binCenter"></a>
# binCenter
binCenter( int ibin, Units units ) &rarr; double



### Parameters:
ibin - an int
<br>units - an Units

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=binCenter&unscoped_q=binCenter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

binCenter( int ibin ) &rarr; Datum<br>
***
<a name="binCenters"></a>
# binCenters
binCenters(  ) &rarr; double



### Returns:
double[]


<a href="https://github.com/autoplot/dev/search?q=binCenters&unscoped_q=binCenters">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="binCentersDV"></a>
# binCentersDV
binCentersDV(  ) &rarr; DatumVector



### Returns:
org.das2.datum.DatumVector


<a href="https://github.com/autoplot/dev/search?q=binCentersDV&unscoped_q=binCentersDV">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="binStart"></a>
# binStart
binStart( int ibin ) &rarr; Datum



### Parameters:
ibin - an int

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=binStart&unscoped_q=binStart">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

binStart( int ibin, Units units ) &rarr; double<br>
***
<a name="binStarts"></a>
# binStarts
binStarts(  ) &rarr; double

return the bin starts of all bins, in units of <tt>getUnits()</tt>

### Returns:
the bin starts of all bins

<a href="https://github.com/autoplot/dev/search?q=binStarts&unscoped_q=binStarts">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="binStop"></a>
# binStop
binStop( int ibin ) &rarr; Datum



### Parameters:
ibin - an int

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=binStop&unscoped_q=binStop">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

binStop( int ibin, Units units ) &rarr; double<br>
***
<a name="binStops"></a>
# binStops
binStops(  ) &rarr; double

return the bin stops of all bins, in units of <tt>getUnits()</tt>

### Returns:
the bin stops of all bins

<a href="https://github.com/autoplot/dev/search?q=binStops&unscoped_q=binStops">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="binWidth"></a>
# binWidth
binWidth(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=binWidth&unscoped_q=binWidth">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="binWidthDatum"></a>
# binWidthDatum
binWidthDatum(  ) &rarr; Datum



### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=binWidthDatum&unscoped_q=binWidthDatum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createSubsumingRebinDescriptor"></a>
# createSubsumingRebinDescriptor
createSubsumingRebinDescriptor( org.das2.dataset.RebinDescriptor ddY, Datum ymin, Datum ymax ) &rarr; RebinDescriptor



### Parameters:
ddY - a RebinDescriptor
<br>ymin - a Datum
<br>ymax - a Datum

### Returns:
org.das2.dataset.RebinDescriptor


<a href="https://github.com/autoplot/dev/search?q=createSubsumingRebinDescriptor&unscoped_q=createSubsumingRebinDescriptor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getUnits"></a>
# getUnits
getUnits(  ) &rarr; Units



### Returns:
org.das2.datum.Units


<a href="https://github.com/autoplot/dev/search?q=getUnits&unscoped_q=getUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isLog"></a>
# isLog
isLog(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isLog&unscoped_q=isLog">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="numberOfBins"></a>
# numberOfBins
numberOfBins(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=numberOfBins&unscoped_q=numberOfBins">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putDepDataSet"></a>
# putDepDataSet
putDepDataSet( QDataSet ds, org.das2.qds.MutablePropertyDataSet result, org.das2.dataset.RebinDescriptor ddX, org.das2.dataset.RebinDescriptor ddY ) &rarr; void

taken from AverageTableRebinner

### Parameters:
ds - the original dataset
<br>result - the rank 2 rebin target.
<br>ddX - the descriptor, or null.
<br>ddY - the descriptor, or null.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putDepDataSet&unscoped_q=putDepDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setOutOfBoundsAction"></a>
# setOutOfBoundsAction
setOutOfBoundsAction( int action ) &rarr; void



### Parameters:
action - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setOutOfBoundsAction&unscoped_q=setOutOfBoundsAction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="whichBin"></a>
# whichBin
whichBin( double x, Units units ) &rarr; int



### Parameters:
x - a double
<br>units - an Units

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=whichBin&unscoped_q=whichBin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

