# org.autoplot.datasource.DataSourceFactory

DataSourceFactories create data sources which resolve a URI into a QDataSet.
 Some DataSourceFactories support discovery, meaning they will provide
 a GUI to create URIs with no other information.

***
<a name="getCapability"></a>
# getCapability
getCapability( java.lang.Class clazz ) &rarr; Object

return additional tools for creating valid URIs, such as TimeSeriesBrowse.  This may soon include
 a file selector, and an automatic GUI created from the completions model.

### Parameters:
clazz - the class, such as org.autoplot.datasource.capability.TimeSeriesBrowse

### Returns:
the capability, such as an instance of org.autoplot.datasource.capability.TimeSeriesBrowse

<a href="https://github.com/autoplot/dev/search?q=getCapability&unscoped_q=getCapability">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCompletions"></a>
# getCompletions
getCompletions( org.autoplot.datasource.CompletionContext cc, ProgressMonitor mon ) &rarr; List

return a list of context-sensitive completions.  If an exception is thrown, then an
 a error dialog is displayed for RuntimeExceptions.  Compile-time exceptions may be
 displayed more gently, relying on getMessage to aid the human operator.

### Parameters:
cc - the context for the completion.
<br>mon - a progress monitor, for example to monitor a file download.

### Returns:
a set of completions

<a href="https://github.com/autoplot/dev/search?q=getCompletions&unscoped_q=getCompletions">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSource"></a>
# getDataSource
getDataSource( java.net.URI uri ) &rarr; DataSource

return a dataSource for the url

### Parameters:
uri - the URI

### Returns:
the DataSource

<a href="https://github.com/autoplot/dev/search?q=getDataSource&unscoped_q=getDataSource">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDescription"></a>
# getDescription
getDescription(  ) &rarr; String

return a short description of the factory, or empty string.  For example,
 "NASA Common Data Format (CDF) Files" or "NASA CDAWeb".  This will 
 be used to identify files or discovery sources.

### Returns:
a short description of the factory.

<a href="https://github.com/autoplot/dev/search?q=getDescription&unscoped_q=getDescription">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isFileResource"></a>
# isFileResource
isFileResource(  ) &rarr; boolean

true if the data source is based on files.  For example, a CDF file
 is true, since the URIs contain cdf file names, and while vap+cdaweb 
 uses files to move data, it is not file based.  This is initially used
 to limit the entries in file choosers.

### Returns:
true if the data source is based on files.

<a href="https://github.com/autoplot/dev/search?q=isFileResource&unscoped_q=isFileResource">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reject"></a>
# reject
reject( String suri, java.util.List problems, ProgressMonitor mon ) &rarr; boolean

quick check to see that an uri looks acceptable.

 since 2012b, this should provide a list of objects marking reasons for rejecting.  Though each object
 is simply a marker, toString method of each should provide some meaningful information to developers.
 This list will be passed into the editor if available.

### Parameters:
suri - the uri.
<br>problems - list to which problems should be added. TODO: human readable or PROB_TIMERANGE?
<br>mon - a progress monitor, for example to monitor a file download.

### Returns:
true if the string cannot be used as a URI.

<a href="https://github.com/autoplot/dev/search?q=reject&unscoped_q=reject">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="supportsDiscovery"></a>
# supportsDiscovery
supportsDiscovery(  ) &rarr; boolean

mark that this source has an editor that allows discovery of data,
 and the GUI can be entered with "vap+ext:"  This must be consistent
 with the reject method of the editor.

### Returns:
true if the data source factory supports discovery.

<a href="https://github.com/autoplot/dev/search?q=supportsDiscovery&unscoped_q=supportsDiscovery">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

