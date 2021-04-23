# org.das2.qstream.SimpleStreamFormatter

Class for formatting QDataSets as QStreams.  Although this is "SimpleStreamFormatter," this is the only formatter written
 thus far, except for SerialStreamFormatter, which formats packet-by-packet.

# SimpleStreamFormatter( )


***
<a name="format"></a>
# format
format( QDataSet ds, java.io.OutputStream osout, boolean asciiTypes ) &rarr; void

serialize the dataset to the output stream.  Presently most datasets can
 be serialized:<ul>
 <li> rank 0
 <li> rank 1
 <li> rank 2 qubes
 <li> array of rank 2 qubes
 <li> rank 3 qubes
 <li> bundle datasets.
 </ul>
 The design goal is that all datasets can be serialized using this formatter,
 however some schemas (e.g. high-rank non-qubes) will be inefficient.

### Parameters:
ds - the dataset to serialize.
<br>osout - the output stream, which will not be closed here.
<br>asciiTypes - use ascii format types so that the stream is completely ascii.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=format&unscoped_q=format">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

