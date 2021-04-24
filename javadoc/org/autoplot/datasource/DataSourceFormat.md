# org.autoplot.datasource.DataSourceFormat



***
<a name="canFormat"></a>
# canFormat
canFormat( QDataSet ds ) &rarr; boolean

return true if the dataset can be formatted

### Parameters:
ds - a QDataSet

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=canFormat&unscoped_q=canFormat">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="formatData"></a>
# formatData
formatData( String uri, QDataSet data, ProgressMonitor mon ) &rarr; void

Format the dataset using the specified URI.  This should be parsed the same way 
 read URIs are parsed, and arguments should reflect those of the reader 
 when possible.  If the uri refers to a file and the folder which will contain
 the file does not exist, it should be created.

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

return a description of this format

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getDescription&unscoped_q=getDescription">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

