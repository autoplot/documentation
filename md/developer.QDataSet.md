Purpose: Notes for the development of QDataSet. As components are
implememented and matured, they should be moved to QDataSet.

Audience: developers

See also: [QDataSet](QDataSet.md "wikilink")
[developer.qdataset](developer.qdataset.md "wikilink")

# Introduction

IDL, Matlab, Java, C and Fortran all model numbers in code. They can
store groups of numbers in arrays, but they do not try to model
measurements of data. When building any analysis system, the developer
must first create a model for storing data. This is typically done
ad-hoc and often with minimal attention, leading to problems down the
road.

QDataSet attempts to introduce a language-agnostic method for modeling
measurements of data. Other similar systems exist, such as NetCDF, and
CDF, but they have components that tend to drag them into a particular
domain. QDataSet tries to be as simple as possible, but still allowing
complex operations to be done. Further, QDataSet is a simple interface,
easily implemented in different environments, often with code that
achieves high-performance without loosing abstraction.

This poster describes most cleanly the interface: [2011
Poster](http://autoplot.org/wiki/images/InsideAutoplot-20110531.ppt) A
QDataSet is basically an array with properties, and some of these
properties may have values that are other QDataSets.

Note: Autoplot uses an implementation of QDataSet, which may very
slightly from the specification here. For example, its UNITS property is
implemented with Das2 units, where a QDataSet could call for a string.

# Model Y vs T

A simple and oft occurring data are when we collect a scalar quantity at
regular intervals. For example, we want to measure plasma density at our
spacecraft each minute for a day. So in this case for the density
values, we have the QDataSet we will call "density." Here are some
example calls to illustrate:

```
density.rank()   --> 1
density.length() --> 1440
density.value(0) --> 2.3
density.property( 'UNITS' ) -> 'cm**-3'
```
This dataset is called a "rank 1" dataset, because one index (0) is used
to access the numbers. Of course we want to know when each measurement
was taken, so we query for a DEPEND\_0 property:

```
density.property( 'DEPEND_0' ) -> time, a rank 1 QDataSet
time.rank()      --> 1
time.value(0)    --> 1.4832294E9   (2017-01-01T10:00Z)
time.property( 'UNITS' )  -->  'seconds since 1970-01-01T00:00Z'
```
To encourage a standard method for concisely representing these
datasets, density would be printed as:

```
density[time=1440]
```
Note, independent data has no "DEPEND\_0" property. Dependent data has a
"DEPEND\_0" property. This rank 1 dataset occupies two physical
dimensions: one for density and one for time.

# Model Flux vs Time and Energy

Now suppose we want to represent a spectrogram of flux values occurring
at grid of time and energy locations.

```
flux.rank()  --> 2
flux.value(0,0) --> 9.04e5
flux.property( 'UNITS' ) --> '1/(cm^2-s-sr)'
flux.property( 'DEPEND_0' ) --> time
flux.property( 'DEPEND_1' ) --> energy
```
# Rank 0 Datasets

Often it's useful to express single measurements, and rank 0 datasets
are used for this. Each dataset has a slice operation which extracts the
data at the slice location. So:

```
density.slice(0) --> '2.3 cm**-3', a rank 0 dataset
```
This rank 0 dataset's value can be accessed (with value()), and it still
has properties.

```
d1= density.slice(0)
d1.property( 'UNITS' ) --> 'cm**-3'
```
The time value is still carried along with the data:

```
d1.property( 'CONTEXT_0' ) --> t1, also a rank 0 dataset.
```
# Vector Time Series

The QDataSet representing a vector time series, like a three-component B
field measured every second of a day, looks like so:

```
bgsm.rank()   -->  2
bgsm.property( 'DEPEND_0' ) --> Time[86400]
bgsm.length() -->  86400
bgsm.length(0) --> 3
bgsm.value(0,0) --> 2.338 nT
bgsm.value(0,1) --> -7.167 nT
bgsm.value(0,2) --> -0.576 nT
```
But how do we know which component is which? Instead of a DEPEND\_1
describing the second index, we find a property BUNDLE\_1. This is a
dataset that contains properties for each index. So,

```
bds= bgsm.property( 'BUNDLE_1' )
bds.length() -->  3
bds.property('LABEL',0)  -->  "Bx (GSM)"
```
This dataset has dimensions \[3,0\].

Note sometimes it is sufficient to have just labels for each component,
and a legacy form for this data is still supported, using nominal data
for the three vector labels in a DEPEND\_1 dataset.

# Join Dimensions

Occasionally instruments have multiple collection modes which change
over the course of collecting data each orbit. For example, from 0:00 to
2:00 we collect at 27 energies from 10 to 20000eV each minute, and then
from 2:00 to 7:00 we collect 101 energies from 500eV to 100000eV, and
then from 7:00 until 9:00 we collect 27 again, and then from 9:00 to
09:30 we collect 101 energies. One way to represent this data is with a
join. Each mode can be thought of as a simple rank 2 spectrogram.
Another index is added, so that we have an "array of" these spectrograms
in a rank 3 dataset. This is the first index of the join data set:

```
jds.rank()  --> 3  # there are three indexes used to get to the data.
jds.length() --> 4  # three simple spectrograms, each in the same Time,Energy space
jds.property('JOIN_0')  --> 'Time'   # this just is any non-empty string. 
jds.slice(0) -->  dataset[120,27]    # 120 minutes, 27 energies
jds.slice(1) -->  dataset[300,101]   # 6 hours, 101 energies
jds.slice(2) -->  dataset[120,27]
jds.slice(3) -->  dataset[300,101]
jds.slice(0).property('DEPEND_0')  --> Time[120]
jds.slice(1).property('DEPEND_0')  --> Time[300]
jds.slice(0).property('DEPEND_1')  --> Energy[27]
```
A join dimension can be considered an "array of" dimension, so it could
be used to indicate when measurement cadence changes as well.

# More Properties

QDataSet is intended to represent everything fully-described science
data, to a simple array of numbers, to a simple scalar number. For this
reason, every property is optional. For example if the UNITS property is
missing, then the data is dimensionless. If the SCALE\_TYPE is missing,
then it is left to the software to infer which axis type should be used.

Here are a few more useful properties:

  - TITLE, a longer length description of the data, one line that could
    be used for a plot title.
  - LABEL, a short description of the data, which could be used for an
    axis label.
  - UNITS, a representation of the physical unit, or units representing
    time, or a unit identifying nominal data.
  - VALID\_MIN, the smallest value considered valid.
  - VALID\_MAX, the largest value considered valid.
  - TYPICAL\_MIN, nice setting for axis minimum.
  - TYPICAL\_MAX, nice setting for axis maximum.
  - SCALE\_TYPE, "log" or "linear"
  - CADENCE, a rank 0 dataset indicating the expected distance between
    measurements.
  - FORMAT, a string for formatting the data, such as '%9.2f' or '%d'

These are all dimension properties, meaning they describe data within
one dimension.

There are structural properties as well, which are the connections
between QDataSets. We've seen already:

  - DEPEND\_i, declare the dependence of the ith index on another
    dataset.
  - BUNDLE\_i, describe the data that are bundled together with the ith
    index.

And there are a few more:

  - DELTA\_PLUS, add this to the data to indicate the one-sigma error
    level.
  - DELTA\_MINUS, subtract this from the data to indicate the one-sigma
    error level.
  - BIN\_PLUS, add this to get the upper limit of the 100% confidence
    level (e.g. time tags).
  - BIN\_MINUS, subtract this to get the lower limit of the 100%
    confidence level (e.g. time tags).
  - BIN\_MAX, the upper limit of the 100% confidence level. (Use this
    instead of BIN\_PLUS.)
  - BIN\_MIN, the limit limit of the 100% confidence level. (Use this
    instead of BIN\_PLUS.)
  - BINS\_i, these are labels for each of the indices, typically
    BINS\_1='min,max' in ds\[n,2\]

Note that just because a property exists, a code might not be using the
property. For example, the total function should return a QDataSet with
the same units as its input, but it might not have implemented a check
for VALID\_MIN. The SeriesRenderer doesn't check for JOIN\_0, but this
would be a reasonable thing to expect. (And kudos to the fellow who goes
in and implements this\!)

# Operators and Scripting

Autoplot's Jython introduces many operators for QDataSets, providing an
environment similar to IDL and Matlab. Different from IDL and Matlab are
the properties and metadata that make Jython scripts more concise and
easier to verify. For example,

```
bgse= getDataSet( 'vap+cdf:http://autoplot.org/data/autoplot.cdf?BGSEc' )
bz= bgse[:,2]
bmag= getDataSet( 'http://autoplot.org/data/autoplot.cdf?Magnitude' )
plot( bz / bmag )
angle= toDegrees( acos( bz/bmag ) )
r= where( angle.lt( 15 ) )
```
bz/bmag is a dimensionless quantity with the label "(Bz GSE)/(\<|B|\>
(nT))", and is still has DEPEND\_0 equal to time.

## Rank Promotion

Note there is logic for reconciling two datasets with unequal rank. For
example, suppose we want to multiply each measurement by 10:

```
bgse= getDataSet( 'vap+cdf:http://autoplot.org/data/autoplot.cdf?BGSEc' )
bz= bgse[:,2] * 10
```
Here the 10 is converted to the rank 0 dataset, and then the rank 0
dataset is repeated to make a rank 1 dataset of the same geometry.

Note too that many operators will automatically convert data to
QDataSets. For example, you can say:

```
r= where( angle.lt('15 degrees') ) 
```
to make code more explicit. Note that if angle were in radians, that it
would have been converted to degrees automatically so that the two could
be compared, or an error would be thrown if the units could not be
converted.

# QDataSets are immutable, kinda

Ideally QDataSets are immutable, and a dataset can be read from but not
modified. However, implementations typically extend the interface so
that they can be modified and are more easily used in code where the
developer knows this is safe to do. For example, DDataSet is backed by a
double array, and it's convenient when implementing a result to just
start plugging the numbers in. Clients receive a QDataSet and generally
don't know that the dataset could actually be modified.

Here's the problem, though, jython provides mutability to its datasets
by making a mutable copy if the mutators are called. I need to check on
this, but my guess is that it cheats and just uses the data if it is
already mutable. The cost of making needless copies is memory.

Scott and folks at Iowa finally ran into the case where this was a
problem, as the reference cache was allowing its data to be mutated.

Fixing the problem would involve having (1) access control switches, and
(2) locking controls. For example, a dataset could be marked as
read-only, so no one could further modify it. Second, it would
interesting to allow for the common case where only one party will be
using a dataset, and it could get a lock and modify the data, perhaps
removing it from the cache...

Also it would be nice if datasets could be documented for optimizations.
For example, I have a code that is checking for the valid entries on a
dataset with fill. These are all valid timetags, but the performance
penalty is severe. For example:

```
 if ( 0==DataSetAnnotations.getInstance().getAnnotation(ds,DataSetAnnotations.ANNOTATION_INVALID_COUNT) { ... optimize ...}
```
An associated problem with this is that many of the operators have
inefficient implementations that are there to support mutations in
jython. For example, Ops.findgen(200000) actually returns a FDataSet
taking all the space.

