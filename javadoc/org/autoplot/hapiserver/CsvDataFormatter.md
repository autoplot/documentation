# org.autoplot.hapiserver.CsvDataFormatter

Comma Separated Value (CSV) formatter

# CsvDataFormatter( )


***
<a name="finalize"></a>
# finalize
finalize( java.io.OutputStream out ) &rarr; void



### Parameters:
out - an OutputStream

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=finalize&unscoped_q=finalize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="initializeReader"></a>
# initializeReader
initializeReader( JSONObject info, String record ) &rarr; QDataSet



### Parameters:
info - a JSONObject
<br>record - a String

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=initializeReader&unscoped_q=initializeReader">[search for examples]</a>

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

***
<a name="readRecord"></a>
# readRecord
readRecord( String record, QDataSet recordInfo ) &rarr; QDataSet

read a record which has been formatted by this.

### Parameters:
record - the formatted record.
<br>recordInfo - example record which provides the units for parsing.

### Returns:
the parsed record.

<a href="https://github.com/autoplot/dev/search?q=readRecord&unscoped_q=readRecord">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

