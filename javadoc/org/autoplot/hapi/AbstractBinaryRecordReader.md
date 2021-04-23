# org.autoplot.hapi.AbstractBinaryRecordReader

read data record-by-record, so the client doesn't need to worry if the file
 is local or coming from the network.

***
<a name="readRecord"></a>
# readRecord
readRecord( java.nio.ByteBuffer buf ) &rarr; int

read data to fill the buffer, or return null if no more data
 is available.

### Parameters:
buf - a ByteBuffer

### Returns:
the number of bytes read, which will be the length of the buffer or -1.

<a href="https://github.com/autoplot/dev/search?q=readRecord&unscoped_q=readRecord">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

