# org.das2.qds.util.AsciiParser.RecordParser



***
<a name="fieldCount"></a>
# fieldCount
fieldCount(  ) &rarr; int

indicate the number of fields this RecordParser is 
 expecting on each line.

### Returns:
the field count.

<a href="https://github.com/autoplot/dev/search?q=fieldCount&unscoped_q=fieldCount">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

fieldCount( String line ) &rarr; int<br>
***
<a name="readNextRecord"></a>
# readNextRecord
readNextRecord( java.io.BufferedReader reader ) &rarr; String

return the next record in a String, or null of no more records exist.

### Parameters:
reader - a BufferedReader

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=readNextRecord&unscoped_q=readNextRecord">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="splitRecord"></a>
# splitRecord
splitRecord( String line, java.lang.String[] fields ) &rarr; boolean

attempts to extract fields from the record, returning true if
 the record could be split.

### Parameters:
line - the line from the file.
<br>fields - array to store the fields.  fieldCount() should be used
 to determine the length of the array.

### Returns:
true if the line is a record that can be split into fields.

<a href="https://github.com/autoplot/dev/search?q=splitRecord&unscoped_q=splitRecord">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="tryParseRecord"></a>
# tryParseRecord
tryParseRecord( String line, int irec, org.das2.qds.util.DataSetBuilder builder ) &rarr; boolean

returns true if the line appears to be a record.  If it is a record,
 then the record is inserted into the builder.

### Parameters:
line - the line from the file.
<br>irec - the record number
<br>builder - the builder into which the data is inserted.

### Returns:
true if the line appeared to be a record.

<a href="https://github.com/autoplot/dev/search?q=tryParseRecord&unscoped_q=tryParseRecord">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

