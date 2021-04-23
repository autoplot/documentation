# org.das2.qds.SemanticOps

Common expressions that apply semantics to QDataSet.  Introduced
 to reduce a lot of repeated code, but also to make it clear where semantics
 are being applied.

***
<a name="bounds"></a>
# bounds
bounds( QDataSet ds ) &rarr; QDataSet

return the bounds DS[ JOIN_0=x,y; BINS_1=min,maxInclusive ] of the datasets
 independent parameters.  This is only implemented for:
 <table summary="">
   <tr><td>rank 2 Tables</td><td>extent(X),extent(Y) and Z is not represented</td></tr>
   <tr><td>rank 3 array of tables</td><td>extent(X),extent(Y) and Z is not represented</td></tr>
   <tr><td>rank 1 Y(X)</td><td>extent(X),extent(Y)</td></tr>
   <tr><td>not for rank 2 bundle dataset</td></tr>
   <tr><td>not for rank 1 bundle dataset</td></tr>
 </table>
 The zeroth dimension will be the physical dimension of the DEPEND_0 values.  Or said another way:
 <table summary="">
   <tr><td>bounds[0,0]= X min</td><td>bounds[0,1] = X max</td><td>bounds.slice(0) is the extent of X<td></tr>
   <tr><td>bounds[1,0]= Y min</td><td>bounds[1,1] = Y max</td><td>bounds.slice(1) is the extent of Y<td></tr>
 </table>

### Parameters:
ds - rank 2 dataset with BINS_1="min,maxInclusive"

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=bounds&unscoped_q=bounds">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="cadenceCheck"></a>
# cadenceCheck
cadenceCheck( QDataSet tds, QDataSet ds ) &rarr; QDataSet

return a dataset with 1's where the cadence following this measurement is acceptable, and 0's where
 there should be a break in the data.  For example, here's some pseudocode:
<blockquote><pre>
   findex= Ops.interpolate( xds, x )
   cadenceCheck= cadenceCheck(xds)
   r= where( cadenceCheck[floor(findex)] eq 0 )
   x[r]= fill
</pre></blockquote>
 Presently this just uses guessXTagWidth to get the cadence, but this may allow a future version to support
 mode changes.

 The result is a dataset with the same length, and the last element is always 1.

### Parameters:
tds - rank 1 dataset of length N.
<br>ds - dataset dependent on tds and used to detect valid measurements, or null.

### Returns:
dataset with length N
### See Also:
<a href='Ops.md#valid which checks for fill and valid_min, valid_max.'>Ops#valid which checks for fill and valid_min, valid_max.</a> which checks for fill and valid_min, valid_max.<br>

<a href="https://github.com/autoplot/dev/search?q=cadenceCheck&unscoped_q=cadenceCheck">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="checkPropertyType"></a>
# checkPropertyType
checkPropertyType( String prop, Object value, boolean throwException ) &rarr; boolean

verify property types.  For example, that UNITS is a org.das2.datum.Units, etc.
 Returns true for unrecognized property names (future expansion) and null.  If 
 throwException is true, then an IllegalArgumentException is thrown.

### Parameters:
prop - the property name, e.g. QDataSet.CADENCE
<br>value - the candidate value for the property.
<br>throwException - if true, throw descriptive exception instead of returning false.

### Returns:
true if the property type is okay.

<a href="https://github.com/autoplot/dev/search?q=checkPropertyType&unscoped_q=checkPropertyType">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="doubleValue"></a>
# doubleValue
doubleValue( Number value ) &rarr; Double

returns the Double value of the number, preserving null and NaN.

### Parameters:
value - a Number

### Returns:
a Double


<a href="https://github.com/autoplot/dev/search?q=doubleValue&unscoped_q=doubleValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getComponentLabels"></a>
# getComponentLabels
getComponentLabels( QDataSet ds ) &rarr; String

return the labels for a dataset using BUNDLE_1 and DEPEND_1.  If BUNDLE_1 is defined and contains a LABEL,
 then it is used, otherwise a string value of the data is used, supporting legacy bundles, and if no DEPEND_1 is found
 then use the NAME properties from the bundle, or "ch_<em>i</em>" for each channel.

### Parameters:
ds - the dataset, with a BUNDLE_1 or DEPEND_1 dimension which could be used.

### Returns:
labels for each bundled dataset.

<a href="https://github.com/autoplot/dev/search?q=getComponentLabels&unscoped_q=getComponentLabels">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getComponentNames"></a>
# getComponentNames
getComponentNames( QDataSet ds ) &rarr; String

return the labels for a bundle dataset.  For a rank 2 bundle, this
 will be found in BUNDLE_1, or legacy ones may have nominal data for DEPEND_1.
 For a rank 1 bundle this will be BUNDLE_0.

### Parameters:
ds - rank 1 or rank 2 bundle.

### Returns:
the column names.

<a href="https://github.com/autoplot/dev/search?q=getComponentNames&unscoped_q=getComponentNames">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDatum"></a>
# getDatum
getDatum( QDataSet ds, double d ) &rarr; Datum

returns the value as a datum.  Note this should be used with reservation,
 this is not very efficient when the operation is done many times.

### Parameters:
ds - dataset providing the UNITS and VALID_MIN, VALID_MAX and FILL_VALUE.
<br>d - the double.

### Returns:
a datum representing the value.

<a href="https://github.com/autoplot/dev/search?q=getDatum&unscoped_q=getDatum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDependentDataSet"></a>
# getDependentDataSet
getDependentDataSet( QDataSet ds ) &rarr; QDataSet

return the dataset that is dependent on others.  For a bundle, we
 use DataSetOps.unbundleDefaultDataSet

### Parameters:
ds - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=getDependentDataSet&unscoped_q=getDependentDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLooseUnitsConverter"></a>
# getLooseUnitsConverter
getLooseUnitsConverter( QDataSet src, QDataSet dst ) &rarr; UnitsConverter

returns the UnitsConverter, or IDENTITY if the converter cannot be found
 and one of the two units is dimensionless.

### Parameters:
src - the dataset from which we get the original units.
<br>dst - the dataset from which we get the destination units.

### Returns:
the UnitsConverter

<a href="https://github.com/autoplot/dev/search?q=getLooseUnitsConverter&unscoped_q=getLooseUnitsConverter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlanarView"></a>
# getPlanarView
getPlanarView( QDataSet ds, String name ) &rarr; QDataSet

returns the plane requested by name, or null if it does not exist.
 If the name is PLANE_i, then return PLANE_i, otherwise return
 the dataset with this name.
 Note QDataSet has the rule that if PLANE_i is null, then all PLANE_(i+1)
 must also be null.

### Parameters:
ds - a QDataSet
<br>name - a String

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=getPlanarView&unscoped_q=getPlanarView">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPropertyType"></a>
# getPropertyType
getPropertyType( String prop ) &rarr; String

return the property type expected for the property.

### Parameters:
prop - a String

### Returns:
QDataSet, String, Number, Units, or CacheTag

<a href="https://github.com/autoplot/dev/search?q=getPropertyType&unscoped_q=getPropertyType">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSimpleTableContaining"></a>
# getSimpleTableContaining
getSimpleTableContaining( QDataSet tds, Datum x, Datum y ) &rarr; QDataSet

return the first table of the bundle containing x and y

### Parameters:
tds - a QDataSet
<br>x - a Datum
<br>y - a Datum

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=getSimpleTableContaining&unscoped_q=getSimpleTableContaining">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getUnits"></a>
# getUnits
getUnits( QDataSet ds ) &rarr; Units

returns the units found in the UNITS property of the dataset,
 or Units.dimensionless if it is not found.

### Parameters:
ds - a QDataSet

### Returns:
the units found in the dataset, or Units.dimensionless.

<a href="https://github.com/autoplot/dev/search?q=getUnits&unscoped_q=getUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getUnitsConverter"></a>
# getUnitsConverter
getUnitsConverter( QDataSet src, QDataSet dst ) &rarr; UnitsConverter

return the UnitsConverter that will convert data from src to the units of dst.

### Parameters:
src - the dataset from which we get the original units.
<br>dst - the dataset from which we get the destination units.

### Returns:
the UnitsConverter

<a href="https://github.com/autoplot/dev/search?q=getUnitsConverter&unscoped_q=getUnitsConverter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="guessXTagWidth"></a>
# guessXTagWidth
guessXTagWidth( QDataSet ds, QDataSet yds ) &rarr; Datum

return a reasonable tag width to use, or null if one cannot be
 guessed.

### Parameters:
ds - the dataset containing data with a cadence.
<br>yds - null or a dataset that may contain fill.

### Returns:
a Datum


<a href="https://github.com/autoplot/dev/search?q=guessXTagWidth&unscoped_q=guessXTagWidth">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isBins"></a>
# isBins
isBins( QDataSet ds ) &rarr; boolean

Test for bins scheme, where BINS_1 (or BINS_0) is set.  
 This is where a two-element index is min, max.
 Note the BINS dimension must be the last index of the QDataSet.

### Parameters:
ds - a QDataSet

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isBins&unscoped_q=isBins">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isBundle"></a>
# isBundle
isBundle( QDataSet ds ) &rarr; boolean

Test for bundle scheme.  Returns true if the BUNDLE_1 is set.

### Parameters:
ds - a QDataSet

### Returns:
true if the dataset is a bundle

<a href="https://github.com/autoplot/dev/search?q=isBundle&unscoped_q=isBundle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isJoin"></a>
# isJoin
isJoin( QDataSet ds ) &rarr; boolean

returns true if the dataset is rank 2 or greater with the first dimension a join dimension.
 Note this does not return true for implicit joins, where JOIN_0 is not set.

### Parameters:
ds - a QDataSet

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isJoin&unscoped_q=isJoin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isLegacyBundle"></a>
# isLegacyBundle
isLegacyBundle( QDataSet zds ) &rarr; boolean

See Ops.isLegacyBundle

### Parameters:
zds - a QDataSet

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isLegacyBundle&unscoped_q=isLegacyBundle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isMonotonic"></a>
# isMonotonic
isMonotonic( QDataSet ds ) &rarr; boolean

returns true if the dataset indicates that it is monotonically
 increasing.  See DataSetUtil.isMonotonic.

### Parameters:
ds - a QDataSet

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isMonotonic&unscoped_q=isMonotonic">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isRank1Bundle"></a>
# isRank1Bundle
isRank1Bundle( QDataSet ds ) &rarr; boolean



### Parameters:
ds - a QDataSet

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isRank1Bundle&unscoped_q=isRank1Bundle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isRank2Waveform"></a>
# isRank2Waveform
isRank2Waveform( QDataSet fillDs ) &rarr; boolean

Test for rank 2 waveform dataset, where DEPEND_1 is offset from DEPEND_0, 
 and the data is the waveform.  Other rules include:<ul>
 <li> DEPEND_1 must be at least 128 elements long.
 <li> DEPEND_1 must not be dimensionless.
 <li> if DEPEND_1 is in the same units as DEPEND_0, then DEPEND_0 can be ignored.

### Parameters:
fillDs - a QDataSet

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isRank2Waveform&unscoped_q=isRank2Waveform">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isRank3JoinOfRank2Waveform"></a>
# isRank3JoinOfRank2Waveform
isRank3JoinOfRank2Waveform( QDataSet ds ) &rarr; boolean

Test for rank 3 dataset that is a join of rank 2 waveform datasets.

### Parameters:
ds - a QDataSet

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isRank3JoinOfRank2Waveform&unscoped_q=isRank3JoinOfRank2Waveform">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isSimpleBundleDataSet"></a>
# isSimpleBundleDataSet
isSimpleBundleDataSet( QDataSet ds ) &rarr; boolean

returns true if the dataset is a bundle of rank 1 datasets.  If no
 dependence is declared, it is assumed that the first one or two datasets
 are the independent datasets, and the last is the dependent. 
<blockquote><pre>
    X,Y   -->  Y(X)
    X,Y,Z -->  Z(X,Y)
</pre></blockquote>

### Parameters:
ds - a QDataSet

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isSimpleBundleDataSet&unscoped_q=isSimpleBundleDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isSimpleTableDataSet"></a>
# isSimpleTableDataSet
isSimpleTableDataSet( QDataSet ds ) &rarr; boolean

returns true if the dataset is the scheme of a legacy TableDataSet
 with only one table.  Note "Tables" have just one X unit and one Y unit,
 no bundles.
 Consider: rule about "duck typing": rules like !Ops.isBundle break this
  because it requires to be a simpleTable, you cannot be a bundle.  LANL
  rich ASCII allows datasets to be both bundles and simple tables.

### Parameters:
ds - a QDataSet

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isSimpleTableDataSet&unscoped_q=isSimpleTableDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isTableDataSet"></a>
# isTableDataSet
isTableDataSet( QDataSet ds ) &rarr; boolean

returns true if the dataset is the scheme of a legacy TableDataSet

### Parameters:
ds - a QDataSet

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isTableDataSet&unscoped_q=isTableDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isTimeSeries"></a>
# isTimeSeries
isTimeSeries( QDataSet ds ) &rarr; boolean

returns true if the dataset is a time series.  This is either something that has DEPEND_0 as a dataset with time
 location units, or a join of other datasets that are time series.

### Parameters:
ds - a QDataSet

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isTimeSeries&unscoped_q=isTimeSeries">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="lookupTimeLengthUnit"></a>
# <del>lookupTimeLengthUnit</del>
Deprecated: use Units.lookupTimeLengthUnit
***
<a name="lookupTimeUnits"></a>
# <del>lookupTimeUnits</del>
Deprecated: use Units.lookupTimeUnits
lookupTimeUnits( Datum base, Units offsetUnits ) &rarr; Units<br>
***
<a name="lookupUnits"></a>
# <del>lookupUnits</del>
Deprecated: use Units.lookupUnits
***
<a name="trim"></a>
# trim
trim( QDataSet ds, DatumRange xrange, DatumRange yrange ) &rarr; QDataSet

return the parts of the dataset within the bounds.  This assumes how
 the data is visualized, so for example see SemanticOps.xtagsDataSet 
 for which dimensions correspond to x and y.

### Parameters:
ds - the rank 1 or more dataset, including joins.
<br>xrange - the range or null if no trimming should be done
<br>yrange - the range or null if no trimming should be done

### Returns:
the trimmed dataset.

<a href="https://github.com/autoplot/dev/search?q=trim&unscoped_q=trim">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="weightsDataSet"></a>
# weightsDataSet
weightsDataSet( QDataSet ds ) &rarr; QDataSet

return the weights dataset, possibly creating one based on VALID_MIN
 VALID_MAX and FILL_VALUE properties.  The weights dataset will have
 value zero where the data is invalid, and a non-zero weight where it is
 valid.  DataSets may also contain a weights table with relative weights,
 but this is not uniformly supported.  
 Note: this uses QDataSet.WEIGHTS_PLANE
 Note: calls org.das2.qds.DataSetUtil.weightsDataSet.

### Parameters:
ds - a QDataSet

### Returns:
QDataSet with same geometry containing zeros and non-zeros.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/ops/Ops.md#valid which is equivalent'>org.das2.qds.ops.Ops#valid which is equivalent</a> which is equivalent<br>
<a href='#cadenceCheck which detects for gaps in cadence.'>cadenceCheck which detects for gaps in cadence.</a> which detects for gaps in cadence.<br>

<a href="https://github.com/autoplot/dev/search?q=weightsDataSet&unscoped_q=weightsDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="xtagsDataSet"></a>
# xtagsDataSet
xtagsDataSet( QDataSet ds ) &rarr; QDataSet

return the dataset containing the x tags for the dataset.  This
 is QDataSet.DEPEND_0, or if that's null then IndexGenDataSet(ds.length).
 For a bundle, this is just the 0th dataset.  
 For a join, this is a join of the xtags datasets of each dataset.

### Parameters:
ds - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=xtagsDataSet&unscoped_q=xtagsDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="ytagsDataSet"></a>
# ytagsDataSet
ytagsDataSet( QDataSet ds ) &rarr; QDataSet

return the ytags for the simple table that is ds.<ul>
   <li>rank 2 spectrogram: Z[X,Y] &rarr; Y
   <li>bundle_1: ds[ :, [x,y,z] ] &rarr; y
   <li>[x,y,z] &rarr; y
 </ul>
 TODO: consider that these break duck typing goal, and really need a scheme
   to tell it how to get the dataset.

### Parameters:
ds - the dataset

### Returns:
the ytags

<a href="https://github.com/autoplot/dev/search?q=ytagsDataSet&unscoped_q=ytagsDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

