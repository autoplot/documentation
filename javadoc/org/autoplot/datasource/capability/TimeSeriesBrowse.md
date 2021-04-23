# org.autoplot.datasource.capability.TimeSeriesBrowseThis capability allows DataSources that know how to produce data sets
 from a long time series to provide views of the DataSource for different
 times and resolutions.
 
 The getURI() method of the DataSource should return the original URI and
 getDataSet should return the original dataset.  getURI if TimeSeriesBrowse
 should return the URI for the range and resolution specified.

 Note DataSources providing this capability must insert CacheTags into the
 QDataSets they produce.
***
<a name="PROB_NO_TIMERANGE_PROVIDED"></a>
# PROB_NO_TIMERANGE_PROVIDED

problem message to use in reject when the timerange was not provided in the URI.

***
<a name="PROB_PARSE_ERROR_IN_TIMERANGE"></a>
# PROB_PARSE_ERROR_IN_TIMERANGE

problem message to use in reject when the timerange does not parse properly.

***
<a name="blurURI"></a>
# blurURI
blurURI(  ) &rarr; String

return the URI without the timeSeriesBrowse settings, for use in .vap files and where the 
 timerange is set elsewhere.

### Returns:
the URI simplified by removing the timerange and resolution.

<a href="https://github.com/autoplot/dev/search?q=blurURI&unscoped_q=blurURI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTimeRange"></a>
# getTimeRange
getTimeRange(  ) &rarr; DatumRange

get the time range for the current view of the timeseries.  Note this 
 may not be the same as getTimeRange

### Returns:
the current time range.

<a href="https://github.com/autoplot/dev/search?q=getTimeRange&unscoped_q=getTimeRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTimeResolution"></a>
# getTimeResolution
getTimeResolution(  ) &rarr; Datum

get the resolution for the current view of the timeseries.  Note this
 may not be the same as setTimeResolution.  Also, this may be null, indicating
 the native resolution is used.

### Returns:
the resolution for the current view of the timeseries.

<a href="https://github.com/autoplot/dev/search?q=getTimeResolution&unscoped_q=getTimeResolution">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getURI"></a>
# getURI
getURI(  ) &rarr; String

return the URI for the current time range and resolution.  This is also
 used to identify the dataset, so the same urls returned from here must
 return the same dataset!

### Returns:
the URI to load this data.

<a href="https://github.com/autoplot/dev/search?q=getURI&unscoped_q=getURI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTimeRange"></a>
# setTimeRange
setTimeRange( DatumRange dr ) &rarr; void

set the time range for the desired view of the timeseries.

### Parameters:
dr - the new time range.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTimeRange&unscoped_q=setTimeRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTimeResolution"></a>
# setTimeResolution
setTimeResolution( Datum d ) &rarr; void

set the resolution for the desired view of the timeseries.

### Parameters:
d - the time resolution

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTimeResolution&unscoped_q=setTimeResolution">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setURI"></a>
# setURI
setURI( String suri ) &rarr; void

Added in effort to make it easier to set the timerange if we have a timerange already.  This
 allows the timerange part of the URI to be set without having to understand the rest of it.
 set the URI, and possibly the timerange part.

### Parameters:
suri - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setURI&unscoped_q=setURI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

