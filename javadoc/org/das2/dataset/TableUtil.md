# org.das2.dataset.TableUtil
TableUtil( )


***
<a name="checkForNaN"></a>
# checkForNaN
checkForNaN( org.das2.dataset.TableDataSet tds ) &rarr; void



### Parameters:
tds - a TableDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=checkForNaN&unscoped_q=checkForNaN">[search for examples]</a>

***
<a name="closestDatum"></a>
# closestDatum
closestDatum( org.das2.dataset.TableDataSet table, Datum x, Datum y ) &rarr; Datum



### Parameters:
table - a TableDataSet
<br>x - a Datum
<br>y - a Datum

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=closestDatum&unscoped_q=closestDatum">[search for examples]</a>

***
<a name="closestRow"></a>
# closestRow
closestRow( org.das2.dataset.TableDataSet table, int itable, Datum datum ) &rarr; int



### Parameters:
table - a TableDataSet
<br>itable - an int
<br>datum - a Datum

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=closestRow&unscoped_q=closestRow">[search for examples]</a>

closestRow( org.das2.dataset.TableDataSet table, int itable, double x, Units units ) &rarr; int<br>
***
<a name="collapse"></a>
# collapse
collapse( org.das2.dataset.TableDataSet ds, int offset, int length ) &rarr; VectorDataSet



### Parameters:
ds - a TableDataSet
<br>offset - an int
<br>length - an int

### Returns:
org.das2.dataset.VectorDataSet


<a href="https://github.com/autoplot/dev/search?q=collapse&unscoped_q=collapse">[search for examples]</a>

***
<a name="dumpToAsciiStream"></a>
# dumpToAsciiStream
dumpToAsciiStream( org.das2.dataset.TableDataSet tds, Datum xmin, Datum xmax, java.io.OutputStream out ) &rarr; void



### Parameters:
tds - a TableDataSet
<br>xmin - a Datum
<br>xmax - a Datum
<br>out - an OutputStream

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dumpToAsciiStream&unscoped_q=dumpToAsciiStream">[search for examples]</a>

dumpToAsciiStream( org.das2.dataset.TableDataSet tds, java.io.OutputStream out ) &rarr; void<br>
dumpToAsciiStream( org.das2.dataset.TableDataSet tds, java.nio.channels.WritableByteChannel out ) &rarr; void<br>
***
<a name="dumpToBinaryStream"></a>
# dumpToBinaryStream
dumpToBinaryStream( org.das2.dataset.TableDataSet tds, java.io.OutputStream out ) &rarr; void



### Parameters:
tds - a TableDataSet
<br>out - an OutputStream

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dumpToBinaryStream&unscoped_q=dumpToBinaryStream">[search for examples]</a>

***
<a name="dumpToDas2Stream"></a>
# dumpToDas2Stream
dumpToDas2Stream( QDataSet tds, java.nio.channels.WritableByteChannel out, boolean asciiTransferTypes, boolean sendStreamDescriptor ) &rarr; void

Write das2stream directly from QDataSet.

### Parameters:
tds - rank 2 table or rank 3 join of tables.
<br>out - output channel which will receive the stream.
<br>asciiTransferTypes - if true then use ascii to transfer data.
<br>sendStreamDescriptor - if true send the stream header, if false don't output it.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dumpToDas2Stream&unscoped_q=dumpToDas2Stream">[search for examples]</a>

dumpToDas2Stream( org.das2.dataset.TableDataSet tds, java.nio.channels.WritableByteChannel out, boolean asciiTransferTypes, boolean sendStreamDescriptor ) &rarr; void<br>
***
<a name="getDatumVector"></a>
# getDatumVector
getDatumVector( org.das2.dataset.TableDataSet tds, int i ) &rarr; DatumVector



### Parameters:
tds - a TableDataSet
<br>i - an int

### Returns:
org.das2.datum.DatumVector


<a href="https://github.com/autoplot/dev/search?q=getDatumVector&unscoped_q=getDatumVector">[search for examples]</a>

***
<a name="getLargestYTag"></a>
# getLargestYTag
getLargestYTag( org.das2.dataset.TableDataSet tds ) &rarr; Datum



### Parameters:
tds - a TableDataSet

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getLargestYTag&unscoped_q=getLargestYTag">[search for examples]</a>

***
<a name="getNextRow"></a>
# getNextRow
getNextRow( org.das2.dataset.TableDataSet ds, int itable, Datum datum ) &rarr; int

return the first row after the datum.  Handles mono decreasing.

### Parameters:
ds - a TableDataSet
<br>itable - an int
<br>datum - a Datum

### Returns:
the row which is greater than or equal to the datum

<a href="https://github.com/autoplot/dev/search?q=getNextRow&unscoped_q=getNextRow">[search for examples]</a>

***
<a name="getPreviousRow"></a>
# getPreviousRow
getPreviousRow( org.das2.dataset.TableDataSet ds, int itable, Datum datum ) &rarr; int

return the first row before the datum.  Handles mono decreasing.

### Parameters:
ds - a TableDataSet
<br>itable - an int
<br>datum - a Datum

### Returns:
the row which is less than or equal to the datum

<a href="https://github.com/autoplot/dev/search?q=getPreviousRow&unscoped_q=getPreviousRow">[search for examples]</a>

***
<a name="getSmallestYTag"></a>
# getSmallestYTag
getSmallestYTag( org.das2.dataset.TableDataSet tds ) &rarr; Datum



### Parameters:
tds - a TableDataSet

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getSmallestYTag&unscoped_q=getSmallestYTag">[search for examples]</a>

***
<a name="getYTagArrayDouble"></a>
# getYTagArrayDouble
getYTagArrayDouble( org.das2.dataset.TableDataSet table, int itable, Units units ) &rarr; double



### Parameters:
table - a TableDataSet
<br>itable - an int
<br>units - an Units

### Returns:
double[]


<a href="https://github.com/autoplot/dev/search?q=getYTagArrayDouble&unscoped_q=getYTagArrayDouble">[search for examples]</a>

***
<a name="getYTagsDatumVector"></a>
# getYTagsDatumVector
getYTagsDatumVector( org.das2.dataset.TableDataSet tds, int itable ) &rarr; DatumVector



### Parameters:
tds - a TableDataSet
<br>itable - an int

### Returns:
org.das2.datum.DatumVector


<a href="https://github.com/autoplot/dev/search?q=getYTagsDatumVector&unscoped_q=getYTagsDatumVector">[search for examples]</a>

***
<a name="guessYTagWidth"></a>
# guessYTagWidth
guessYTagWidth( org.das2.dataset.TableDataSet table ) &rarr; Datum



### Parameters:
table - a TableDataSet

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=guessYTagWidth&unscoped_q=guessYTagWidth">[search for examples]</a>

guessYTagWidth( org.das2.dataset.TableDataSet table, int itable ) &rarr; Datum<br>
***
<a name="tableIndexAt"></a>
# tableIndexAt
tableIndexAt( org.das2.dataset.TableDataSet table, int i ) &rarr; int



### Parameters:
table - a TableDataSet
<br>i - an int

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=tableIndexAt&unscoped_q=tableIndexAt">[search for examples]</a>

***
<a name="tableMax"></a>
# tableMax
tableMax( org.das2.dataset.TableDataSet tds, Units units ) &rarr; double



### Parameters:
tds - a TableDataSet
<br>units - an Units

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=tableMax&unscoped_q=tableMax">[search for examples]</a>

***
<a name="toString"></a>
# toString
toString( org.das2.dataset.TableDataSet tds ) &rarr; String



### Parameters:
tds - a TableDataSet

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

