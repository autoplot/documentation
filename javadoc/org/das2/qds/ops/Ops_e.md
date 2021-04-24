***
<a name="ellipse"></a>
# ellipse
ellipse( double xwidth, double ywidth ) &rarr; QDataSet

return a dataset with X and Y forming a ellipse, introduced as a convenient way to indicate 
 planet location of any planet, according to Masafumi.

### Parameters:
xwidth - a double
<br>ywidth - a double

### Returns:
QDataSet that when plotted is an ellipse.

<a href="https://github.com/autoplot/dev/search?q=ellipse&unscoped_q=ellipse">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="ensureMonotonic"></a>
# ensureMonotonic
ensureMonotonic( QDataSet ds ) &rarr; QDataSet

possibly sort the data where the DEPEND_0 tags are
 monotonically increasing.  If the data is already monotonic,
 then nothing is done to the data.

### Parameters:
ds - the dataset

### Returns:
the dataset, sorted if necessary.
### See Also:
<a href='DataSetUtil_i.md#isMonotonic'>DataSetUtil#isMonotonic</a> <br>

<a href="https://github.com/autoplot/dev/search?q=ensureMonotonic&unscoped_q=ensureMonotonic">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="ensureMonotonicAndIncreasingWithFill"></a>
# ensureMonotonicAndIncreasingWithFill
ensureMonotonicAndIncreasingWithFill( QDataSet ds ) &rarr; QDataSet

Return data where the DEPEND_0 tags are 
 monotonically increasing and non repeating. Instead of sorting the data, simply replace repeat records with
 a fill record.

### Parameters:
ds - the dataset

### Returns:
the dataset, sorted if necessary.
 TODO: It's surprising that monotonic doesn't imply non-repeating, and this really needs to be revisited.
### See Also:
<a href='DataSetUtil_i.md#isMonotonicAndIncreasingQuick'>DataSetUtil#isMonotonicAndIncreasingQuick</a> <br>

<a href="https://github.com/autoplot/dev/search?q=ensureMonotonicAndIncreasingWithFill&unscoped_q=ensureMonotonicAndIncreasingWithFill">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="eq"></a>
# eq
eq( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

element-wise equality test.  1.0 is returned where the two datasets are
 equal.  Fill is returned where either measurement is invalid.

### Parameters:
ds1 - rank n dataset
<br>ds2 - rank m dataset with compatible geometry.

### Returns:
rank n or m dataset.

<a href="https://github.com/autoplot/dev/search?q=eq&unscoped_q=eq">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

eq( Object ds1, Object ds2 ) &rarr; QDataSet<br>
***
<a name="equalProperties"></a>
# equalProperties
equalProperties( java.util.Map m1, java.util.Map m2 ) &rarr; HashMap

returns the subset of two groups of properties that are equal, so these
 may be preserved through operations.

### Parameters:
m1 - map of dataset properties, including DEPEND properties.
<br>m2 - map of dataset properties, including DEPEND properties.

### Returns:
the subset of two groups of properties that are equal

<a href="https://github.com/autoplot/dev/search?q=equalProperties&unscoped_q=equalProperties">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="equivalent"></a>
# equivalent
equivalent( QDataSet ds1, QDataSet ds2 ) &rarr; boolean

returns true iff the dataset values are equivalent.  Note this
 may promote rank, etc.  If the two datasets have enumerations, then we 
 create datums and check .equals.  This does not check TITLE, etc,  
 just that the units and values are equal.

### Parameters:
ds1 - the first dataset
<br>ds2 - the second dataset

### Returns:
true if the dataset values are equivalent.

<a href="https://github.com/autoplot/dev/search?q=equivalent&unscoped_q=equivalent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

equivalent( Object ds1, Object ds2 ) &rarr; boolean<br>
***
<a name="eventsComplement"></a>
# eventsComplement
eventsComplement( QDataSet events, DatumRange range, int color, String msg ) &rarr; QDataSet

Return an events list of time intervals which are not covered in the events list.
 A new events list is returned, containing events with the given color and message.
 This is expected to have a number of uses, one being identifying where data is 
 missing.  Note this assumes events are not overlapping.

### Parameters:
events - an events list
<br>range - find gaps in events within this range
<br>color - color for the missing events
<br>msg - message to attach to these events

### Returns:
the events data set.
### See Also:
<a href='Ops_c.md#createEvent'>createEvent(java.lang.String, int, java.lang.String)</a> <br>
<a href='Ops_e.md#eventsConjunction'>eventsConjunction(QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=eventsComplement&unscoped_q=eventsComplement">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="eventsConjunction"></a>
# eventsConjunction
eventsConjunction( QDataSet tE, QDataSet tB ) &rarr; QDataSet

return an events list of when events are found in both events lists. 
 (This might have been better called "eventsIntersection")

### Parameters:
tE - rank 2 canonical events list
<br>tB - rank 2 canonical events list

### Returns:
rank 2 canonical events list
### See Also:
<a href='Schemes_e.md#eventsList'>Schemes#eventsList()</a> <br>
<a href='Ops_d.md#dataIntersection'>dataIntersection(QDataSet, QDataSet)</a> <br>
<a href='Ops_e.md#eventsComplement'>eventsComplement(QDataSet, org.das2.datum.DatumRange, int, java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=eventsConjunction&unscoped_q=eventsConjunction">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="exp"></a>
# exp
exp( QDataSet ds ) &rarr; QDataSet

element-wise exponentiate e**x.

### Parameters:
ds - the dataset

### Returns:
dataset of the same geometry

<a href="https://github.com/autoplot/dev/search?q=exp&unscoped_q=exp">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

exp( double d ) &rarr; double<br>
exp( Object ds1 ) &rarr; QDataSet<br>
***
<a name="exp10"></a>
# exp10
exp10( QDataSet ds ) &rarr; QDataSet

element-wise exponentiate 10**x.

### Parameters:
ds - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=exp10&unscoped_q=exp10">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

exp10( double ds1 ) &rarr; double<br>
exp10( Object ds1 ) &rarr; QDataSet<br>
***
<a name="expandToFillGaps"></a>
# expandToFillGaps
expandToFillGaps( QDataSet ds ) &rarr; QDataSet



### Parameters:
ds - a QDataSet

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=expandToFillGaps&unscoped_q=expandToFillGaps">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

expandToFillGaps( QDataSet ds, double factor ) &rarr; QDataSet<br>
***
<a name="expandWaveform"></a>
# expandWaveform
expandWaveform( QDataSet ds ) &rarr; QDataSet

special function needed by the RPW Group at U. Iowa, which reassigns timetags so the small waveform 
 packets are visible.

### Parameters:
ds - rank 2 waveform

### Returns:
a QDataSet

### See Also:
<a href='Schemes_r.md#rank2Waveform'>Schemes#rank2Waveform()</a> <br>
<a href='Ops_e.md#expandToFillGaps'>expandToFillGaps(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=expandWaveform&unscoped_q=expandWaveform">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="expm1"></a>
# expm1
expm1( QDataSet ds ) &rarr; QDataSet

Returns <i>e</i><sup>x</sup>&nbsp;-1.  Note that for values of
 <i>x</i> near 0, the exact sum of
 <code>expm1(x)</code>&nbsp;+&nbsp;1 is much closer to the true
 result of <i>e</i><sup>x</sup> than <code>exp(x)</code>.

### Parameters:
ds - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=expm1&unscoped_q=expm1">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

expm1( double ds ) &rarr; double<br>
expm1( Object ds ) &rarr; QDataSet<br>
***
<a name="extent"></a>
# extent
extent( QDataSet ds ) &rarr; QDataSet

returns a two element, rank 1 dataset containing the extent of the data.
 Note this accounts for DELTA_PLUS, DELTA_MINUS properties.
 Note this accounts for BIN_PLUS, BIN_MINUS properties.
 The property QDataSet.SCALE_TYPE is set to lin or log.
 The property count is set to the number of valid measurements.
 TODO: this could use MONOTONIC, but it doesn't.  DELTA_PLUS, DELTA_MINUS make that more difficult.

### Parameters:
ds - the dataset to measure the extent

### Returns:
two element, rank 1 "bins" dataset.
### See Also:
<a href='DataSetUtil_r.md#rangeOfMonotonic'>DataSetUtil#rangeOfMonotonic(QDataSet)</a> <br>
<a href='AutoRangeUtil_s.md#simpleRange in Autoplot.'>AutoRangeUtil#simpleRange in Autoplot.</a> in Autoplot.<br>

<a href="https://github.com/autoplot/dev/search?q=extent&unscoped_q=extent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

extent( QDataSet ds, QDataSet range ) &rarr; QDataSet<br>
extent( QDataSet ds, QDataSet wds, QDataSet range ) &rarr; QDataSet<br>
***
<a name="extent445"></a>
# extent445
extent445( QDataSet ds ) &rarr; QDataSet



### Parameters:
ds - a QDataSet

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=extent445&unscoped_q=extent445">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="extentSimple"></a>
# extentSimple
extentSimple( QDataSet ds, QDataSet wds, QDataSet range ) &rarr; QDataSet

like extent, but does not account for DELTA_PLUS, DELTA_MINUS,
 BIN_PLUS, BIN_MINUS, BIN_MIN or BIN_MAX properties.  This was introduced to provide
 a fast way to identify constant datasets and the extent that non-constant 
 datasets vary.

### Parameters:
ds - the dataset to measure the extent rank 1 or rank 2 bins
<br>wds - a weights dataset, containing zero where the data is not valid, positive non-zero otherwise.  If null, then all finite data is treated as valid.
<br>range - if non-null, return the union of this range and the extent.  This must not contain fill!

### Returns:
two element, rank 1 "bins" dataset.
### See Also:
<a href='Ops_e.md#extent'>extent(QDataSet, QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=extentSimple&unscoped_q=extentSimple">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

extentSimple( QDataSet ds, QDataSet range ) &rarr; QDataSet<br>
