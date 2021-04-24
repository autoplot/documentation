# org.autoplot.datasource.jython.JythonExtensionDataSourceFactory

Creates JythonExceptionDataSource's, which are data sources defined
 by Jython scripts, but the script need not be in the URI.

# JythonExtensionDataSourceFactory( )


***
<a name="getDataSource"></a>
# getDataSource
getDataSource( java.net.URI uri ) &rarr; DataSource



### Parameters:
uri - an URI

### Returns:
org.autoplot.datasource.DataSource


<a href="https://github.com/autoplot/dev/search?q=getDataSource&unscoped_q=getDataSource">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInternalScriptForResource"></a>
# getInternalScriptForResource
getInternalScriptForResource( java.net.URI uri ) &rarr; String

include an internal version of the script, so that the data source will
 work offline, for example when presenting the data source to a group
 of new users at a conference without network access.

### Parameters:
uri - the Autoplot URI.

### Returns:
null or the name of the file to use.

<a href="https://github.com/autoplot/dev/search?q=getInternalScriptForResource&unscoped_q=getInternalScriptForResource">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getJydsUri"></a>
# getJydsUri
getJydsUri( java.net.URI uri ) &rarr; String

return the URI which would be used for this resource, if it were 
 called directly.

### Parameters:
uri - an URI

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getJydsUri&unscoped_q=getJydsUri">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getScriptForResource"></a>
# getScriptForResource
getScriptForResource( java.net.URI uri ) &rarr; String

this is the lookup table from URI (*.sps) to script (readTypeSps.jyds)

### Parameters:
uri - the Autoplot URI.

### Returns:
string containing the script.

<a href="https://github.com/autoplot/dev/search?q=getScriptForResource&unscoped_q=getScriptForResource">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

