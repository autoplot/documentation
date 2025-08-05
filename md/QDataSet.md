**The Definitive Specification to QDataSet.**

Purpose: This document describes QDataSet as implemented for Autoplot,
and should serve as the definition of the working model. Other documents
should be considered specifications of a future version of QDataSet.
This document will also attempt to version the spec of QDataSet, so that
codes can describe compliance.

Keywords: qdataset dataset rank property qube bundle bins

See also [developer.qdataset](developer.qdataset.md "wikilink") which is a
new version of this document, in progress.

# Introduction

IDL, Matlab, Java, C and Fortran all model numbers in code. They can
store groups of numbers in arrays, but they do not try to model
measurements of data. When building any analysis system, the developer
must first create a model for storing data. This is typically done
ad-hoc and often with minimal attention, leading to problems down the
road.

QDataSet attempts to introduce a language-agnostic method for modelling
measurements of data. Other similar systems exist, such as NetCDF, and
CDF, but they have components that tend to drag them into a particular
domain. QDataSet tries to be as simple as possible, but still allowing
complex operations to be done. Further, QDataSet is a simple interface,
easily implemented in different environments, often with code that
achieves high-performance without loosing abstraction.

This poster describes most cleanly the interface: [2011
Poster](https://cottagesystems.com/~jbf/autoplot/posters/InsideAutoplot-20110531.ppt)

# QDataSet v1.0

A QDataSet is simply an array with properties describing the array, such
as physical units and labels. For example, to access the i-th element of
a QDataSet ds, call its value function: ds.value(i). QDataSets can have
0, 1, 2, 3, or 4 indexes, and its rank() function indicates the number
of indexes: ds.rank()-\>2 means that the dataset has two indexes and is
accessed like so: ds.value(i,j). Rank 0 QDataSets are simply scalars or
datasets with no indices, but they can still have properties describing
the value. To find out something about the numbers, we call the property
method: ds.property('LABEL') or ds.property('UNITS'). QDataSets needn't
define any properties, so all codes must handle these cases. (The value
null (or None) is returned when the property is not set.)

QDataSet describes models relationships of data with the DEPEND
properties. For example, take the tabulated function d\[t\] where for
every time t there is a value d. To model this with QDataSet, t is a
QDataSet, and d is a QDataSet with the property('DEPEND\_0') returning
t. Now for every element of d, we have a t to go with it. For a rank 2
dataset ds\[t,e\] we have two independent datasets t and e accessed with
'DEPEND\_0' and 'DEPEND\_1'. Note the dataset t will have all its own
properties, and must only be the same length as ds.

This is the model as it exists in Autoplot. QDataSet is short for Quick
Data Set, which uses a thin syntax layer and semantics to build
abstraction. This allows QDataSet to be implemented in many languages
such as Python, IDL, Fortran and C as well as in Java.

The list below describes all the properties that can describe datasets.
There are "dimension" properties which describe a physical dimension
that the data occupy: UNITS, SCALE\_TYPE, VALID\_MIN, TITLE. There are
structural properties that relate datasets: DEPEND\_0, BUNDLE\_0,
BINS\_0, JOIN\_0, PLANE\_0, DELTA\_PLUS. Also there are global
properties which allow us to describe the dataset itself:
USER\_PROPERTIES, METADATA, METADATA\_MODEL, RENDER\_TYPE.

Note: Autoplot uses the Java implementation of QDataSet, which may very
slightly from the specification here. For example, its UNITS property is
implemented with Das2 units, where a QDataSet could call for a string.
In Jython, the value method is simply the \_\_getitem\_\_ method so
ds\[i,j\] can be used.

# QDataSet of the Present

QDataSet has evolved from its original implementation in the IDL
software PaPCO to support new data types. Now that you get the general
idea, here are more advanced features of the model.

## Bundles

A Bundle index is one that combines a number of datasets into one
dataset. For example, imagine an ASCII table with columns containing
time, density and velocity in three components. This looks a lot like a
rank 2 bundle dataset. Unlike the ASCII table, there's no need for human
interpretation, and the property BUNDLE\_1 returns a dataset that
describes each column. So for example:

```
ds[time,bds]
ds.property( 'BUNDLE_1' ) -> bds
bds.property('UNITS',0) -> 'Seconds since 2012-01-01T00:00'
bds.property('UNITS',1) -> 'cm^-3'
bds.property('UNITS',2) -> 'K'
```
Note Autoplot's QDataSet implementation contains a useful 'unbundle'
function which extracts any of the datasets.

```
bundle( time[1440], density[time=1440], temperature[time=1440] ) -> data[time=1440,3]
unbundle( data[time=1440,3], 'density' ) -> density[time=1440]
```
## Bins Index

A Bins index indicates that the index describes ranges of a dimension.
This is a comma-delineated string with boundary identifiers. For
example:

```
ds[time,2]
ds.property(BINS_1)='min,max'
```
This would mean that ds\[0,0\] is the lower bound of the first time, and
ds\[0,1\] is the upper bound. Autoplot looks only for 'min,max' to
indicate bins in the LANL Nearest Neighbor mode for spectrograms
(lanlNearestNeighbor rebinner).

## Joins

A Join index is a zeroth that contains multiple datasets with the same
"scheme" or type of data. For example, if you have seven days with
spectra for each day, you can join them together to form a seven-day
spectrogram. This is also used with an instrument that operates in
several modes (e.g. low, middle and high frequency sampling), with a
join of data from each mode.

Suppose we have roughly 1440 measurements each day:

```
join( ds[time=1440,energy=32], ds[time=1441,energy=32 ) -> ds[join=2,time=1440*,energy=32*]
```
Note the asterisk (\*) which indicates the result is not a qube.

Note a join of joins can often be reduced so that there is just one join
dimension. For example, the data aggregator would implement the join
with the existing join dimension:

```
join( ds[time=1440,energy=32], ds[time=1441,energy=32 ) -> ds[time=2881,energy=32]
```
## QDataSet libraries

Any QDataSet library should provide functions for operating on the data.
For example, slicing is commonly done (slice a rank 2 dataset to get a
rank 1), and operators that correctly propagate properties should be
provided.

Note that Autoplot uses an implementation of QDataSet, so there may be
minor inconsistencies between the spec here and its use.

# Schemes Introduced

Along with versioning the interface, it's useful to identify qdataset
schemes encountered and supported.

  - rank 1 timeseries (time)
  - single table spectrogram (time,freq)
  - rank 3 qube (time,energy,pitch)
  - image (hpixels, vpixels, rgb )
  - lat-lon timeseries (lat, lon, time )
  - array of vectors (time,component)
  - array of complex numbers (time,component)
  - array of waveforms (time,offset). DEPEND\_1 offsets are rank 2.
    2009/08/21
  - engineering spectrogram using RENDER\_TYPE=nnSpectrogram
  - array of spectrograms (table,time,freq) This is the general das2
    TableDataSet.
  - array F\[X,Y,Z\] where Y and Z are time-varying with X. (As with
    CDF.)

# QDataSet Properties

The properties attached to each dataset allow the dataset to describe
complicated things.

From
<https://sourceforge.net/p/autoplot/code/HEAD/tree/autoplot/trunk/QDataSet/src/org/das2/qds/QDataSet.java>

DEPEND\_0. type QDataSet. This dataset is a dependent parameter of the
independent parameter represented in this DataSet. The tags for the
DataSet's 0th index are identified by this tags dataset.

DEPEND\_1. type QDataSet. This dataset is a dependent parameter of the
independent parameter represented in this DataSet. The tags for the
DataSet's 1st index are identified by this tags dataset. When DEPEND\_1
is rank 2, then its first dimension goes with DEPEND\_0 and its second
are the tags for the second dimension. When DEPEND\_1 is a rank 1
dataset, then the data is a qube.

DEPEND\_2. type QDataSet. This dataset is a dependent parameter of the
independent parameter represented in this DataSet. The tags for the
DataSet's 2nd index are identified by this tags dataset. When DEPEND\_2
is rank 2, then its first dimension goes with DEPEND\_0 and its second
are the tags for the second dimension. When DEPEND\_\* is a rank 1
dataset, then the data is a qube.

DEPEND\_3. type QDataSet. This dataset is a dependent parameter of the
independent parameter represented in this DataSet. The tags for the
DataSet's 3nd index are identified by this tags dataset. When DEPEND\_2
is rank 2, then its first dimension goes with DEPEND\_0 and its second
are the tags for the second dimension. When DEPEND\_\* is a rank 1
dataset, then the data is a qube.

JOIN\_0. type String. Any string of length\>1 indicates that the 0th
dimension is a group of similar datasets, implicitly appending them.

BUNDLE\_1. type QDataSet. This dataset describes how the columns should
be split up into separate parameters. This rank 2 dataset has a length
that is equal to the number of elements it is describing. The
values(i,\*) are the qube dimensions of the dataset, except for the
first dimension. When all the bundled datasets are rank 1, then
length(i) will be equal to zero. property(\*,UNITS) will yield the unit
for each dataset. Bundle dimensions generally add one physical dimension
for each bundled dataset. property(\*,DEPEND\_NAME\_0) should be used
instead of DEPEND\_0, because it will return a string rather than a
QDataSet. This string should refer to one of the bundled datasets by its
NAME property. (Any property that returns a QDataSet should return a
string referring to another dataset in the bundle.) Also the dataset
being described is necessarily a QUBE.

BUNDLE\_0. type QDataSet. This dataset describes how the columns should
be split up into separate parameters. See BUNDLE\_1. Note slicing a
dataset on the zeroth dimension will move BUNDLE\_1 to BUNDLE\_0.
Properties defined in this dataset will be overwritten by the BUNDLE
dataset's properties. For example, if the dataset has property( UNITS, 0
) defined as "Hz" but the bundle has property( UNITS,0 ) as "Hertz" then
"Hertz" is used.

START\_INDEX. type Integer. Only found in a bundle descriptor (BUNDLE\_0
or BUNDLE\_1), this returns the integer index of the start of the
current dataset. If this is null, then the index used to access the
value may be used. (E.g. a bundle of Rank 1 datasets.)

DEPEND\_NAME\_0. type String. Only found in a bundle descriptor, the
name of the dataset to use for DEPEND\_0 when unbundling.

DEPEND\_NAME\_1. type String. Only found in a bundle descriptor, the
name of the dataset to use for DEPEND\_1 when unbundling. Note typically
this is for when DEPEND\_1 is rank 2, otherwise DEPEND\_1 can be used
instead of DEPEND\_NAME\_1.

ELEMENT\_NAME. type String. The NAME of the dataset when unbundling the
high rank dataset. If not set, then the common parts of the NAMES are
used. ELEMENT\_NAME=B\_GSM, NAME\[0\]="UT TIME" NAME\[1\]="B\_GSM\_X"

ELEMENT\_LABEL. type String. The LABEL to use when unbundling the high
rank dataset. If not set, then the common parts of the LABELS are used.
ELEMENT\_LABEL="B, GSM", LABEL\[0\]="UT TIME" LABEL\[1\]="B, GSM X"

BINS\_1. type String. This comma-delimited list of keywords that
describe the boundary type for each column. For example, "min,max" or
"c95min,mean,c95max" A bins dimension doesn't add a physical dimension.
Note Autoplot uses only "min,max"

BINS\_0. type String. This comma-delimited list of keywords that
describe the boundary type for each column. For example, "min,max" or
"c95min,mean,c95max" A bins dimension doesn't add a physical dimension.

PLANE\_0. type QDataSet. Correlated plane of data. An additional
dependent DataSet that is correlated by the first index. Note "0" is
just a count, and does not refer to the 0th index. All correlated
datasets must be correlated by the first index. TODO: what about two
rank 2 datasets?

CONTEXT\_0. type QDataSet. A dataset that stores the position of a slice
or range in a collapsed dimension. In "Flux(Energy) @
Time=2009-03-16T11:19 UT", the Time=... comes from a context property.
Note "0" is just a count, and does not refer to the 0th index. A dataset
can have any number of contexts: Temperature @ ( Time, Long, Lat ): 37
deg F @ ( 2009-03-16T11:19 UT, 91.5331 deg West, 41.6579 deg North )
Typically this will be a rank 0 dataset, but may also be a rank 1
dataset with a bins dimension.

UNITS. type org.das2.units.Units. The dataset units, found in
org.das2.units.Units. This will change to a String, with codes that
provide units conversion and "Datum" handling.

FORMAT. type String. Java/C format string for formatting the values.
This should imply precision, and codes that serialize data can use this
to correctly format the data. Note Java 5 supports field specs like
%tY-%tj, and these may be used for time data, as long as only these
field types are in the string. Empty values ("") are to be interpreted
as default formatting.

FILL\_VALUE. type Number, value to be considered fill (invalid) data.
Note NaN is always considered fill and its use is encouraged.

VALID\_MIN. type Number. Range bounding measurements to be considered
valid. Lower and Upper bounds are inclusive. FILL\_VALUE should be used
to make the lower bound or upper bound exclusive. Note DatumRange in
das2 contains logic is exclusive on the upper bound.

VALID\_MAX. type Number. Range bounding measurements to be considered
valid. Lower and Upper bounds are inclusive. FILL\_VALUE should be used
to make the lower bound or upper bound exclusive. Note DatumRange in
das2 contains logic is exclusive on the upper bound.

TYPICAL\_MIN. type Number. Range used to discover datasets. This should
be a reasonable representation of the expected dynamic range of the
dataset.

TYPICAL\_MAX. type Number. Range used to discover datasets. This should
be a reasonable representation of the expected dynamic range of the
dataset.

SCALE\_TYPE. String, "linear" or "log" "mod24" "mod360" etc.

AVERAGE\_TYPE. String, "linear" "geometric" "mod24" "mod360" "modpi"
"modtau" "none". Some data handling codes will check to see how data
should be averaged. For example, Autoplot's interpolate will call this
to see how interpolation is to be done.

NAME. String, a java identifier that should can be used when an
identifier is needed. This is originally introduced for debugging
purposes, so datasets can have a concise, meaningful name that is
decoupled from the label. When NAMEs are used, properties with the same
name should only refer to the named dataset.

LABEL. String, Concise Human-consumable label suitable for a plot label.
(10 chars)

TITLE. String, Human-consumable string suitable for a plot title. (100
chars).

DESCRIPTION. String, Human-consumable string, between one sentence and
four paragraphs in length. Note the ordering: NAME, LABEL, TITLE,
DESCRIPTION.

MONOTONIC. Boolean, Boolean.TRUE if dataset is monotonically increasing.
Also, the data must not contain invalid values. Generally this will be
used with tags datasets. Negative CADENCE implies monotonic decreasing.

WEIGHTS. QDataSet, dataset of same geometry that indicates the weights
for each point. Often weights are computed in processing, and this is
where they should be stored for other routines. When the weights plane
is present, routines can safely ignore the FILL\_VALUE, VALID\_MIN, and
VALID\_MAX properties, and use non-zero weight to indicate valid data.
Further, averages of averages will compute accurately.

CADENCE. Rank 0 QDataSet, the expected distance between successive
measurements where it is valid to make inferences about the data. For
example, interpolation is disallowed for points 1.5\*CADENCE apart. This
property only makes sense with a tags dataset.

DELTA\_PLUS. QDataSet of rank 0 or correlated plane limits accuracy,
using positive numbers. This should be interpreted as the one standard
deviation confidence level. See also BINS\_i for measurement intervals.

DELTA\_MINUS. QDataSet of rank 0 or correlated plane limits accuracy,
using positive numbers. This should be interpreted as the one standard
deviation confidence level. See also BINS\_i for measurement intervals.

CACHE\_TAG. CacheTag, to be attached to tags datasets. This is an object
that represents the coverage and resolution of the interval covered. For
example, in Autoplot the TimeSeriesBrowse uses this to keep track of
what's already been read. The cache tag object might represent
'2012-02-25 @ 6.0 min', so if the user needed to plot data at 1 minute
resolution, the dataset would not be sufficient, and the
TimeSeriesBrowse capability is used to retrieve a finer resolution
dataset.

RENDER\_TYPE. String, hint as to preferred rendering method. Examples
include "spectrogram", "time\_series", and "stack\_plot". In Autoplot,
this may the name of one of it's render types, represented as a string
like "contour". This will be built up to support more precise
descriptions, for example "contour\>levels=1,3,5,7,10" or similar.
"eventsBar\>color=red"

QUBE. Boolean.TRUE indicates that the dataset is a "qube," meaning that
all dimensions have fixed length and certain optimizations and operators
are allowed. Note that when DEPEND\_1 is a rank 1 dataset, this implies
QUBE. Likewise BUNDLE\_1 is a qube.

COORDINATE\_FRAME. String, representing the coordinate frame of the
vector index. The units of a dataset should be EnumerationUnits which
convert the data in this dimension to dimension labels that are
understood in the coordinate frame label context. (E.g. X,Y,Z in GSM.)
(Note this is before BUNDLE dimensions were formalized and is not used.)
Complex numbers should use "ComplexNumber" for this.

METADATA. Map\<String,Object\> representing additional properties used
by client codes. No interpretation is done of these properties, but they
are passed around as much as possible. Object can be String, Integer,
Double, or Map\<String,Object\>. METADATA\_MODEL is a string identifying
the type of metadata, a scheme for the metadata tree, such as ISTP-CDF
or SPASE.

METADATA\_MODEL. String identifying a scheme for the metadata tree, such
as ISTP or SPASE. This should identify a node's type when the node is
present, but should not require that the node be present. When a
required node is missing, this should be treated as if none of the
metadata is available. This logic is to support aggregating metadata.
The constants VALUE\_METADATA\_MODEL\_ISTP and
VALUE\_METADATA\_MODEL\_SPASE should be used to identify these.

VERSION. String, human consumable identifying version. Presently this is
intended for human consumption, but eventually we may make them usable
by software as well. Note if multiple versions go into making a product
(e.g. aggregation), The version string should contain space-delimited
version ids, so versions must not contain spaces for other purposes.
Also two version strings containing the same value can be coalesced. If
this is prefixed with "<scheme>:", then this is to be interpreted as
such: sep: period-delimited list of numeric sorted: 2.2.0 \< 2.15.2 \<
10.2.0 alpha: alpha-numeric sorted: 20030202B\>20030202A otherwise it
should be numerically sorted. (see org.das2.fsm.FileStorageModelNew)
Examples: "sep:2.15.2" "2.15" "alpha:20030202B"

SOURCE. String, Human-consumable string identifying the source of a
dataset, such as the file or URI from which it was read. Clearly this is
easily lost as processes are applied to the data, but when no other
source is involved in a process (excluding library code itself), then
the source should be preserved.

MESSAGES. QDataSet. QDataSet of events scheme, containing a list of
messages encountered during processing that annotate the data. For
example, the AggregatingDataSource in Autoplot would add an event to the
dataset when a file could not be used. This is a rank 2 dataset with
BUNDLE\_1=startTime,stopTime,message for now, but may soon allow for
bounding boxes (BUNDLE\_1=startTime,stopTime,startEn,stopEn,message).
This property can be be visualized via the EventsRenderer.

USER\_PROPERTIES. Map\<String,Object\> representing additional
properties used by client codes. No interpretation is done of these
properties, but they are passed around as much as possible.

# Schemes

I thought it would be useful to enumerate colloquial terms for datasets.
I use these phrases all over the place in the Autoplot documentation.

  - **time series** is a dataset with DEPEND\_0 a set of timetags, or a
    JOIN dataset of time series datasets.
  - **simple table** is a rank 2 dataset, maybe with DEPEND\_0 and
    DEPEND\_1 set. E.g. Flux\[Time=1440,Energy=32\]
  - **vector time series** is a bundle of 3 rank 1 datasets for each
    component. E.g. Bgsm\[Time=1440,3\]
  - **join dataset** is a dataset that has JOIN\_0 set to combine
    similar datasets into one dataset. "Array of" dimension.
  - **join of simple tables** is a rank 3 JOIN of simple tables
    datasets. These are used a lot at the Plasma Wave Group for
    representing data with instrument mode changes.
  - **rank zero dataset** is a single value and metadata. This
    corresponds to a das2 Datum.
  - **bounds** is a rank 1 dataset with BINs dimension specifying min
    and max. Typically max would be exclusive and min would be
    inclusive. This corresponds to a das2 DatumRange.
  - **bounding cube** is a rank 2 dataset joining a set of bounds. Has
    JOIN\_0. For example, ds\[0,0\] is x min, ds\[0,1\] is x max. This
    can have any number of elements in the 0th (join) index, but this is
    typically two, for x and y. Examples: Renderer.autorange. Sometimes
    called a bounding box for two dimensions.
  - **bundle** is a set of datasets with different units and possibly
    rank. This is rank 1 or rank 2, and BUNDLE\_0 or BUNDLE\_1 is a
    QDataSet containing the properties and rank of each bundled dataset.
  - **tuple** is a rank 1 bundle of rank 0 datasets, like \[
    time,density, positionx, positiony, positionz \].
  - **simple bundle** is a set of datasets all having the same rank and
    geometry.
  - **rich bundle** is a bundle of rank 1, rank 2, and rank N datasets.
  - **bundle descriptor** is the dataset that BUNDLE\_1 points to,
    describing each of the bundled datasets.

Note more abstract schemes are coming to describe scientific use of
datasets.

See
<http://sourceforge.net/p/autoplot/code/HEAD/tree/autoplot/trunk/QDataSet/src/org/das2/qds/examples/Schemes.java>
which starts to experiment with detecting schemes programmatically.

# Schemes Not Described

## Points along a curve

Take trajectory X,Y. Collect data D1,D2,D3,D4 collected along X,Y.
D1,D2,D3,D4 -\> X,Y -\> T. One thought is that a rank 2 bundle could be
allowed for DEPEND\_0. This competes with the alternate spec that a rank
2 DEPEND\_0 would be interpreted as a join, but I don't believe that
either interpretation is used anywhere. Spectra collected along a curve
should be considered as well, but I think the bundle rule would capture
that.

See TickCurveRenderer.java.

## Complex Numbers

SciPy and IDL support complex numbers, and QDataSet's support has been
ad hoc.

```
dep1.putProperty(QDataSet.COORDINATE_FRAME, "ComplexNumber");
```
is used in the fft function, but you could have a COORDINATE\_FRAME with
complex components.

# Dataset Mutability

The QDataSet interface provides read-only access to the data. Many
implementations provide write-access as well, implementing the
"WritableDataSet" interface. For these, one calls putValue to overwrite
values in the data. Such datasets are said to be mutable. There is also
a MutablePropertyDataSet which allows the just properties to be
modified.

Mutability is important, because many implementations are more easily
implemented when the data cannot be modified, such as mapping data
directly from storage into memory, and performance improved.
Additionally, data can be cached without having to worry about a code
using the cached data modifying it.

Part of the MutablePropertyDataSet and WritableDataSet interface then is
a flag that will make the data immutable. This allows codes to create
data then mark the data as immutable before handing off the result. Once
the data is marked as immutable, then there is no way to modify the
data. Codes that check to see if data can be modified (checking
instanceof MutablePropertyDataSet) must also check the isImmutable
method to see if it can be modified directly.

There is a handy putProperty method which will make a copy of the data
so that properties can be added:

```
    ds= putProperty( ds, 'FilesRead', file )
```
Note that there are optimal implementations doing this, such as copying
over the properties but leaving the data immutable.

## Capabilities

Another new method for managing mutability is to avoid instanceof use
altogether and use the capability method. For example,

```
    WriteCapability write= ds.capability( WriteCapability.class )
```
would return null if the data cannot be modified, or the
WriteCapability. This method exists in the interface but is not used.

## DataSetAnnotations

Last, there is a DataSetAnnotations mechanism that allows information to
be stored about live QDataSets. For example, one might want to record
the file read to make a QDataSet. The file location could be added as a
property, but this requires that the QDataSet would have to be mutable.
Another way to record this would be using

```
    DataSetAnnotations.getInstance().getAnnotation( ds, 'fileSource' )
```
Note that when the dataset is no longer used and is garbage collected,
the annotation will also be removed. (A WeakHashMap is used to store
them.)

# Notation

Someday conventions for notation of datasets needs to be standardized.
For example, I can say Density\[Time=1440\] for density measurements
taken at 1440 times. But things have never been nailed down for bundles,
etc. For the points along a curve, maybe this is how it would be
indicated:

```
  D[T=1440;D1,D2,D2,D4]
```
so a semicolon would delineate each index. Then

```
  D[T=1440;D1,Spec[32],D2] 
```
would indicate the rich bundle.

Why is this important? Documentation and user feedback depends on this.
When the user mouses over an expression in Jython, we have to show what
it is. If you don't have a word for it you can't talk about it.

## Tests

The where command returns a rank 1 list of indices when the argument is
rank 1, and a rank 2 bundle of indices when the argument is rank N. How
should this be documented?

"where(ds) returns a rank 2 dataset of indices Indexes\[m,N\] where m is
the number of points where the array is non-zero and N is the rank of
the dataset."

"The TickCurveRenderer plots data Traj\[T=1440;X,Y\] along a curve. At
each point, we collect 4 measurements: D\[Traj;D1,D2,D3,D4\]"

## 20150323

I've been experimenting with a different style of notation for the
ScienceDataInterfaces library
(http://jfaden.net/\~jbf/autoplot/ScienceDataInterfaces/javadoc/). I saw
this originally used by Doug Lindholm at LASP, and it does solve some of
the problems I've had. For example,

```
   D[T=1440] 
```
would be stated as:

```
   T(i)->D(i)
```
or just:

```
   T->D
```
For spectrograms you can have:

```
   X(i),Y(j)->Z(i,j)
```
and buckshot data would be:

```
   X(i),Y(i)->Z(i)
```
What would a bundle look like (I'm not sure):

```
   T(i),BDS(j->X,Y,Z)->Z(i,j)
   
```
&quot;The TickCurveRenderer plots data T(i\&lt;1440),(j&rarr;X,Y)&rarr;Traj(i,j) along a
curve. At each point, we collect 4 measurements:
Traj,(j&rarr;D1,D2,D3,D4)&rarr;D(i,j)&quot; &quot;i,j(0=low,1=high) &rarr; BinBoundary(i,j)&quot;

Unicode can also be used: &isin; \&amp;isin; &rarr; \&amp;rarr;

This also needs the rule that i,j,k,l,m,n,i0,i1,..i9 are reserved for
index names.

## 20150514

Index slice when BUNDLE\_0 is present. This operation should return null
or None because otherwise there would be ambiguity.

# TODO

Items for this documentation.

  - QFunction is a similar interface used for functions instead of
    discrete data. A QFunction has an example input, and then one method
    "value" which takes the example input.
    [1](http://autoplot.org//QFunction)

# Modification History

## 2009-May (v.1.05)

### Rank 0 Support introduced

rank zero added to QDataSet, removing need for RankZeroDataSet
interface.

## 2009-July (v1.10)

### Rank 4 Support introduced

QDataSet interface extended to support rank 4 datasets.

### Bundle dimension added

BUNDLE\_1. An index can refer to a bundle dimension that bundles
datasets together. Previously, DEPEND\_1 was used, and it would point to
a dataset of dataset labels. Bundles may deprecate planes. Bundle
dimension must be the 1st dimension, may not be the zeroth dimension.

### Bundle DataSets with DEPEND\_0 in property(DEPEND\_0,idx)

Slice0 dataset has code that checks for property(DEPEND\_0,idx) to see
if the DEPEND\_0 dataset needs to be moved to the zeroth dimension.

## 2009-Aug (v1.20)

### Rank 2 DEPEND\_1

DEPEND\_1 can be a rank 2 dataset, in which case the dataset is a
non-qube. slice0 should slice DEPEND\_1 as well. slice1 is an invalid
operation. There is code that checks for rank 2 DEPEND\_0, and it is
illegal for both DEPEND\_0 and DEPEND\_1 to have rank\>1.

### CONTEXT\_0 property

Slice operations that remove a dimension can identify the slice position
using the CONTEXT\_<idx> property which is equal to a rank 0 dataset.

  - In "Flux(Energy) @ Time=2009-03-16T11:19 UT", the Time=... comes
    from a context property.
  - A dataset can have any number of contexts, and "%{CONTEXT}" may
    refer to a string representing all of them.
      - Temperature @ ( Time, Long, Lat ): 37 &deg;F @ ( 2009-03-16T11:19
        UT, 91.5331&deg; West, 41.6579&deg; North )

Conventionally, the contexts should reflect the original nesting of the
contexts. If flux(time,energy,pitch) is sliced on energy then time, the
context should still be @ ( time, energy ), regardless of the slice
order. This will be difficult to implement, so this is not required.

## 2009-Sep-28 (v1.30)

### Metadata Handling

  - Introduce METADATA property (Map\<String,Object\>) and
    METADATA\_MODEL property.
  - These will be treated similar to the USER\_PROPERTIES property.
  - Aggregation logic to be determined:
      - propagate nodes with equal value, or
      - allow nodes to have multiple values by appending uniq number
        (RANGE-1, RANGE-2, etc.), and metadata models should handle
        aggregation.

### Schemes Used

  - Rank 1 "Bins" dataset with SCALE\_TYPE property used to indicate
    autorange result. This is formatted with the DataSetUtil.format.

## 2009-Nov-12

  - With Jon Vandegriff, we agreed that scheme identifiers should be
    like:
      - duck typing. If it has the properties of an X it is an X. Scheme
        implementations must be able to identify.
      - inheritance used and should be indicated: Series\>GageHeight. I
        don't have to know what a GageHeight is to know that it is a
        Series.
      - multiple inheritance used: timetagged,spectrogram means it has
        the properties of a "timetagged" and "spectrogram"

## 2010-Jun-24

  - properties for dimensions (DEPEND\_0, BUNDLE\_0, BINS\_0, JOIN\_0,
    etc) have their scope limited to that dimension. e.g.
    property(TITLE,0) would often be the same as property(TITLE), and
    this was true for dimensional properties as well. Some datasets have
    property(DEPEND\_0), but should not have property(DEPEND\_0,0),
    which is the same as property(DEPEND\_1).
  - property names like "LABEL\[0,2\]" are allowed only if they are the
    same as property("LABEL",0,2).

## 2010-Sep-23

  - rank 2 DEPEND\_2 and DEPEND\_3 imply dependence varying with
    DEPEND\_0. Slice0 operator must slice these as well when DEPEND\_2
    and DEPEND\_3 rank==2.

## 2011-Feb-14

  - introduce VERSION and SOURCE. In Autoplot, VERSION can be reported
    in Renderer label with %{VERSION}
  - Indexed properties can be aliased with <name>\_\_<i0>\_<i1>. In
    Autoplot this is implemented in AbstractDataSource, which stores all
    properties in one hashmap. Slice0 needs to go through and move
    <name>\_\_<i0>\_<i1> to <name>\_\_<i1>.

## 2011-Feb-28

  - indexed property change shows other problems, and now we remove
    high-rank indexed properties completely. Now property(NAME) and
    property(NAME,Index) are the only property accessors (autoplot
    2011).
  - JOIN\_0 property is now a QDataSet, not a string. This contains an
    empty dataset which may have the property QDataSet.CACHE\_TAG set.
  - "strict" JOIN datasets have the property that all the joined
    datasets have the same UNITS. Bounding box is a JOIN of BINS
    datasets, but is not strict. If the JOIN\_0 property is set, then
    the dataset is a strict JOIN. If no property is set, then it is an
    implicit join.

## 2011-Apr-13

  - Bundles now have same length as the dataset they describe. Before,
    bundling rank 2 datasets would mean datasets would have different
    lengths. This resulted in a bunch of broken code that assumed a
    bundle of Rank 1 datasets, even though the spec always had this. The
    new property START\_INDEX points to the first index of the high-rank
    dataset, and values and properties are repeated product(qubedims)
    times. This also allows slice1 to be used to unbundle a rank 1
    dataset, even if it is a single component of a rank 2 dataset.

<!-- end list -->

  - DEPENDNAME\_1 added so that DEPEND\_1 is always a QDataSet. Before
    DEPEND\_1 could be a string if it was in a BUNDLE.

<!-- end list -->

  - ELEMENT\_NAME and ELEMENT\_LABEL added, so that individual elements
    can have different NAME and LABEL properties, and ELEMENT\_NAME
    contains the name of the unbundled dataset. If not found, then the
    NAME for the unbundled dataset should be the common parts of the
    element names. (B\_GSM\_X, B\_GSM\_Y, B\_GSM\_Z --\> B\_GSM).

## 2011-Jun-14

  - Consider duck-typing to allow a dataset to be both a simple table
    (with DEPEND\_1) and a bundle (with BUNDLE\_1). LANL wants to be
    able to go back and forth. There's lots of code that assumes that if
    it's a bundle then it is not a simple table, but the intention all
    along has been more like duck typing.

## 2011-Nov-18

  - unbundle(ds,'ch\_1') will always slice on the channel. Before this
    was limited to datasets that didn't have labels for each channel.
    <http://cdaweb.gsfc.nasa.gov/istp_public/data/ace/mfi_h3/1998/ac_h3_mfi_19980101_v01.cdf?BRTN>
    has the bug that all the channels had the same label. So we detect
    this and use "ch\_\<i\>" instead.

## 2012-Feb-14

  - Declare DESCRIPTION as part of the properties. This is not supported
    anywhere, but we've talked about this for a while and we ought to at
    least pick a name.

## 2012-July-17

  - BUNDLE\_2 and BUNDLE\_3 can be used as long as it and BUNDLE\_1 are
    simple bundles (varying only by label and name). Unbundle will only
    work on the BUNDLE\_1.
  - BINS\_2 and BINS\_3 supported for consistency.

## 2012-10-12

  - NOTES added, so that the aggregating data source can document why a
    read failed.

## 2013-02-16

  - BIN\_PLUS and BIN\_MINUS added which are like DELTA\_PLUS and
    DELTA\_MINUS but represent the 100% confidence interval of a
    presumably uniform distribution, for example when data is
    accumulated over a time interval. Note this is not redundant with
    BINS\_0, because this is a string property describing the meaning of
    each index of a dimension.

## 2016-09-27

  - high-rank bundles should use ELEMENT\_DIMENSIONS int\[\] property,
    instead of the values of the dataset. This old method might have
    been clever, but it made forming high-rank bundles difficult, and
    makes the dataset more difficult to serialize to QStream or other
    forms.

## 2014-10-26

  - The result of any slice must be a qube. The RPWS group returns
    QDataSets with mode changes, but each mode is itself a qube. This
    assertion makes it possible to make WritableJoinDataSets and
    properly cache data.
  - BUNDLE\_i must point to a dataset with properties that are at most
    rank 0. This has never been stated, but properties such as
    DEPEND0\_NAME are a result of this formerly implicit rule.

## 2015-05-14

  - When BUNDLE\_0 is present, indexed properties are not allowed.
    Otherwise there would be an ambiguity about where the properties
    would come from.

## 2016-11-02

Chris and I discovered that BIN\_PLUS was misused in the
StackedHistogramRenderer, so BIN\_MAX and BIN\_MIN will be introduced to
explicitly state ranges. BIN\_PLUS and BIN\_MINUS will continue to be
supported.

## 2018-06-18

Rank 3 depend 2 is supported. This allows some data to be correlated
one-to-one while other channels are simple rank 1 depends.

## 2022-06-10

AVERAGE\_TYPE property added.

