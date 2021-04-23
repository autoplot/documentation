# org.autoplot.cdf.CdfVirtualVarsImplementations of the CDF virtual variables seen in CDAWeb, but implemented in QDataSet.
 These should reflect a subset of those functions, with the IDL implementations at
 http://spdf.gsfc.nasa.gov/CDAWlib.html
 see ftp://cdaweb.gsfc.nasa.gov/pub/CDAWlib/unix/CDAWlib.tar.gz, routine read_myCDF.pro
CdfVirtualVars( )


***
<a name="convPos"></a>
# convPos
convPos( java.util.List args, String coordSys ) &rarr; QDataSet



### Parameters:
args - a java.util.List
<br>coordSys - a String

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=convPos&unscoped_q=convPos">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="execute"></a>
# execute
execute( java.util.Map metadata, String function, java.util.List args, ProgressMonitor mon ) &rarr; QDataSet

Implementations of CDF virtual functions.  These are a subset of those in the CDAWeb library, plus a couple
 extra that they will presumably add to the library at some point.

### Parameters:
metadata - the metadata for the new result dataset, CDF semantics such as FILLVAL=-1e31
<br>function - the function name, which is case insensitive.  See code isSupported for list of function names.
<br>args - list of QDataSets that are the arguments to the function
<br>mon - monitor for the function

### Returns:
the computed variable.
### See Also:
<a href='#isSupported'>isSupported(java.lang.String)</a> <br>
<a href='https://spdf.gsfc.nasa.gov/istp_guide/vattributes.html'>https://spdf.gsfc.nasa.gov/istp_guide/vattributes.html</a> <br>

<a href="https://github.com/autoplot/dev/search?q=execute&unscoped_q=execute">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isSupported"></a>
# isSupported
isSupported( String function ) &rarr; boolean

return true if the function is supported.

### Parameters:
function - the function name, such as "compute_magnitude"

### Returns:
true if the function is supported.

<a href="https://github.com/autoplot/dev/search?q=isSupported&unscoped_q=isSupported">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

