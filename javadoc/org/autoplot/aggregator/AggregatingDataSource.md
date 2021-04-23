# org.autoplot.aggregator.AggregatingDataSourceData Source that aggregates (or combines) the data from granule files containing 
 data for intervals.  For example, 
 https://cdaweb.gsfc.nasa.gov/istp_public/data/polar/hydra/hyd_h0/$Y/po_h0_hyd_$Y$m$d_v$v.cdf?ELECTRON_DIFFERENTIAL_ENERGY_FLUX&timerange=20000109
 is the aggregation of daily files from the CDAWeb.  This provides an 
 easy method for storing a long time series without having a complex 
 data server.
 
 The result of this is not guaranteed to be monotonically increasing in 
 time.  See https://sourceforge.net/p/autoplot/bugs/1326/
AggregatingDataSource( java.net.URI uri, org.autoplot.datasource.DataSourceFactory delegateFactory )
Creates a new instance of AggregatingDataSource

***
<a name="MSG_NO_FILES_FOUND"></a>
# MSG_NO_FILES_FOUND

message used when no files are found in the interval.

***
<a name="PARAM_AVAIL"></a>
# PARAM_AVAIL



***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void

Adds a PropertyChangeListener to the listener list.

### Parameters:
l - The listener to add.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSet"></a>
# getDataSet
getDataSet( ProgressMonitor mon ) &rarr; QDataSet

read the data.  This supports reference caching.

### Parameters:
mon - a ProgressMonitor

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getDataSet( ProgressMonitor mon, DatumRange lviewRange, Datum lresolution ) &rarr; QDataSet<br>
***
<a name="getFsm"></a>
# getFsm
getFsm(  ) &rarr; FileStorageModel



### Returns:
org.das2.fsm.FileStorageModel


<a href="https://github.com/autoplot/dev/search?q=getFsm&unscoped_q=getFsm">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMetadata"></a>
# getMetadata
getMetadata( ProgressMonitor mon ) &rarr; Map

returns the metadata provided by the first delegate dataset.

### Parameters:
mon - a ProgressMonitor

### Returns:
a java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getMetadata&unscoped_q=getMetadata">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMetadataModel"></a>
# getMetadataModel
getMetadataModel(  ) &rarr; MetadataModel



### Returns:
org.autoplot.datasource.MetadataModel


<a href="https://github.com/autoplot/dev/search?q=getMetadataModel&unscoped_q=getMetadataModel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getResolution"></a>
# getResolution
getResolution(  ) &rarr; Datum



### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getResolution&unscoped_q=getResolution">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getURI"></a>
# getURI
getURI(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getURI&unscoped_q=getURI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getViewRange"></a>
# getViewRange
getViewRange(  ) &rarr; DatumRange

Getter for property viewRange.

### Returns:
Value of property viewRange.

<a href="https://github.com/autoplot/dev/search?q=getViewRange&unscoped_q=getViewRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void

Removes a PropertyChangeListener from the listener list.

### Parameters:
l - The listener to remove.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFsm"></a>
# setFsm
setFsm( org.das2.fsm.FileStorageModel fsm ) &rarr; void



### Parameters:
fsm - a FileStorageModel

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFsm&unscoped_q=setFsm">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setParams"></a>
# setParams
setParams( String params ) &rarr; void

Setter for property args.

### Parameters:
params - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setParams&unscoped_q=setParams">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setResolution"></a>
# setResolution
setResolution( Datum resolution ) &rarr; void



### Parameters:
resolution - a Datum

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setResolution&unscoped_q=setResolution">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setViewRange"></a>
# setViewRange
setViewRange( DatumRange viewRange ) &rarr; void

Setter for property viewRange.

### Parameters:
viewRange - New value of property viewRange.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setViewRange&unscoped_q=setViewRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

