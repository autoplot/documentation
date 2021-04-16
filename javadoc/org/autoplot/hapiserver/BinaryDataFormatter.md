# org.autoplot.hapiserver.BinaryDataFormatterFormat to binary types.  Note that TransferTypes use doubles to communicate,
 so floating point numbers may not format precisely.
BinaryDataFormatter( )


***
<a name="finalize"></a>
# finalize
finalize( java.io.OutputStream out ) &rarr; void

perform any final operations to the stream.  This 
 DOES NOT close the stream!

### Parameters:
out - an OutputStream

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=finalize&unscoped_q=finalize">[search for examples]</a>

***
<a name="initialize"></a>
# initialize
initialize( JSONObject info, java.io.OutputStream out, QDataSet record ) &rarr; void



### Parameters:
info - a JSONObject
<br>out - an OutputStream
<br>record - a QDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=initialize&unscoped_q=initialize">[search for examples]</a>

***
<a name="sendRecord"></a>
# sendRecord
sendRecord( java.io.OutputStream out, QDataSet record ) &rarr; void



### Parameters:
out - an OutputStream
<br>record - a QDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=sendRecord&unscoped_q=sendRecord">[search for examples]</a>

