# org.autoplot.dom.DataSourceControllerController node manages a DataSourceFilter node.
DataSourceController( org.autoplot.ApplicationModel model, org.autoplot.dom.DataSourceFilter dsf )


***
<a name="PROP_RAWPROPERTIES"></a>
# PROP_RAWPROPERTIES

raw properties provided by the datasource after the data load.

***
<a name="PROP_TSB"></a>
# PROP_TSB



***
<a name="PROP_TSBSURI"></a>
# PROP_TSBSURI



***
<a name="PROP_CACHING"></a>
# PROP_CACHING



***
<a name="PROP_DATASOURCE"></a>
# PROP_DATASOURCE

object that can provide data sets and capabilities.

***
<a name="PROP_DATASET"></a>
# PROP_DATASET



***
<a name="PROP_FILLDATASET"></a>
# PROP_FILLDATASET



***
<a name="PROP_EXCEPTION"></a>
# PROP_EXCEPTION



***
<a name="PROP_HISTOGRAM"></a>
# PROP_HISTOGRAM



***
<a name="PROP_PROPERTIES"></a>
# PROP_PROPERTIES



***
<a name="PROP_FILLPROPERTIES"></a>
# PROP_FILLPROPERTIES



***
<a name="PROP_REDUCEDATASETSTRING"></a>
# PROP_REDUCEDATASETSTRING



***
<a name="PROP_URINEEDSRESOLUTION"></a>
# PROP_URINEEDSRESOLUTION

true if the URI has been changed, and must be resolved into a DataSource.

***
<a name="PROP_DATASETNEEDSLOADING"></a>
# PROP_DATASETNEEDSLOADING

true is the DataSource has been changed, and we need to reload.

***
<a name="PROP_RESETDIMENSIONS"></a>
# PROP_RESETDIMENSIONS

true if the data source is changed and we need to reset the dimension
 names when we get our first data set.

***
<a name="cancel"></a>
# cancel
cancel(  ) &rarr; void

cancel the loading process.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=cancel&unscoped_q=cancel">[search for examples]</a>

***
<a name="doFillValidRange"></a>
# doFillValidRange
doFillValidRange(  ) &rarr; void

look in the metadata for fill and valid range.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=doFillValidRange&unscoped_q=doFillValidRange">[search for examples]</a>

***
<a name="getApplication"></a>
# getApplication
getApplication(  ) &rarr; Application



### Returns:
org.autoplot.dom.Application


<a href="https://github.com/autoplot/dev/search?q=getApplication&unscoped_q=getApplication">[search for examples]</a>

***
<a name="getAppliedFiltersString"></a>
# getAppliedFiltersString
getAppliedFiltersString(  ) &rarr; String

return documentation of any processes applied to the data within the
 DataSourceFilter. This will be an empty string when no processes were
 applied. See getFilters which specified which should be applied.

### Returns:
reduceDataSetString the string, which may be empty but will not
 be null.

<a href="https://github.com/autoplot/dev/search?q=getAppliedFiltersString&unscoped_q=getAppliedFiltersString">[search for examples]</a>

***
<a name="getCaching"></a>
# getCaching
getCaching(  ) &rarr; Caching



### Returns:
org.autoplot.datasource.capability.Caching


<a href="https://github.com/autoplot/dev/search?q=getCaching&unscoped_q=getCaching">[search for examples]</a>

***
<a name="getDataSet"></a>
# getDataSet
getDataSet(  ) &rarr; QDataSet



### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>

***
<a name="getDataSource"></a>
# getDataSource
getDataSource(  ) &rarr; DataSource

return the controller's current datasource. This was synchronized, but
 this would mean that external clients could not query what the current
 source was. Since this is only reading the variable, this seems harmless.
 Note, findbugs prompted the code change, not an observed bug. TODO: there
 is probably a better way to do this, synchronizing properly on several
 objects.

### Returns:
the controller's current datasource.

<a href="https://github.com/autoplot/dev/search?q=getDataSource&unscoped_q=getDataSource">[search for examples]</a>

***
<a name="getException"></a>
# getException
getException(  ) &rarr; Exception



### Returns:
java.lang.Exception


<a href="https://github.com/autoplot/dev/search?q=getException&unscoped_q=getException">[search for examples]</a>

***
<a name="getFillDataSet"></a>
# getFillDataSet
getFillDataSet(  ) &rarr; QDataSet



### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=getFillDataSet&unscoped_q=getFillDataSet">[search for examples]</a>

***
<a name="getFillProperties"></a>
# getFillProperties
getFillProperties(  ) &rarr; Map



### Returns:
java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getFillProperties&unscoped_q=getFillProperties">[search for examples]</a>

***
<a name="getHistogram"></a>
# getHistogram
getHistogram(  ) &rarr; QDataSet



### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=getHistogram&unscoped_q=getHistogram">[search for examples]</a>

***
<a name="getMaxSliceIndex"></a>
# <del>getMaxSliceIndex</del>
Deprecated: this is leftover from an ancient version of the code.
***
<a name="getProperties"></a>
# getProperties
getProperties(  ) &rarr; Map



### Returns:
java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getProperties&unscoped_q=getProperties">[search for examples]</a>

***
<a name="getRawProperties"></a>
# getRawProperties
getRawProperties(  ) &rarr; Map



### Returns:
java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getRawProperties&unscoped_q=getRawProperties">[search for examples]</a>

***
<a name="getTimeSeriesBrowseController"></a>
# getTimeSeriesBrowseController
getTimeSeriesBrowseController(  ) &rarr; TimeSeriesBrowseController



### Returns:
org.autoplot.dom.TimeSeriesBrowseController


<a href="https://github.com/autoplot/dev/search?q=getTimeSeriesBrowseController&unscoped_q=getTimeSeriesBrowseController">[search for examples]</a>

***
<a name="getTsb"></a>
# getTsb
getTsb(  ) &rarr; TimeSeriesBrowse



### Returns:
org.autoplot.datasource.capability.TimeSeriesBrowse


<a href="https://github.com/autoplot/dev/search?q=getTsb&unscoped_q=getTsb">[search for examples]</a>

***
<a name="getTsbSuri"></a>
# getTsbSuri
getTsbSuri(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getTsbSuri&unscoped_q=getTsbSuri">[search for examples]</a>

***
<a name="isDataSetNeedsLoading"></a>
# isDataSetNeedsLoading
isDataSetNeedsLoading(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isDataSetNeedsLoading&unscoped_q=isDataSetNeedsLoading">[search for examples]</a>

***
<a name="isPendingChanges"></a>
# isPendingChanges
isPendingChanges(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isPendingChanges&unscoped_q=isPendingChanges">[search for examples]</a>

***
<a name="isResetDimensions"></a>
# isResetDimensions
isResetDimensions(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isResetDimensions&unscoped_q=isResetDimensions">[search for examples]</a>

***
<a name="isTimeSeries"></a>
# isTimeSeries
isTimeSeries( QDataSet ds ) &rarr; boolean

return true if the dataset is rank 1 or greater, and has timetags for the
 xtagsDataSet. This will often be DEPEND_0, but for JoinDataSets which are
 like an array of datasets, each dataset would have DEPEND_0.

### Parameters:
ds - any dataset

### Returns:
true if the dataset is rank 1 or greater, and has timetags for
 the xtagsDataSet.

<a href="https://github.com/autoplot/dev/search?q=isTimeSeries&unscoped_q=isTimeSeries">[search for examples]</a>

***
<a name="isUriNeedsResolution"></a>
# isUriNeedsResolution
isUriNeedsResolution(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isUriNeedsResolution&unscoped_q=isUriNeedsResolution">[search for examples]</a>

***
<a name="pendingChanges"></a>
# pendingChanges
pendingChanges( java.util.Map changes ) &rarr; void



### Parameters:
changes - a java.util.Map

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=pendingChanges&unscoped_q=pendingChanges">[search for examples]</a>

***
<a name="resetDataSource"></a>
# resetDataSource
resetDataSource( boolean valueWasAdjusting, org.autoplot.datasource.DataSource dataSource ) &rarr; void

This might be considered the heart of the DataSourceController. This is
 where TimeSeriesBrowse is set up as well as Caching.

 This might also be a good spot to make sure we are not on the event
 thread, and this is being studied.

### Parameters:
valueWasAdjusting - true if the app was loading a vap, or locked because of changes.
<br>dataSource - a DataSource

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resetDataSource&unscoped_q=resetDataSource">[search for examples]</a>

***
<a name="resetSuri"></a>
# resetSuri
resetSuri( String suri, ProgressMonitor mon ) &rarr; void

Set the data source URI, forcing a reload if it is the same.

### Parameters:
suri - a String
<br>mon - a ProgressMonitor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resetSuri&unscoped_q=resetSuri">[search for examples]</a>

***
<a name="setAppliedFiltersString"></a>
# setAppliedFiltersString
setAppliedFiltersString( String appliedFilters ) &rarr; void

set the documentation of any processes applied to the data within the
 DataSourceFilter. This will be an empty string when no processes were
 applied. See getFilters which specified which should be applied.

### Parameters:
appliedFilters - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAppliedFiltersString&unscoped_q=setAppliedFiltersString">[search for examples]</a>

***
<a name="setCaching"></a>
# setCaching
setCaching( org.autoplot.datasource.capability.Caching caching ) &rarr; void



### Parameters:
caching - a Caching

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCaching&unscoped_q=setCaching">[search for examples]</a>

***
<a name="setDataSet"></a>
# setDataSet
setDataSet( QDataSet dataSet ) &rarr; void

see setDataSetInternal, which does autoranging, etc. TODO: fix this and
 the fillDataSet stuff...

### Parameters:
dataSet - a QDataSet

### Returns:
void (returns nothing)

### See Also:
<a href='#setDataSetInternal'>setDataSetInternal(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setDataSet&unscoped_q=setDataSet">[search for examples]</a>

***
<a name="setDataSetInternal"></a>
# setDataSetInternal
setDataSetInternal( QDataSet ds ) &rarr; void

set the dataset for the DataSourceFilter.

### Parameters:
ds - the dataset

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSetInternal&unscoped_q=setDataSetInternal">[search for examples]</a>

setDataSetInternal( QDataSet ds, java.util.Map rawProperties, boolean immediately ) &rarr; void<br>
***
<a name="setDataSetNeedsLoading"></a>
# setDataSetNeedsLoading
setDataSetNeedsLoading( boolean dataSetNeedsLoading ) &rarr; void



### Parameters:
dataSetNeedsLoading - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSetNeedsLoading&unscoped_q=setDataSetNeedsLoading">[search for examples]</a>

***
<a name="setDataSource"></a>
# setDataSource
setDataSource( org.autoplot.datasource.DataSource dataSource ) &rarr; void



### Parameters:
dataSource - a DataSource

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSource&unscoped_q=setDataSource">[search for examples]</a>

***
<a name="setException"></a>
# setException
setException( java.lang.Exception exception ) &rarr; void



### Parameters:
exception - an Exception

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setException&unscoped_q=setException">[search for examples]</a>

***
<a name="setFillDataSet"></a>
# setFillDataSet
setFillDataSet( QDataSet fillDataSet ) &rarr; void



### Parameters:
fillDataSet - a QDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFillDataSet&unscoped_q=setFillDataSet">[search for examples]</a>

***
<a name="setFillProperties"></a>
# setFillProperties
setFillProperties( java.util.Map fillProperties ) &rarr; void



### Parameters:
fillProperties - a java.util.Map

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFillProperties&unscoped_q=setFillProperties">[search for examples]</a>

***
<a name="setHistogram"></a>
# setHistogram
setHistogram( QDataSet histogram ) &rarr; void



### Parameters:
histogram - a QDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setHistogram&unscoped_q=setHistogram">[search for examples]</a>

***
<a name="setProperties"></a>
# setProperties
setProperties( java.util.Map properties ) &rarr; void



### Parameters:
properties - a java.util.Map

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setProperties&unscoped_q=setProperties">[search for examples]</a>

***
<a name="setRawProperties"></a>
# setRawProperties
setRawProperties( java.util.Map rawProperties ) &rarr; void



### Parameters:
rawProperties - a java.util.Map

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRawProperties&unscoped_q=setRawProperties">[search for examples]</a>

***
<a name="setResetDimensions"></a>
# setResetDimensions
setResetDimensions( boolean resetDimensions ) &rarr; void



### Parameters:
resetDimensions - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setResetDimensions&unscoped_q=setResetDimensions">[search for examples]</a>

***
<a name="setSuri"></a>
# setSuri
setSuri( String suri, ProgressMonitor mon ) &rarr; void

Set the data source URI.

### Parameters:
suri - a String
<br>mon - a ProgressMonitor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSuri&unscoped_q=setSuri">[search for examples]</a>

***
<a name="setTsb"></a>
# setTsb
setTsb( org.autoplot.datasource.capability.TimeSeriesBrowse tsb ) &rarr; void



### Parameters:
tsb - a TimeSeriesBrowse

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTsb&unscoped_q=setTsb">[search for examples]</a>

***
<a name="setTsbSuri"></a>
# setTsbSuri
setTsbSuri( String tsbSuri ) &rarr; void



### Parameters:
tsbSuri - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTsbSuri&unscoped_q=setTsbSuri">[search for examples]</a>

***
<a name="setUriNeedsResolution"></a>
# setUriNeedsResolution
setUriNeedsResolution( boolean uriNeedsResolution ) &rarr; void



### Parameters:
uriNeedsResolution - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUriNeedsResolution&unscoped_q=setUriNeedsResolution">[search for examples]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

***
<a name="update"></a>
# update
update(  ) &rarr; void

update the model and view using the new DataSource to create a new
 dataset. This calls update(false), indicating this was not triggered in
 response to a human event.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=update&unscoped_q=update">[search for examples]</a>

update( boolean user ) &rarr; void<br>
