# org.das2.qds.DataSetUtilUtilities for QDataSet, such as conversions from various forms
 to QDataSet, and doing a units conversion.  
 
 TODO: DataSetUtil, DataSetOps, and org.virbo.dsops.Ops have become blurred 
 over the years.  These should either be combined or new mission statements 
 need to be created.
DataSetUtil( )


***
<a name="PROPERTY_TYPE_STRING"></a>
# PROPERTY_TYPE_STRING



***
<a name="PROPERTY_TYPE_NUMBER"></a>
# PROPERTY_TYPE_NUMBER



***
<a name="PROPERTY_TYPE_BOOLEAN"></a>
# PROPERTY_TYPE_BOOLEAN



***
<a name="PROPERTY_TYPE_MAP"></a>
# PROPERTY_TYPE_MAP



***
<a name="PROPERTY_TYPE_QDATASET"></a>
# PROPERTY_TYPE_QDATASET



***
<a name="PROPERTY_TYPE_CACHETAG"></a>
# PROPERTY_TYPE_CACHETAG



***
<a name="PROPERTY_TYPE_UNITS"></a>
# PROPERTY_TYPE_UNITS



***
<a name="addContext"></a>
# addContext
addContext( org.das2.qds.MutablePropertyDataSet ds, QDataSet cds ) &rarr; void

adds the rank 0 dataset (a Datum) to the dataset's properties, after all
 the other CONTEXT_&lt;i&gt; properties.

### Parameters:
ds - a MutablePropertyDataSet
<br>cds - a QDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addContext&unscoped_q=addContext">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addContext( java.util.Map props, QDataSet cds ) &rarr; void<br>
***
<a name="addQube"></a>
# addQube
addQube( org.das2.qds.MutablePropertyDataSet ds ) &rarr; void

add QUBE property to dataset, maybe verifying that it is a qube.  This is
 intended to reduce code that builds datasets, not to verify that a dataset
 is a qube.

### Parameters:
ds - the dataset

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addQube&unscoped_q=addQube">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="as2DArrayOfDoubles"></a>
# as2DArrayOfDoubles
as2DArrayOfDoubles( QDataSet d ) &rarr; double

convert the QDataSet to an array.  Units and fill are ignored...

### Parameters:
d - the rank 2 dataset

### Returns:
2-D array of doubles

<a href="https://github.com/autoplot/dev/search?q=as2DArrayOfDoubles&unscoped_q=as2DArrayOfDoubles">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="asArrayOfDoubles"></a>
# asArrayOfDoubles
asArrayOfDoubles( QDataSet d ) &rarr; double

convert the QDataSet to an array.  Units and fill are ignored...

### Parameters:
d - the rank 1 dataset.

### Returns:
an array of doubles

<a href="https://github.com/autoplot/dev/search?q=asArrayOfDoubles&unscoped_q=asArrayOfDoubles">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="asDataSet"></a>
# asDataSet
asDataSet( org.das2.datum.DatumVector dv ) &rarr; QDataSet

return the rank 1 dataset equivalent to the DatumVector

### Parameters:
dv - a DatumVector

### Returns:
rank 1 QDataSet.

<a href="https://github.com/autoplot/dev/search?q=asDataSet&unscoped_q=asDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

asDataSet( DatumRange dr ) &rarr; QDataSet<br>
asDataSet( double d, Units u ) &rarr; DRank0DataSet<br>
asDataSet( double d ) &rarr; DRank0DataSet<br>
asDataSet( Datum d ) &rarr; DRank0DataSet<br>
asDataSet( Object arr ) &rarr; QDataSet<br>
asDataSet( Object x, Object y ) &rarr; QDataSet<br>
asDataSet( Object x, Object y, Object z ) &rarr; QDataSet<br>
***
<a name="asDatum"></a>
# asDatum
asDatum( org.das2.qds.RankZeroDataSet ds ) &rarr; Datum



### Parameters:
ds - a RankZeroDataSet

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=asDatum&unscoped_q=asDatum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

asDatum( QDataSet ds ) &rarr; Datum<br>
***
<a name="asDatumRange"></a>
# asDatumRange
asDatumRange( QDataSet ds, boolean sloppy ) &rarr; DatumRange

return the DatumRange equivalent of this 2-element, rank 1 bins dataset.

### Parameters:
ds - a rank 1, 2-element bins dataset.
<br>sloppy - true indicates we don't check BINS_0 property.

### Returns:
an equivalent DatumRange

<a href="https://github.com/autoplot/dev/search?q=asDatumRange&unscoped_q=asDatumRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

asDatumRange( QDataSet ds ) &rarr; DatumRange<br>
***
<a name="asDatumVector"></a>
# asDatumVector
asDatumVector( QDataSet ds ) &rarr; DatumVector

return DatumVector, which is a 1-d array of Datums.

### Parameters:
ds - a rank 1 QDataSet

### Returns:
a DatumVector

<a href="https://github.com/autoplot/dev/search?q=asDatumVector&unscoped_q=asDatumVector">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bestFormatter"></a>
# bestFormatter
bestFormatter( QDataSet datums ) &rarr; DatumFormatter

return a DatumFormatter that can accurately format all of the datums
 in the dataset.  The goal is to identify a formatter which is also 
 efficient, and doesn't waste an excess of digits.  This sort of code
 is often needed, and is also found in: <ul>
 <li>QStream--where ASCII mode needs efficient representation
 </ul>
 TODO: make one code for this.
 TODO: there also needs to be an optional external context ('2017-03-15') so that 'HH:mm' is a valid response.
 See sftp://jbf@jfaden.net/home/jbf/ct/autoplot/script/development/bestDataSetFormatter.jy

### Parameters:
datums - a rank 1 dataset, or if rank&gt;1, then return the formatter for a slice.

### Returns:
DatumFormatter for the dataset.

<a href="https://github.com/autoplot/dev/search?q=bestFormatter&unscoped_q=bestFormatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="binarySearch"></a>
# binarySearch
binarySearch( QDataSet ds, double key, int low, int high ) &rarr; int

perform a binary search for key within ds, constraining the search to between low and high.

### Parameters:
ds - a rank 1 monotonic dataset.
<br>key - the value to find.
<br>low - an int
<br>high - an int

### Returns:
a positive index of the found value or -index-1 the insertion point.

<a href="https://github.com/autoplot/dev/search?q=binarySearch&unscoped_q=binarySearch">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bundleNames"></a>
# bundleNames
bundleNames( QDataSet ds ) &rarr; String

return the name for each column of the bundle.  This simply
 calls SemanticOps.getComponentNames.

### Parameters:
ds - dataset, presumably with BUNDLE_1 property.

### Returns:
array of names.

<a href="https://github.com/autoplot/dev/search?q=bundleNames&unscoped_q=bundleNames">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bundleWeightsDataSet"></a>
# bundleWeightsDataSet
bundleWeightsDataSet( QDataSet ds ) &rarr; QDataSet

special weightsDataSet for when there is a bundle, and each
 component could have its own FILL_VALID and VALID_MAX.  Each component
 gets its own weights dataset in a JoinDataSet.

### Parameters:
ds - rank 2 bundle dataset

### Returns:
dataset with the same geometry but a weightsDataSet of each bundled dataset.

<a href="https://github.com/autoplot/dev/search?q=bundleWeightsDataSet&unscoped_q=bundleWeightsDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="canonizeFill"></a>
# canonizeFill
canonizeFill( QDataSet ds ) &rarr; WritableDataSet

Iterate through the dataset, changing all points outside of validmin,
 validmax and with zero weight to fill=-1e31.  VALID_MIN and VALID_MAX 
 properties are cleared, and FILL_VALUE is set to -1e31.
 If the dataset is writable, then the dataset is modified.

### Parameters:
ds - rank N QUBE dataset.

### Returns:
ds with same geometry as ds.

<a href="https://github.com/autoplot/dev/search?q=canonizeFill&unscoped_q=canonizeFill">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="checkListOfIndeces"></a>
# checkListOfIndeces
checkListOfIndeces( QDataSet ds, QDataSet indices ) &rarr; void

verify that the indeces really are indeces, and a warning may be printed
 if the indeces don't appear to match the array by
 looking at the MAX_VALUE property of the indeces.

### Parameters:
ds - the dataset.
<br>indices - the indeces which refer to a subset of dataset.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=checkListOfIndeces&unscoped_q=checkListOfIndeces">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="checkQube"></a>
# checkQube
checkQube( QDataSet ds ) &rarr; boolean

check to see if a dataset really is a qube, even if there is a
 rank 2 dep1.  Note this ignores BUNDLE_1 property if there is a DEPEND_1.
 This was motivated by the fftPower routine, which returned a rank 2 DEPEND_1,
 but is typically constant, and RBSP/ECT datasets that often have rank 2 
 DEPEND_1s that are constant.  This
 will putProperty(QDataSet.QUBE,Boolean.TRUE) when the dataset really is
 a qube, or Boolean.FALSE if is clearly not a qube.

### Parameters:
ds - any dataset

### Returns:
true if the dataset really is a qube.

<a href="https://github.com/autoplot/dev/search?q=checkQube&unscoped_q=checkQube">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="closest"></a>
# closest
closest( QDataSet ds, double d, int guess ) &rarr; int

return the index of the closest value in ds to d, using guess as a starting point.  This
 implementation ignores guess, but wise clients will supply it as a parameter.

### Parameters:
ds - a rank 1, monotonic dataset.
<br>d - the value to find.
<br>guess - a guess at a close index, or -1 if no guess should be made.  In this case, a binary search is performed.

### Returns:
index of the closest.

<a href="https://github.com/autoplot/dev/search?q=closest&unscoped_q=closest">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="closestIndex"></a>
# closestIndex
closestIndex( QDataSet ds, Datum datum ) &rarr; int

returns the index of the closest index in the data. 
 This supports rank 1 datasets, and rank 2 bins datasets where the bin is min,max.

### Parameters:
ds - tags dataset
<br>datum - the location to find

### Returns:
the index of the closest point.

<a href="https://github.com/autoplot/dev/search?q=closestIndex&unscoped_q=closestIndex">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

closestIndex( QDataSet table, double x, Units units ) &rarr; int<br>
***
<a name="contextAsString"></a>
# contextAsString
contextAsString( QDataSet ds ) &rarr; String

provide the context as a string, for example to label a plot.  The dataset CONTEXT_i properties are inspected,
 each of which must be one of:<ul>
 <li>rank 0 dataset
 <li>rank 1 bins dataset
 <li>rank 1 bundle
 </ul>
 Here a comma is used as the delimiter.

### Parameters:
ds - the dataset containing context properties which are rank 0 datums or rank 1 datum ranges.

### Returns:
a string describing the context.

<a href="https://github.com/autoplot/dev/search?q=contextAsString&unscoped_q=contextAsString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

contextAsString( QDataSet ds, String delim ) &rarr; String<br>
***
<a name="convertTo"></a>
# convertTo
convertTo( QDataSet ds, Units u ) &rarr; QDataSet

convert the dataset to the given units.

### Parameters:
ds - the dataset
<br>u - new Units

### Returns:
equivalent dataset with the new units.

<a href="https://github.com/autoplot/dev/search?q=convertTo&unscoped_q=convertTo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="copyDimensionProperties"></a>
# copyDimensionProperties
copyDimensionProperties( QDataSet source, org.das2.qds.MutablePropertyDataSet dest ) &rarr; void

Copy over all the dimension properties, including:
       UNITS, FORMAT, SCALE_TYPE,
       TYPICAL_MIN, TYPICAL_MAX,
       VALID_MIN, VALID_MAX, FILL_VALUE,
       NAME, LABEL, TITLE,
       USER_PROPERTIES
 These are dimension properties, as opposed to structural
 see dimensionProperties() for a list of dimension properties.
 TODO: This DOES NOT support join datasets yet.

### Parameters:
source - a QDataSet
<br>dest - a MutablePropertyDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=copyDimensionProperties&unscoped_q=copyDimensionProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="correlativeProperties"></a>
# correlativeProperties
correlativeProperties(  ) &rarr; String

properties that go along with the zeroth index.  These are all QDataSets with dimensions compatible with the datasets.
 If you trim the dataset, then these must be trimmed as well.

### Returns:
the properties that go along with the zeroth index

<a href="https://github.com/autoplot/dev/search?q=correlativeProperties&unscoped_q=correlativeProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="courserCadence"></a>
# courserCadence
courserCadence( org.das2.qds.RankZeroDataSet yTagWidth0, org.das2.qds.RankZeroDataSet yTagWidth1 ) &rarr; RankZeroDataSet

return the courser cadence of the two cadences.  Das2's AverageTableRebinner needs to get the coursest of all the ytags.

### Parameters:
yTagWidth0 - rank 0 dataset that is one cadence (e.g. 84 sec)
<br>yTagWidth1 - rank 0 dataset that is the second cadence (e.g. 70 sec)

### Returns:
the courser of the two cadences.  (e.g. 84 sec)

<a href="https://github.com/autoplot/dev/search?q=courserCadence&unscoped_q=courserCadence">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="dimensionProperties"></a>
# dimensionProperties
dimensionProperties(  ) &rarr; String

return the list of properties that pertain to the dimension that dataset
 values exist.  These are the properties that survive through most operations.
 For example, if you flattened the dataset, what properties 
 would still exist?  If you shuffled the data?  These are not structural
 properties like DEPEND_0, BUNDLE_1, etc.
 Note that BUNDLE_1 will carry dimension properties as well.

### Returns:
a java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=dimensionProperties&unscoped_q=dimensionProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="firstValidPoint"></a>
# firstValidPoint
firstValidPoint( QDataSet ds ) &rarr; QDataSet

returns the first valid point found in a dataset, or null if
 no such point is found.

### Parameters:
ds - non-bundle dataset.

### Returns:
rank zero dataset containing the first valid point, or null.

<a href="https://github.com/autoplot/dev/search?q=firstValidPoint&unscoped_q=firstValidPoint">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="format"></a>
# format
format( QDataSet ds ) &rarr; String

return a human-readable string representing the dataset

### Parameters:
ds - the dataset to represent

### Returns:
a human-readable string

<a href="https://github.com/autoplot/dev/search?q=format&unscoped_q=format">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

format( QDataSet ds, boolean showContext ) &rarr; String<br>
***
<a name="gcd"></a>
# gcd
gcd( QDataSet ds, QDataSet d, QDataSet limit ) &rarr; QDataSet

return the greatest common divisor, which is the unit for which 
 all elements in the dataset are integer multiples of the result.
 This works on continuous data, however, so limit is used to determine 
 the fuzz allowed.  TODO: this needs review and is not for production use.

### Parameters:
ds - any dataset
<br>d - rank 0 dataset, first factor for the dataset, error is used to detect non-zero significance.
<br>limit - rank 0 dataset, the resolution for which data is considered equal, and this
 limit should be greater than numerical precision.

### Returns:
the greatest common divisor.

<a href="https://github.com/autoplot/dev/search?q=gcd&unscoped_q=gcd">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

gcd( QDataSet ds, QDataSet limit ) &rarr; QDataSet<br>
***
<a name="getCadenceWaveform"></a>
# getCadenceWaveform
getCadenceWaveform( QDataSet ds ) &rarr; RankZeroDataSet

return the cadence between measurements of a waveform dataset.  This is
 different than the cadence typically quoted, which is the cadence between
 waveform records.

### Parameters:
ds - a QDataSet

### Returns:
the cadence, possibly null.

<a href="https://github.com/autoplot/dev/search?q=getCadenceWaveform&unscoped_q=getCadenceWaveform">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDimensionProperties"></a>
# getDimensionProperties
getDimensionProperties( QDataSet ds, java.util.Map def ) &rarr; Map

return just the properties attached to the dataset, like 
 UNITS and SCALE_TYPE, and not like DEPEND_x, etc.

### Parameters:
ds - the dataset
<br>def - default values or null.

### Returns:
a map of all the properties.
### See Also:
<a href='#dimensionProperties'>dimensionProperties()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getDimensionProperties&unscoped_q=getDimensionProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNextIndex"></a>
# getNextIndex
getNextIndex( QDataSet ds, Datum datum ) &rarr; int

returns the first column that is after the given datum.  Note the
 if the datum identifies (==) an xtag, then the previous column is
 returned.

### Parameters:
ds - the dataset
<br>datum - a datum in the same units of the dataset.

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=getNextIndex&unscoped_q=getNextIndex">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNextIndexStrict"></a>
# getNextIndexStrict
getNextIndexStrict( QDataSet ds, Datum datum ) &rarr; Integer

Returns the index of the value which is greater than the
 value less of the datum.  Note for rank 2 bins, the first bin which
 has an beginning less than the datum.

### Parameters:
ds - rank 1 monotonic tags, or rank 2 bins.
<br>datum - a datum of the same or convertible units.

### Returns:
the index, or null (None).

<a href="https://github.com/autoplot/dev/search?q=getNextIndexStrict&unscoped_q=getNextIndexStrict">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNextInterval"></a>
# getNextInterval
getNextInterval( QDataSet ds, DatumRange dr0 ) &rarr; DatumRange

return the next interval (typically time) containing data, centered on data, with the
 roughly the same width.

### Parameters:
ds - the dataset
<br>dr0 - the current interval

### Returns:
the next interval

<a href="https://github.com/autoplot/dev/search?q=getNextInterval&unscoped_q=getNextInterval">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPreviousIndex"></a>
# getPreviousIndex
getPreviousIndex( QDataSet ds, Datum datum ) &rarr; int

returns the first index that is before the given datum, or zero
 if no data is found before the datum.
 PARV!
 if the datum identifies (==) an xtag, then the previous column is
 returned.

### Parameters:
ds - the dataset
<br>datum - a datum in the same units of the dataset.

### Returns:
the index

<a href="https://github.com/autoplot/dev/search?q=getPreviousIndex&unscoped_q=getPreviousIndex">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPreviousIndexStrict"></a>
# getPreviousIndexStrict
getPreviousIndexStrict( QDataSet ds, Datum datum ) &rarr; Integer

Returns the index of the value which is less than the
 value less of the datum.  Note for rank 2 bins, the first bin which
 has an end less than the datum.

### Parameters:
ds - rank 1 monotonic tags, or rank 2 bins.
<br>datum - a datum of the same or convertible units.

### Returns:
the index, or null (None).

<a href="https://github.com/autoplot/dev/search?q=getPreviousIndexStrict&unscoped_q=getPreviousIndexStrict">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPreviousInterval"></a>
# getPreviousInterval
getPreviousInterval( QDataSet ds, DatumRange dr0 ) &rarr; DatumRange

return the previous interval (typically time) containing data, centered on data, with the
 roughly the same width.

### Parameters:
ds - the dataset
<br>dr0 - the current interval

### Returns:
the previous interval

<a href="https://github.com/autoplot/dev/search?q=getPreviousInterval&unscoped_q=getPreviousInterval">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getProperties"></a>
# getProperties
getProperties( QDataSet ds, java.lang.String[] names, java.util.Map def ) &rarr; Map

return the properties listed, using the defaults if provided.
 See dimensionProperties(), globalProperties().

### Parameters:
ds - dataset source of the properties.
<br>names - array of names
<br>def - defaults, or null if no defaults are to be used.

### Returns:
map of the properties.

<a href="https://github.com/autoplot/dev/search?q=getProperties&unscoped_q=getProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getProperties( QDataSet ds, java.util.Map def ) &rarr; Map<br>
getProperties( QDataSet ds ) &rarr; Map<br>
***
<a name="getProperty"></a>
# getProperty
getProperty( QDataSet ds, String name, Object deflt ) &rarr; Object



### Parameters:
ds - a QDataSet
<br>name - a String
<br>deflt - an Object

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=getProperty&unscoped_q=getProperty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPropertyClass"></a>
# getPropertyClass
getPropertyClass( String name ) &rarr; Class

return the class for the property, to support Jython.

### Parameters:
name - the property name, e.g. QDataSet.TITLE

### Returns:
String.class
### See Also:
<a href='#getPropertyType'>getPropertyType(java.lang.String)</a> //TODO: super inefficient, this needs to be rewritten as switch<br>

<a href="https://github.com/autoplot/dev/search?q=getPropertyClass&unscoped_q=getPropertyClass">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPropertyType"></a>
# getPropertyType
getPropertyType( String name ) &rarr; String

return the type of the property, as a string to support use in Jython:
 String,Number,Boolean,Map,QDataSet,CacheTag,Units

### Parameters:
name - the property name

### Returns:
the property type or null if the name is not recognized
### See Also:
<a href='#getPropertyClass'>getPropertyClass(java.lang.String)</a> <br>
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/QDataSet.md'>QDataSet</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getPropertyType&unscoped_q=getPropertyType">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getStringValue"></a>
# getStringValue
getStringValue( QDataSet ds, double value, int i ) &rarr; String

return the value, which gets units from index i. from rank 1 bundle dataset.

### Parameters:
ds - the dataset providing units and format information.
<br>value - double value from the dataset
<br>i - the index of the value

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getStringValue&unscoped_q=getStringValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getStringValue( QDataSet yds, double value ) &rarr; String<br>
getStringValue( QDataSet ds ) &rarr; String<br>
***
<a name="getUserProperty"></a>
# getUserProperty
getUserProperty( QDataSet ds, String name ) &rarr; Object

return the "User" property, which allow for extensions of the data model that
 aren't used.  This returns the property "name" under the name USER_PROPERTIES,
 which must either be null or a Map&lt;String,Object&gt;.

### Parameters:
ds - The dataset containing the property.
<br>name - The name of the user property.

### Returns:
an Object


<a href="https://github.com/autoplot/dev/search?q=getUserProperty&unscoped_q=getUserProperty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="globalProperties"></a>
# globalProperties
globalProperties(  ) &rarr; String

properties that describe the dataset itself, rather than those of a dimension
 or structural properties.

### Returns:
the properties that describe the dataset itself

<a href="https://github.com/autoplot/dev/search?q=globalProperties&unscoped_q=globalProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="guessCadence"></a>
# guessCadence
guessCadence( QDataSet xds, QDataSet yds ) &rarr; QDataSet

return the cadence for the given x tags.  The goal will be a rank 0
 dataset that describes the intervals, but this will also return a rank 1
 dataset when multiple cadences are found.  The yds values for each xds value can 
 also be set, specifying where the x values can be ignored because of fill.  When this
 is.
 TODO: this needs review.

### Parameters:
xds - the x tags, which may not contain fill values for non-null result.
<br>yds - the y values, which if non-null is only used for fill values.  This is only used if it is rank 1.

### Returns:
rank 0 or rank 1 dataset.

<a href="https://github.com/autoplot/dev/search?q=guessCadence&unscoped_q=guessCadence">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

guessCadence( QDataSet xds, QDataSet yds, QDataSet zds ) &rarr; QDataSet<br>
***
<a name="guessCadenceNew"></a>
# guessCadenceNew
guessCadenceNew( QDataSet xds, QDataSet yds ) &rarr; RankZeroDataSet

returns a rank 0 dataset indicating the cadence of the dataset.  Using a
 dataset as the result allows the result to indicate SCALE_TYPE and UNITS.
 History:<ul>
    <li>2011-02-21: keep track of repeat values, allowing zero to be considered either mono increasing or mono decreasing
    <li>2011-02-21: deal with interleaved fill values, keeping track of last valid value.
 </ul>

### Parameters:
xds - the x tags, which may not contain fill values for non-null result.
<br>yds - the y values, which if non-null is only used for fill values.  This
   is only used if it is rank 1.

### Returns:
null or the cadence in a rank 0 dataset.  The following may be
    properties of the result:<ul>
    <li>SCALE_TYPE  may be "log"
    <li>UNITS       will be a ratiometric unit when the SCALE_TYPE is log, and
       will be the offset unit for interval units like Units.t2000.
    </ul>

<a href="https://github.com/autoplot/dev/search?q=guessCadenceNew&unscoped_q=guessCadenceNew">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="indexGenDataSet"></a>
# indexGenDataSet
indexGenDataSet( int n ) &rarr; MutablePropertyDataSet

creates a dataset of integers 0,1,2,...,n-1.

### Parameters:
n - the bound

### Returns:
the dataset

<a href="https://github.com/autoplot/dev/search?q=indexGenDataSet&unscoped_q=indexGenDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="inferBins"></a>
# inferBins
inferBins( QDataSet yds ) &rarr; QDataSet

This is the one code to infer bin boundaries when only the 
 centers are available.  This uses centers of adjacent data, and
 extrapolates to get the edge boundaries to create an acceptable limit.
 When the data is log-spaced, the centers are done in the ratiometric
 space.  Small (&lt;1000 element) datasets will be sorted if necessary.

### Parameters:
yds - rank 1 dataset.

### Returns:
rank 2 bins dataset.

<a href="https://github.com/autoplot/dev/search?q=inferBins&unscoped_q=inferBins">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="inferBinsRank2"></a>
# inferBinsRank2
inferBinsRank2( QDataSet ydss ) &rarr; QDataSet

infer the bins for the rank 2 ytags.  This was first used with Juno
 high-rate data, where the ytags follow the FCE implied by the magnetic 
 field detector.

### Parameters:
ydss - rank 2 dataset[n,m]

### Returns:
two-element array of rank 2 datasets[n,m], where 0 is the min and 1 is the max.

<a href="https://github.com/autoplot/dev/search?q=inferBinsRank2&unscoped_q=inferBinsRank2">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isConstant"></a>
# isConstant
isConstant( QDataSet ds ) &rarr; boolean

return true if each record of DEPEND_0 is the same.  Rank 0 datasets
 are trivially constant.
 TODO: ds.slice(i) can be slow because equivalent does so much with the metadata.

### Parameters:
ds - any dataset

### Returns:
true if the dataset doesn't change with DEPEND_0 or is rank 0.

<a href="https://github.com/autoplot/dev/search?q=isConstant&unscoped_q=isConstant">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

isConstant( QDataSet ds, int dim ) &rarr; boolean<br>
***
<a name="isDimensionProperty"></a>
# isDimensionProperty
isDimensionProperty( String name ) &rarr; boolean

return true if the property name is a valid dimension property
 like "UNITS" or "FORMAT".  See dimensionProperties().

### Parameters:
name - property name to test

### Returns:
true if the property is a dimension property.

<a href="https://github.com/autoplot/dev/search?q=isDimensionProperty&unscoped_q=isDimensionProperty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isInheritedProperty"></a>
# isInheritedProperty
isInheritedProperty( String prop ) &rarr; boolean

true if the property is one that is global and is relevant throughout the
 dataset, such as a title or the units.
    property( "TITLE",0,0 ) often returns property("TITLE"), but
    property( "DEPEND_0",0,0 ) should never return property("DEPEND_0").
 This is false, for example, for DEPEND_1.

### Parameters:
prop - the property name.

### Returns:
true if the property is inherited

<a href="https://github.com/autoplot/dev/search?q=isInheritedProperty&unscoped_q=isInheritedProperty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isLogSpacing"></a>
# isLogSpacing
isLogSpacing( QDataSet ds ) &rarr; boolean

return true if the data appears to have log spacing.  The 
 data is assumed to be monotonically increasing or decreasing.

### Parameters:
ds - rank 1 dataset.

### Returns:
true if the data is roughly log spaced.

<a href="https://github.com/autoplot/dev/search?q=isLogSpacing&unscoped_q=isLogSpacing">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isMonotonic"></a>
# isMonotonic
isMonotonic( QDataSet ds ) &rarr; boolean

returns true if the dataset is monotonically increasing.
 If the dataset has the MONOTONIC property set to Boolean.TRUE, believe it.
 The data can contain repeated values. 
 An empty dataset is not monotonic.
 We now use a weights dataset to more thoroughly check for fill.
 The dataset may contain fill data, only the non-fill portions are considered.

### Parameters:
ds - the rank 1 dataset with physical units.

### Returns:
true when the dataset is monotonically increasing.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/QDataSet.md#MONOTONIC'>QDataSet#MONOTONIC</a> <br>
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/ArrayDataSet.md#monotonicSubset'>org.das2.qds.ArrayDataSet#monotonicSubset(org.das2.qds.ArrayDataSet)</a> <br>
<a href='#isMonotonicAndIncreasing'>isMonotonicAndIncreasing(QDataSet)</a> <br>
<a href='Ops.md#ensureMonotonic'>Ops#ensureMonotonic</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isMonotonic&unscoped_q=isMonotonic">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isMonotonicAndIncreasing"></a>
# isMonotonicAndIncreasing
isMonotonicAndIncreasing( QDataSet ds ) &rarr; boolean

returns true if the dataset is monotonically increasing 
 and does not contain repeat values.
 An empty dataset is not monotonic.
 The dataset may contain fill data, only the non-fill portions are considered.

### Parameters:
ds - the rank 1 dataset with physical units.

### Returns:
true when the dataset is monotonically increasing.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/QDataSet.md#MONOTONIC'>QDataSet#MONOTONIC</a> <br>
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/ArrayDataSet.md#monotonicSubset'>org.das2.qds.ArrayDataSet#monotonicSubset(org.das2.qds.ArrayDataSet)</a> <br>
<a href='#isMonotonic'>isMonotonic(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isMonotonicAndIncreasing&unscoped_q=isMonotonicAndIncreasing">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isMonotonicAndIncreasingQuick"></a>
# isMonotonicAndIncreasingQuick
isMonotonicAndIncreasingQuick( QDataSet ds ) &rarr; boolean

quickly determine, with high accuracy, if data is monotonic.  This should
 be a constant-time operation, and be extremely unlikely to fail.

### Parameters:
ds - a QDataSet

### Returns:
true if the data does pass quick tests for monotonic increasing.
### See Also:
<a href='#isMonotonicAndIncreasing'>isMonotonicAndIncreasing(QDataSet)</a> <br>
<a href='QDataSet.md#MONOTONIC'>QDataSet#MONOTONIC</a> <br>
<a href='Ops.md#ensureMonotonicAndIncreasingWithFill'>Ops#ensureMonotonicAndIncreasingWithFill(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isMonotonicAndIncreasingQuick&unscoped_q=isMonotonicAndIncreasingQuick">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isMonotonicQuick"></a>
# isMonotonicQuick
isMonotonicQuick( QDataSet ds ) &rarr; boolean

quickly determine, with high accuracy, if data is monotonic (repeated values
 allowed).  This should
 be a constant-time operation, and be extremely unlikely to fail.

### Parameters:
ds - a QDataSet

### Returns:
true if the data does pass quick tests for monotonic.
### See Also:
<a href='#isMonotonicAndIncreasing'>isMonotonicAndIncreasing(QDataSet)</a> <br>
<a href='QDataSet.md#MONOTONIC'>QDataSet#MONOTONIC</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isMonotonicQuick&unscoped_q=isMonotonicQuick">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isQube"></a>
# isQube
isQube( QDataSet ds ) &rarr; boolean

test to see that the dataset is a qube.  
 TODO: this all needs review.

### Parameters:
ds - QDataSet of any rank.

### Returns:
true if the dataset is a qube.

<a href="https://github.com/autoplot/dev/search?q=isQube&unscoped_q=isQube">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="kmeansCadence"></a>
# kmeansCadence
kmeansCadence( QDataSet xds, int n ) &rarr; QDataSet

use K-means algorithm to find N means in a rank 1 dataset.

### Parameters:
xds - dataset containing data from N normal distributions
<br>n - number of divisions.

### Returns:
dataset containing the index for each point.

<a href="https://github.com/autoplot/dev/search?q=kmeansCadence&unscoped_q=kmeansCadence">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="makeValid"></a>
# makeValid
makeValid( org.das2.qds.MutablePropertyDataSet ds ) &rarr; void

throw out DEPEND and PLANE to make dataset valid.

### Parameters:
ds - a MutablePropertyDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=makeValid&unscoped_q=makeValid">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="maybeCopyRenderType"></a>
# maybeCopyRenderType
maybeCopyRenderType( QDataSet source, org.das2.qds.MutablePropertyDataSet dest ) &rarr; void

copy over the render type, if it is still appropriate.  This nasty bit of code was introduced
 to support LANL data, where high-rank data is preferably plotted as a spectrogram, but can be
 plotted as a stack of lineplots.

### Parameters:
source - a QDataSet
<br>dest - a MutablePropertyDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=maybeCopyRenderType&unscoped_q=maybeCopyRenderType">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="nLargest"></a>
# nLargest
nLargest( QDataSet set, int n ) &rarr; QDataSet

return the value of the nth biggest item.  This keeps n values in memory.

### Parameters:
set - rank 1 dataset containing comparable data.
<br>n - the number of items to find

### Returns:
the n largest elements, sorted.

<a href="https://github.com/autoplot/dev/search?q=nLargest&unscoped_q=nLargest">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="product"></a>
# product
product( int[] qube ) &rarr; int

returns 1 for zero-length qube, the product otherwise.

### Parameters:
qube - int array

### Returns:
the product of the elements of the array

<a href="https://github.com/autoplot/dev/search?q=product&unscoped_q=product">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="propertyNames"></a>
# propertyNames
propertyNames(  ) &rarr; String

Return the names of non-structural properties of the dataset, like the UNITS and CADENCE.
 These are the dimensionProperties, plus others specific to the dataset, such as CADENCE and
 DELTA_PLUS.

### Returns:
the names of non-structural properties of the dataset, like the UNITS and CADENCE.

<a href="https://github.com/autoplot/dev/search?q=propertyNames&unscoped_q=propertyNames">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putProperties"></a>
# putProperties
putProperties( java.util.Map properties, org.das2.qds.MutablePropertyDataSet ds ) &rarr; void

copy all properties into the dataset by iterating through the map.  Properties
 that are equal to null are not copied, since null is equivalent to the
 property not found.

### Parameters:
properties - the properties
<br>ds - the mutable property dataset, which is still mutable.

### Returns:
void (returns nothing)

### See Also:
<a href='#getProperties'>getProperties(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=putProperties&unscoped_q=putProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="qubeDims"></a>
# qubeDims
qubeDims( QDataSet ds ) &rarr; int

provides a convenient way of indexing qubes, returning an int[] of 
 length ds.rank() containing each dimension's length,
 or null if the dataset is not a qube.

### Parameters:
ds - a QDataSet

### Returns:
int[] of length ds.rank() containing each dimension's length, or null if the dataset is not a qube.

<a href="https://github.com/autoplot/dev/search?q=qubeDims&unscoped_q=qubeDims">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rangeOfMonotonic"></a>
# rangeOfMonotonic
rangeOfMonotonic( QDataSet ds ) &rarr; int

returns the indeces of the min and max elements of the monotonic dataset.
 This uses DataSetUtil.isMonotonic() which would be slow if MONOTONIC is
 not set.

### Parameters:
ds - monotonic, rank 1 dataset.

### Returns:
the indeces [min,max] note max is inclusive.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/ops/Ops.md#extent which returns the range containing any data.'>org.das2.qds.ops.Ops#extent which returns the range containing any data.</a> which returns the range containing any data.<br>
<a href='#isMonotonic'>isMonotonic(QDataSet)</a> which must be true<br>

<a href="https://github.com/autoplot/dev/search?q=rangeOfMonotonic&unscoped_q=rangeOfMonotonic">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="repeatingSignal"></a>
# repeatingSignal
repeatingSignal( QDataSet yds ) &rarr; int

return 0 or the number of values after which the signal repeats.  For example,
 <code>
 ds= dataset([1,2,3,4,1,2,3,4,1,2,3,4,1,2,3,4,1,2])
 assert repeatingSignal(ds)==4
 </code>
 if the data contains fill, then it is also not repeating.

### Parameters:
yds - the rank 1 dataset.

### Returns:
the number of samples before a repeat, or 0 if the signal is not repeating.
### See Also:
<a href='#guessCadenceNew'>guessCadenceNew</a> <br>

<a href="https://github.com/autoplot/dev/search?q=repeatingSignal&unscoped_q=repeatingSignal">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="replicateDataSet"></a>
# replicateDataSet
replicateDataSet( int n, double value ) &rarr; MutablePropertyDataSet

creates a dataset with the given cadence, start and length.

### Parameters:
n - the number of elements
<br>value - the value for each element

### Returns:
the dataset

<a href="https://github.com/autoplot/dev/search?q=replicateDataSet&unscoped_q=replicateDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="samePopulation"></a>
# samePopulation
samePopulation( QDataSet ds1, QDataSet ds2 ) &rarr; boolean

true if the two datasets appear to be from the same population.

### Parameters:
ds1 - first dataset
<br>ds2 - second dataset

### Returns:
true if the two datasets appear to be from the same population

<a href="https://github.com/autoplot/dev/search?q=samePopulation&unscoped_q=samePopulation">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="sliceProperties"></a>
# sliceProperties
sliceProperties( QDataSet ds, int index, java.util.Map result ) &rarr; Map

return properties attached to the slice at index.  Note the slice
 implementations use this, and this only returns properties from
 dimensionProperties().
 
 http://autoplot.org//QDataSet#20150514
 
 Note this does not look at BUNDLE_1 properties.  TODO: consider this.

### Parameters:
ds - the dataset to slice.
<br>index - index to slice at.
<br>result - a map to insert the new properties, or null if a new one should be created.

### Returns:
a map of properties attached to the slice at index

<a href="https://github.com/autoplot/dev/search?q=sliceProperties&unscoped_q=sliceProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="statsString"></a>
# statsString
statsString( QDataSet ds ) &rarr; String

return a human readable statistical representation of the dataset.  Currently
 this is the mean, stddev ad number of points.

### Parameters:
ds - the data

### Returns:
return a human readable statistical representation

<a href="https://github.com/autoplot/dev/search?q=statsString&unscoped_q=statsString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="sum"></a>
# sum
sum( int[] qube ) &rarr; int

returns 0 for zero-length qube, the sum otherwise.

### Parameters:
qube - int array

### Returns:
the sum of the elements of the array

<a href="https://github.com/autoplot/dev/search?q=sum&unscoped_q=sum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="tagGenDataSet"></a>
# tagGenDataSet
tagGenDataSet( int n, double start, double cadence ) &rarr; MutablePropertyDataSet

creates a dataset with the given cadence, start and length.
 This is danger code, because the CADENCE must be reset if the UNITS are reset.
 use tagGenDataSet( int n, final double start, final double cadence, Units units ) if
 units are going to be specified.

### Parameters:
n - the number of elements
<br>start - the value for the first element.
<br>cadence - the step size between elements

### Returns:
the dataset

<a href="https://github.com/autoplot/dev/search?q=tagGenDataSet&unscoped_q=tagGenDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

tagGenDataSet( int n, double start, double cadence, Units units ) &rarr; MutablePropertyDataSet<br>
***
<a name="toBundleDs"></a>
# toBundleDs
toBundleDs( QDataSet labels ) &rarr; MutablePropertyDataSet

make a proper bundle ds from a simple bundle containing ordinal units
 This assumes that labels is a unique set of labels.
 See http://autoplot.org/QDataSet#DataSet_Properties under BUNDLE_1.
 See DataSetOps.unbundle

### Parameters:
labels - a QDataSet

### Returns:
a BundleDescriptor to be set as BUNDLE_i.  See BundleDataSet

<a href="https://github.com/autoplot/dev/search?q=toBundleDs&unscoped_q=toBundleDs">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toSparkline"></a>
# toSparkline
toSparkline( QDataSet ds, QDataSet extent, boolean bar ) &rarr; String

Make a unicode spark line http://www.ssec.wisc.edu/~tomw/java/unicode.html.
 This should be for human consumption, because future versions may include data
 reduction and doubling up characters.
 See commented code in MetadataPanel.histStr. (I knew I had done this before...)

### Parameters:
ds - the rank N (typically 1) dataset
<br>extent - None or the range, see Ops.extent(ds)
<br>bar - true indicates bars should be used instead of scatter

### Returns:
string that is a sparkline.

<a href="https://github.com/autoplot/dev/search?q=toSparkline&unscoped_q=toSparkline">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString( QDataSet ds ) &rarr; String

provide a string representation of the dataset.  This is intended for
 human consumption, but does follow rules outlined in 
 http://autoplot.org//developer.datasetToString

### Parameters:
ds - any dataset.

### Returns:
a short, human-readable representation of the dataset.
### See Also:
<a href='#format'>format(QDataSet, boolean)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

toString( int[] qube ) &rarr; String<br>
***
<a name="totalLength"></a>
# totalLength
totalLength( QDataSet ds ) &rarr; int

return the total number of values in the dataset.  For qubes this is the product
 of the dimension lengths, for other datasets we create a dataset of lengths
 and total all the elements.

### Parameters:
ds - a QDataSet

### Returns:
the number of values in the dataset.

<a href="https://github.com/autoplot/dev/search?q=totalLength&unscoped_q=totalLength">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="trimProperties"></a>
# trimProperties
trimProperties( QDataSet ds, int start, int stop ) &rarr; Map

help out implementations of the QDataSet.trim() command.  This does the dimension properties
 and geometric properties like DEPEND_0  and DELTA_PLUS.  This also
 checks for indexed properties, which are NAME__i.

### Parameters:
ds - the dataset with properties to trim.
<br>start - start index of trim operation
<br>stop - exclusive stop index of the trim operation.

### Returns:
the properties of ds, trimmed to the indices.

<a href="https://github.com/autoplot/dev/search?q=trimProperties&unscoped_q=trimProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="validPoints"></a>
# validPoints
validPoints( QDataSet ds ) &rarr; QDataSet

return just the valid points of the dataset.

### Parameters:
ds - a dataset rank &gt; 0.

### Returns:
the valid points of the dataset in a rank 1 dataset.

<a href="https://github.com/autoplot/dev/search?q=validPoints&unscoped_q=validPoints">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="validate"></a>
# validate
validate( QDataSet ds, java.util.List problems ) &rarr; boolean

returns true if the dataset is valid, false otherwise.  If problems is
 non-null, then problems will be indicated here.

### Parameters:
ds - rank N dataset.
<br>problems - insert problem descriptions here, if null then ignore

### Returns:
true if the dataset is valid, false otherwise

<a href="https://github.com/autoplot/dev/search?q=validate&unscoped_q=validate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

validate( QDataSet xds, QDataSet yds, java.util.List problems ) &rarr; boolean<br>
validate( QDataSet xds, QDataSet yds, QDataSet zds, java.util.List problems ) &rarr; boolean<br>
***
<a name="value"></a>
# value
value( org.das2.qds.RankZeroDataSet ds, Units tu ) &rarr; double

get the value of the rank 0 dataset in the specified units.
 For example, value( ds, Units.km )

### Parameters:
ds - a RankZeroDataSet
<br>tu - target units

### Returns:
the double in target units.

<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="weightsDataSet"></a>
# weightsDataSet
weightsDataSet( QDataSet ds ) &rarr; QDataSet

Provide consistent valid logic to operators by providing a QDataSet
 with &gt;0.0 where the data is valid, and 0.0 where the data is invalid.
 VALID_MIN, VALID_MAX and FILL_VALUE properties are used.  
 
 Note, when FILL_VALUE is not specified, -1e31 is used.  This is to
 support legacy logic.
 
 For convenience, the property SUGGEST_FILL is set to the fill value used.

### Parameters:
ds - the dataset

### Returns:
a dataset with the same geometry with zero or positive weights.

<a href="https://github.com/autoplot/dev/search?q=weightsDataSet&unscoped_q=weightsDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="xTagBinarySearch"></a>
# xTagBinarySearch
xTagBinarySearch( QDataSet ds, Datum datum, int low, int high ) &rarr; int

returns the index of a tag, or the  <tt>(-(<i>insertion point</i>) - 1)</tt>.  (See Arrays.binarySearch)

### Parameters:
ds - monotonically increasing data.
<br>datum - value we are looking for
<br>low - inclusive lower bound of the search
<br>high - inclusive upper bound of the search

### Returns:
the index of a tag, or the  <tt>(-(<i>insertion point</i>) - 1)</tt>

<a href="https://github.com/autoplot/dev/search?q=xTagBinarySearch&unscoped_q=xTagBinarySearch">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

