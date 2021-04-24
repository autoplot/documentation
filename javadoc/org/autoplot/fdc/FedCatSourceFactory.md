# org.autoplot.fdc.FedCatSourceFactory

Generates data sources based off URIs of the form: vap+dfc:LOCATION

# FedCatSourceFactory( )


***
<a name="getCompletions"></a>
# getCompletions
getCompletions( org.autoplot.datasource.CompletionContext cc, ProgressMonitor mon ) &rarr; List



### Parameters:
cc - a CompletionContext
<br>mon - a ProgressMonitor

### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=getCompletions&unscoped_q=getCompletions">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSource"></a>
# getDataSource
getDataSource( java.net.URI uri ) &rarr; DataSource

Break a catalog URI down into parts
 
 Federated Catalog Paths are very different from many Autoplot URIs,
 provide parsing for these.

### Parameters:
uri - an URI

### Returns:
A Map<String,String> that always has the following keys:
         "handler" - Should always be 'vap+dc'
         "rootUrl" - The URL to the root node, will often be null, meaning that the
                     URLs must be found in the global catalog
         "path"    - The sub path of interest offset from the root URL
         "params"  - The query parameters.  Will be null for default datasets

<a href="https://github.com/autoplot/dev/search?q=getDataSource&unscoped_q=getDataSource">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isFileResource"></a>
# isFileResource
isFileResource(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isFileResource&unscoped_q=isFileResource">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reject"></a>
# reject
reject( String sUrl, java.util.List lProblems, ProgressMonitor mon ) &rarr; boolean

We have to reject the URI in order to pop up the inspection dialog box. 
 This makes sense because if the URI is good, folks just want to see the data.

### Parameters:
sUrl - a String
<br>lProblems - a java.util.List
<br>mon - a ProgressMonitor

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=reject&unscoped_q=reject">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="supportsDiscovery"></a>
# supportsDiscovery
supportsDiscovery(  ) &rarr; boolean

This data source is pretty much only discovery, so of course we return true here.

### Returns:
true

<a href="https://github.com/autoplot/dev/search?q=supportsDiscovery&unscoped_q=supportsDiscovery">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

