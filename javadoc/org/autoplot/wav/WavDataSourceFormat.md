# org.autoplot.wav.WavDataSourceFormat

Format data to binary wav file.  The wav file format contains metadata in the first bytes, 
 and then the data as interleaved channels.  Java AudioFormat is used to format the header,
 and the BinaryDataSource is used to format the rest of the wav file.

# WavDataSourceFormat( )


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

