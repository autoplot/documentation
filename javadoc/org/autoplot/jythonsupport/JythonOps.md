# org.autoplot.jythonsupport.JythonOpsContains operations that are only available to Jython code, and is dependent
 on the jython libraries.
JythonOps( )


***
<a name="addToSearchPath"></a>
# addToSearchPath
addToSearchPath( PyList syspath, String path, ProgressMonitor mon ) &rarr; String

download the jar file resource, unpack it, and add it to the search path.  Note
 such scripts will not work with Webstart releases!  The code is only
 loaded once per session, so Autoplot must be restarted if the library is updated.

 Here is an example use:
 <blockquote><pre><small>
import sys
addToSearchPath( sys.path, 'http://www-us.apache.org/dist//commons/math/binaries/commons-math3-3.6.1-bin.zip/commons-math3-3.6.1/commons-math3-3.6.1.jar', monitor )
from org.apache.commons.math3.distribution import BetaDistribution
beta= BetaDistribution(2,5)

xx= linspace(0,1.0,100)
yy= zeros(100)
for i in indgen(100):
    yy[i]= beta.density(xx[i].value())
#yy= map( xx, beta.density )
plot( xx, yy )
</small></pre></blockquote>

### Parameters:
syspath - the list of folders to search, should be sys.path.
<br>path - the path to add, which should be a jar file, possibly contained within a zip on an http site.
<br>mon - monitor for the download.

### Returns:
the name of the folder or jar file added.
### See Also:
<a href='https://sourceforge.net/p/autoplot/feature-requests/584/, which shows example use.'>https://sourceforge.net/p/autoplot/feature-requests/584/, which shows example use.</a> <br>

<a href="https://github.com/autoplot/dev/search?q=addToSearchPath&unscoped_q=addToSearchPath">[search for examples]</a>

addToSearchPath( PyList syspath, String path, String docPath, ProgressMonitor mon ) &rarr; String<br>
***
<a name="applyLambda"></a>
# applyLambda
applyLambda( QDataSet ds, PyFunction f ) &rarr; QDataSet



### Parameters:
ds - a QDataSet
<br>f - a PyFunction

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=applyLambda&unscoped_q=applyLambda">[search for examples]</a>

applyLambda( QDataSet ds1, QDataSet ds2, PyFunction f ) &rarr; QDataSet<br>
applyLambda( QDataSet ds1, QDataSet ds2, QDataSet ds3, PyFunction f ) &rarr; QDataSet<br>
***
<a name="coerceToDs"></a>
# <del>coerceToDs</del>
Deprecated: use dataset command.
***
<a name="color"></a>
# color
color( PyObject val ) &rarr; Color

get the color from the python object, for example:
 <ul>
 <li>Color.RED
 <li>16711680   (int for red)
 <li>16711680.  (float from QDataSet)
 <li>(255,0,0)
 <li>(1.0,0,0)
 </ul>

### Parameters:
val - the value

### Returns:
java.awt.Color

<a href="https://github.com/autoplot/dev/search?q=color&unscoped_q=color">[search for examples]</a>

***
<a name="currentLine"></a>
# currentLine
currentLine(  ) &rarr; String

return the current line in the Jython script as &lt;filename&gt;:&lt;linenum&gt;
 or ??? if this cannot be done.  Note calls to this will collect a stack
 trace and will affect performance.

### Returns:
the current line or ???
### See Also:
<a href='QubeDataSetIterator.md#currentJythonLine'>QubeDataSetIterator#currentJythonLine()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=currentLine&unscoped_q=currentLine">[search for examples]</a>

***
<a name="dataset"></a>
# dataset
dataset( PyObject arg0 ) &rarr; QDataSet

coerce a python array or list into a QDataSet.

### Parameters:
arg0 - Python object or Datum

### Returns:
QDataSet
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/ops/Ops.md#dataset'>org.das2.qds.ops.Ops#dataset(java.lang.Object)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=dataset&unscoped_q=dataset">[search for examples]</a>

dataset( PyObject arg0, Units u ) &rarr; QDataSet<br>
***
<a name="datum"></a>
# datum
datum( PyObject arg0 ) &rarr; Datum

coerce python objects to Datum

### Parameters:
arg0 - Python object, one of rank 0 dataset, int, float, or String.

### Returns:
Datum
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/ops/Ops.md#datum'>org.das2.qds.ops.Ops#datum(java.lang.Object)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=datum&unscoped_q=datum">[search for examples]</a>

***
<a name="datumRange"></a>
# datumRange
datumRange( PyObject arg0 ) &rarr; DatumRange

coerce python objects to DatumRange
 See http://jfaden.net:8080/hudson/job/autoplot-test029/
 This supports:<ul>
   <li>2-element rank 1 QDataSet
   <li>Strings like ("5 to 15 s" or "2014-01-01")
   <li>2-element arrays and lists
 </ul>

### Parameters:
arg0 - PyQDataSet, String, array or List.

### Returns:
DatumRange

<a href="https://github.com/autoplot/dev/search?q=datumRange&unscoped_q=datumRange">[search for examples]</a>

datumRange( PyObject arg0, PyObject arg1 ) &rarr; DatumRange<br>
datumRange( PyObject arg0, Units context ) &rarr; DatumRange<br>
***
<a name="findJavaPathRoots"></a>
# findJavaPathRoots
findJavaPathRoots( org.das2.util.filesystem.FileSystem destDir ) &rarr; List

search the folder for the names of packages.  This could trivially
 return "edu", but instead navigate to find a more precise name, or names.

### Parameters:
destDir - a FileSystem

### Returns:
list of packages.

<a href="https://github.com/autoplot/dev/search?q=findJavaPathRoots&unscoped_q=findJavaPathRoots">[search for examples]</a>

***
<a name="formUri"></a>
# formUri
formUri( String vapScheme, String resourceUri, Object args ) &rarr; String

convenience method for creating URIs.

### Parameters:
vapScheme - null or the data source scheme, such as "vap+das2server" or "vap+cdaweb"
<br>resourceUri - null or the resource uri, such as "http://www-pw.physics.uiowa.edu/das/das2Server"
<br>args - null or a map/dictionary of arguments, including "arg_0" for a positional argument.

### Returns:
the URI.  If vapScheme is null, then the URI will be implicit.

<a href="https://github.com/autoplot/dev/search?q=formUri&unscoped_q=formUri">[search for examples]</a>

***
<a name="invokeSometime"></a>
# invokeSometime
invokeSometime( PyObject func ) &rarr; void

run the function on a different thread

### Parameters:
func - a jython callable.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=invokeSometime&unscoped_q=invokeSometime">[search for examples]</a>

invokeSometime( PyObject func, PyObject arg ) &rarr; void<br>
***
<a name="putProperty"></a>
# putProperty
putProperty( QDataSet ds, String name, Object value ) &rarr; MutablePropertyDataSet

converts types often seen in Jython codes to the correct type.  For
 example, ds= putProperty( ds, 'UNITS', 'seconds since 2012-01-01').

### Parameters:
ds - a QDataSet
<br>name - a String
<br>value - an Object

### Returns:
the dataset, possibly converted to a mutable dataset.

<a href="https://github.com/autoplot/dev/search?q=putProperty&unscoped_q=putProperty">[search for examples]</a>

