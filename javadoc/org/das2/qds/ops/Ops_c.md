***
<a name="ceil"></a>
# ceil
ceil( QDataSet ds1 ) &rarr; QDataSet

element-wise ceil function.

### Parameters:
ds1 - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=ceil&unscoped_q=ceil">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

ceil( double x ) &rarr; double<br>
ceil( Object x ) &rarr; QDataSet<br>
***
<a name="chirp"></a>
# chirp
chirp( QDataSet t, Datum df0, Datum dt1, Datum df1 ) &rarr; QDataSet

scipy chirp function, used for testing.

### Parameters:
t - Times at which to evaluate the waveform.
<br>df0 - Frequency (e.g. Hz) at time t=0.
<br>dt1 - Time at which `f1` is specified.
<br>df1 - Frequency (e.g. Hz) of the waveform at time `t1`.

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=chirp&unscoped_q=chirp">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="circle"></a>
# circle
circle( QDataSet radius, QDataSet x, QDataSet y ) &rarr; QDataSet

return a dataset with X and Y forming a circle, introduced as a convenient way to indicate planet location.

### Parameters:
radius - rank 0 dataset
<br>x - the x coordinate of the circle
<br>y - the y coordinate of the circle

### Returns:
QDataSet that when plotted is a circle.

<a href="https://github.com/autoplot/dev/search?q=circle&unscoped_q=circle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

circle( double radius, double x, double y ) &rarr; QDataSet<br>
circle( QDataSet radius ) &rarr; QDataSet<br>
circle( double dradius ) &rarr; QDataSet<br>
circle( String sradius ) &rarr; QDataSet<br>
***
<a name="cleanData"></a>
# cleanData
cleanData( QDataSet ds ) &rarr; QDataSet

remove the data which is 3 sigmas from the mean of the data.

### Parameters:
ds - rank 1 dataset.

### Returns:
cleaned dataset of the same geometry.

<a href="https://github.com/autoplot/dev/search?q=cleanData&unscoped_q=cleanData">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

cleanData( QDataSet ds, int size ) &rarr; QDataSet<br>
cleanData( QDataSet ds, double nsigma, int size ) &rarr; QDataSet<br>
***
<a name="clearWritable"></a>
# clearWritable
clearWritable( org.das2.qds.WritableDataSet ds ) &rarr; void

assign zeros to all the values of the dataset.  The 
 dataset must be mutable.  This was used to verify Jython behavior.

### Parameters:
ds - a WritableDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=clearWritable&unscoped_q=clearWritable">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="collapse0"></a>
# collapse0
collapse0( QDataSet fillDs, int st, int en ) &rarr; QDataSet

this is introduced to mimic the in-line function which reduces the dimensionality by averaging over the zeroth dimension.
   collapse0( ds[30,20] ) &rarr; ds[20]

### Parameters:
fillDs - a QDataSet
<br>st - the start index
<br>en - the non-inclusive end index

### Returns:
the averaged dataset

<a href="https://github.com/autoplot/dev/search?q=collapse0&unscoped_q=collapse0">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

collapse0( QDataSet fillDs ) &rarr; QDataSet<br>
***
<a name="collapse0R4"></a>
# collapse0R4
collapse0R4( QDataSet ds, ProgressMonitor mon ) &rarr; QDataSet

Collapse the rank 4 dataset on the zeroth index.

### Parameters:
ds - rank 4 dataset
<br>mon - a ProgressMonitor

### Returns:
rank 3 dataset
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/OperationsProcessor_s.md#sprocess'>org.das2.qds.OperationsProcessor#sprocess(java.lang.String, QDataSet, org.das2.util.monitor.ProgressMonitor)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=collapse0R4&unscoped_q=collapse0R4">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="collapse1"></a>
# collapse1
collapse1( QDataSet ds ) &rarr; QDataSet

this is introduced to mimic the in-line function which reduces the dimensionality by averaging over the first dimension
   collapse1( ds[30,20] ) &rarr; ds[30]

### Parameters:
ds - a QDataSet

### Returns:
the averaged dataset

<a href="https://github.com/autoplot/dev/search?q=collapse1&unscoped_q=collapse1">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="collapse1R4"></a>
# collapse1R4
collapse1R4( QDataSet ds, ProgressMonitor mon ) &rarr; QDataSet

Collapse the rank 4 dataset on the first index.

### Parameters:
ds - rank 4 dataset
<br>mon - a ProgressMonitor

### Returns:
rank 3 dataset
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/OperationsProcessor_s.md#sprocess'>org.das2.qds.OperationsProcessor#sprocess(java.lang.String, QDataSet, org.das2.util.monitor.ProgressMonitor)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=collapse1R4&unscoped_q=collapse1R4">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="collapse2"></a>
# collapse2
collapse2( QDataSet fillDs ) &rarr; QDataSet

this is introduced to mimic the in-line function which reduces the dimensionality by averaging over the first dimension
   collapse2( ds[30,20,10,5] ) &rarr; ds[30,20,5]

### Parameters:
fillDs - a QDataSet

### Returns:
the averaged dataset

<a href="https://github.com/autoplot/dev/search?q=collapse2&unscoped_q=collapse2">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="collapse2R4"></a>
# collapse2R4
collapse2R4( QDataSet ds, ProgressMonitor mon ) &rarr; QDataSet

Collapse the rank 4 dataset on the second index.

### Parameters:
ds - rank 4 dataset
<br>mon - a ProgressMonitor

### Returns:
rank 3 dataset
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/OperationsProcessor_s.md#sprocess'>org.das2.qds.OperationsProcessor#sprocess(java.lang.String, QDataSet, org.das2.util.monitor.ProgressMonitor)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=collapse2R4&unscoped_q=collapse2R4">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="collapse3"></a>
# collapse3
collapse3( QDataSet fillDs ) &rarr; QDataSet

this is introduced to mimic the in-line function which reduces the dimensionality by averaging over the first dimension
   collapse3( ds[30,20,10,5] ) &rarr; ds[30,20,10]

### Parameters:
fillDs - a QDataSet

### Returns:
the averaged dataset

<a href="https://github.com/autoplot/dev/search?q=collapse3&unscoped_q=collapse3">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="collapse3R4"></a>
# collapse3R4
collapse3R4( QDataSet ds, ProgressMonitor mon ) &rarr; QDataSet

Collapse the rank 4 dataset on the third index.

### Parameters:
ds - rank 4 dataset
<br>mon - a ProgressMonitor

### Returns:
rank 3 dataset
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/OperationsProcessor_s.md#sprocess'>org.das2.qds.OperationsProcessor#sprocess(java.lang.String, QDataSet, org.das2.util.monitor.ProgressMonitor)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=collapse3R4&unscoped_q=collapse3R4">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="colorFromString"></a>
# colorFromString
colorFromString( String sval ) &rarr; Color

return the color encoded as one of:<ul>
 <li>"red" or "RED" or X11 color names like "LightPink" 
 <li>#FF0000
 <li>255,0,0 or 1.0,0,0
 </ul>

### Parameters:
sval - the string representation

### Returns:
the color

<a href="https://github.com/autoplot/dev/search?q=colorFromString&unscoped_q=colorFromString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="complexConj"></a>
# complexConj
complexConj( QDataSet ds ) &rarr; QDataSet

return the complex conjugate of the rank 1 or rank 2 QDataSet.

### Parameters:
ds - ds[2] or ds[n,2]

### Returns:
ds[2] or ds[n,2]
### See Also:
<a href='Ops_c.md#complexMultiply'>complexMultiply(QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=complexConj&unscoped_q=complexConj">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="complexDataset"></a>
# complexDataset
complexDataset( QDataSet realPart, QDataSet imaginaryPart ) &rarr; QDataSet

create a complex dataset.

### Parameters:
realPart - the real component.
<br>imaginaryPart - the complex component.

### Returns:
complex dataset
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/examples/Schemes_r.md#rank2ComplexNumbers'>org.das2.qds.examples.Schemes#rank2ComplexNumbers()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=complexDataset&unscoped_q=complexDataset">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="complexMultiply"></a>
# complexMultiply
complexMultiply( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

perform complex multiplication, where the two datasets must have the same
 rank and must both end with a complex dimension.

### Parameters:
ds1 - ds[2] or ds[n,2] or ds[n,m,2]
<br>ds2 - ds[2] or ds[n,2] or ds[n,m,2]

### Returns:
ds[2] or ds[n,2] or ds[n,m,2]
### See Also:
<a href='Ops_c.md#complexConj'>complexConj(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=complexMultiply&unscoped_q=complexMultiply">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="concatenate"></a>
# <del>concatenate</del>
Deprecated: use append instead.
concatenate( Object ds1, Object ds2 ) &rarr; QDataSet<br>
***
<a name="contour"></a>
# contour
contour( QDataSet tds, QDataSet vv ) &rarr; QDataSet

contour the data in rank 2 table tds at rank 0 vv.  The result
 is a rank 2 bundle of [:,'x,y,z'] where i is the contour number.
 The result will have DEPEND_0 be an monotonically increasing sequence with
 jumps indicating new contours.

### Parameters:
tds - rank 2 table
<br>vv - rank 2 bundle

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=contour&unscoped_q=contour">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

contour( Object tds, Object vv ) &rarr; QDataSet<br>
***
<a name="convertPropertyValue"></a>
# convertPropertyValue
convertPropertyValue( QDataSet context, String name, Object value ) &rarr; Object

convert the object into the type needed for the property.

### Parameters:
context - the dataset to which we are assigning the value.
<br>name - the property name
<br>value - the value

### Returns:
the correct value.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/autoplot/jythonsupport/PyQDataSet_c.md#convertPropertyValue'>org.autoplot.jythonsupport.PyQDataSet#convertPropertyValue</a> <br>

<a href="https://github.com/autoplot/dev/search?q=convertPropertyValue&unscoped_q=convertPropertyValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="convertUnitsTo"></a>
# convertUnitsTo
convertUnitsTo( QDataSet ds, Units u ) &rarr; QDataSet

convert the dataset to the target units

### Parameters:
ds - the original dataset.
<br>u - units of the new dataset

### Returns:
a new dataset with all the same properties but with the new units.

<a href="https://github.com/autoplot/dev/search?q=convertUnitsTo&unscoped_q=convertUnitsTo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

convertUnitsTo( DatumRange dr, Units u ) &rarr; DatumRange<br>
convertUnitsTo( Datum d, Units u ) &rarr; Datum<br>
***
<a name="copy"></a>
# copy
copy( QDataSet src ) &rarr; WritableDataSet

copy the dataset to make a new one that is writable.  When a join dataset is copied, a WritableJoinDataSet is used
 to copy each dataset.  This is a deep copy, so for example DEPEND_0 is copied as well.
 Note that BufferDataSets will be copied to BufferDataSets, and ArrayDataSets 
 will be copied to ArrayDataSets.

### Parameters:
src - a QDataSet

### Returns:
a copy of src.

<a href="https://github.com/autoplot/dev/search?q=copy&unscoped_q=copy">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="copyIndexedProperties"></a>
# copyIndexedProperties
copyIndexedProperties( QDataSet srcds, org.das2.qds.MutablePropertyDataSet mds ) &rarr; void

copy over all the indexed properties into the mutable property dataset.
 This was introduced to support DataSetOps.unbundle, but should probably
 always be used.
 See https://sourceforge.net/p/autoplot/bugs/1704/

### Parameters:
srcds - the source dataset
<br>mds - the destination dataset

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=copyIndexedProperties&unscoped_q=copyIndexedProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="copyProperties"></a>
# copyProperties
copyProperties( QDataSet ds ) &rarr; Map

copies the properties, copying depend datasets as well.  
 TODO: This is not thorough, and this needs to be reviewed.

### Parameters:
ds - the data from which the properties are extracted.

### Returns:
a map of the properties.
### See Also:
<a href='DataSetUtil_g.md#getProperties'>DataSetUtil#getProperties(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=copyProperties&unscoped_q=copyProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="copysign"></a>
# copysign
copysign( QDataSet magnitude, QDataSet sign ) &rarr; QDataSet

Returns the first floating-point argument with the sign of the
 second floating-point argument.

### Parameters:
magnitude - a QDataSet
<br>sign - a QDataSet

### Returns:
a QDataSet

### See Also:
<a href='Ops_s.md#signum'>signum</a> <br>
<a href='Ops_n.md#negate'>negate</a> <br>

<a href="https://github.com/autoplot/dev/search?q=copysign&unscoped_q=copysign">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

copysign( double x, double y ) &rarr; double<br>
copysign( Object x, Object y ) &rarr; QDataSet<br>
***
<a name="cos"></a>
# cos
cos( QDataSet ds ) &rarr; QDataSet

element-wise cos.

### Parameters:
ds - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=cos&unscoped_q=cos">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

cos( double ds ) &rarr; double<br>
cos( Object ds ) &rarr; QDataSet<br>
***
<a name="cosh"></a>
# cosh
cosh( QDataSet ds ) &rarr; QDataSet

element-wise cosh.

### Parameters:
ds - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=cosh&unscoped_q=cosh">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

cosh( double ds ) &rarr; double<br>
cosh( Object ds ) &rarr; QDataSet<br>
***
<a name="createEvent"></a>
# createEvent
createEvent( String timeRange, int rgbcolor, String annotation ) &rarr; QDataSet

tool for creating ad-hoc events datasets.

### Parameters:
timeRange - a timerange like "2010-01-01" or "2010-01-01/2010-01-10" or "2010-01-01 through 2010-01-09"
<br>rgbcolor - and RGB color like 0xFF0000 (red), 0x00FF00 (green), or 0x0000FF (blue),
<br>annotation - label for event, possibly including granny codes.

### Returns:
a rank 2 QDataSet with [[ startTime, stopTime, rgbColor, annotation  ]]
### See Also:
<a href='Ops_e.md#eventsComplement'>eventsComplement(QDataSet, int, java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=createEvent&unscoped_q=createEvent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

createEvent( QDataSet append, String timeRange, int rgbcolor, String annotation ) &rarr; QDataSet<br>
createEvent( QDataSet append, DatumRange dr, int rgbcolor, String annotation ) &rarr; QDataSet<br>
***
<a name="createEvents"></a>
# createEvents
createEvents( QDataSet vds ) &rarr; QDataSet

make canonical rank 2 bundle dataset of min,max,color,text
 This was originally part of EventsRenderer, but it became
 clear that this was generally useful.

### Parameters:
vds - dataset in a number of forms that can be converted to an events dataset.

### Returns:
rank 2 QDataSet [ index; 4( time, stopTime, rgbColor, label ) ]

<a href="https://github.com/autoplot/dev/search?q=createEvents&unscoped_q=createEvents">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

createEvents( QDataSet vds, java.awt.Color deftColor ) &rarr; QDataSet<br>
***
<a name="cubicRoot"></a>
# cubicRoot
cubicRoot( QDataSet coefficients ) &rarr; QDataSet

Solves each of a set of cubic equations of the form:
 a*x^3 + b*x^2 + c*x + d = 0.
 Takes a rank 2 dataset with each equation across the first dimension and
 coefficients of each equation across the second.

### Parameters:
coefficients - Set of all coefficients.

### Returns:
Roots of each equation. Double.NaN is returned for complex roots.

<a href="https://github.com/autoplot/dev/search?q=cubicRoot&unscoped_q=cubicRoot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

cubicRoot( double a, double b, double c, double d ) &rarr; double<br>
***
<a name="cumulativeMax"></a>
# cumulativeMax
cumulativeMax( QDataSet ds ) &rarr; QDataSet

for each element i of ds, set the result[i] to the maximum of ds[0:(i+1)]

### Parameters:
ds - rank 1 dataset

### Returns:
the cumulative maximum

<a href="https://github.com/autoplot/dev/search?q=cumulativeMax&unscoped_q=cumulativeMax">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="cumulativeMin"></a>
# cumulativeMin
cumulativeMin( QDataSet ds ) &rarr; QDataSet

for each element i of ds, set the result[i] to the minimum of ds[0:(i+1)]

### Parameters:
ds - rank 1 dataset

### Returns:
the cumulative minimum

<a href="https://github.com/autoplot/dev/search?q=cumulativeMin&unscoped_q=cumulativeMin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

