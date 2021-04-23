# org.das2.qds.QDataSet

<p>QDataSets are less abstract and more flexible data model for das2.  das2's 
 old data model was developed to deliver spectrogram time series data sets
 where the dataset structure would change over time, and the interface is highly
 optimized for that environment.  It's difficult to express many datasets in these
 terms, so the simpler "quick" QDataSet was introduced.  </p>

 <p>The QDataSet can be thought of as a fast java array that has name-value metadata
 attached to it.  These arrays of data can have arbitrary rank, although currently
 the interface limits rank to 0,1,2,3, and 4.  (Rank N is proposed but not
 developed.)  Each dimension's length can vary, like Java arrays, and datasets 
 where the dimensions do not vary in length are colloquially called "Qubes."</p>

 <p>QDataSets can have other QDataSets as property values, for example the property
 QDataSet.DEPEND_0 indicates that the values are dependent parameters of the "tags"
 QDataSet found there.  This how how we get to the same abstraction level of 
 the legacy Das2 dataset.  </p>
 
 <p>This is inspired by the CDF data model and PaPCo's dataset model.</p>

***
<a name="DEPEND_0"></a>
# DEPEND_0

type QDataSet, this dataset is a dependent parameter of the independent parameter represented in this DataSet.
 The tags for the DataSet's 0th index are identified by this tags dataset.

***
<a name="DEPEND_1"></a>
# DEPEND_1

type QDataSet, this dataset is a dependent parameter of the independent parameter represented in this DataSet.
 The tags for the DataSet's 1st index are identified by this tags dataset.  When DEPEND_1 is rank 2,
 then its first dimension goes with DEPEND_0 and its second are the tags for the second dimension.

***
<a name="DEPEND_2"></a>
# DEPEND_2

type QDataSet, this dataset is a dependent parameter of the independent parameter represented in this DataSet.
 The tags for the DataSet's 2nd index are identified by this tags dataset.  When DEPEND_2 is rank 2,
 then it's first dimension goes with DEPEND_0 and it's second are the tags for the second dimension.

***
<a name="DEPEND_3"></a>
# DEPEND_3

type QDataSet, this dataset is a dependent parameter of the independent parameter represented in this DataSet.
 The tags for the DataSet's 3nd index are identified by this tags dataset.  When DEPEND_3 is rank 2,
 then it's first dimension goes with DEPEND_0 and it's second are the tags for the second dimension.

***
<a name="BUNDLE_1"></a>
# BUNDLE_1

type QDataSet describing each of the bundled datasets (Bundle Descriptor).  This dataset describes 
 how the columns should be split up
 into separate parameters.  This rank 2 dataset has a length that is equal to the number
 of bundled datasets.  The values(i,*) are the qube dimensions of the dataset,
 except for the first dimension.  When all the bundled datasets are rank 1, then
 length(*) will be equal to zero.  property(*,UNITS) will yield the unit for each
 dataset.  Bundle dimensions generally add one physical dimension for each
 bundled dataset.  property(*,DEPEND_0) is special, because it will return a string
 rather than a QDataSet.  This string should refer to one of the bundled datasets by
 its NAME property.  (Any property that returns a QDataSet should return a
 string referring to another dataset in the bundle.)  Also the dataset is necessarily
 a QUBE.

***
<a name="BUNDLE_0"></a>
# BUNDLE_0

type QDataSet describing each position of the rank 1 dataset (Bundle Descriptor).  This dataset describes how the columns should be split up
 into separate parameters.  See BUNDLE_1.  Note slicing a dataset on the zeroth
 dimension will move BUNDLE_1 to BUNDLE_0.  
 Properties defined in this dataset will be overwritten by the BUNDLE dataset's properties.
 For example, if the dataset has property( UNITS, 0 ) defined as "Hz" but the
 bundle has property( UNITS,0 ) as "Hertz" then "Hertz" is used.

***
<a name="BUNDLE_2"></a>
# BUNDLE_2

type QDataSet Bundle Descriptor.  When multiple BUNDLES are present, they must be simple bundles, bundling just
 rank 1 datasets.

***
<a name="BUNDLE_3"></a>
# BUNDLE_3

type QDataSet Bundle Descriptor.  When multiple BUNDLES are present, they must be simple bundles, bundling just
 rank 1 datasets.

***
<a name="START_INDEX"></a>
# START_INDEX

type Integer, only found in a bundle descriptor (BUNDLE_0 or BUNDLE_1), this returns the integer
 index of the start of the current dataset.  If this is null, then the index used to access
 the value may be used.  (E.g. a bundle of Rank 1 datasets.)

***
<a name="BINS_1"></a>
# BINS_1

type String which is a comma-delimited list of keywords that describe the boundary
 type for each column.  For example, "min,max" "min,maxInclusive" or "c95min,mean,c95max".
 A bins dimension doesn't add a physical dimension.  Autoplot uses just "min,max" and "min,maxInclusive"

***
<a name="BINS_0"></a>
# BINS_0

type String which is a comma-delimited list of keywords that describe the boundary
 type for each column.  This comma-delimited list of keywords that describe the boundary
 type for each column.  For example, "min,max" "min,maxInclusive" or "c95min,mean,c95max".
 A bins dimension doesn't add a physical dimension.   Autoplot uses just "min,max" and "min,maxInclusive"

***
<a name="JOIN_0"></a>
# JOIN_0

type String, non-null string identifies that elements in this dimension are
 instances of data with the same dimensions.  ds[2,20] where JOIN_0="DEPEND_1" should
 be equivalent to ds[40].  It's not clear if the text should indicate anything, but
 for now let's just indicate the next dimension.

***
<a name="PLANE_0"></a>
# PLANE_0

type QDataSet, a correlated plane of data.  An additional dependent DataSet that is correlated by the first index.  
 Note "0" is just a count, and does not refer to the 0th index.  All correlated datasets must be 
 correlated by the first index.  TODO: what about two rank 2 datasets?  
 Note that if PLANE_i==null then PLANE_(i+1) must also be null.

***
<a name="CONTEXT_0"></a>
# CONTEXT_0

type QDataSet, that stores the position of a slice or range in
 a collapsed dimension.  In "Flux(Energy) @ Time=2009-03-16T11:19 UT", the Time=... comes from
 a context property.  Note "0" is just a count, and does not refer to the 0th index.
 A dataset can have any number of contexts:
 Temperature @ ( Time, Long, Lat ): 37 deg F @ ( 2009-03-16T11:19 UT, 91.5331 deg West, 41.6579 deg North )
 Typically this will be a rank 0 dataset, but may also be a rank 1 dataset with a bins dimension.

***
<a name="CONTEXT_1"></a>
# CONTEXT_1

type QDataSet, that stores the position of a slice or range in
 a collapsed dimension.  In "Flux(Energy) @ Time=2009-03-16T11:19 UT", the Time=... comes from
 a context property.  Note "1" is just a count, and does not refer to the 1th index.
 A dataset can have any number of contexts:
 Temperature @ ( Time, Long, Lat ): 37 deg F @ ( 2009-03-16T11:19 UT, 91.5331 deg West, 41.6579 deg North )
 Typically this will be a rank 0 dataset, but may also be a rank 1 dataset with a bins dimension.

***
<a name="MAX_PLANE_COUNT"></a>
# MAX_PLANE_COUNT

the maximum number of allowed planes.  This should be used to enumerate all the planes.

***
<a name="MAX_UNIT_BUNDLE_COUNT"></a>
# MAX_UNIT_BUNDLE_COUNT

maximum number of same-unit bundled dimensions (e.g. B_GSM[time,Bundle]).  This was introduced when cdf dataset
 fa_k0_tms_20040224_v01.cdf?O+_en had 48 energy channels, was marked as time_series but wouldn't render because
 view code limited to 12.

 Seth's file vap+cdf:file:///home/jbf/ct/hudson/data.backup/cdf/lanl/rbspa_pre_ect-mageisHIGH-sp-L1_20130213_v1.0.0.cdf?Count_Rate_elec
 RBSP/Hope has 72 channels.

***
<a name="MAX_RANK"></a>
# MAX_RANK

the highest rank supported by the library.   Arbitrary high rank datasets are supported through
 RankNDataSet, but must be sliced to be accessed.

***
<a name="MAX_HIGH_RANK"></a>
# MAX_HIGH_RANK

the highest rank supported by the library, without direct access 
 to datums.  Some codes may choose to use this when supporting high rank
 data is trivial.

***
<a name="UNITS"></a>
# UNITS

type Units indicating the units of the dataset in the enumeration of
 org.das2.datum.Units, as in org.das2.datum.Units.km.  New unit types
 can be introduced with Units.lookup.  For example,
 <blockquote><pre>
from org.das2.datum import Units
u= Units.lookupUnits('seconds since 2015-001T00:00')
ds= findgen(3600)
ds= putProperty( ds, QDataSet.UNITS, u )
plot( ds )  # plots line from 00:00 to 01:00.
</pre></blockquote>

***
<a name="FORMAT"></a>
# FORMAT

type String, Java/C format string for formatting the values.  This
 should imply precision, and codes that serialize data can use this
 to correctly format the data.  Examples include:<ul>
 <li>%d integers</li>
 <li>%5.1f floats with one decimal place</li>
 <li>%.3e exponential notation</li>
 <li>%x hex of the integer</li>
 </ul>

***
<a name="FILL_VALUE"></a>
# FILL_VALUE

type Number, value to be considered fill (invalid) data.  Note because
 all data is accessed as doubles, noise may be inadvertently affect numbers.

***
<a name="VALID_MIN"></a>
# VALID_MIN

type Number, minimum bounding measurements to be considered valid.  Lower
 and Upper bounds are inclusive.  FILL_VALUE should be used to make the 
 lower bound or upper bound exclusive.  Note DatumRange contains logic is
 exclusive on the upper bound.

***
<a name="VALID_MAX"></a>
# VALID_MAX

type Number, maximum bounding measurements to be considered valid.  Lower
 and Upper bounds are inclusive.  FILL_VALUE should be used to make the 
 lower bound or upper bound exclusive.  Note DatumRange contains logic is
 exclusive on the upper bound.

***
<a name="TYPICAL_MIN"></a>
# TYPICAL_MIN

type Number that is min used to discover datasets.  This should be a reasonable representation
 of the expected dynamic range of the dataset.

***
<a name="TYPICAL_MAX"></a>
# TYPICAL_MAX

type Number that is the max used to discover datasets.  This should be a reasonable representation
 of the expected dynamic range of the dataset.

***
<a name="SCALE_TYPE"></a>
# SCALE_TYPE

String, "linear" or "log", hinting at the preference for linear or a log
 axis.

***
<a name="LABEL"></a>
# LABEL

String, Concise Human-consumable label suitable for a plot label (~10 chars).

***
<a name="TITLE"></a>
# TITLE

String, Human-consumable string suitable for a plot title (~100 chars).

***
<a name="DESCRIPTION"></a>
# DESCRIPTION

String, Human-consumable string suitable for describing the data more fully.  
 This should be html text, or just a link to other documentation (one URL, 
 or two sentences to one page of text).

***
<a name="WEIGHTS"></a>
# WEIGHTS

QDataSet, dataset of same geometry that indicates the weights for each point.  Often weights are computed
 in processing, and this is where they should be stored for other routines.  When the weights plane is 
 present, routines can safely ignore the FILL_VALUE, VALID_MIN, and VALID_MAX properties, and use non-zero weight to 
 indicate valid data.  Further, averages of averages will compute accurately.

***
<a name="MONOTONIC"></a>
# MONOTONIC

Boolean, Boolean.TRUE if dataset is monotonically increasing, and the data is rank 1.
 Data may only contain invalid values at the beginning or end, and may contain repeated 
 values.  Generally this will be used with tags datasets.

***
<a name="CADENCE"></a>
# CADENCE

QDataSet of rank0, which is the expected distance between successive 
 measurements where it is valid to make inferences about the data.
 For example, interpolation is disallowed for points 1.5*CADENCE apart.  
 This property only makes sense with a tags dataset.  Note this may be
 a "ratiometric" datum, like 110 percentIncrease, for logarithmically 
 spaced data.  Cadence must be positive.

***
<a name="DELTA_PLUS"></a>
# DELTA_PLUS

QDataSet of rank 0, or correlated QDataSet that limits accuracy.  This should
 be interpreted as the one standard deviation confidence level, and must
 be positive.

***
<a name="DELTA_MINUS"></a>
# DELTA_MINUS

QDataSet of rank 0, or correlated QDataSet that limits accuracy.  This should
 be interpreted as the one standard deviation confidence level, and must
 be positive.

***
<a name="BIN_PLUS"></a>
# BIN_PLUS

QDataSet of rank 0 or correlated QDataSet identifies boundary. This is added to the
 measurements and should be interpreted as the upper limit of 100% confidence 
 interval where a measurement was collected.   
 Note if both DELTA_PLUS and BIN_PLUS are found,
 then BIN_PLUS must be greater than DELTA_PLUS.

***
<a name="BIN_MINUS"></a>
# BIN_MINUS

QDataSet of rank 0 or correlated QDataSet identifies boundary. This is subtracted from the
 measurements and should be interpreted as the lower limit of the 100% confidence interval where a measurement was collected.

***
<a name="BIN_MAX"></a>
# BIN_MAX

QDataSet of rank 1 identifies boundary in the same units as the dataset. 
 This should be interpreted as the upper limit of 100% confidence 
 interval where a measurement was collected.  When this is found, BIN_PLUS
 and BIN_MINUS should be ignored.

***
<a name="BIN_MIN"></a>
# BIN_MIN

QDataSet of rank 1 identifies boundary in the same units as the dataset.
 This should be interpreted as the lower limit of the 100% confidence 
 interval where a measurement was collected.  When this is found, BIN_PLUS
 and BIN_MINUS should be ignored.

***
<a name="BIN_MIN_NAME"></a>
# BIN_MIN_NAME

name of the dataset in a bundle to be connected to BIN_MIN.

***
<a name="BIN_MAX_NAME"></a>
# BIN_MAX_NAME

name of the dataset in a bundle to be connected to BIN_MAX.

***
<a name="BIN_MINUS_NAME"></a>
# BIN_MINUS_NAME

name of the dataset in a bundle to be connected to BIN_MINUS.

***
<a name="BIN_PLUS_NAME"></a>
# BIN_PLUS_NAME

name of the dataset in a bundle to be connected to BIN_PLUS.

***
<a name="DELTA_PLUS_NAME"></a>
# DELTA_PLUS_NAME

name of the dataset in a bundle to be connected to DELTA_PLUS.

***
<a name="DELTA_MINUS_NAME"></a>
# DELTA_MINUS_NAME

name of the dataset in a bundle to be connected to DELTA_MINUS.

***
<a name="CACHE_TAG"></a>
# CACHE_TAG

CacheTag, indicating the coverage and resolution of a dimension.  This is 
 an object that represents
 the coverage and resolution of the interval covered.  For example, in Autoplot
 the TimeSeriesBrowse uses this to keep track of what's already been read.

***
<a name="RENDER_TYPE"></a>
# RENDER_TYPE

String, hint as to preferred rendering method.  Examples include "spectrogram", "time_series", and "stack_plot", 
 "nnSpectrogram", "hugeScatter", "series", "scatter", "colorScatter", "stairSteps", "fillToZero"
 "digital", "image", "pitchAngleDistribution", "eventsBar".  Note these are just suggestions and are not
 interpreted in the library.

***
<a name="VALUE_RENDER_TYPE_SERIES"></a>
# VALUE_RENDER_TYPE_SERIES

full-fidelity rendering of buckshot and connect-a-dot plots

***
<a name="VALUE_RENDER_TYPE_NNSPECTROGRAM"></a>
# VALUE_RENDER_TYPE_NNSPECTROGRAM

use blocks to draw each point, so data extents can be seen.

***
<a name="VALUE_RENDER_TYPE_EVENTS_BAR"></a>
# VALUE_RENDER_TYPE_EVENTS_BAR

draw events bars

***
<a name="VALUE_RENDER_TYPE_DIGITAL"></a>
# VALUE_RENDER_TYPE_DIGITAL

values are drawn.

***
<a name="VALUE_RENDER_TYPE_COMPOSITE_IMAGE"></a>
# VALUE_RENDER_TYPE_COMPOSITE_IMAGE

values are an RGB image, a rank 3 dataset [w,h,3] or [w,h,4].  The
 "3" should be R,G, and B channels, and when "4" is used, ARGB is the
 default.  There can be a DEPEND_2 that is a QDataSet with ordinal data,
 specifying the channels like so Ops.labelsDataset(['a','b','g','r']) or
 Ops.labelsDataset(['a','b','g','r']).  Only bgr or rgb models are supported
 in the RGBImageRenderer, but future versions could support other color
 models.

***
<a name="NAME"></a>
# NAME

String, a java identifier that should can be used when an identifier is needed. This is
 originally introduced for debugging purposes, so datasets can have a concise, meaningful name 
 that is decoupled from the label. When NAMEs are used, properties with the same 
 name should only refer to the named dataset.

***
<a name="QUBE"></a>
# QUBE

Boolean.TRUE indicates that the dataset is a "qube," meaning 
 that all dimensions have fixed length and certain optimizations and 
 operators are allowed.  Note that when DEPEND_1 is a rank 1 dataset,
 this implies QUBE.  Likewise BUNDLE_1 is a qube.
 Note the result of any slice must be a qube.

***
<a name="COORDINATE_FRAME"></a>
# COORDINATE_FRAME

String, representing the coordinate frame of the vector index.  The units
 of a dataset should be EnumerationUnits which convert the data in this 
 dimension to dimension labels that are understood in the coordinate frame
 label context.  (E.g. X,Y,Z in GSM.)
 (Note this is before BUNDLE dimensions were formalized and is not used.)

***
<a name="METADATA"></a>
# METADATA

Map&lt;String,Object&gt; representing additional properties used by client codes.  No
 interpretation is done of these properties, but they are passed around as much
 as possible.  Note Object can be String, Double, or Map&lt;String,Object&gt;.  METADATA_MODEL
 is a string identifying the type of metadata,
 a scheme for the metadata tree, such as ISTP-CDF or SPASE.

***
<a name="METADATA_MODEL"></a>
# METADATA_MODEL

String, a scheme for the metadata tree, such as ISTP or SPASE.  This should identify
 a node's type when the node is present, but should not require that the node
 be present.  When a required node is missing, this should be treated as if
 none of the metadata is available.  This logic is to support aggregating
 metadata.

***
<a name="VALUE_METADATA_MODEL_ISTP"></a>
# VALUE_METADATA_MODEL_ISTP

the metadata is ISTP-CDF metadata

***
<a name="VALUE_METADATA_MODEL_SPASE"></a>
# VALUE_METADATA_MODEL_SPASE

the metadata is SPASE (Space Physics Archive Search Extract)

***
<a name="VALUE_COORDINATE_FRAME_COMPLEX_NUMBER"></a>
# VALUE_COORDINATE_FRAME_COMPLEX_NUMBER

the value is a complex number, having two elements, the first is real second is imaginary.

***
<a name="VERSION"></a>
# VERSION

String, human consumable identifying data version.  Presently this 
 is intended for human consumption, but eventually we may make them usable 
 by software as well.  Note if multiple versions go into making a product 
 (e.g. aggregation), the version string should contain space-delimited 
 version ids, so note versions must not contain spaces for other purposes.  
 Also two version strings containing the same value can be coalesced.  If this
 is prefixed with "&lt;scheme&gt;:", then this is to be interpreted as such:<ul>
  <li>sep: period-delimited list of numeric sorted: 2.2.0 &lt; 2.15.2 &lt; 10.2.0
  <li>alpha: alpha-numeric sorted: 20030202B&gt;20030202A
 </ul>
 otherwise it should be numerically sorted.
 (see org.das2.fsm.FileStorageModel)

***
<a name="SOURCE"></a>
# SOURCE

String, Human-consumable string identifying the source of a dataset, such as the file or URI from
 which it was read.  Clearly this is easily lost as processes are applied to the
 data, but when no other source is involved in a process (excluding library code
 itself), then the source should be preserved.

***
<a name="NOTES"></a>
# NOTES

QDataSet of events scheme, containing a list of messages encountered during processing that annotate the data.  
 For example, the AggregatingDataSource in Autoplot would add an event to the dataset when a file could not be used.
 This is a rank 2 dataset with BUNDLE_1=startTime,stopTime,message for now, but may soon allow for bounding qubes:
 BUNDLE_1=startTime,stopTime,startEn,stopEn,message, and this should be visualized via the EventsRenderer.

***
<a name="DEPENDNAME_0"></a>
# DEPENDNAME_0

String, the name of another dataset in the bundle descriptor.  Before this was introduced,
 a BundleDescriptor could have DEPEND_0 be a string.

***
<a name="DEPENDNAME_1"></a>
# DEPENDNAME_1

String, the name of another dataset in the bundle descriptor.  Before this was introduced,
 a BundleDescriptor could have DEPEND_1 be a string.  Note this should only be used if
 DEPEND_1 is rank 2, otherwise the dataset should be a property of DEPEND_1.

***
<a name="ELEMENT_NAME"></a>
# ELEMENT_NAME

String, the name of the rank 2 or more dataset in a bundle descriptor.

***
<a name="ELEMENT_LABEL"></a>
# ELEMENT_LABEL

String, the label of the rank 2 or more dataset in a bundle descriptor.

***
<a name="ELEMENT_DIMENSIONS"></a>
# ELEMENT_DIMENSIONS

int array, the dimensions of the element.  A rank 0 is implicitly [], 
 a rank 1, n by 1, would be [1].  This is similar to the size command, for
 one record of the data.

***
<a name="USER_PROPERTIES"></a>
# USER_PROPERTIES

Map&lt;String,Object&gt; representing additional properties used by client codes.  No
 interpretation is done of these properties, but they are passed around as much
 as possible.  The object values should be but don't have to be limited to: double, double array,
 datum, QDataSet, String, String array.

***
<a name="VALUE_BINS_MIN_MAX"></a>
# VALUE_BINS_MIN_MAX

typical bin is min,max with min inclusive and max exclusive.

***
<a name="VALUE_SCALE_TYPE_LOG"></a>
# VALUE_SCALE_TYPE_LOG

scale type to suggest log axes and bins.

***
<a name="VALUE_SCALE_TYPE_LINEAR"></a>
# VALUE_SCALE_TYPE_LINEAR

scale type to suggest linear axes and bins.

***
<a name="MIN_WAVEFORM_LENGTH"></a>
# MIN_WAVEFORM_LENGTH

the minimum length of each of the waveform packets in a rank 2 waveform dataset.

***
<a name="DEFAULT_FILL_VALUE"></a>
# DEFAULT_FILL_VALUE

the fill value often used in codes.

***
<a name="capability"></a>
# capability
capability( java.lang.Class clazz ) &rarr; Object

return null or an object implementing the capability for the given interface
 For example:
<blockquote><pre>
ds= DDataSet.createRank1(100);
WriteCapability write= ds.capability( WriteCapability.class );
write.putValue( 99, -1e31 );
</pre></blockquote>
 This allows operations to be performed efficiently.  Note there is no WriteCapability class, this is 
 just an example.

### Parameters:
clazz - the class, such as WriteCapability.class

### Returns:
the implementing class, or null (Jython None) if the capability is not provided.

<a href="https://github.com/autoplot/dev/search?q=capability&unscoped_q=capability">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="length"></a>
# length
length(  ) &rarr; int

return the length of the first dimension

### Returns:
the length of the first dimension

<a href="https://github.com/autoplot/dev/search?q=length&unscoped_q=length">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

length( int i ) &rarr; int<br>
length( int i, int j ) &rarr; int<br>
length( int i, int j, int k ) &rarr; int<br>
***
<a name="property"></a>
# property
property( String name ) &rarr; Object

accessor for properties attached to the dataset.  See final static members
 for example properties.

### Parameters:
name - property name, such as "DEPEND_0" or "UNITS"

### Returns:
the value
### See Also:
<a href='#DEPEND_0'>DEPEND_0</a> <br>
<a href='#UNITS'>UNITS</a> <br>

<a href="https://github.com/autoplot/dev/search?q=property&unscoped_q=property">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

property( String name, int i ) &rarr; Object<br>
***
<a name="rank"></a>
# rank
rank(  ) &rarr; int

returns the rank of the dataset, which is the number of indeces used to access data.  Only rank 0, 1, 2, 3, and 4 datasets
 are supported in the interface.   When a dataset's rank is 5 or greater, it should implement the HighRankDataSet interface
 which affords a slice operation to reduce rank.

### Returns:
the rank, or number of indeces used to access data.

<a href="https://github.com/autoplot/dev/search?q=rank&unscoped_q=rank">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="slice"></a>
# slice
slice( int i ) &rarr; QDataSet

return a dataset that is a slice of this dataset, slicing on the zeroth 
 dimension.
 A slice will be the elements at this index, for example if this dataset
 is a rank 2 dataset flux(Time,Energy) then the slice of this will be
 a rank 1 dataset flux(Energy).
 The result of any slice will be a qube.

### Parameters:
i - the index to slice at

### Returns:
the rank n-1 QDataSet at index i.

<a href="https://github.com/autoplot/dev/search?q=slice&unscoped_q=slice">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="svalue"></a>
# svalue
svalue(  ) &rarr; String

rank 0 accessor which provides the string value

### Returns:
the value, see the property UNITS to interpret this.

<a href="https://github.com/autoplot/dev/search?q=svalue&unscoped_q=svalue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="trim"></a>
# trim
trim( int start, int end ) &rarr; QDataSet

return a dataset that is a subset of this dataset.
 For example:
 <pre>
 
    ds= DDataSet.createRank1(100);
    QDataSet trim= ds.trim(50,60);
    assert( trim.length()==10 );
 
 </pre>

### Parameters:
start - the first index to be included in the new dataset.
<br>end - the exclusive index indicating the last index.

### Returns:
a QDataSet with the same rank but fewer elements.

<a href="https://github.com/autoplot/dev/search?q=trim&unscoped_q=trim">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="value"></a>
# value
value(  ) &rarr; double

rank 0 accessor.

### Returns:
the value, see the property UNITS to interpret this.

<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

value( int i ) &rarr; double<br>
value( int i0, int i1 ) &rarr; double<br>
value( int i0, int i1, int i2 ) &rarr; double<br>
value( int i0, int i1, int i2, int i3 ) &rarr; double<br>
