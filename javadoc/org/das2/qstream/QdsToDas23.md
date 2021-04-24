# org.das2.qstream.QdsToDas23

Write QDataSets that vary over at most 3 independent variables as a Das2 
 stream.
 
 This is the general structure of arrays streamed in a das2.3 stream
 
 x [yset yset ...] [y y ...] [zset zset ...] [z z ...] [wset wset ...] [w w ...]
 
 Though it's unlikely that all possible components will ever be needed to
 describe a single dataset.
 
 All binary output is streamed in machine-native order.  Since datasets written
 on one architecture are most likely to be read on the same architecture this
 choice causes the least amount of byte swapping.  
 
 This is a direct serialization of QDataSet and does not require any legacy
 das2 classes

# QdsToDas23( )


# QdsToDas23( int genSigDigits, int fracSecDigits )


***
<a name="OFFSET_1"></a>
# OFFSET_1



***
<a name="OFFSET_2"></a>
# OFFSET_2



***
<a name="OFFSET_3"></a>
# OFFSET_3



***
<a name="REFERENCE"></a>
# REFERENCE



***
<a name="AXIS"></a>
# AXIS



***
<a name="DEF_SEQ_JITTER"></a>
# DEF_SEQ_JITTER



***
<a name="canWrite"></a>
# canWrite
canWrite( QDataSet qds ) &rarr; boolean

Determine if a given dataset be serialized as a das2.3/basic stream

### Parameters:
qds - The dataset to write

### Returns:
true if this dataset can be serialized as a das2.3/basic stream,
         false otherwise

<a href="https://github.com/autoplot/dev/search?q=canWrite&unscoped_q=canWrite">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="write"></a>
# write
write( QDataSet qds, java.io.OutputStream os ) &rarr; boolean

Write a QDataSet as a das2.3 stream
 
 To test whether it looks like this code could stream a dataset use the
 canWrite() function.  This function may be called multiple times to add
 additional data to the stream.  If a compatible header has already been
 emitted for a particular dataset it is not re-sent.

### Parameters:
qds - The dataset to write, may have join's bundles etc. but no
        rank 3 or higher component datasets.
<br>os - an open output stream, which is not closed by this code.

### Returns:
true if the entire dataset could be written, false otherwise.
         IO failures do not return false, they throw.  False simply 
         means that this code does not know how (or can't) stream the 
         given dataset.  Since deeper inspection occurs when actually
         writing the data then when testing, false may be returned even
         if canWrite() returned true.

<a href="https://github.com/autoplot/dev/search?q=write&unscoped_q=write">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

