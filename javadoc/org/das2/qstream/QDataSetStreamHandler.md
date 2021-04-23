# org.das2.qstream.QDataSetStreamHandlerreads a stream and produces QDataSets representing the data found on the stream. The stream is read in, and
 then getDataSet or getDataSet(name) is called to retrieve datasets.
QDataSetStreamHandler( )


***
<a name="BUILDER_JOIN_CHILDREN"></a>
# BUILDER_JOIN_CHILDREN



***
<a name="flattenJoin"></a>
# flattenJoin
flattenJoin( QDataSet ds ) &rarr; MutablePropertyDataSet

since an appended series of rank 1 datasets will return as a rank 2 join, this utility provides a
 standard place to flatten it. This will also flatten DEPENDNAME_0.

### Parameters:
ds - rank 2 or 3 join dataset.

### Returns:
rank 1 or 2 dataset.

<a href="https://github.com/autoplot/dev/search?q=flattenJoin&unscoped_q=flattenJoin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSet"></a>
# getDataSet
getDataSet( String name ) &rarr; QDataSet

return the dataset from the stream.

### Parameters:
name - the name of the dataset to retrieve.

### Returns:
the dataset

<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getDataSet(  ) &rarr; QDataSet<br>
***
<a name="getDataSetNames"></a>
# getDataSetNames
getDataSetNames(  ) &rarr; List

return a list of available datasets

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=getDataSetNames&unscoped_q=getDataSetNames">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSetNamesAndDescriptions"></a>
# getDataSetNamesAndDescriptions
getDataSetNamesAndDescriptions(  ) &rarr; Map

return a list of available datasets and their label (or name if not available).

### Returns:
a java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getDataSetNamesAndDescriptions&unscoped_q=getDataSetNamesAndDescriptions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getReadPackets"></a>
# getReadPackets
getReadPackets(  ) &rarr; boolean

if true, then packets are interpreted.

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=getReadPackets&unscoped_q=getReadPackets">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isFlattenableJoin"></a>
# isFlattenableJoin
isFlattenableJoin( QDataSet ds ) &rarr; boolean

If the dataset is a join of appendable datasets, then we can append them to reduce the rank by 1 and
 make one long time series. These datasets should be equivalent, however most of the system doesn't
 implement this (and probably never will). So this is a bit of a kludge, where I don't want to flatten a
 dataset automatically, but we probably want to.

### Parameters:
ds - a join dataset of rank 2 or rank 3.

### Returns:
true if the data can be joined.

<a href="https://github.com/autoplot/dev/search?q=isFlattenableJoin&unscoped_q=isFlattenableJoin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="packet"></a>
# packet
packet( org.das2.qstream.PacketDescriptor pd, java.nio.ByteBuffer data ) &rarr; void



### Parameters:
pd - a PacketDescriptor
<br>data - a ByteBuffer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=packet&unscoped_q=packet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="packetDescriptor"></a>
# packetDescriptor
packetDescriptor( org.das2.qstream.PacketDescriptor pd ) &rarr; void



### Parameters:
pd - a PacketDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=packetDescriptor&unscoped_q=packetDescriptor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setReadPackets"></a>
# setReadPackets
setReadPackets( boolean val ) &rarr; void

set this is false if you just want to look at the empty dataset metadata.

### Parameters:
val - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setReadPackets&unscoped_q=setReadPackets">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="streamClosed"></a>
# streamClosed
streamClosed( org.das2.qstream.StreamDescriptor sd ) &rarr; void



### Parameters:
sd - a StreamDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=streamClosed&unscoped_q=streamClosed">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="streamComment"></a>
# streamComment
streamComment( org.das2.qstream.StreamComment se ) &rarr; void



### Parameters:
se - a StreamComment

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=streamComment&unscoped_q=streamComment">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="streamDescriptor"></a>
# streamDescriptor
streamDescriptor( org.das2.qstream.StreamDescriptor sd ) &rarr; void



### Parameters:
sd - a StreamDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=streamDescriptor&unscoped_q=streamDescriptor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="streamException"></a>
# streamException
streamException( org.das2.qstream.StreamException se ) &rarr; void



### Parameters:
se - a StreamException

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=streamException&unscoped_q=streamException">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

