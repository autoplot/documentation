# org.autoplot.datasource.URISplitClass for containing the elemental parts of a URI, and utility
 routines for working with URIs.

 We need a working definition of well-formed and colloquial URIs:
<blockquote><pre>
 = well-formed URIs =
   <vapScheme>:<fileResource>?<params>
   <vapScheme>:[<identifier>?]<params>
   <vapScheme>:<params>
   * they are valid URIs: they contain no spaces, etc.
 == params ==
   ampersand-delimited (&) list of name=value pairs, or just value.
   vap+cdaweb:ds=ac_k0_epm&H_lo&timerange=2010-01
 = colloquial URIs =
   * these are Strings that can be converted into URIs.
   * spaces in file names are converted into %20. 
   * spaces in parameter lists are converted into pluses.
   * pluses in parameter lists are converted into %2B.
   * note that if there are pluses but the URI is valid, then pluses may be left alone. 
 </pre></blockquote>
 
 This routine knows nothing about the data source that will interpret the
 URI, so this needs to be established.
URISplit( )


***
<a name="PARAM_TIME_RANGE"></a>
# PARAM_TIME_RANGE

time range subset.

***
<a name="PARAM_TIME_RESOLUTION"></a>
# PARAM_TIME_RESOLUTION



***
<a name="PARAM_RANK2"></a>
# PARAM_RANK2

subset of rank 2 data.  For example, columns of excel workbook or ascii table.
 rank2=[3,5] or rank2=Bx-Bz

***
<a name="PARAM_REC_COUNT"></a>
# PARAM_REC_COUNT

used for the number of records to read.

***
<a name="PARAM_ARG_0"></a>
# PARAM_ARG_0

first positional parameter, typically interpreted the same as PARAM_ID

***
<a name="PARAM_ID"></a>
# PARAM_ID

typically the dataset id.

***
<a name="PARAM_FILE_POLL_UPDATES"></a>
# PARAM_FILE_POLL_UPDATES

some datasources support periodic checks to see if data sources have updated, such as:
   AggregatingDataSource
   AbstractDataSources (most of those based on files)

***
<a name="vapScheme"></a>
# vapScheme

scheme for Autoplot, if provided.  e.g.  vap+cdf.

***
<a name="scheme"></a>
# scheme

scheme for resource, e.g. "file" or "https"

***
<a name="surl"></a>
# surl

the complete, modified surl.   file:///home/jbf/mydata.qds
 this is the resource name, and doesn't contain the vapScheme.

***
<a name="resourceUri"></a>
# resourceUri

the resource that is handled by the DataSource.  This may be null if surl doesn't form a valid uri.

***
<a name="authority"></a>
# authority

the resource uri up to the authority, e.g. http://autoplot.org

***
<a name="path"></a>
# path

the resource uri including the path part.

***
<a name="file"></a>
# file

contains the resource string up to the query part.

***
<a name="ext"></a>
# ext

the file/resource extention, like ".cdf" or ".dat".

***
<a name="params"></a>
# params

contains the parameters part, a ampersand-delimited set of parameters. For example, column=field2&amp;rank2.

***
<a name="filters"></a>
# filters

additional processes to be applied to the URI.  For example, slice0(0) means slice the dataset at this point.

***
<a name="resourceUriCarotPos"></a>
# resourceUriCarotPos

position of the caret after modifications to the surl are made.  This
 is with respect to surl, the URI for the datasource, without the "vap" scheme.

***
<a name="formatCarotPos"></a>
# formatCarotPos

position of the caret after modifications to the surl are made.  This
 is with respect to formatted URI, which probably includes the explicit "vap:" scheme.

***
<a name="format"></a>
# format
format( org.autoplot.datasource.URISplit split ) &rarr; String

format the URI using vapScheme, file and params.  
 If file is missing but params is present, then return params:
   vap+cdaweb:ds=myds
 If file is present, then format with file and params:
   vap+cdf:file://tmp/my.cdf?myVar
 Else, just use the surl that is in there already. 
 Note if split.params is non-null, it will be appended with a question mark, even if empty.

### Parameters:
split - an URISplit

### Returns:
formatted URI.

<a href="https://github.com/autoplot/dev/search?q=format&unscoped_q=format">[search for examples]</a>

format( String vapScheme, String resourceUri, java.util.Map args ) &rarr; String<br>
***
<a name="formatParams"></a>
# formatParams
formatParams( java.util.Map parms ) &rarr; String

spaces and other URI syntax elements are URL-encoded.  
 Note some calls of this routine should check for an empty string result
 and then set split.params=null instead of "", to avoid the extraneous
 question mark.

### Parameters:
parms - a java.util.Map

### Returns:
"" or the parameters delimited by ampersands.

<a href="https://github.com/autoplot/dev/search?q=formatParams&unscoped_q=formatParams">[search for examples]</a>

***
<a name="getParam"></a>
# getParam
getParam( String surl, String name, String deft ) &rarr; String

convenient method for getting a parameter in the URI.

### Parameters:
surl - a String
<br>name - parameter name.
<br>deft - default value if the parameter is not found.

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getParam&unscoped_q=getParam">[search for examples]</a>

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

<a href="https://github.com/autoplot/dev/search?q=guardedSplit&unscoped_q=guardedSplit">[search for examples]</a>

***
<a name="implicitVapScheme"></a>
# implicitVapScheme
implicitVapScheme( org.autoplot.datasource.URISplit split ) &rarr; String

return the vap scheme in split.vapScheme or the one inferred by the 
 extension.  Returns an empty string (not "vap") if one cannot be inferred.
 e.g:
    /home/jbf/myfile.jyds --> vap+jyds
    vap+txt:/home/jbf/myfile.csv --> vap+txt
 This was introduced as part of the effort to get rid of extraneous "vap:"s
 that would be added to URIs.

### Parameters:
split - an URISplit

### Returns:
the vap scheme or empty string.

<a href="https://github.com/autoplot/dev/search?q=implicitVapScheme&unscoped_q=implicitVapScheme">[search for examples]</a>

***
<a name="isUriEncoded"></a>
# isUriEncoded
isUriEncoded( String surl ) &rarr; boolean

We need a standard way to detect if a string has already been URL encoded.
 The problem is we want valid URIs that are also readable, so just using
 simple encode/decode logic is not practical.

 This means:<ul>
 <li> no spaces
 <li> contains %[0-9][0-9]
 </ul>

### Parameters:
surl - the URI

### Returns:
true if it appears to be encoded.

<a href="https://github.com/autoplot/dev/search?q=isUriEncoded&unscoped_q=isUriEncoded">[search for examples]</a>

***
<a name="makeAbsolute"></a>
# makeAbsolute
makeAbsolute( String path, String suri ) &rarr; String

ensure that the reference, which may be relative, absolute.
 NOTE this is only implemented for unix filenames. TODO: Windows.
 For example:<ul>
 <li>/tmp/,foo.dat &rarr; /home/t/foo.dat
 <li>/tmp/,/home/jbf/foo.dat &rarr; /home/jbf/foo.dat
 </ul>

### Parameters:
path - the absolute directory.
<br>suri - the URI, which may be relative to path.

### Returns:
the absolute path

<a href="https://github.com/autoplot/dev/search?q=makeAbsolute&unscoped_q=makeAbsolute">[search for examples]</a>

***
<a name="makeCanonical"></a>
# makeCanonical
makeCanonical( String suri ) &rarr; String

make the URI canonical, with the vap+&lt;ext&gt;: prefix. 
 This will also now sort the parameters, when this can be done.

### Parameters:
suri - a String

### Returns:
"vap+cdf:file:///tmp/x.cdf"

<a href="https://github.com/autoplot/dev/search?q=makeCanonical&unscoped_q=makeCanonical">[search for examples]</a>

***
<a name="makeColloquial"></a>
# makeColloquial
makeColloquial( String suri ) &rarr; String

make the URI colloquial, e.g. removing "vap+cdf:" from "vap+cdf:file:///tmp/x.cdf"
 URIs that do not have a resource URI are left alone.

### Parameters:
suri - a URI

### Returns:
the URI, more colloquial and readable.

<a href="https://github.com/autoplot/dev/search?q=makeColloquial&unscoped_q=makeColloquial">[search for examples]</a>

***
<a name="maybeAddFile"></a>
# maybeAddFile
maybeAddFile( String surl, int caretPos ) &rarr; URISplit

add "file:/" to a resource string that appears to reference the local filesystem.
 return the parsed string, or null if the string doesn't appear to be from a file.

### Parameters:
surl - a String
<br>caretPos - an int

### Returns:
null or the URISplit

<a href="https://github.com/autoplot/dev/search?q=maybeAddFile&unscoped_q=maybeAddFile">[search for examples]</a>

***
<a name="parse"></a>
# parse
parse( java.net.URI uri ) &rarr; URISplit

added to avoid widespread use of parse(uri.toString).  This way its all being done with same code,
 and keep the URI abstraction.

### Parameters:
uri - an URI

### Returns:
an org.autoplot.datasource.URISplit


<a href="https://github.com/autoplot/dev/search?q=parse&unscoped_q=parse">[search for examples]</a>

parse( String suri ) &rarr; URISplit<br>
parse( String surl, int caretPos, boolean normalize ) &rarr; URISplit<br>
***
<a name="parseParams"></a>
# parseParams
parseParams( String params ) &rarr; LinkedHashMap

Split the parameters (if any) into name,value pairs. URLEncoded parameters are decoded, but the string may be decoded 
 already.  Items without equals (=) are inserted as "arg_N"=name.

### Parameters:
params - null or String containing the list of ampersand-delimited parameters.

### Returns:
the map, which will be empty when there are no params.

<a href="https://github.com/autoplot/dev/search?q=parseParams&unscoped_q=parseParams">[search for examples]</a>

***
<a name="parseTimeRange"></a>
# parseTimeRange
parseTimeRange( String uri ) &rarr; DatumRange

Helper method to get the timerange from the URI

### Parameters:
uri - a String

### Returns:
the DatumRange if "timerange=" is found, or null if not.

<a href="https://github.com/autoplot/dev/search?q=parseTimeRange&unscoped_q=parseTimeRange">[search for examples]</a>

***
<a name="putParam"></a>
# putParam
putParam( String surl, String name, String value ) &rarr; String

convenient method for adding or replacing a parameter to the URI.

### Parameters:
surl - any URI or web address
<br>name - the parameter name to add
<br>value - the parameter value to add

### Returns:
the uri with the question mark and parameter added.

<a href="https://github.com/autoplot/dev/search?q=putParam&unscoped_q=putParam">[search for examples]</a>

***
<a name="removeParam"></a>
# removeParam
removeParam( String surl, java.lang.String[] parm ) &rarr; String

convenient method to remove a parameter (or parameters) from the list of parameters

### Parameters:
surl - any URI or web address
<br>parm - the name to remove

### Returns:
the URI with the parameter removed, and the question mark removed when no parameters remain.

<a href="https://github.com/autoplot/dev/search?q=removeParam&unscoped_q=removeParam">[search for examples]</a>

***
<a name="setOtherSchemes"></a>
# setOtherSchemes
setOtherSchemes( java.util.List otherSchemes ) &rarr; void

allow parsing of script:, bookmarks:, pngwalk:, etc

### Parameters:
otherSchemes - a java.util.List

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setOtherSchemes&unscoped_q=setOtherSchemes">[search for examples]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

***
<a name="uriDecode"></a>
# uriDecode
uriDecode( String s ) &rarr; String

convert "+" to " ", etc, by using URLDecoder and catching the UnsupportedEncodingException that will never occur.
 We have to be careful for elements like %Y than are
 not to be decoded.
 TODO: we need to use standard escape/unescape code, possibly changing %Y to $Y beforehand.

### Parameters:
s - a String

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=uriDecode&unscoped_q=uriDecode">[search for examples]</a>

***
<a name="uriEncode"></a>
# uriEncode
uriEncode( String surl ) &rarr; String

convert " " to "%20", etc, by looking for and encoding illegal characters.
 We can't just aggressively convert...

### Parameters:
surl - the URI

### Returns:
the URL-encoded URI

<a href="https://github.com/autoplot/dev/search?q=uriEncode&unscoped_q=uriEncode">[search for examples]</a>

