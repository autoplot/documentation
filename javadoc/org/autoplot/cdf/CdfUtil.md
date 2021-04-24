# org.autoplot.cdf.CdfUtil

static methods supporting CdfFileDataSource

# CdfUtil( )
Creates a new instance of CdfUtil

***
<a name="getDimensions"></a>
# getDimensions
getDimensions( gov.nasa.gsfc.spdf.cdfj.CDFReader cdf, String variableName ) &rarr; int

This is cdf.getDimensions( variableName ), but then check varies
 to see if varies[0] is false (for rvariables)

### Parameters:
cdf - a CDFReader
<br>variableName - a String

### Returns:
the dimensions for each record.

<a href="https://github.com/autoplot/dev/search?q=getDimensions&unscoped_q=getDimensions">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlottable"></a>
# getPlottable
getPlottable( gov.nasa.gsfc.spdf.cdfj.CDFReader cdf, boolean dataOnly, int rankLimit ) &rarr; Map

Return a map where keys are the names of the variables, and values are descriptions.

### Parameters:
cdf - the cdf reader reference.
<br>dataOnly - show only the DATA and not SUPPORT_DATA.  Note I reclaimed this parameter because I wasn't using it.
<br>rankLimit - show only variables with no more than this rank.

### Returns:
map of parameter name to short description

<a href="https://github.com/autoplot/dev/search?q=getPlottable&unscoped_q=getPlottable">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getPlottable( gov.nasa.gsfc.spdf.cdfj.CDFReader cdf, boolean dataOnly, int rankLimit, boolean deep, boolean master ) &rarr; Map<br>
***
<a name="getRange"></a>
# getRange
getRange( java.util.HashMap attrs ) &rarr; DatumRange

returns the range of the data by looking for the SCALEMIN/SCALEMAX params,
 or the required VALIDMIN/VALIDMAX parameters.  This is not used.

### Parameters:
attrs - the properties for the variable

### Returns:
the range

<a href="https://github.com/autoplot/dev/search?q=getRange&unscoped_q=getRange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getScaleType"></a>
# getScaleType
getScaleType( java.util.HashMap attrs ) &rarr; String



### Parameters:
attrs - a java.util.HashMap

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getScaleType&unscoped_q=getScaleType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getStringDataType"></a>
# getStringDataType
getStringDataType( int type ) &rarr; String

return the data type for the encoding.  From
 ftp://cdaweb.gsfc.nasa.gov/pub/cdf/doc/cdf33/cdf33ifd.pdf  page 33.

### Parameters:
type - integer type, such as 44 for CDF_FLOAT

### Returns:
string like "CDF_FLOAT"

<a href="https://github.com/autoplot/dev/search?q=getStringDataType&unscoped_q=getStringDataType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasAttribute"></a>
# hasAttribute
hasAttribute( gov.nasa.gsfc.spdf.cdfj.CDFReader cdf, String var, String attrname ) &rarr; boolean

return true if the attribute is set for the variable.

### Parameters:
cdf - the cdf file reader
<br>var - the variable name
<br>attrname - the attribute name.

### Returns:
true if the attribute is set for the variable.

<a href="https://github.com/autoplot/dev/search?q=hasAttribute&unscoped_q=hasAttribute">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="jvmMemory"></a>
# jvmMemory
jvmMemory( QDataSet ds ) &rarr; int

returns the amount of JVM memory in bytes occupied by the dataset. This is an approximation,
 calculated by taking the element type size (e.g. float=4 bytes) times the number of elements for
 the dataset.  This does not include the memory consumed by DEPEND_0, etc.

### Parameters:
ds - the ArrayDataSet, or TrArrayDataSet, or BufferDataSet.

### Returns:
the approximate memory consumption in bytes

<a href="https://github.com/autoplot/dev/search?q=jvmMemory&unscoped_q=jvmMemory">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="loadVariable"></a>
# loadVariable
loadVariable( gov.nasa.gsfc.spdf.cdfj.CDFReader cdf, String svariable ) &rarr; MutablePropertyDataSet

Return the named variable as a QDataSet.  This does not look at the
 metadata for DEPEND_0, etc, and only adds metadata to represent time units
 (e.g. the data is in TT2000) and ordinal data.

### Parameters:
cdf - the value of CDF
<br>svariable - name of the variable

### Returns:
the dataset

<a href="https://github.com/autoplot/dev/search?q=loadVariable&unscoped_q=loadVariable">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

loadVariable( gov.nasa.gsfc.spdf.cdfj.CDFReader cdf, String svariable, long recStart, long recCount, long recInterval, int slice1, ProgressMonitor mon ) &rarr; MutablePropertyDataSet<br>
***
<a name="maybeAddValidRange"></a>
# maybeAddValidRange
maybeAddValidRange( java.util.Map props, org.das2.qds.MutablePropertyDataSet ds ) &rarr; void

add the valid range only if it looks like it is correct.  It must contain some of the data.

### Parameters:
props - the properties for the variable
<br>ds - the dataset to which the valid range would be added.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=maybeAddValidRange&unscoped_q=maybeAddValidRange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="maybeShorten"></a>
# maybeShorten
maybeShorten( String context, String name ) &rarr; String

abbreviate names, motivated by Cluster CDF files which have 
 Data__C1_CP_PEA_3DRH_cnts with DEPEND_0 of
 time_tags__C1_CP_PEA_3DRH_cnts.

### Parameters:
context - a String
<br>name - a String

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=maybeShorten&unscoped_q=maybeShorten">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="wrapCdfData"></a>
# <del>wrapCdfData</del>
Deprecated: use loadCdfVariable instead
wrapCdfData( gov.nasa.gsfc.spdf.cdfj.CDFReader cdf, String svariable, long recStart, long recCount, long recInterval, int slice1, boolean depend, ProgressMonitor mon ) &rarr; MutablePropertyDataSet<br>
