# org.autoplot.cdaweb.CDAWebDataSourceSpecial data source for reading time series from NASA Goddard's CDAWeb
 database.  This uses an XML file to locate data files (soon a web service), and
 delegates to the CDF file reader to read them.  This code handles the
 aggregation into a time series.
CDAWebDataSource( java.net.URI uri )


***
<a name="PARAM_ID"></a>
# PARAM_ID



***
<a name="PARAM_DS"></a>
# PARAM_DS



***
<a name="PARAM_TIMERANGE"></a>
# PARAM_TIMERANGE



***
<a name="PARAM_WS"></a>
# PARAM_WS



***
<a name="PARAM_AVAIL"></a>
# PARAM_AVAIL



***
<a name="getCapability"></a>
# getCapability
getCapability( java.lang.Class clazz ) &rarr; Object

caution: see also CDAWebDataSourceFactory.getCapability!

### Parameters:
clazz - a java.lang.Class

### Returns:
an Object


<a href="https://github.com/autoplot/dev/search?q=getCapability&unscoped_q=getCapability">[search for examples]</a>

***
<a name="getDataSet"></a>
# getDataSet
getDataSet( ProgressMonitor mon ) &rarr; QDataSet



### Parameters:
mon - a ProgressMonitor

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>

***
<a name="getMetadata"></a>
# getMetadata
getMetadata( ProgressMonitor mon ) &rarr; Map



### Parameters:
mon - a ProgressMonitor

### Returns:
java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getMetadata&unscoped_q=getMetadata">[search for examples]</a>

***
<a name="getMetadataModel"></a>
# getMetadataModel
getMetadataModel(  ) &rarr; MetadataModel



### Returns:
org.autoplot.datasource.MetadataModel


<a href="https://github.com/autoplot/dev/search?q=getMetadataModel&unscoped_q=getMetadataModel">[search for examples]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

