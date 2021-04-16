# org.autoplot.datasource.capability.CachingCaching allows datasets to cache other URIs along with the one requested.
 For example, a Jython script is executed resulting in four datasets being
 calculated.  Since the URI must only correspond to one dataset, only one of
 the datasets is used, but instead of throwing out the result, we keep them
 around in case the client wants to plot a related URI.
***
<a name="reset"></a>
# reset
reset(  ) &rarr; void

reset any internal storage, and any subsequent calls should return false
 to satisfies.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reset&unscoped_q=reset">[search for examples]</a>

***
<a name="resetURI"></a>
# resetURI
resetURI( String surl ) &rarr; void

Set the DataSource's URI to this new one.  This must be a URI where
 satisifies() is true.

### Parameters:
surl - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resetURI&unscoped_q=resetURI">[search for examples]</a>

***
<a name="satisfies"></a>
# satisfies
satisfies( String surl ) &rarr; boolean

return true if the DataSource is able to quickly resolve the data set.

### Parameters:
surl - a String

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=satisfies&unscoped_q=satisfies">[search for examples]</a>

