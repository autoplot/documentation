# org.das2.dataset.DataSetStreamProducerConfigurable class for serializing a DataSet into a das2Stream.  This class
 handles both VectorDataSets and TableDataSets, and uses java beans properties
 to control how the stream is produced.  This code subsumes the functionality
 of TableUtil.dumpToDas2Stream and VectorUtil.dumpToDas2Stream.
DataSetStreamProducer( )
Creates a new instance of DataSetStreamProducer

***
<a name="getDataSet"></a>
# getDataSet
getDataSet(  ) &rarr; DataSet

Getter for property dataSet.

### Returns:
Value of property dataSet.

<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isAsciiTransferTypes"></a>
# isAsciiTransferTypes
isAsciiTransferTypes(  ) &rarr; boolean

Getter for property asciiTransferTypes.

### Returns:
Value of property asciiTransferTypes.

<a href="https://github.com/autoplot/dev/search?q=isAsciiTransferTypes&unscoped_q=isAsciiTransferTypes">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isCompressed"></a>
# isCompressed
isCompressed(  ) &rarr; boolean

Getter for property compressed.

### Returns:
Value of property compressed.

<a href="https://github.com/autoplot/dev/search?q=isCompressed&unscoped_q=isCompressed">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAsciiTransferTypes"></a>
# setAsciiTransferTypes
setAsciiTransferTypes( boolean asciiTransferTypes ) &rarr; void

If true, use ascii-type transfer types when creating the stream, so the 
 stream is more easily read by humans and stream-naive parsers.

### Parameters:
asciiTransferTypes - New value of property asciiTransferTypes.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAsciiTransferTypes&unscoped_q=setAsciiTransferTypes">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setCompressed"></a>
# setCompressed
setCompressed( boolean compressed ) &rarr; void

If true, create a compressed stream.

### Parameters:
compressed - New value of property compressed.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCompressed&unscoped_q=setCompressed">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataSet"></a>
# setDataSet
setDataSet( org.das2.dataset.DataSet dataSet ) &rarr; void

Setter for property dataSet.

### Parameters:
dataSet - New value of property dataSet.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSet&unscoped_q=setDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="writeStream"></a>
# writeStream
writeStream( java.io.OutputStream out ) &rarr; void

convenient method for writing to an OutputStream.  Simply
 uses Channels.newChannel to create a WritableByteChannel.

### Parameters:
out - an OutputStream

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeStream&unscoped_q=writeStream">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

writeStream( java.nio.channels.WritableByteChannel out ) &rarr; void<br>
