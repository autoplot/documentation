# org.autoplot.jythonsupport.Util

Utilities for Jython scripts in both the datasource and application contexts.

# Util( )


***
<a name="fileCanRead"></a>
# fileCanRead
fileCanRead( String file ) &rarr; boolean

return true if the file can be read.
 This is introduced to avoid imports of java.io.File.

### Parameters:
file - the file or directory.

### Returns:
true if the file can be read.
 //TODO: this could support remote file systems

<a href="https://github.com/autoplot/dev/search?q=fileCanRead&unscoped_q=fileCanRead">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="fileExists"></a>
# fileExists
fileExists( String file ) &rarr; boolean

return true if the file exists.  
 This is introduced to avoid imports of java.io.File.

### Parameters:
file - file or local file Autoplot URI

### Returns:
true if the file exists.
 //TODO: this could support remote file systems

<a href="https://github.com/autoplot/dev/search?q=fileExists&unscoped_q=fileExists">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="generateTimeRanges"></a>
# generateTimeRanges
generateTimeRanges( String spec, String srange ) &rarr; String

Given a spec to format timeranges and a range to contain each timerange,
 produce a list of all timeranges covering the range formatted with the
 spec.  For example, <code>generateTimeRanges( "%Y-%m-%d", "Jun 2009" )</code> would result in
 2009-06-01, 2009-06-02, ..., 2009-06-30.  This is limited to create no more than 
 100000 elements.

### Parameters:
spec - such as "%Y-%m".  Note specs like "%Y%m" will not be parsable.
<br>srange - range limiting the list, such as "2009"

### Returns:
a string array of formatted time ranges, such as [ "2009-01", "2009-02", ..., "2009-12" ]
### See Also:
<a href='DatumRangeUtil.md#parseTimeRangeValid'>DatumRangeUtil#parseTimeRangeValid(java.lang.String)</a> to convert to DatumRange objects.<br>

<a href="https://github.com/autoplot/dev/search?q=generateTimeRanges&unscoped_q=generateTimeRanges">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getAllCompletions"></a>
# getAllCompletions
getAllCompletions( String file ) &rarr; String

return a list of all completions, even if they are not complete.  
 This is useful in the IDL context
 as well as Jython scripts.  This will perform the completion for where the carot is
 at the end of the string.  All completions are returned, so for example 
 http://autoplot.org/data/somedata.cdf?noDep is returned as well as
 http://autoplot.org/data/somedata.cdf?Magnitude.

### Parameters:
file - for example http://autoplot.org/data/somedata.cdf?

### Returns:
list of completions, containing the entire URI.

<a href="https://github.com/autoplot/dev/search?q=getAllCompletions&unscoped_q=getAllCompletions">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getAutoplotScriptingVersion"></a>
# getAutoplotScriptingVersion
getAutoplotScriptingVersion(  ) &rarr; String

this returns a double indicating the current scripting version, found
 at the top of autoplot2017.py in AUTOPLOT_DATA/jython/autoplot2017.py.  Do
 not parse this number and expect it to work in future versions!

### Returns:
the version, such as v1.50.

<a href="https://github.com/autoplot/dev/search?q=getAutoplotScriptingVersion&unscoped_q=getAutoplotScriptingVersion">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCompletions"></a>
# getCompletions
getCompletions( String file ) &rarr; String

return a list of completions.  This is useful in the IDL context
 as well as Jython scripts.  This will perform the completion for where the carot is
 at the end of the string.  Only completions where maybePlot indicates the URI is now 
 valid are returned, so for example http://autoplot.org/data/somedata.cdf?noDep is not
 returned and http://autoplot.org/data/somedata.cdf?Magnitude is.

### Parameters:
file - for example http://autoplot.org/data/somedata.cdf?

### Returns:
list of completions, containing the entire URI.

<a href="https://github.com/autoplot/dev/search?q=getCompletions&unscoped_q=getCompletions">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSet"></a>
# getDataSet
getDataSet( String suri, String stimeRange, ProgressMonitor mon ) &rarr; QDataSet

load the data specified by URI into Autoplot's internal data model.  This will
 block until the load is complete, and a ProgressMonitor object can be used to
 monitor the load.

 This adds a timeRange parameter so that TimeSeriesBrowse-capable datasources
 can be used from AutoplotServer.

### Parameters:
suri - the URI of the dataset, such as "http://autoplot.org/data/2010_061_17_41_40.txt?column=field8"
<br>stimeRange - a string representing the timerange to load, such as 2012-02-02/2012-02-03
<br>mon - progress monitor object.

### Returns:
QDataSet from the load.

<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getDataSet( String suri, DatumRange timeRange, ProgressMonitor monitor ) &rarr; QDataSet<br>
getDataSet( String suri, ProgressMonitor mon ) &rarr; QDataSet<br>
getDataSet( String suri ) &rarr; QDataSet<br>
getDataSet( String suri, String stimerange ) &rarr; QDataSet<br>
getDataSet( String suri, DatumRange timerange ) &rarr; QDataSet<br>
getDataSet( String spec, java.io.InputStream in, ProgressMonitor mon ) &rarr; QDataSet<br>
***
<a name="getDataSets"></a>
# getDataSets
getDataSets( java.util.List uris, ProgressMonitor mon ) &rarr; List

experiment with multiple, simultaneous reads in Jython codes.  This will read all the data
 at once, returning all data or throwing one of the exceptions.

### Parameters:
uris - a list of URI strings.
<br>mon - monitor for the aggregate load.  TODO: Each uri should given equal shares of the task.

### Returns:
list of loaded data

<a href="https://github.com/autoplot/dev/search?q=getDataSets&unscoped_q=getDataSets">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSource"></a>
# getDataSource
getDataSource( String suri ) &rarr; DataSource

returns the dataSource for the given URI.  This will include capabilities, like TimeSeriesBrowse.

### Parameters:
suri - the data address to load.

### Returns:
the DataSource to load the URI.

<a href="https://github.com/autoplot/dev/search?q=getDataSource&unscoped_q=getDataSource">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMetadata"></a>
# getMetadata
getMetadata( String suri, ProgressMonitor mon ) &rarr; Map

load the metadata for the url.  This can be called independently from getDataSet,
 and data sources should not assume that getDataSet is called before getMetaData.
 Some may, in which case a bug report should be submitted.
 
 The metadata is a tree of name/value pairs, for human consumption, and
 used when a particular metadata model is expects.

### Parameters:
suri - the data address to load.
<br>mon - monitor, or null (None in Jython) for no feedback.

### Returns:
metadata tree created by the data source.

<a href="https://github.com/autoplot/dev/search?q=getMetadata&unscoped_q=getMetadata">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTimeRangesFor"></a>
# getTimeRangesFor
getTimeRangesFor( String surl, String timeRange, String format ) &rarr; String

return an array of URLs that match the spec for the time range provided.
 For example,
 <p><blockquote><pre>
  uri= 'https://cdaweb.gsfc.nasa.gov/istp_public/data/polar/hyd_h0/$Y/po_h0_hyd_$Y$m$d_v01.cdf?ELECTRON_DIFFERENTIAL_ENERGY_FLUX'
  xx= getTimeRangesFor( uri, '2000-jan', '$Y-$d-$m' )
  for x in xx:
    print x
 </pre></blockquote><p>

### Parameters:
surl - an Autoplot uri with an aggregation specifier.
<br>timeRange - a string that is parsed to a time range, such as "2001"
<br>format - format for the result, such as "%Y-%m-%d"

### Returns:
a list of URLs without the aggregation specifier.

<a href="https://github.com/autoplot/dev/search?q=getTimeRangesFor&unscoped_q=getTimeRangesFor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTimeSeriesBrowse"></a>
# getTimeSeriesBrowse
getTimeSeriesBrowse( org.autoplot.datasource.DataSource ds ) &rarr; TimeSeriesBrowse

get the TimeSeriesBrowse capability, if available.  Null (None) is returned if it is not found.

### Parameters:
ds - the data source.

### Returns:
the TimeSeriesBrowse if available, or null (None)

<a href="https://github.com/autoplot/dev/search?q=getTimeSeriesBrowse&unscoped_q=getTimeSeriesBrowse">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="guardedSplit"></a>
# guardedSplit
guardedSplit( String s, char delim, char exclude1, char exclude2 ) &rarr; String

only split on the delimiter when we are not within the exclude delimiters.  For example,
 <code>
 x=getDataSet("http://autoplot.org/data/autoplot.cdf?Magnitude&noDep=T")&y=getDataSet('http://autoplot.org/data/autoplot.cdf?BGSEc&slice1=2')&sqrt(x)
 </code>

### Parameters:
s - the string to split.
<br>delim - the delimiter to split on, for example the ampersand (&).
<br>exclude1 - for example the single quote (')
<br>exclude2 - for example the double quote (")  Note URIs don't support these anyway.

### Returns:
the split.
 
 This is a copy of another code.

<a href="https://github.com/autoplot/dev/search?q=guardedSplit&unscoped_q=guardedSplit">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isLegacyImports"></a>
# isLegacyImports
isLegacyImports(  ) &rarr; boolean

return true if we should do the imports as before, where all of Autoplot is
 imported with each session.  This is used to ease migration.

### Returns:
true if the old behavior should be used.

<a href="https://github.com/autoplot/dev/search?q=isLegacyImports&unscoped_q=isLegacyImports">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="listDirectory"></a>
# listDirectory
listDirectory( String suri ) &rarr; String

returns an array of the files in the local or remote filesystem pointed to by suri.  The files are returned
 without the path, and directories are marked with a trailing slash character.  Windows a forward 
 slash is still used, even though a back slash is more conventional.  When the suri ends in slash, all 
 entries in the directory are listed, and when it ends in a file glob, all matching files are returned.

 <p><blockquote><pre>
 print listDirectory( 'http://autoplot.org/data/pngwalk/' )
  --> 'product.vap', 'product_20080101.png', 'product_20080102.png', ...
 print listDirectory( 'http://autoplot.org/data/pngwalk/*.png' )
  --> 'product_20080101.png', 'product_20080102.png', ...
 </pre></blockquote><p>

### Parameters:
suri - local or web directory.

### Returns:
an array of the files pointed to by surl.

<a href="https://github.com/autoplot/dev/search?q=listDirectory&unscoped_q=listDirectory">[search for examples]</a>
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
<a name="popString"></a>
# popString
popString( String line ) &rarr; String



### Parameters:
line - a String

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=popString&unscoped_q=popString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="requireAutoplotScriptingVersion"></a>
# requireAutoplotScriptingVersion
requireAutoplotScriptingVersion( String v ) &rarr; void

throw an exception if the scripting version cannot be supported.  These
 versions are numeric--so note that v1.7 is newer than v1.50, and for this
 reason versions should always be vNNN.NN.

### Parameters:
v - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=requireAutoplotScriptingVersion&unscoped_q=requireAutoplotScriptingVersion">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="runInParallel"></a>
# runInParallel
runInParallel( PyFunction job, java.util.List argument, ProgressMonitor mon ) &rarr; List

run the python jobs in parallel.

### Parameters:
job - a python function which takes one argument
<br>argument - list of arguments to invoke.
<br>mon - monitor for the group of processes

### Returns:
list of results for each call of the function.

<a href="https://github.com/autoplot/dev/search?q=runInParallel&unscoped_q=runInParallel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="sleep"></a>
# sleep
sleep( int millis ) &rarr; void

sleep for so many milliseconds.  This is introduced to avoid the import,
 which makes running scripts securely non-trivial.

### Parameters:
millis - number of milliseconds to pause execution

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=sleep&unscoped_q=sleep">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

