# org.das2.dataset.parser.VectorDataSetParserClass for reading ascii tables into a VectorDataSet.  This parses a
 file by looking at each line to see if it matches one of
 two Patterns: one for properties and one for records.  If a record matched,
 then the record is matched and fields pulled out, parsed and insered a
 VectorDataSetBuilder.  If a property is matched, then the builder property
 is set.  Two Patterns are provided NAME_COLON_VALUE_PATTERN and
 NAME_EQUAL_VALUE_PATTERN for convenience.  The record pattern is currently
 the number of fields identified with whitespace in between.  Note the X
 tags are just the record numbers.
***
<a name="NAME_COLON_VALUE_PATTERN"></a>
# NAME_COLON_VALUE_PATTERN



***
<a name="NAME_EQUAL_VALUE_PATTERN"></a>
# NAME_EQUAL_VALUE_PATTERN



***
<a name="guessFieldCount"></a>
# guessFieldCount
guessFieldCount( String filename ) &rarr; int

return the field count that would result in the largest number of records parsed.  The 
 entire file is scanned, and for each line the number of decimal fields is counted.  At the end
 of the scan, the fieldCount with the highest record count is returned.

### Parameters:
filename - a String

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=guessFieldCount&unscoped_q=guessFieldCount">[search for examples]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

***
<a name="newParser"></a>
# newParser
newParser( int fieldCount ) &rarr; VectorDataSetParser

creates a parser with @param fieldCount fields, named "field0,...,fieldN"

### Parameters:
fieldCount - an int

### Returns:
org.das2.dataset.parser.VectorDataSetParser


<a href="https://github.com/autoplot/dev/search?q=newParser&unscoped_q=newParser">[search for examples]</a>

newParser( java.lang.String[] fieldNames ) &rarr; VectorDataSetParser<br>
***
<a name="readFile"></a>
# readFile
readFile( String filename ) &rarr; VectorDataSet

Parse the file using the current settings.

### Parameters:
filename - a String

### Returns:
org.das2.dataset.VectorDataSet


<a href="https://github.com/autoplot/dev/search?q=readFile&unscoped_q=readFile">[search for examples]</a>

***
<a name="readStream"></a>
# readStream
readStream( java.io.InputStream in ) &rarr; VectorDataSet

Parse the stream using the current settings.

### Parameters:
in - an InputStream

### Returns:
org.das2.dataset.VectorDataSet


<a href="https://github.com/autoplot/dev/search?q=readStream&unscoped_q=readStream">[search for examples]</a>

***
<a name="setPropertyPattern"></a>
# setPropertyPattern
setPropertyPattern( java.util.regex.Pattern propertyPattern ) &rarr; void

specify the Pattern used to recognize properties.  Note property
 values are not parsed, they are provided as Strings.

### Parameters:
propertyPattern - a Pattern

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPropertyPattern&unscoped_q=setPropertyPattern">[search for examples]</a>

***
<a name="setRecordCountLimit"></a>
# setRecordCountLimit
setRecordCountLimit( int recordCountLimit ) &rarr; void

limit the number of records read.  parsing will stop at this limit.

### Parameters:
recordCountLimit - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRecordCountLimit&unscoped_q=setRecordCountLimit">[search for examples]</a>

***
<a name="setSkipLines"></a>
# setSkipLines
setSkipLines( int skipLines ) &rarr; void

skip a number of lines before trying to parse anything.

### Parameters:
skipLines - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSkipLines&unscoped_q=setSkipLines">[search for examples]</a>

