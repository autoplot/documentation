# org.das2.dataset.DataSetGeneral interface for objects encapsulating a data set
***
<a name="PROPERTY_CACHE_TAG"></a>
# PROPERTY_CACHE_TAG

CacheTag object describing the start, end, and resolution of the dataset.

***
<a name="PROPERTY_X_CACHE_RNG"></a>
# PROPERTY_X_CACHE_RNG

DatumRange describing the range of a dataset in the X dimension

***
<a name="PROPERTY_X_CACHE_RES"></a>
# PROPERTY_X_CACHE_RES

Datum providing the resolution in the X dimension

***
<a name="PROPERTY_Y_CACHE_RNG"></a>
# PROPERTY_Y_CACHE_RNG

DatumRange describing the range of a dataset in the X dimension

***
<a name="PROPERTY_Y_CACHE_RES"></a>
# PROPERTY_Y_CACHE_RES

Datum providing the resolution in the X dimension

***
<a name="PROPERTY_SIZE_BYTES"></a>
# PROPERTY_SIZE_BYTES

Long estimating the size of the dataset in memory.  For example, if a dataset is
 backed by a local file, then zero for this indicates no penalty for storing this
 dataset.

***
<a name="PROPERTY_X_TAG_WIDTH"></a>
# PROPERTY_X_TAG_WIDTH

Datum which is the nominal distance between successive xTags.  This is used for example to prevent
 interpolation between distant measurements

***
<a name="PROPERTY_Y_TAG_WIDTH"></a>
# PROPERTY_Y_TAG_WIDTH

Datum, see xTagWidth

***
<a name="PROPERTY_X_RANGE"></a>
# PROPERTY_X_RANGE

DatumRange useful for setting scales

***
<a name="PROPERTY_X_VALID_MIN"></a>
# PROPERTY_X_VALID_MIN

Double, used to indicate minimum valid X value

***
<a name="PROPERTY_X_VALID_MAX"></a>
# PROPERTY_X_VALID_MAX

Double, used to indicate maximum valid X value

***
<a name="PROPERTY_Y_RANGE"></a>
# PROPERTY_Y_RANGE

Datum, useful for setting scales

***
<a name="PROPERTY_Y_VALID_MIN"></a>
# PROPERTY_Y_VALID_MIN

Double, used to indicate minimum valid X value

***
<a name="PROPERTY_Y_VALID_MAX"></a>
# PROPERTY_Y_VALID_MAX

Double, used to indicate maximum valid X value

***
<a name="PROPERTY_Z_RANGE"></a>
# PROPERTY_Z_RANGE

DatumRange useful for setting scales

***
<a name="PROPERTY_Z_VALID_MIN"></a>
# PROPERTY_Z_VALID_MIN

Double, used to indicate minimum valid X value

***
<a name="PROPERTY_Z_VALID_MAX"></a>
# PROPERTY_Z_VALID_MAX

Double, used to indicate maximum valid X value

***
<a name="PROPERTY_Y_FILL"></a>
# PROPERTY_Y_FILL

Double: Raw value used to indicate fill data.

***
<a name="PROPERTY_Z_FILL"></a>
# PROPERTY_Z_FILL

Raw value used to indicate fill data.
 Since yscan's are rectangular it's handy to have a fill value to indicate
 gaps in the rectangle

***
<a name="PROPERTY_RENDERER"></a>
# PROPERTY_RENDERER

suggest render method to use.  These are 
 canonical:
    spectrogram
    symbolLine
    stackedHistogram

***
<a name="PROPERTY_Y_SCALETYPE"></a>
# PROPERTY_Y_SCALETYPE

String "log" or "linear"

***
<a name="PROPERTY_Z_SCALETYPE"></a>
# PROPERTY_Z_SCALETYPE

String "log" or "linear"

***
<a name="PROPERTY_X_LABEL"></a>
# PROPERTY_X_LABEL



***
<a name="PROPERTY_Y_LABEL"></a>
# PROPERTY_Y_LABEL



***
<a name="PROPERTY_Z_LABEL"></a>
# PROPERTY_Z_LABEL



***
<a name="PROPERTY_X_SUMMARY"></a>
# PROPERTY_X_SUMMARY

A brief description of the x direction values

***
<a name="PROPERTY_Y_SUMMARY"></a>
# PROPERTY_Y_SUMMARY

A brief description of the y direction values

***
<a name="PROPERTY_Z_SUMMARY"></a>
# PROPERTY_Z_SUMMARY

A brief description of the z direction values

***
<a name="PROPERTY_SUMMARY"></a>
# PROPERTY_SUMMARY

A brief description for the entire stream

***
<a name="PROPERTY_X_FORMAT"></a>
# PROPERTY_X_FORMAT

The format for printing X, Y and Z items, see the Das 2.2.2 (or higher) ICD 
 for a list of valid foramt strings

***
<a name="PROPERTY_Y_FORMAT"></a>
# PROPERTY_Y_FORMAT



***
<a name="PROPERTY_Z_FORMAT"></a>
# PROPERTY_Z_FORMAT



***
<a name="PROPERTY_TITLE"></a>
# PROPERTY_TITLE

finally, this data model is done with the addition of title.

***
<a name="PROPERTY_X_MONOTONIC"></a>
# PROPERTY_X_MONOTONIC

Boolean assuring that the dataset is monotonic in X.  This allows 
 some optimizations to be made.

***
<a name="PROPERTY_Y_MONOTONIC"></a>
# PROPERTY_Y_MONOTONIC

Boolean assuring that the dataset is monotonic in Y.  This allows 
 some optimizations to be made.

***
<a name="PROPERTY_PLANE_PEAKS"></a>
# PROPERTY_PLANE_PEAKS

dataset containing the peaks when available

***
<a name="PROPERTY_SOURCE"></a>
# PROPERTY_SOURCE

Indicator that dataset is not intrinsic but was derived from some other dataset

***
<a name="PROPERTY_OPERATION"></a>
# PROPERTY_OPERATION

Indicator of which operation was performed on the input source

***
<a name="PROPERTY_PLANE_WEIGHTS"></a>
# PROPERTY_PLANE_WEIGHTS

dataset containing the weights when available

***
<a name="PROPERTY_FORMATTER"></a>
# PROPERTY_FORMATTER

DatumFormatter for formatting data in the dataset.

***
<a name="getPlanarView"></a>
# getPlanarView
getPlanarView( String planeID ) &rarr; DataSet

Returns a <code>DataSet</code> with the specified view as the primary
 view.

### Parameters:
planeID - the <code>String</code> id of the requested plane.

### Returns:
the specified view, as a <code>DataSet</code>

<a href="https://github.com/autoplot/dev/search?q=getPlanarView&unscoped_q=getPlanarView">[search for examples]</a>

***
<a name="getPlaneIds"></a>
# getPlaneIds
getPlaneIds(  ) &rarr; String

Returns a list of auxiliary planes (e.g. weights, peaks) for the dataset.
 Note that the default plane, "" may or may not be returned, based on
 implementations.

### Returns:
java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=getPlaneIds&unscoped_q=getPlaneIds">[search for examples]</a>

***
<a name="getProperties"></a>
# getProperties
getProperties(  ) &rarr; Map

Returns all dataset properties in a Map.

### Returns:
a Map of all properties.

<a href="https://github.com/autoplot/dev/search?q=getProperties&unscoped_q=getProperties">[search for examples]</a>

***
<a name="getProperty"></a>
# getProperty
getProperty( String name ) &rarr; Object

Returns the property value associated with the string <code>name</code>

### Parameters:
name - the name of the property requested

### Returns:
the property value for <code>name</code> or null

<a href="https://github.com/autoplot/dev/search?q=getProperty&unscoped_q=getProperty">[search for examples]</a>

***
<a name="getXLength"></a>
# getXLength
getXLength(  ) &rarr; int

Returns the number of x tags in this data set.  XTags must be
      monotonically increasing with i.

### Returns:
the number of x tags in this data set.

<a href="https://github.com/autoplot/dev/search?q=getXLength&unscoped_q=getXLength">[search for examples]</a>

***
<a name="getXTagDatum"></a>
# getXTagDatum
getXTagDatum( int i ) &rarr; Datum

Returns the value of the x tag at the given index i as a
      <code>Datum</code>.

### Parameters:
i - the index of the requested x tag

### Returns:
the value of the x tag at the given index i as a
      <code>Datum</code>.

<a href="https://github.com/autoplot/dev/search?q=getXTagDatum&unscoped_q=getXTagDatum">[search for examples]</a>

***
<a name="getXTagDouble"></a>
# getXTagDouble
getXTagDouble( int i, Units units ) &rarr; double

Returns the value of the x tag at the given index i as a
      <code>double</code> in the given units.  XTags must be
      monotonically increasing with i.

### Parameters:
i - the index of the requested x tag
<br>units - the units of the returned value

### Returns:
the value of the x tag at the given index i as a
      <code>double</code>.

<a href="https://github.com/autoplot/dev/search?q=getXTagDouble&unscoped_q=getXTagDouble">[search for examples]</a>

***
<a name="getXTagInt"></a>
# getXTagInt
getXTagInt( int i, Units units ) &rarr; int

Returns the value of the x tag at the given index i as an
      <code>int</code> in the given units.  XTags must be
      monotonically increasing with i.

### Parameters:
i - the index of the requested x tag
<br>units - the units of the returned value.

### Returns:
the value of the x tag at the given index i as an
      <code>int</code>.

<a href="https://github.com/autoplot/dev/search?q=getXTagInt&unscoped_q=getXTagInt">[search for examples]</a>

***
<a name="getXUnits"></a>
# getXUnits
getXUnits(  ) &rarr; Units

Returns the Units object representing the unit type of the x tags
 for this data set.

### Returns:
the x units

<a href="https://github.com/autoplot/dev/search?q=getXUnits&unscoped_q=getXUnits">[search for examples]</a>

***
<a name="getYUnits"></a>
# getYUnits
getYUnits(  ) &rarr; Units

Returns the Units object representing the unit type of the y tags
 or y values for this data set.

### Returns:
the y units

<a href="https://github.com/autoplot/dev/search?q=getYUnits&unscoped_q=getYUnits">[search for examples]</a>

