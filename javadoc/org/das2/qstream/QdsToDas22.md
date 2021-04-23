# org.das2.qstream.QdsToDas22Write QDataSets that vary over at most 2 independent variables as a Das2 
 stream.
 Since Das2 streams can have at most 2 independent variables, higher
 dimensional (not necessarily higher rank) QDataSets can't be written using
 this code.  Streams that can be written have the following plane structure
 
   X Y [Y Y Y Y ... ]
   X YScan [YScan YScan YScan ... ]
   X Y Z [Z Z Z Z ... ]
 
 All binary output is streamed in machine-native order.  Since datasets written
 on one architecture are most likely to be read on the same architecture this
 choice causes the least amount of byte swapping.  
 
 This is a direct serialization of QDataSet and does not require any legacy
 das2 dataset classes such as VectorDataset or TableDataset.
QdsToDas22( )


QdsToDas22( int genSigDigits, int fracSecDigits )


***
<a name="canWrite"></a>
# canWrite
canWrite( QDataSet qds ) &rarr; boolean

Determine if a given dataset be serialized as a das2.2 stream

### Parameters:
qds - The dataset to write

### Returns:
true if this dataset can be serialized as a das2.2 stream, false
         otherwise

<a href="https://github.com/autoplot/dev/search?q=canWrite&unscoped_q=canWrite">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="write"></a>
# write
write( QDataSet qds, java.io.OutputStream os ) &rarr; boolean

Write a QDataSet as a das2.2 stream
 
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

