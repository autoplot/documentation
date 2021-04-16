# org.autoplot.binarydatasource.BinaryDataSourceBinaryDataSource returns data backed by binary data files.  Data
 is downloaded using the usual mechanisms, then mapped into memory
 using Java NIO, and presented as a QDataSet using BufferDataSet.
BinaryDataSource( java.net.URI uri )


***
<a name="getDataSet"></a>
# getDataSet
getDataSet( ProgressMonitor mon ) &rarr; QDataSet



### Parameters:
mon - a ProgressMonitor

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>

***
<a name="parseRecFormat"></a>
# parseRecFormat
parseRecFormat( String recFormat ) &rarr; Object

returns [ int[] offsets, Object[] types, Integer count, Integer recSizeBytes ].

### Parameters:
recFormat - a String

### Returns:
a java.lang.Object[]


<a href="https://github.com/autoplot/dev/search?q=parseRecFormat&unscoped_q=parseRecFormat">[search for examples]</a>

