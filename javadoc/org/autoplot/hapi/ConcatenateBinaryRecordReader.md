# org.autoplot.hapi.ConcatenateBinaryRecordReader

concatenates multiple readers so that they appear as one reader.

# ConcatenateBinaryRecordReader( )


***
<a name="close"></a>
# close
close(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=close&unscoped_q=close">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="concatenateReader"></a>
# concatenateReader
concatenateReader( org.autoplot.hapi.AbstractBinaryRecordReader r ) &rarr; void

add the reader to the readers, so that this reader will be used after the
 others are used.

### Parameters:
r - an AbstractBinaryRecordReader

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=concatenateReader&unscoped_q=concatenateReader">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readRecord"></a>
# readRecord
readRecord( java.nio.ByteBuffer buf ) &rarr; int



### Parameters:
buf - a ByteBuffer

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=readRecord&unscoped_q=readRecord">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

