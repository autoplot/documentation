# org.das2.dataset.VectorUtil
VectorUtil( )


***
<a name="closestXTag"></a>
# closestXTag
closestXTag( org.das2.dataset.DataSet ds, Datum datum ) &rarr; int



### Parameters:
ds - a DataSet
<br>datum - a Datum

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=closestXTag&unscoped_q=closestXTag">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

closestXTag( org.das2.dataset.DataSet ds, double x, Units units ) &rarr; int<br>
***
<a name="dumpToAsciiStream"></a>
# dumpToAsciiStream
dumpToAsciiStream( org.das2.dataset.VectorDataSet vds, Datum xmin, Datum xmax, java.io.OutputStream out ) &rarr; void



### Parameters:
vds - a VectorDataSet
<br>xmin - a Datum
<br>xmax - a Datum
<br>out - an OutputStream

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dumpToAsciiStream&unscoped_q=dumpToAsciiStream">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

dumpToAsciiStream( org.das2.dataset.VectorDataSet vds, java.io.OutputStream out ) &rarr; void<br>
dumpToAsciiStream( org.das2.dataset.VectorDataSet vds, java.nio.channels.WritableByteChannel out ) &rarr; void<br>
***
<a name="dumpToBinaryStream"></a>
# dumpToBinaryStream
dumpToBinaryStream( org.das2.dataset.VectorDataSet vds, java.io.OutputStream out ) &rarr; void



### Parameters:
vds - a VectorDataSet
<br>out - an OutputStream

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dumpToBinaryStream&unscoped_q=dumpToBinaryStream">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="dumpToDas2Stream"></a>
# dumpToDas2Stream
dumpToDas2Stream( org.das2.dataset.VectorDataSet vds, java.nio.channels.WritableByteChannel out, boolean asciiTransferTypes, boolean sendStreamDescriptor ) &rarr; void

write the data to a das2Stream

### Parameters:
vds - a VectorDataSet
<br>out - a WritableByteChannel
<br>asciiTransferTypes - a boolean
<br>sendStreamDescriptor - if false, then don't send the stream and don't close

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dumpToDas2Stream&unscoped_q=dumpToDas2Stream">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="finiteDerivative"></a>
# finiteDerivative
finiteDerivative( org.das2.dataset.VectorDataSet ds, int n ) &rarr; VectorDataSet

Return the finite difference derivative of the dataset, between elements that
 are n steps apart.
 Because we don't have a general-purpose way to divide units, the units returned
 are dimensionless.

### Parameters:
ds - a VectorDataSet
<br>n - an int

### Returns:
org.das2.dataset.VectorDataSet


<a href="https://github.com/autoplot/dev/search?q=finiteDerivative&unscoped_q=finiteDerivative">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getXTagArrayDouble"></a>
# getXTagArrayDouble
getXTagArrayDouble( org.das2.dataset.DataSet vds, Units units ) &rarr; double



### Parameters:
vds - a DataSet
<br>units - an Units

### Returns:
double[]


<a href="https://github.com/autoplot/dev/search?q=getXTagArrayDouble&unscoped_q=getXTagArrayDouble">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="median"></a>
# median
median( org.das2.dataset.VectorDataSet ds ) &rarr; Datum



### Parameters:
ds - a VectorDataSet

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=median&unscoped_q=median">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reduce2D"></a>
# reduce2D
reduce2D( QDataSet xds, QDataSet ds, int start, int finish, Datum xLimit, Datum yLimit ) &rarr; QDataSet

produce a simpler version of the dataset by averaging adjacent data.
 code taken from org.das2.graph.GraphUtil.reducePath.  Adjacent points are
 averaged together until a point is found that is not in the bin, and then
 a new bin is started.  The bin's lower bounds are integer multiples
 of xLimit and yLimit.

 If yLimit is null, then averaging is done for all points in the x bin,
 regardless of how close they are in Y.  This is similarly true when
 xLimit is null.

 xLimit and yLimit are rank 0 datasets, so that they can indicate that binning
 should be done in log space rather than linear.  In this case, a SCALE_TYPE
 for the dataset should be "log" and its unit should be convertible to
 Units.logERatio (for example, Units.log10Ratio or Units.percentIncrease).
 Note when either is log, then averaging is done in the log space.

### Parameters:
xds - the x tags
<br>ds - the y tags
<br>start - first index.
<br>finish - last (non-inclusive) index.
<br>xLimit - the size of the bins or null to indicate no limit.
<br>yLimit - the size of the bins or null to indicate no limit.

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=reduce2D&unscoped_q=reduce2D">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString( org.das2.dataset.VectorDataSet ds ) &rarr; String



### Parameters:
ds - a VectorDataSet

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

