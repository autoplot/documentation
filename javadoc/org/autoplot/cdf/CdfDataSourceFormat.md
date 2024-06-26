# org.autoplot.cdf.CdfDataSourceFormat

Format the QDataSet into CDF tables, using Nand Lal's library.
 Datasets will be assigned names if they don't have a NAME property.
 If the append=T parameter is set, then variables should have names.
 if the bundle=T parameter is set, then bundles should be unbundled into separate variables.

# CdfDataSourceFormat( )


***
<a name="canFormat"></a>
# canFormat
canFormat( QDataSet ds ) &rarr; boolean



### Parameters:
ds - a QDataSet

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=canFormat&unscoped_q=canFormat">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="formatData"></a>
# formatData
formatData( String uri, QDataSet data, ProgressMonitor mon ) &rarr; void



### Parameters:
uri - a String
<br>data - a QDataSet
<br>mon - a ProgressMonitor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=formatData&unscoped_q=formatData">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDescription"></a>
# getDescription
getDescription(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getDescription&unscoped_q=getDescription">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="streamData"></a>
# streamData
streamData( java.util.Map params, java.util.Iterator data, java.io.OutputStream out ) &rarr; boolean



### Parameters:
params - a java.util.Map
<br>data - a java.util.Iterator
<br>out - an OutputStream

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=streamData&unscoped_q=streamData">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

