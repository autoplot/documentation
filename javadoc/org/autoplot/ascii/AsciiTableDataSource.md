# org.autoplot.ascii.AsciiTableDataSource

DataSource for reading data in ASCII files, where each record is 
 one line of the file, and each record has the same number of fields.  
 This reads in each record and splits on the delimiter, which is typically
 guessed by examining the first 5 viable records.  This also supports
 combining times that are in several fields.  
 
 This also handles true CSV files, where a quoted field may contain a 
 newline character.  
 
 Last, a three or four column ASCII file containing two ISO8601 strings 
 for the first two columns is automatically treated as an "events list",
 a list of named intervals.

# AsciiTableDataSource( java.net.URI uri )
Creates a new instance of AsciiTableDataSource

***
<a name="PARAM_INTERVAL_TAG"></a>
# PARAM_INTERVAL_TAG



***
<a name="getDataSet"></a>
# getDataSet
getDataSet( ProgressMonitor mon ) &rarr; QDataSet



### Parameters:
mon - a ProgressMonitor

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMetadata"></a>
# getMetadata
getMetadata( ProgressMonitor mon ) &rarr; Map



### Parameters:
mon - a ProgressMonitor

### Returns:
java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getMetadata&unscoped_q=getMetadata">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parseColumns"></a>
# parseColumns
parseColumns( String s, int fieldCount ) &rarr; int

return a list of column names, supporting:<ul>
 <li>field1,field3,field5
 <li>field1,field3-field5
 <li>field1,field3:field5  exclusive
 </ul>

### Parameters:
s - a String
<br>fieldCount - an int

### Returns:
an int[]

### See Also:
<a href='#parseRangeStr'>parseRangeStr(java.lang.String, int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=parseColumns&unscoped_q=parseColumns">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

