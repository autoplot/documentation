# org.autoplot.datasource.DefaultTimeSeriesBrowse

Default implementation commonly found, which handles the resolution parameter
 but doesn't implement it.  This uses URISplit.PARAM_TIME_RANGE='timerange' 
 and URISplit.PARAM_TIME_RESOLUTION='resolution'
 for representing the TSB state.

# DefaultTimeSeriesBrowse( )


***
<a name="uri"></a>
# uri



***
<a name="blurURI"></a>
# blurURI
blurURI(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=blurURI&unscoped_q=blurURI">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="create"></a>
# create
create( String uri, String timerange ) &rarr; TimeSeriesBrowse

create the TimeSeriesBrowse with the initial URI which may contain the
 parameter "timerange."  The timerange may also be specified using the 
 second parameter.

### Parameters:
uri - the URI
<br>timerange - if non-null, then reset with this timerange.

### Returns:
TimeSeriesBrowse implementation.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/datum/DatumRangeUtil.md#parseTimeRange'>org.das2.datum.DatumRangeUtil#parseTimeRange(java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTimeRange"></a>
# getTimeRange
getTimeRange(  ) &rarr; DatumRange



### Returns:
org.das2.datum.DatumRange


<a href="https://github.com/autoplot/dev/search?q=getTimeRange&unscoped_q=getTimeRange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTimeResolution"></a>
# getTimeResolution
getTimeResolution(  ) &rarr; Datum



### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getTimeResolution&unscoped_q=getTimeResolution">[search for examples]</a>
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
<a name="reject"></a>
# reject
reject( java.util.Map map, java.util.List problems ) &rarr; boolean



### Parameters:
map - a java.util.Map
<br>problems - a java.util.List

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=reject&unscoped_q=reject">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTimeRange"></a>
# setTimeRange
setTimeRange( DatumRange dr ) &rarr; void



### Parameters:
dr - a DatumRange

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTimeRange&unscoped_q=setTimeRange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTimeResolution"></a>
# setTimeResolution
setTimeResolution( Datum d ) &rarr; void



### Parameters:
d - a Datum

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTimeResolution&unscoped_q=setTimeResolution">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setURI"></a>
# setURI
setURI( String suri ) &rarr; void



### Parameters:
suri - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setURI&unscoped_q=setURI">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

