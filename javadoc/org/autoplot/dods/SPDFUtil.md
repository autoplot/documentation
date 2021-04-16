# org.autoplot.dods.SPDFUtilstatic methods for helping to use the SPDF dods server.
SPDFUtil( )


***
<a name="interpretAttributes"></a>
# interpretAttributes
interpretAttributes( org.autoplot.dods.DodsAdapter da ) &rarr; void

set up the DodsAdapter based on the metadata returned from the dods server,
 interpreting the metadata provided by the SPDF server.

### Parameters:
da - a DodsAdapter

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=interpretAttributes&unscoped_q=interpretAttributes">[search for examples]</a>

***
<a name="interpretProps"></a>
# interpretProps
interpretProps( java.util.Map attr ) &rarr; Map

return the properties in a canonical way.  Presumably this will be done for other data sources, to unify the metadata for use with das2.
 For keys supported, see QDataSet.

### Parameters:
attr - a java.util.Map

### Returns:
a Map of the properties.

<a href="https://github.com/autoplot/dev/search?q=interpretProps&unscoped_q=interpretProps">[search for examples]</a>

