# org.autoplot.idlsupport.QDataSetBridgeSee http://autoplot.org/IDL and http://autoplot.org/Matlab which show how this is used in the environments.
***
<a name="PROP_FILTER"></a>
# PROP_FILTER



***
<a name="clearFillValue"></a>
# clearFillValue
clearFillValue(  ) &rarr; void

don't use fill value.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=clearFillValue&unscoped_q=clearFillValue">[search for examples]</a>

***
<a name="clearMemory"></a>
# clearMemory
clearMemory(  ) &rarr; void

clear existing data from memory, in case the bridge object is not cleared
 from in IDL or Matlab memory.

### Returns:
void (returns nothing)

### See Also:
<a href='#reportMemory'>reportMemory()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=clearMemory&unscoped_q=clearMemory">[search for examples]</a>

***
<a name="clearPreferredUnits"></a>
# clearPreferredUnits
clearPreferredUnits(  ) &rarr; void

clear any preference for units.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=clearPreferredUnits&unscoped_q=clearPreferredUnits">[search for examples]</a>

***
<a name="depend"></a>
# depend
depend( int dim ) &rarr; String



### Parameters:
dim - an int

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=depend&unscoped_q=depend">[search for examples]</a>

***
<a name="doGetDataSet"></a>
# doGetDataSet
doGetDataSet(  ) &rarr; void

performs the read.  Note no progress status is available and this blocks until the read is done.
 doGetDataSet(mon) should be called if progress is needed.
 2011-01-01: getStatus or getStatusMessage should be called afterwards to check the result of the load, this will no longer throw an exception.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=doGetDataSet&unscoped_q=doGetDataSet">[search for examples]</a>

doGetDataSet( ProgressMonitor mon ) &rarr; void<br>
***
<a name="dumpStack"></a>
# dumpStack
dumpStack(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dumpStack&unscoped_q=dumpStack">[search for examples]</a>

***
<a name="dumpStackInNSeconds"></a>
# dumpStackInNSeconds
dumpStackInNSeconds( double n ) &rarr; void

desperate method for debugging where JPype/Python would hang, in hopes that
 this might show where it's hanging.

### Parameters:
n - number of seconds.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dumpStackInNSeconds&unscoped_q=dumpStackInNSeconds">[search for examples]</a>

***
<a name="freeMemory"></a>
# freeMemory
freeMemory(  ) &rarr; int

return the total memory and free memory available to the Java process,
 in megabytes (1e6 bytes).

### Returns:
an integer array [ used, total ]

<a href="https://github.com/autoplot/dev/search?q=freeMemory&unscoped_q=freeMemory">[search for examples]</a>

***
<a name="getException"></a>
# getException
getException(  ) &rarr; Exception

return the Exception from the last doGetDataSet call.

### Returns:
a java.lang.Exception


<a href="https://github.com/autoplot/dev/search?q=getException&unscoped_q=getException">[search for examples]</a>

***
<a name="getFilter"></a>
# getFilter
getFilter(  ) &rarr; String

get the filter that is applied to the data immediately after it is loaded.

### Returns:
the filter string, empty string means no filters.

<a href="https://github.com/autoplot/dev/search?q=getFilter&unscoped_q=getFilter">[search for examples]</a>

***
<a name="getProgressMonitor"></a>
# getProgressMonitor
getProgressMonitor(  ) &rarr; ProgressMonitor

returns an object that can be used to monitor the progress of a download.
 
 mon= qds->getProgressMonitor();
 qds->doGetDataSet( mon )
 while ( ! mon->isFinished() ) do begin
    print, strtrim( mon->getTaskProgress(), 2 ) + "  " + strtrim( mon->getTaskSize(), 2 )
    wait, 0.2   ; don't overload the thread
 endwhile

### Returns:
a ProgressMonitor


<a href="https://github.com/autoplot/dev/search?q=getProgressMonitor&unscoped_q=getProgressMonitor">[search for examples]</a>

***
<a name="getStatus"></a>
# getStatus
getStatus(  ) &rarr; int

returns 0 for last get operation successful

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=getStatus&unscoped_q=getStatus">[search for examples]</a>

***
<a name="getStatusMessage"></a>
# getStatusMessage
getStatusMessage(  ) &rarr; String

returns "" for last operation successful, or non-empty indicating the problem.  Note
 getException will return the Java exception for deeper inspection.

### Returns:
"" or the error message

<a href="https://github.com/autoplot/dev/search?q=getStatusMessage&unscoped_q=getStatusMessage">[search for examples]</a>

***
<a name="hasProperty"></a>
# hasProperty
hasProperty( String name, String propname, int i ) &rarr; boolean



### Parameters:
name - a String
<br>propname - a String
<br>i - an int

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=hasProperty&unscoped_q=hasProperty">[search for examples]</a>

hasProperty( String name, String propname ) &rarr; boolean<br>
hasProperty( String propname ) &rarr; boolean<br>
hasProperty( String propname, int i ) &rarr; boolean<br>
***
<a name="isQube"></a>
# isQube
isQube(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isQube&unscoped_q=isQube">[search for examples]</a>

***
<a name="labelsAlias"></a>
# labelsAlias
labelsAlias( String name, java.lang.String[] result ) &rarr; void

get the string values of the data instead of the numbers.  This provides
 a means to decode times and nominal data such as labels data sets.

### Parameters:
name - a String
<br>result - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=labelsAlias&unscoped_q=labelsAlias">[search for examples]</a>

***
<a name="length"></a>
# length
length( String name ) &rarr; int

return the length of the zeroth dimension of the dataset

### Parameters:
name - a String

### Returns:
the length of the zeroth dimension

<a href="https://github.com/autoplot/dev/search?q=length&unscoped_q=length">[search for examples]</a>

length(  ) &rarr; int<br>
***
<a name="lengths"></a>
# lengths
lengths( String name ) &rarr; int

return the lengths of the dimensions of the specified dataset.

### Parameters:
name - a String

### Returns:
an int[]


<a href="https://github.com/autoplot/dev/search?q=lengths&unscoped_q=lengths">[search for examples]</a>

lengths(  ) &rarr; int<br>
lengths( String name, int i ) &rarr; int<br>
lengths( int i ) &rarr; int<br>
***
<a name="name"></a>
# name
name(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=name&unscoped_q=name">[search for examples]</a>

***
<a name="nameFor"></a>
# nameFor
nameFor( QDataSet dep0 ) &rarr; String

return the name used to refer to the dataset.  
 This may add to the list of datasets.

### Parameters:
dep0 - the dataset

### Returns:
the name for the dataset.

<a href="https://github.com/autoplot/dev/search?q=nameFor&unscoped_q=nameFor">[search for examples]</a>

***
<a name="names"></a>
# names
names(  ) &rarr; String



### Returns:
java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=names&unscoped_q=names">[search for examples]</a>

***
<a name="plane"></a>
# plane
plane( int iplane ) &rarr; String



### Parameters:
iplane - an int

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=plane&unscoped_q=plane">[search for examples]</a>

***
<a name="properties"></a>
# properties
properties( String name, int i ) &rarr; Map

get the properties for the named dataset

### Parameters:
name - a String
<br>i - the index

### Returns:
a java.util.Map


<a href="https://github.com/autoplot/dev/search?q=properties&unscoped_q=properties">[search for examples]</a>

properties( String name ) &rarr; Map<br>
properties(  ) &rarr; Map<br>
properties( int i ) &rarr; Map<br>
***
<a name="property"></a>
# property
property( String name, String propname, int i ) &rarr; Object

returns one of String, int, double, float, int[], double, float[]

### Parameters:
name - a String
<br>propname - a String
<br>i - an int

### Returns:
the property

<a href="https://github.com/autoplot/dev/search?q=property&unscoped_q=property">[search for examples]</a>

property( String name, String propname ) &rarr; Object<br>
property( String propname ) &rarr; Object<br>
property( String propname, int i ) &rarr; Object<br>
***
<a name="propertyAsDouble"></a>
# propertyAsDouble
propertyAsDouble( String property ) &rarr; double



### Parameters:
property - a String

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=propertyAsDouble&unscoped_q=propertyAsDouble">[search for examples]</a>

propertyAsDouble( String name, String property ) &rarr; double<br>
***
<a name="propertyAsString"></a>
# propertyAsString
propertyAsString( String property ) &rarr; String

return the default dataset property value as a string.

### Parameters:
property - property name

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=propertyAsString&unscoped_q=propertyAsString">[search for examples]</a>

propertyAsString( String name, String property ) &rarr; String<br>
***
<a name="rank"></a>
# rank
rank( String name ) &rarr; int

return the number of dimensions of the specified dataset.

### Parameters:
name - a String

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=rank&unscoped_q=rank">[search for examples]</a>

rank(  ) &rarr; int<br>
***
<a name="readLogConfiguration"></a>
# readLogConfiguration
readLogConfiguration(  ) &rarr; void

load the configuration from autoplot_data/config/logging.properties

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=readLogConfiguration&unscoped_q=readLogConfiguration">[search for examples]</a>

***
<a name="reportMemory"></a>
# reportMemory
reportMemory(  ) &rarr; void

print the Java memory stats to stderr.

### Returns:
void (returns nothing)

### See Also:
<a href='#clearMemory'>clearMemory()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=reportMemory&unscoped_q=reportMemory">[search for examples]</a>

***
<a name="setDebug"></a>
# setDebug
setDebug( boolean debug ) &rarr; void

turn on/off debug messages

### Parameters:
debug - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDebug&unscoped_q=setDebug">[search for examples]</a>

***
<a name="setFillDouble"></a>
# setFillDouble
setFillDouble( double d ) &rarr; void

set the value to return when the data is invalid, when the data is known to be stored as doubles
 (8-byte numbers).  Python JPype doesn't allow for operator overloading, so this should be used.

### Parameters:
d - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFillDouble&unscoped_q=setFillDouble">[search for examples]</a>

***
<a name="setFillValue"></a>
# setFillValue
setFillValue( double d ) &rarr; void

set the value to return when the data is invalid.  Note in IDL, where I echoed which was being called:
 IDL> apds.setFillValue, 89.
 % setFillValue(float)
 IDL> apds.setFillValue, 89.d
 % setFillValue(double)

### Parameters:
d - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFillValue&unscoped_q=setFillValue">[search for examples]</a>

setFillValue( float f ) &rarr; void<br>
***
<a name="setFilter"></a>
# setFilter
setFilter( String filter ) &rarr; void

set the filter that is applied to the data immediately after it is loaded.

### Parameters:
filter - filter string like "|histogram()" or "" for no filters.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFilter&unscoped_q=setFilter">[search for examples]</a>

***
<a name="setPreferredUnits"></a>
# setPreferredUnits
setPreferredUnits( String sunit ) &rarr; void

set the preferred units for the data.  The code will convert
 to these units when a converter is found.
 If a preference is indicated when it is convertible to an existing
 preference, the existing preference is removed.
 See clearPreferredUnits to remove all preferences.
 Example units strings (capitalization matters):
<blockquote><pre><small>
    seconds since 2010-01-01T00:00
    days since 2010-01-01T00:00
    Hz
    kHz
    MHz
</small></pre></blockquote>

### Parameters:
sunit - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPreferredUnits&unscoped_q=setPreferredUnits">[search for examples]</a>

***
<a name="slice"></a>
# slice
slice( String name, int i, double[] result ) &rarr; void

accessor for non-qube

### Parameters:
name - a String
<br>i - an int
<br>result - a double[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=slice&unscoped_q=slice">[search for examples]</a>

slice( String name, int i, double[][] result ) &rarr; void<br>
slice( String name, int i, double[][][] result ) &rarr; void<br>
slice( int i, double[] result ) &rarr; void<br>
slice( int i, double[][] result ) &rarr; void<br>
slice( int i, double[][][] result ) &rarr; void<br>
slice( String name, int i ) &rarr; Object<br>
slice( int i0 ) &rarr; Object<br>
***
<a name="slice1"></a>
# slice1
slice1( int index ) &rarr; Object

slice on the first dimension, which is useful for extracting 
 data component by component.

### Parameters:
index - an int

### Returns:
array of floats or doubles.

<a href="https://github.com/autoplot/dev/search?q=slice1&unscoped_q=slice1">[search for examples]</a>

slice1( int index, String name ) &rarr; Object<br>
***
<a name="svalues"></a>
# svalues
svalues( String name, java.lang.String[] result ) &rarr; void



### Parameters:
name - a String
<br>result - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=svalues&unscoped_q=svalues">[search for examples]</a>

svalues( java.lang.String[] result ) &rarr; void<br>
svalues(  ) &rarr; String<br>
svalues( String name ) &rarr; String<br>
***
<a name="values"></a>
# values
values( String name, double[] result ) &rarr; void



### Parameters:
name - a String
<br>result - a double[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=values&unscoped_q=values">[search for examples]</a>

values( String name, double[][] result ) &rarr; void<br>
values( String name, double[][][] result ) &rarr; void<br>
values( String name, double[][][][] result ) &rarr; void<br>
values( double[] result ) &rarr; void<br>
values( double[][] result ) &rarr; void<br>
values( double[][][] result ) &rarr; void<br>
values( double[][][][] result ) &rarr; void<br>
values(  ) &rarr; Object<br>
values( String name ) &rarr; Object<br>
***
<a name="valuesAlias"></a>
# valuesAlias
valuesAlias( String name, double[] result ) &rarr; void

copy the data into a 1-D array.  Rank 2 and 3 dataset array are then
 aliased with the highest dimension the most tightly packed.

### Parameters:
name - a String
<br>result - a double[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=valuesAlias&unscoped_q=valuesAlias">[search for examples]</a>

