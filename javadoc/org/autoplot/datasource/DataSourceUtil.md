# org.autoplot.datasource.DataSourceUtilDataSource utilities.
***
<a name="DEFAULT_TIME_RANGE"></a>
# DEFAULT_TIME_RANGE

used in Autoplot's Application object and in the DataSetSelector.

***
<a name="addMakeAggregationForScheme"></a>
# addMakeAggregationForScheme
addMakeAggregationForScheme( String scheme, org.autoplot.datasource.DataSourceUtil.URIMap map ) &rarr; void

register a map which might modify a URI so that it uses aggregation. 
 This was introduced for "vap+inline" URIs which must be taken apart and
 then each of the getDataSet calls is aggregated.

### Parameters:
scheme - the scheme where this should be used, e.g. "vap+inline"
<br>map - the map, which might return the input URI or an aggregated one.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addMakeAggregationForScheme&unscoped_q=addMakeAggregationForScheme">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="findAggregations"></a>
# findAggregations
findAggregations( java.util.List files, boolean remove ) &rarr; List



### Parameters:
files - a java.util.List
<br>remove - a boolean

### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=findAggregations&unscoped_q=findAggregations">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

findAggregations( java.util.List files, boolean remove, boolean loose ) &rarr; List<br>
***
<a name="getMessage"></a>
# getMessage
getMessage( java.lang.Exception ex ) &rarr; String

return a one-line string representation of the exception.  This was introduced
 when a NullPointerException was represented as "null", and it was somewhat
 unclear about what was going on.

### Parameters:
ex - an exception

### Returns:
a 1-line string representation of the error, for the end user.

<a href="https://github.com/autoplot/dev/search?q=getMessage&unscoped_q=getMessage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTimeSeriesBrowse"></a>
# getTimeSeriesBrowse
getTimeSeriesBrowse( org.autoplot.datasource.DataSource dss ) &rarr; TimeSeriesBrowse

for IDL, where I can't look up a class

### Parameters:
dss - a DataSource

### Returns:
an org.autoplot.datasource.capability.TimeSeriesBrowse


<a href="https://github.com/autoplot/dev/search?q=getTimeSeriesBrowse&unscoped_q=getTimeSeriesBrowse">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getXPathFactory"></a>
# getXPathFactory
getXPathFactory(  ) &rarr; XPathFactory

Matlab uses net.sf.saxon.xpath.XPathEvaluator by default, so we explicitly look for the Java 6 one.

### Returns:
com.sun.org.apache.xpath.internal.jaxp.XPathFactoryImpl, probably.

<a href="https://github.com/autoplot/dev/search?q=getXPathFactory&unscoped_q=getXPathFactory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="guessNameFor"></a>
# guessNameFor
guessNameFor( String uri ) &rarr; String

returns a variable name generated from the URI.  This was written for Jython scripting.  A future
 version of this might attempt to load the resource, and use the name from the result.

### Parameters:
uri - a String

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=guessNameFor&unscoped_q=guessNameFor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

guessNameFor( String uri, java.util.List otherURIs, java.util.List otherNames ) &rarr; String<br>
***
<a name="guessRenderType"></a>
# guessRenderType
guessRenderType( QDataSet fillds ) &rarr; String



### Parameters:
fillds - a QDataSet

### Returns:
a String

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/Autoplot org/autoplot/AutoplotUtil/guessRenderType/.md'>Autoplot org.autoplot.AutoplotUtil.guessRenderType.</a> org.autoplot.AutoplotUtil.guessRenderType.<br>

<a href="https://github.com/autoplot/dev/search?q=guessRenderType&unscoped_q=guessRenderType">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isConstant"></a>
# isConstant
isConstant( java.lang.String[] others, int st, int en ) &rarr; boolean

return true if the characters in the range st to en do not change.

### Parameters:
others - a java.lang.String[]
<br>st - an int
<br>en - an int

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isConstant&unscoped_q=isConstant">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isHtmlStream"></a>
# isHtmlStream
isHtmlStream( String text ) &rarr; boolean

returns true if the text appears to be html.  Right now the test is
 for "<htm" "<HTM" or "<!doc" "<!DOC".

### Parameters:
text - the text.

### Returns:
true if the stream appears to be html.

<a href="https://github.com/autoplot/dev/search?q=isHtmlStream&unscoped_q=isHtmlStream">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isJavaDouble"></a>
# isJavaDouble
isJavaDouble( String myString ) &rarr; boolean

from java.lang.Double javadoc, this tests if a number is a double.

### Parameters:
myString - a String

### Returns:
true if the number is a double.

<a href="https://github.com/autoplot/dev/search?q=isJavaDouble&unscoped_q=isJavaDouble">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isJavaIdentifier"></a>
# isJavaIdentifier
isJavaIdentifier( String label ) &rarr; boolean

return true if the string is a java identifier.

### Parameters:
label - a String

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isJavaIdentifier&unscoped_q=isJavaIdentifier">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="makeAggregation"></a>
# makeAggregation
makeAggregation( String surl, java.lang.String[] surls ) &rarr; String

attempt to make an aggregation from the URLs.  If one cannot be created
 (for example if the filenames are not consistent), then the original
 URI is returned.

### Parameters:
surl - a String
<br>surls - a java.lang.String[]

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=makeAggregation&unscoped_q=makeAggregation">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

makeAggregation( String surl ) &rarr; String<br>
***
<a name="makeAggregationForGroup"></a>
# makeAggregationForGroup
makeAggregationForGroup( String surl, java.lang.String[] others ) &rarr; String

attempt to create a String that uses an aggregation template
 instead of the particular time.  This also return null when things 
 go wrong.  For example, 
 file:/tmp/20091102.dat -> file:/tmp/$Y$m$d.dat?timerange=20091102
 Also, look for version numbers.  If multiple periods are found, then use 
 $(v,sep) otherwise use numeric $v.
<blockquote><pre><small>
ss= [ "1991_095/1993/19930303.dat","1991_095/1993/19930304.dat","1991_095/1991/19930305.dat" ]
y= makeAggregationForGroup("1991_095/1993/19930303.dat",ss)       // 1991_095/$Y/$Y$m$d.dat?timerange=2009-11-02
</small></pre></blockquote>

### Parameters:
surl - the URI.
<br>others - other URIs in the group, used to reject solutions which would not produce unique results.

### Returns:
null or the string with aggregations ($Y.dat) instead of filename (1999.dat), or the original filename.
### See Also:
<a href='https://github.com/autoplot/dev/blob/master/bugs/sf/0484/makeAggregationForGroup_001.jy'>https://github.com/autoplot/dev/blob/master/bugs/sf/0484/makeAggregationForGroup_001.jy</a> <br>

<a href="https://github.com/autoplot/dev/search?q=makeAggregationForGroup&unscoped_q=makeAggregationForGroup">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="newURL"></a>
# newURL
newURL( java.net.URL context, String spec ) &rarr; URL

interprets spec within the context of URL context.

### Parameters:
context - the context for the spec.  null may be used to
    indicate no context.
<br>spec - if spec is a fully specified URL, then it is used, otherwise
    it is appended to context.  If spec refers to the name of a file,
    but doesn't start with "file:/", "file:/" is appended.

### Returns:
the URL.

<a href="https://github.com/autoplot/dev/search?q=newURL&unscoped_q=newURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="openBrowser"></a>
# openBrowser
openBrowser( String url ) &rarr; void

open the URL in a browser.   Borrowed from http://www.centerkey.com/java/browser/.  
 See also openBrowser in Autoplot,
 which this replaces.
 
 Java 6 introduced standard code for doing this.  The old code is still 
 used in case there's a problem.

### Parameters:
url - the URL

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=openBrowser&unscoped_q=openBrowser">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parseConstraint"></a>
# parseConstraint
parseConstraint( String constraint, long[] qubeDims ) &rarr; Map

returns the [ start, stop, stride ] or [ start, -1, -1 ] for slice, but also
 supports slice notations like [:,1]. This is
 provided to reduce code and for uniform behavior.
 
 Examples:
 <ul>
 <li>[::1,:]
 <li>[:,2]
 </ul>

### Parameters:
constraint - a String
<br>qubeDims - the dimension of the data.

### Returns:
the [startRecord,stopRecordExclusive,stride]

<a href="https://github.com/autoplot/dev/search?q=parseConstraint&unscoped_q=parseConstraint">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

parseConstraint( String constraint, long recCount ) &rarr; long<br>
***
<a name="setTimeRange"></a>
# setTimeRange
setTimeRange( String uri, DatumRange timeRange, ProgressMonitor mon ) &rarr; String

With the URI, establish if it has time series browse and set the timerange
 to the given timerange if it does.  For example, modify the bookmark so that the
 timerange is the current axis timerange before using it.

### Parameters:
uri - An Autoplot URI, which must resolve to a DataSource.
<br>timeRange - the timerange to use.  If this is null or a non-timerange, then the URI is returned unchanged.
<br>mon - the monitor

### Returns:
A URI that would yield data from the same dataset but for a different time.

<a href="https://github.com/autoplot/dev/search?q=setTimeRange&unscoped_q=setTimeRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showMessageDialog"></a>
# showMessageDialog
showMessageDialog( java.awt.Component parent, String msg, String title, int messageType, java.lang.Exception causeBy ) &rarr; void

this will make the exception available.  (Someday. TODO: where is this used?)

### Parameters:
parent - a Component
<br>msg - a String
<br>title - a String
<br>messageType - an int
<br>causeBy - an Exception

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showMessageDialog&unscoped_q=showMessageDialog">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="strjoin"></a>
# strjoin
strjoin( java.util.Collection c, String delim ) &rarr; String



### Parameters:
c - a java.util.Collection
<br>delim - a String

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=strjoin&unscoped_q=strjoin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

strjoin( long[] dims, String delim ) &rarr; String<br>
strjoin( int[] dims, String delim ) &rarr; String<br>
***
<a name="toJavaIdentifier"></a>
# toJavaIdentifier
toJavaIdentifier( String label ) &rarr; String

make a valid Java identifier from the label.  Data sources may wish
 to allow labels to be used to identify data sources, and this contains
 the standard logic.  Strings are replaced with underscores, invalid
 chars removed, etc.

### Parameters:
label - a String

### Returns:
valid Java identifier.

<a href="https://github.com/autoplot/dev/search?q=toJavaIdentifier&unscoped_q=toJavaIdentifier">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="transfer"></a>
# transfer
transfer( java.nio.channels.ReadableByteChannel src, java.nio.channels.WritableByteChannel dest ) &rarr; void

transfers the data from one channel to another.  src and dest are
 closed after the operation is complete.

### Parameters:
src - a ReadableByteChannel
<br>dest - a WritableByteChannel

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=transfer&unscoped_q=transfer">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

transfer( java.io.InputStream src, java.io.OutputStream dest ) &rarr; void<br>
transfer( java.io.InputStream src, java.io.OutputStream dest, boolean close ) &rarr; void<br>
***
<a name="trimScatterToTimeRange"></a>
# trimScatterToTimeRange
trimScatterToTimeRange( QDataSet tsbData, DatumRange timeRange ) &rarr; QDataSet

We've loaded the data, but it needs to be trimmed to exactly what the TSB requests, because a time axis
 is not visible.  This was introduced to support where TSB returns data that needs to be trimmed.

### Parameters:
tsbData - a QDataSet
<br>timeRange - the range where the data was requested.

### Returns:
the trimmed data
### See Also:
<a href='https://sourceforge.net/p/autoplot/bugs/1559/'>https://sourceforge.net/p/autoplot/bugs/1559/</a> <br>

<a href="https://github.com/autoplot/dev/search?q=trimScatterToTimeRange&unscoped_q=trimScatterToTimeRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="unescape"></a>
# unescape
unescape( String s ) &rarr; String

remove escape sequences like %20 to create a human-editable string
 This contains a kludge that looks for single spaces that are the result of
 cut-n-pasting on Linux.  If there is a space and a "%3A", then single spaces
 are removed.
 <code>&amp;amp;</code> is replaced with <code>&</code>.

### Parameters:
s - a String

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=unescape&unscoped_q=unescape">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="unescapeParam"></a>
# unescapeParam
unescapeParam( String s ) &rarr; String

Carefully remove pluses from URIs that mean to interpret pluses
 as spaces.  Note this is not done automatically because some data sources
 need the pluses, like vap+inline:ripples(20)+linspace(0.,10.,20).
 This should be done carefully, because we realize that some pluses may
 intentionally exist in URIs, such as &where=energy.gt(1e+3).  While this
 is discouraged, it will inevitably happen.  
 
 <table>
 <tr><td>&where=energy.gt(1e+3)</td><td>&where=energy.gt(1e+3)</td><tr>
 <tr><td>&where=energy.within(1e+3+to+1e+5)</td><td>&where=energy.gt(1e+3 to 1e+5)</td><tr>
 </table>

### Parameters:
s - the parameter string, such as

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=unescapeParam&unscoped_q=unescapeParam">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="unquote"></a>
# unquote
unquote( String s ) &rarr; String

remove quotes from string, which pops up a lot in metadata

### Parameters:
s - the string.

### Returns:
the string without quotes.

<a href="https://github.com/autoplot/dev/search?q=unquote&unscoped_q=unquote">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="urlWithinContext"></a>
# urlWithinContext
urlWithinContext( java.net.URL context, String url ) &rarr; String

presents the spec for the url within a context.

### Parameters:
context - the context.
<br>url - the URL.

### Returns:
the part made relative, if possible, to context.

<a href="https://github.com/autoplot/dev/search?q=urlWithinContext&unscoped_q=urlWithinContext">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

