# org.autoplot.dods.MetaDataScraperScrape the metadata from the &lt;dods URL&gt;.html form of the data.  
 Get a new instance, call parse( &lt;dods URL&gt;.html ), then 
 call getAttr(String varName) which returns a Map of the properties.

 Note the scraping is only necessary because Jeremy forgot about the
 .das and .dds extensions.  .dds returns the stream syntax.  .das returns 
 the metadata.
MetaDataScraper( )
Creates a new instance of SPDFMetaDataScraper.  Use parseData then getAttr after creating the instance.

***
<a name="getAttr"></a>
# getAttr
getAttr( String varName ) &rarr; Map

provides the attributes for this variable in a map.  The keys are the String 
 attribute name (e.g. UNITS) and the values are either type String or Double.

### Parameters:
varName - the variable name

### Returns:
the attributes

<a href="https://github.com/autoplot/dev/search?q=getAttr&unscoped_q=getAttr">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRecDims"></a>
# getRecDims
getRecDims( String varName ) &rarr; int



### Parameters:
varName - a String

### Returns:
int[]


<a href="https://github.com/autoplot/dev/search?q=getRecDims&unscoped_q=getRecDims">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parseURL"></a>
# parseURL
parseURL( java.net.URL url ) &rarr; void

retrieve the URL, which should be a dods server form.  The
 content is scraped, looking for textareas with the name
 <i>varname</i>_attr.  The textarea content is assumed to
 be a newline delimited set of name value pairs, name: value.
 Value is of type Double or String.

 After parseURL is performed, getAttr is used to get Attributes.

### Parameters:
url - an URL

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=parseURL&unscoped_q=parseURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

