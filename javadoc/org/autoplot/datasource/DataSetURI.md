# org.autoplot.datasource.DataSetURIWorks with DataSourceRegistry to translate a URI into a DataSource.  Also,
 will provide completions.
DataSetURI( )


***
<a name="abbreviateForHumanComsumption"></a>
# abbreviateForHumanComsumption
abbreviateForHumanComsumption( String ssuri, int len ) &rarr; String

return a human-readable abbreviation of the URI, limiting to len characters.

### Parameters:
ssuri - a String
<br>len - an int

### Returns:
a string of length no more than len characters

<a href="https://github.com/autoplot/dev/search?q=abbreviateForHumanComsumption&unscoped_q=abbreviateForHumanComsumption">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="blurTsbResolutionUri"></a>
# blurTsbResolutionUri
blurTsbResolutionUri( String value ) &rarr; String

create the URI without the timerange.

### Parameters:
value - a uri. e.g. /tmp/foo$Y$m$d.dat?timerange=2014-001

### Returns:
null or the value without the timerange, e.g. /tmp/foo$Y$m$d.dat

<a href="https://github.com/autoplot/dev/search?q=blurTsbResolutionUri&unscoped_q=blurTsbResolutionUri">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="blurTsbUri"></a>
# blurTsbUri
blurTsbUri( String value ) &rarr; String

create the URI without the timerange.

### Parameters:
value - a uri. e.g. /tmp/foo$Y$m$d.dat?timerange=2014-001

### Returns:
null or the value without the timerange, e.g. /tmp/foo$Y$m$d.dat

<a href="https://github.com/autoplot/dev/search?q=blurTsbUri&unscoped_q=blurTsbUri">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="checkLength"></a>
# checkLength
checkLength( java.io.File file ) &rarr; void

check that the file has length&gt;0 and throw EmptyFileException if it does.  This
 code is the standard way this should be done.

### Parameters:
file - a File

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=checkLength&unscoped_q=checkLength">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="downloadResourceAsTempFile"></a>
# downloadResourceAsTempFile
downloadResourceAsTempFile( java.net.URL url, ProgressMonitor mon ) &rarr; File

This loads the URL to a local temporary file.  If the temp file
 is already downloaded and less than 10 seconds old, it will be used.

### Parameters:
url - the address to download.
<br>mon - a progress monitor.

### Returns:
a File in the FileSystemCache.  The file will have question marks and ampersands removed.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/DataSetURI/downloadResourceAsTempFile/.md'>DataSetURI.downloadResourceAsTempFile.</a> <br>

<a href="https://github.com/autoplot/dev/search?q=downloadResourceAsTempFile&unscoped_q=downloadResourceAsTempFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

downloadResourceAsTempFile( java.net.URL url, int timeoutSeconds, ProgressMonitor mon ) &rarr; File<br>
***
<a name="fromFile"></a>
# fromFile
fromFile( java.io.File file ) &rarr; String

canonical method for converting from File to human-readable string.  This
 simply tacks on "file://" to the filename.  This was introduced so that there
 is one canonical way to do this.

### Parameters:
file - a File

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=fromFile&unscoped_q=fromFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="fromUri"></a>
# fromUri
fromUri( java.net.URI uri ) &rarr; String

canonical method for converting URI to human-readable string, containing
 spaces and other illegal characters.  Note pluses in the query part
 are interpreted as spaces.
 See also URISplit.uriDecode,etc.

### Parameters:
uri - an URI

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=fromUri&unscoped_q=fromUri">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCacheFilename"></a>
# getCacheFilename
getCacheFilename( java.net.URI suri ) &rarr; File

provide standard logic for identifying the cache location for a file.  The file
 will not be downloaded, but clients can check to see if such resource has already been loaded.
 There is one case where this might be slow, and that's when a zip file must be downloaded to get
 the location.

### Parameters:
suri - the uri like http://autoplot.org/data/autoplot.dat

### Returns:
the cache file, like /home/jbf/autoplot_data/fscache/http/autoplot.org/data/autoplot.dat

<a href="https://github.com/autoplot/dev/search?q=getCacheFilename&unscoped_q=getCacheFilename">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCompletions"></a>
# getCompletions
getCompletions( String surl, int carotpos, ProgressMonitor mon ) &rarr; List

this is never used in the application code.  It must be left over from an earlier system.
 This is used in Test005, some scripts, and IDL codes, so don't delete it!

### Parameters:
surl - a String
<br>carotpos - an int
<br>mon - a ProgressMonitor

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=getCompletions&unscoped_q=getCompletions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSource"></a>
# getDataSource
getDataSource( java.net.URI uri ) &rarr; DataSource

get the data source for the URI.

### Parameters:
uri - the URI.

### Returns:
the data source from which the data set can be retrieved.

<a href="https://github.com/autoplot/dev/search?q=getDataSource&unscoped_q=getDataSource">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getDataSource( String suri ) &rarr; DataSource<br>
***
<a name="getDataSourceFactory"></a>
# getDataSourceFactory
getDataSourceFactory( java.net.URI uri, ProgressMonitor mon ) &rarr; DataSourceFactory

get the datasource factory for the URL.  This has the rarely-used 
 logic that looks up MIME types for HTTP requests.

### Parameters:
uri - the URI of the data source.
<br>mon - progress monitor

### Returns:
the factory that produces the data source.

<a href="https://github.com/autoplot/dev/search?q=getDataSourceFactory&unscoped_q=getDataSourceFactory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSourceFormat"></a>
# getDataSourceFormat
getDataSourceFormat( java.net.URI uri ) &rarr; DataSourceFormat

for now, just hide the URI stuff from clients, let's not mess with factories

### Parameters:
uri - the URI describing the output format and any arguments.

### Returns:
the DataSourceFormat that formats a dataset to the format.

<a href="https://github.com/autoplot/dev/search?q=getDataSourceFormat&unscoped_q=getDataSourceFormat">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSourceUri"></a>
# getDataSourceUri
getDataSourceUri( org.autoplot.datasource.DataSource ds ) &rarr; String

Prefix the URL with the datasource extension if necessary, so that
 the URL would resolve to the dataSource.  This is to support TimeSeriesBrowse,
 and any time a resouce URL must be understood out of context.

 TODO: note ds.getURI() should return the fully-qualified URI, so this is
 no longer necessary.

### Parameters:
ds - the data source.

### Returns:
the canonical URI.

<a href="https://github.com/autoplot/dev/search?q=getDataSourceUri&unscoped_q=getDataSourceUri">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDiscoverableExtensions"></a>
# getDiscoverableExtensions
getDiscoverableExtensions(  ) &rarr; List

return a list of the extensions we were can immediately enter the editor,
 so new users can plot things without knowing how to start a URI.
 Since rev 10581, this uses introspection to call the reject method to support
 compiling the applet.

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=getDiscoverableExtensions&unscoped_q=getDiscoverableExtensions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getExplicitExt"></a>
# getExplicitExt
getExplicitExt( String surl ) &rarr; String

return the extension prefix of the URI, if specified.

### Parameters:
surl - a String

### Returns:
null or an extension like "tsds"

<a href="https://github.com/autoplot/dev/search?q=getExplicitExt&unscoped_q=getExplicitExt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getExt"></a>
# getExt
getExt( String surl ) &rarr; String

returns the explicit extension, or the file extension if found, or null.
 The extension will not contain a period.  
 Inputs include:<ul>
 <li>ac_h2_cris_20111221_v06.cdf &rarr; "cdf"
 <li>/tmp/ac_h2_cris_20111221_v06.cdf &rarr; "cdf"
 <li>/tmp/ac_h2_cris_20111221_v06 &rarr; null
 </ul>

### Parameters:
surl - a String

### Returns:
the extension found, without the ".", or null if no period is found in the filename.

<a href="https://github.com/autoplot/dev/search?q=getExt&unscoped_q=getExt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFactoryCompletions"></a>
# getFactoryCompletions
getFactoryCompletions( String surl1, int carotPos, ProgressMonitor mon ) &rarr; List

get the completions from the plug-in factory..

### Parameters:
surl1 - a String
<br>carotPos - an int
<br>mon - a ProgressMonitor

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=getFactoryCompletions&unscoped_q=getFactoryCompletions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFile"></a>
# getFile
getFile( java.net.URL url, ProgressMonitor mon ) &rarr; File

return a file reference for the url.  This is initially to fix the problem
 for Windows where new URL( "file://c:/myfile.dat" ).getPath() -> "/myfile.dat".
 This will use a temporary local file in some cases, such as when the URL
 has parameters, which prevent use with the FileSystem model.

 TODO: why is there both getFile(url,mon) and getFile( suri, allowHtml, mon )???

### Parameters:
url - the URL of the file.
<br>mon - progress monitor or null.  If null then AlertProgressMonitor is used to show when the download time is not trivial.

### Returns:
the File
### See Also:
<a href='#getFile'>getFile(java.lang.String, boolean, org.das2.util.monitor.ProgressMonitor)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getFile&unscoped_q=getFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getFile( String suri, boolean allowHtml, ProgressMonitor mon ) &rarr; File<br>
getFile( java.net.URI uri, ProgressMonitor mon ) &rarr; File<br>
getFile( String uri, ProgressMonitor mon ) &rarr; File<br>
***
<a name="getFileSystemAggCompletions"></a>
# getFileSystemAggCompletions
getFileSystemAggCompletions( String surl, int carotpos, ProgressMonitor mon ) &rarr; List

get completions within the filesystem that appear to form aggregations.  Note this does not appear
 to be used, having no Java references.

### Parameters:
surl - a String
<br>carotpos - an int
<br>mon - a ProgressMonitor

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=getFileSystemAggCompletions&unscoped_q=getFileSystemAggCompletions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFileSystemCacheCompletions"></a>
# getFileSystemCacheCompletions
getFileSystemCacheCompletions( String surl, int carotpos, boolean inclAgg, boolean inclFiles, String acceptPattern, ProgressMonitor mon ) &rarr; List

gets completions based on cached folders.  This supports use when the
 filesystem is offline, when parents are not web filesystems, and presents 
 used folders separately.

### Parameters:
surl - http://sarahandjeremy.net/
<br>carotpos - the position of the carot.  Presently everything after the carot is ignored.
<br>inclAgg - include aggregations it sees.  These are a guess.
<br>inclFiles - include files as well as aggregations.
<br>acceptPattern - if non-null, files and aggregations much match this.
<br>mon - a ProgressMonitor

### Returns:
possibly immutable list.

<a href="https://github.com/autoplot/dev/search?q=getFileSystemCacheCompletions&unscoped_q=getFileSystemCacheCompletions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFileSystemCompletions"></a>
# getFileSystemCompletions
getFileSystemCompletions( String surl, int carotpos, boolean inclAgg, boolean inclFiles, String acceptPattern, ProgressMonitor mon ) &rarr; List

get completions within the filesystem for the directory listing of files.

### Parameters:
surl - a String
<br>carotpos - an int
<br>inclAgg - include aggregations it sees.  These are a guess.
<br>inclFiles - include files as well as aggregations.
<br>acceptPattern - if non-null, files and aggregations much match this.
<br>mon - a ProgressMonitor

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=getFileSystemCompletions&unscoped_q=getFileSystemCompletions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getFileSystemCompletions( String surl, int carotpos, boolean inclAgg, java.util.List inclFiles, String acceptPattern, ProgressMonitor mon ) &rarr; List<br>
***
<a name="getHostCompletions"></a>
# getHostCompletions
getHostCompletions( String surl, int carotpos, ProgressMonitor mon ) &rarr; List

get completions for hosts, by looking in the user's cache area.

### Parameters:
surl - a String
<br>carotpos - an int
<br>mon - a ProgressMonitor

### Returns:
possibly immutable list.

<a href="https://github.com/autoplot/dev/search?q=getHostCompletions&unscoped_q=getHostCompletions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getHtmlFile"></a>
# getHtmlFile
getHtmlFile( java.net.URL url, ProgressMonitor mon ) &rarr; File

get the file, allowing it to have "&lt;html&gt;" in the front.  Normally this is not
 allowed because of http://sourceforge.net/tracker/?func=detail&aid=3379717&group_id=199733&atid=970682

### Parameters:
url - an URL
<br>mon - a ProgressMonitor

### Returns:
a java.io.File


<a href="https://github.com/autoplot/dev/search?q=getHtmlFile&unscoped_q=getHtmlFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInputStream"></a>
# getInputStream
getInputStream( java.net.URL url, ProgressMonitor mon ) &rarr; InputStream

get the InputStream from the path part of the URI.  The stream must be closed by the client.

### Parameters:
url - URL like http://autoplot.org/data/autoplot.dat
<br>mon - monitor that will monitor the stream as it is transmitted.

### Returns:
the InputStream, which must be closed by the client. TODO: check usages...

<a href="https://github.com/autoplot/dev/search?q=getInputStream&unscoped_q=getInputStream">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getInputStream( java.net.URI uri, ProgressMonitor mon ) &rarr; InputStream<br>
***
<a name="getResourceURI"></a>
# getResourceURI
getResourceURI( java.net.URI uri ) &rarr; URI

returns the URI to be interpreted by the DataSource.  This identifies
 a file (or database) resource that can be passed to VFS.

### Parameters:
uri - an URI

### Returns:
the URI for the datasource resource, or null if it is not valid.

<a href="https://github.com/autoplot/dev/search?q=getResourceURI&unscoped_q=getResourceURI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getResourceURI( String surl ) &rarr; URI<br>
***
<a name="getSortedDiscoverableExtentions"></a>
# getSortedDiscoverableExtentions
getSortedDiscoverableExtentions(  ) &rarr; List

return the list of discoverable extentions, sorted by recent use.

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=getSortedDiscoverableExtentions&unscoped_q=getSortedDiscoverableExtentions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTypesCompletions"></a>
# getTypesCompletions
getTypesCompletions( String surl, int carotpos, ProgressMonitor mon ) &rarr; List

return a list of completions showing discovery plugins, and the list of supported filesystem types.

### Parameters:
surl - a String
<br>carotpos - an int
<br>mon - a ProgressMonitor

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=getTypesCompletions&unscoped_q=getTypesCompletions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getURI"></a>
# getURI
getURI( String surl ) &rarr; URI

canonical method for getting the Autoplot URI.  If no protocol is specified, then file:// is
 used.  Note URIs may contain prefix like vap+bin:http://www.cdf.org/data.cdf.  The
 result will start with an Autoplot scheme like "vap:" or "vap+cdf:"

 Note 20111117: "vap+cdaweb:" -> URI( "vap+cdaweb:file:///"  that's why this works to toUri doesn't.

### Parameters:
surl - the string from the user that should be representable as a URI.

### Returns:
the URI or null if it's clearly not a URI.

<a href="https://github.com/autoplot/dev/search?q=getURI&unscoped_q=getURI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getURIValid"></a>
# getURIValid
getURIValid( String surl ) &rarr; URI

get a URI from the string which is believed to be valid.  This was introduced
 because a number of codes called getURI without checking for null, which could be
 returned when the URI could not be parsed ("This is not a uri").  Codes that
 didn't check would produce a null pointer exception, and now they will produce
 a more accurate error.

### Parameters:
surl - a String

### Returns:
a java.net.URI


<a href="https://github.com/autoplot/dev/search?q=getURIValid&unscoped_q=getURIValid">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getURL"></a>
# getURL
getURL( String surl ) &rarr; URL

canonical method for getting the URL.  These will always be web-downloadable 
 URLs.

### Parameters:
surl - the string from the user that should be representable as a URI.

### Returns:
null or the URL if available.

<a href="https://github.com/autoplot/dev/search?q=getURL&unscoped_q=getURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getWebURL"></a>
# getWebURL
getWebURL( java.net.URI uri ) &rarr; URL

returns a downloadable URL from the Autoplot URI, perhaps popping off the
 data source specifier.  This assumes that the resource is a URL,
 and getResourceURI().toURL() should be used to handle all cases.

### Parameters:
uri - An Autoplot URI.

### Returns:
a URL that can be downloaded, or null if it is not found.

<a href="https://github.com/autoplot/dev/search?q=getWebURL&unscoped_q=getWebURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="init"></a>
# init
init(  ) &rarr; void

call this to trigger initialization

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=init&unscoped_q=init">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isAggregating"></a>
# isAggregating
isAggregating( String surl ) &rarr; boolean

check that the string uri is aggregating by looking for %Y's (etc) in the
 file part of the URI.  This also looks for:<ul>
 <li>$y -- two digit year
 <li>$(o -- orbit number
 <li>$(periodic -- interval number
 <li>$v -- version
 </ul>

### Parameters:
surl - a String

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isAggregating&unscoped_q=isAggregating">[search for examples]</a>

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
<a name="maybePlusToSpace"></a>
# maybePlusToSpace
maybePlusToSpace( String ssheet ) &rarr; String

Legacy behavior was to convert pluses into spaces in URIs.  This caused problems
 distinguishing spaces from pluses, so we dropped this as the default behavior.
 If data sources are to support legacy URIs, then they should use this routine
 to mimic the behavior.
 This checks if the URI already contains spaces, and will not convert if there
 are already spaces.

### Parameters:
ssheet - a String

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=maybePlusToSpace&unscoped_q=maybePlusToSpace">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resetUriTsbTime"></a>
# resetUriTsbTime
resetUriTsbTime( String value, DatumRange timeRange ) &rarr; String

return the URI with a new time.

### Parameters:
value - a String
<br>timeRange - a DatumRange

### Returns:
the URI with a new time.

<a href="https://github.com/autoplot/dev/search?q=resetUriTsbTime&unscoped_q=resetUriTsbTime">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toUri"></a>
# toUri
toUri( String suri ) &rarr; URI

canonical method for converting string from the wild into a URI-safe string.
 This contains the code that converts a colloquial string URI into a
 properly formed URI.
 For example:
    space is converted to "%20"
    %Y is converted to $Y
 This does not add file: or vap:.  Pluses are only changed in the params part.

### Parameters:
suri - a String

### Returns:
a java.net.URI


<a href="https://github.com/autoplot/dev/search?q=toUri&unscoped_q=toUri">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="unaggregate"></a>
# unaggregate
unaggregate( String resourceURI, DatumRange timerange ) &rarr; String

taken from unaggregate.jy in the servlet.

### Parameters:
resourceURI - resource URI like "file://tmp/data$Y$m$d.dat"
<br>timerange - a timerange that will be covered by the span.

### Returns:
the strings resolved.

<a href="https://github.com/autoplot/dev/search?q=unaggregate&unscoped_q=unaggregate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

