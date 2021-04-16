# org.das2.qds.util.AsciiParserClass for reading ASCII tables into a QDataSet.  This parses a file by breaking
 it up into records, and passing the record off to a delegate record parser.
 The record parser then breaks up the record into fields, and each field is 
 parsed by a delegate field parser.  Each column of the table has a Unit, field name,
 and field label associated with it.
 
 Examples of record parsers include 
 DelimParser, which splits the record by a delimiter such as a tab or comma,
 RegexParser, which processes each record with a regular expression to get the fields,
 and FixedColumnsParser, which splits the record by character positions.
 Example of field parsers include DOUBLE_PARSER which parses the value
 as a double, and UNITS_PARSER, which uses the Unit attached to the column
 to interpret the value.

 When the first record with the correct number of fields is found but is not
 parseable, we look for field labels and units.
 
 The skipLines property tells the parser to skip a given number of header lines 
 before attempting to parse the record.  Also, commentPrefix identifies lines to be 
 ignored.  In either the header or in comments, we look for propertyPattern, and
 if a property is matched, then the builder property
 is set.  Two Patterns are provided NAME_COLON_VALUE_PATTERN and
 NAME_EQUAL_VALUE_PATTERN for convenience.   

 Adapted to QDataSet model, Jeremy, May 2007.
AsciiParser( )
Creates a new instance.  This is created and then 
 configured before any files can be parsed.

***
<a name="NAME_COLON_VALUE_PATTERN"></a>
# NAME_COLON_VALUE_PATTERN

pattern for name:value.

***
<a name="NAME_EQUAL_VALUE_PATTERN"></a>
# NAME_EQUAL_VALUE_PATTERN

pattern for name=value.

***
<a name="PROPERTY_FIELD_NAMES"></a>
# PROPERTY_FIELD_NAMES



***
<a name="PROPERTY_FILE_HEADER"></a>
# PROPERTY_FILE_HEADER



***
<a name="PROPERTY_FIRST_RECORD"></a>
# PROPERTY_FIRST_RECORD



***
<a name="PROPERTY_FIELD_PARSER"></a>
# PROPERTY_FIELD_PARSER



***
<a name="DELIM_COMMA"></a>
# DELIM_COMMA



***
<a name="DELIM_TAB"></a>
# DELIM_TAB



***
<a name="DELIM_WHITESPACE"></a>
# DELIM_WHITESPACE



***
<a name="UNIT_UTC"></a>
# UNIT_UTC

Convenient unit for parsing UTC times.

***
<a name="PROP_HEADERDELIMITER"></a>
# PROP_HEADERDELIMITER



***
<a name="DOUBLE_PARSER"></a>
# DOUBLE_PARSER

parses the field using Double.parseDouble, Java's double parser.

***
<a name="UNITS_PARSER"></a>
# UNITS_PARSER

delegates to the unit object set for this field to parse the data.

***
<a name="ENUMERATION_PARSER"></a>
# ENUMERATION_PARSER

uses the EnumerationUnits for the field to create a Datum.

***
<a name="PROP_VALIDMIN"></a>
# PROP_VALIDMIN



***
<a name="PROP_VALIDMAX"></a>
# PROP_VALIDMAX



***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void

Adds a PropertyChangeListener to the listener list.

### Parameters:
l - The listener to add.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

***
<a name="getDelimParser"></a>
# getDelimParser
getDelimParser( int fieldCount, String delim ) &rarr; DelimParser

provide more control to external codes by providing a way to assert that
 an N-column delim parser should be used.

### Parameters:
fieldCount - an int
<br>delim - the delimiter pattern, such as "," or "\s+"

### Returns:
the DelimParser.

<a href="https://github.com/autoplot/dev/search?q=getDelimParser&unscoped_q=getDelimParser">[search for examples]</a>

***
<a name="getFieldCount"></a>
# getFieldCount
getFieldCount(  ) &rarr; int

return the number of fields in each record.  Note the RecordParsers
 also have a fieldCount, which should be equal to this.  This allows them
 to be independent of the parser.

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=getFieldCount&unscoped_q=getFieldCount">[search for examples]</a>

***
<a name="getFieldIndex"></a>
# getFieldIndex
getFieldIndex( String string ) &rarr; int

returns the index of the field.  Supports the name, or field0, or 0, etc.
 returns -1 when the column is not identified.

### Parameters:
string - the label for the field, such as "field2" or "time"

### Returns:
-1 or the index of the field.

<a href="https://github.com/autoplot/dev/search?q=getFieldIndex&unscoped_q=getFieldIndex">[search for examples]</a>

***
<a name="getFieldLabels"></a>
# getFieldLabels
getFieldLabels(  ) &rarr; String

return the labels found for each field.  If a label wasn't found,
 then the name is returned.

### Returns:
a java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=getFieldLabels&unscoped_q=getFieldLabels">[search for examples]</a>

***
<a name="getFieldNames"></a>
# getFieldNames
getFieldNames(  ) &rarr; String

return the name of each field.  field0, field1, ... are the default names when
 names are not discovered in the table.  Changing the array will not affect
 internal representation.

### Returns:
a java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=getFieldNames&unscoped_q=getFieldNames">[search for examples]</a>

***
<a name="getFieldUnits"></a>
# getFieldUnits
getFieldUnits(  ) &rarr; String

return the units that were associated with the field.  This might also be
 the channel label for spectrograms.  
 In "field0(str)" or "field0[str]" this is str.
 elements may be null if not found.

### Returns:
a java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=getFieldUnits&unscoped_q=getFieldUnits">[search for examples]</a>

***
<a name="getFillValue"></a>
# getFillValue
getFillValue(  ) &rarr; double

return the fillValue.  numbers that parse to this value are considered 
 to be fill. Note validMin and validMax may be used as well.

### Returns:
Value of property fillValue.

<a href="https://github.com/autoplot/dev/search?q=getFillValue&unscoped_q=getFillValue">[search for examples]</a>

***
<a name="getHeaderDelimiter"></a>
# getHeaderDelimiter
getHeaderDelimiter(  ) &rarr; String

get the header delimiter

### Returns:
the header delimiter.

<a href="https://github.com/autoplot/dev/search?q=getHeaderDelimiter&unscoped_q=getHeaderDelimiter">[search for examples]</a>

***
<a name="getRecordParser"></a>
# getRecordParser
getRecordParser(  ) &rarr; RecordParser

Getter for property recordParser.

### Returns:
Value of property recordParser.

<a href="https://github.com/autoplot/dev/search?q=getRecordParser&unscoped_q=getRecordParser">[search for examples]</a>

***
<a name="getRegexForFormat"></a>
# getRegexForFormat
getRegexForFormat( String format ) &rarr; String

Convert FORTRAN (F77) style format to C-style format specifiers.

### Parameters:
format - for example "%5d%5d%9f%s"

### Returns:
for example "d5,d5,f9,a"
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/autoplot/metatree/MetadataUtil.md#normalizeFormatSpecifier'>org.autoplot.metatree.MetadataUtil#normalizeFormatSpecifier</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getRegexForFormat&unscoped_q=getRegexForFormat">[search for examples]</a>

***
<a name="getRegexParser"></a>
# getRegexParser
getRegexParser( String regex ) &rarr; RegexParser

return a regex parser for the given regular expression.  Groups are used 
 for the fields, for example getRegexParser( 'X (\d+) (\d+)' ) would 
 parse lines like "X 00005 00006".

### Parameters:
regex - a String

### Returns:
the regex parser

<a href="https://github.com/autoplot/dev/search?q=getRegexParser&unscoped_q=getRegexParser">[search for examples]</a>

***
<a name="getRegexParserForFormat"></a>
# getRegexParserForFormat
getRegexParserForFormat( String format ) &rarr; RegexParser

see  private TimeParser(String formatString, Map<String,FieldHandler> fieldHandlers)</tt>,
 which is very similar.<ul>
 <li>"%5d%5d%9f%s"
 <li>"d5,d5,f9,a"
 </ul>

### Parameters:
format - a String

### Returns:
an org.das2.qds.util.AsciiParser.RegexParser

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/datum/TimeParser.md'>org.das2.datum.TimeParser</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getRegexParserForFormat&unscoped_q=getRegexParserForFormat">[search for examples]</a>

***
<a name="getRichFields"></a>
# getRichFields
getRichFields(  ) &rarr; Map

returns the high rank rich fields in a map from NAME to LABEL.
 NAME:&gt;fieldX&lt;  or NAME:&gt;fieldX-fieldY&lt;

### Returns:
the high rank rich fields in a map from NAME to LABEL.

<a href="https://github.com/autoplot/dev/search?q=getRichFields&unscoped_q=getRichFields">[search for examples]</a>

***
<a name="getUnits"></a>
# getUnits
getUnits( int index ) &rarr; Units

Indexed getter for property units.

### Parameters:
index - Index of the property.

### Returns:
Value of the property at <CODE>index</CODE>.

<a href="https://github.com/autoplot/dev/search?q=getUnits&unscoped_q=getUnits">[search for examples]</a>

***
<a name="getValidMax"></a>
# getValidMax
getValidMax(  ) &rarr; double

get the maximum value for any field.

### Returns:
the validMax

<a href="https://github.com/autoplot/dev/search?q=getValidMax&unscoped_q=getValidMax">[search for examples]</a>

***
<a name="getValidMin"></a>
# getValidMin
getValidMin(  ) &rarr; double

get the minimum valid value for any field.

### Returns:
validMin

<a href="https://github.com/autoplot/dev/search?q=getValidMin&unscoped_q=getValidMin">[search for examples]</a>

***
<a name="guessDelimParser"></a>
# guessDelimParser
guessDelimParser( String line ) &rarr; DelimParser



### Parameters:
line - a String

### Returns:
org.das2.qds.util.AsciiParser.DelimParser


<a href="https://github.com/autoplot/dev/search?q=guessDelimParser&unscoped_q=guessDelimParser">[search for examples]</a>

guessDelimParser( String line, int lineNumber ) &rarr; DelimParser<br>
***
<a name="guessFieldCount"></a>
# guessFieldCount
guessFieldCount( String filename ) &rarr; int

return the field count that would result in the largest number of records parsed.  The
 entire file is scanned, and for each line the number of decimal fields is counted.  At the end
 of the scan, the fieldCount with the highest record count is returned.

### Parameters:
filename - the file name, a local file opened with a FileReader

### Returns:
the apparent field count.

<a href="https://github.com/autoplot/dev/search?q=guessFieldCount&unscoped_q=guessFieldCount">[search for examples]</a>

***
<a name="guessSkipAndDelimParser"></a>
# guessSkipAndDelimParser
guessSkipAndDelimParser( String filename ) &rarr; DelimParser

read in records, allowing for a header of non-records before
 guessing the delim parser.  This will return a reference to the
 DelimParser and set skipLines.  DelimParser header field is set as well.
 One must set the record parser explicitly.

### Parameters:
filename - a String

### Returns:
the record parser to use, or null if no records are found.

<a href="https://github.com/autoplot/dev/search?q=guessSkipAndDelimParser&unscoped_q=guessSkipAndDelimParser">[search for examples]</a>

***
<a name="guessSkipLines"></a>
# guessSkipLines
guessSkipLines( String filename, org.das2.qds.util.AsciiParser.RecordParser recParser ) &rarr; int

try to figure out how many lines to skip by looking for the line where
 the number of fields becomes stable.

### Parameters:
filename - a String
<br>recParser - an AsciiParser.RecordParser

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=guessSkipLines&unscoped_q=guessSkipLines">[search for examples]</a>

***
<a name="isHeader"></a>
# isHeader
isHeader( int iline, String lastLine, String thisLine, int recCount ) &rarr; boolean

returns true if the line is a header or comment.

### Parameters:
iline - the line number in the file, starting with 0.
<br>lastLine - the last line read.
<br>thisLine - the line we are testing.
<br>recCount - the number of records successfully read.

### Returns:
true if the line is a header line.

<a href="https://github.com/autoplot/dev/search?q=isHeader&unscoped_q=isHeader">[search for examples]</a>

***
<a name="isIso8601Time"></a>
# isIso8601Time
isIso8601Time( String s ) &rarr; boolean

quick-n-dirty check to see if a string appears to be an ISO8601 time.
 minimally 2000-002T00:00, but also 2000-01-01T00:00:00Z etc. 
 Note that an external code may explicitly indicate that the field is a time,
 This is just to catch things that are obviously times.

### Parameters:
s - a String

### Returns:
true if this is clearly an ISO time.

<a href="https://github.com/autoplot/dev/search?q=isIso8601Time&unscoped_q=isIso8601Time">[search for examples]</a>

***
<a name="isKeepFileHeader"></a>
# isKeepFileHeader
isKeepFileHeader(  ) &rarr; boolean

Getter for property keepHeader.

### Returns:
Value of property keepHeader.

<a href="https://github.com/autoplot/dev/search?q=isKeepFileHeader&unscoped_q=isKeepFileHeader">[search for examples]</a>

***
<a name="isRichHeader"></a>
# isRichHeader
isRichHeader( String header ) &rarr; boolean

return true if the header appears to contain JSON code which could be
 interpreted as a "Rich Header" (a.k.a. JSONHeadedASCII).  This is 
 a very simple test, simply looking for <code>#{</code> and <code>#}</code>
 with a colon contained within.

### Parameters:
header - string containing the commented header.

### Returns:
true if parsing as a Rich Header should be attempted.
### See Also:
<a href='https://github.com/JSONheadedASCII/examples'>https://github.com/JSONheadedASCII/examples</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isRichHeader&unscoped_q=isRichHeader">[search for examples]</a>

isRichHeader(  ) &rarr; boolean<br>
***
<a name="newParser"></a>
# newParser
newParser( int fieldCount ) &rarr; AsciiParser

creates a parser with @param fieldCount fields, named "field0,...,fieldN"

### Parameters:
fieldCount - the number of fields

### Returns:
the file parser

<a href="https://github.com/autoplot/dev/search?q=newParser&unscoped_q=newParser">[search for examples]</a>

newParser( java.lang.String[] fieldNames ) &rarr; AsciiParser<br>
***
<a name="readFile"></a>
# readFile
readFile( String filename, ProgressMonitor mon ) &rarr; WritableDataSet

Parse the file using the current settings.

### Parameters:
filename - the file to read
<br>mon - a monitor

### Returns:
a rank 2 dataset.

<a href="https://github.com/autoplot/dev/search?q=readFile&unscoped_q=readFile">[search for examples]</a>

***
<a name="readFirstParseableRecord"></a>
# readFirstParseableRecord
readFirstParseableRecord( String filename ) &rarr; String

returns the first record that the record parser parses successfully.  The
 recordParser should be set and configured enough to identify the fields.
 If no records can be parsed, then null is returned.

 The first record should be in the first 1000 lines.

### Parameters:
filename - a String

### Returns:
the first parseable line, or null if no such line exists.

<a href="https://github.com/autoplot/dev/search?q=readFirstParseableRecord&unscoped_q=readFirstParseableRecord">[search for examples]</a>

***
<a name="readFirstRecord"></a>
# readFirstRecord
readFirstRecord( String filename ) &rarr; String

return the first record that the parser would parse.  If skipLines is 
 more than the total number of lines, or all lines are comments, then null
 is returned.

### Parameters:
filename - a String

### Returns:
the first line after skip lines and comment lines.

<a href="https://github.com/autoplot/dev/search?q=readFirstRecord&unscoped_q=readFirstRecord">[search for examples]</a>

readFirstRecord( java.io.BufferedReader reader ) &rarr; String<br>
***
<a name="readStream"></a>
# readStream
readStream( java.io.Reader in, ProgressMonitor mon ) &rarr; WritableDataSet

Parse the stream using the current settings.

### Parameters:
in - the input stream
<br>mon - a ProgressMonitor

### Returns:
an org.das2.qds.WritableDataSet


<a href="https://github.com/autoplot/dev/search?q=readStream&unscoped_q=readStream">[search for examples]</a>

readStream( java.io.Reader in, String firstRecord, ProgressMonitor mon ) &rarr; WritableDataSet<br>
***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void

Removes a PropertyChangeListener from the listener list.

### Parameters:
l - The listener to remove.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

***
<a name="setCommentPrefix"></a>
# setCommentPrefix
setCommentPrefix( String comment ) &rarr; void

Records starting with this are not processed as data, for example "#".
 This is initially "#".  Setting this to null disables this check.

### Parameters:
comment - the prefix

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCommentPrefix&unscoped_q=setCommentPrefix">[search for examples]</a>

***
<a name="setDelimParser"></a>
# setDelimParser
setDelimParser( String filename, String delim ) &rarr; DelimParser

The DelimParser splits each record into fields using a delimiter like ","
 or "\\s+".

### Parameters:
filename - filename to read in.
<br>delim - the delimiter, such as "," or "\t" or "\s+"

### Returns:
the record parser that will split each line into fields

<a href="https://github.com/autoplot/dev/search?q=setDelimParser&unscoped_q=setDelimParser">[search for examples]</a>

setDelimParser( java.io.Reader in, String delimRegex ) &rarr; DelimParser<br>
***
<a name="setFieldParser"></a>
# setFieldParser
setFieldParser( int field, org.das2.qds.util.AsciiParser.FieldParser fp ) &rarr; void

set the special parser for a field.

### Parameters:
field - the field number, 0 is the first column.
<br>fp - the parser

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFieldParser&unscoped_q=setFieldParser">[search for examples]</a>

***
<a name="setFillValue"></a>
# setFillValue
setFillValue( double fillValue ) &rarr; void

numbers that parse to this value are considered to be fill.

### Parameters:
fillValue - New value of property fillValue.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFillValue&unscoped_q=setFillValue">[search for examples]</a>

***
<a name="setFixedColumnsParser"></a>
# setFixedColumnsParser
setFixedColumnsParser( String filename, String delim ) &rarr; FixedColumnsParser

looks at the first line after skipping, and splits it to calculate where 
 the columns are.  The FixedColumnsParser is the fastest of the three parsers.

### Parameters:
filename - filename to read in.
<br>delim - regex to split the initial line into the fixed columns.

### Returns:
the record parser that will split each line.

<a href="https://github.com/autoplot/dev/search?q=setFixedColumnsParser&unscoped_q=setFixedColumnsParser">[search for examples]</a>

setFixedColumnsParser( java.io.Reader in, String delim ) &rarr; FixedColumnsParser<br>
setFixedColumnsParser( int[] columnOffsets, int[] columnWidths, org.das2.qds.util.AsciiParser.FieldParser[] parsers ) &rarr; FixedColumnsParser<br>
***
<a name="setHeaderDelimiter"></a>
# setHeaderDelimiter
setHeaderDelimiter( String headerDelimiter ) &rarr; void

set the delimiter which explicitly separates header from the data.
 For example "-------" could be used.  Normally the parser just looks at
 the number of fields and this is sufficient.

### Parameters:
headerDelimiter - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setHeaderDelimiter&unscoped_q=setHeaderDelimiter">[search for examples]</a>

***
<a name="setKeepFileHeader"></a>
# setKeepFileHeader
setKeepFileHeader( boolean keepHeader ) &rarr; void

Setter for property keepHeader.  By default false but if true, the file header
 ignored by skipLines is put into the property PROPERTY_FILE_HEADER.

### Parameters:
keepHeader - New value of property keepHeader.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setKeepFileHeader&unscoped_q=setKeepFileHeader">[search for examples]</a>

***
<a name="setPropertyPattern"></a>
# setPropertyPattern
setPropertyPattern( java.util.regex.Pattern propertyPattern ) &rarr; void

specify the Pattern used to recognize properties.  Note property
 values are not parsed, they are provided as Strings.  This is a regular
 expression with two groups for the property name and value.
 For example, (.+)=(.+)

### Parameters:
propertyPattern - regular expression Pattern with two groups.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPropertyPattern&unscoped_q=setPropertyPattern">[search for examples]</a>

***
<a name="setRecordCountLimit"></a>
# setRecordCountLimit
setRecordCountLimit( int recordCountLimit ) &rarr; void

limit the number of records read.  parsing will stop once this number of
 records is read into the result.  This is Integer.MAX_VALUE by default.

### Parameters:
recordCountLimit - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRecordCountLimit&unscoped_q=setRecordCountLimit">[search for examples]</a>

***
<a name="setRecordParser"></a>
# setRecordParser
setRecordParser( org.das2.qds.util.AsciiParser.RecordParser recordParser ) &rarr; void

Setter for property recordParser.

### Parameters:
recordParser - New value of property recordParser.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRecordParser&unscoped_q=setRecordParser">[search for examples]</a>

***
<a name="setRecordStart"></a>
# setRecordStart
setRecordStart( int recordStart ) &rarr; void

set the number of records to skip before accumulating the result.

### Parameters:
recordStart - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRecordStart&unscoped_q=setRecordStart">[search for examples]</a>

***
<a name="setRegexParser"></a>
# setRegexParser
setRegexParser( java.lang.String[] fieldNames ) &rarr; RecordParser

The regex parser is a slow parser, but gives precise control.

### Parameters:
fieldNames - a java.lang.String[]

### Returns:
the parser for each record.

<a href="https://github.com/autoplot/dev/search?q=setRegexParser&unscoped_q=setRegexParser">[search for examples]</a>

***
<a name="setSkipLines"></a>
# setSkipLines
setSkipLines( int skipLines ) &rarr; void

skip a number of lines before trying to parse anything.  This can be
 set to point at the first valid line, and the RecordParser will be 
 configured using that line.

### Parameters:
skipLines - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSkipLines&unscoped_q=setSkipLines">[search for examples]</a>

***
<a name="setUnits"></a>
# setUnits
setUnits( int index, Units units ) &rarr; void

Indexed setter for property units.  This now sets the field parser for 
 the field to be a UNITS_PARSER if it is the default DOUBLE_PARSER.

### Parameters:
index - Index of the property.
<br>units - New value of the property at <CODE>index</CODE>.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUnits&unscoped_q=setUnits">[search for examples]</a>

setUnits( org.das2.datum.Units[] u ) &rarr; void<br>
***
<a name="setValidMax"></a>
# setValidMax
setValidMax( double validMax ) &rarr; void

set the maximum value for any field.  Values above this are to be
 considered invalid.

### Parameters:
validMax - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setValidMax&unscoped_q=setValidMax">[search for examples]</a>

***
<a name="setValidMin"></a>
# setValidMin
setValidMin( double validMin ) &rarr; void

set the minimum valid value for any field.  Values less than 
 this are to be considered invalid.

### Parameters:
validMin - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setValidMin&unscoped_q=setValidMin">[search for examples]</a>

***
<a name="setWhereConstraint"></a>
# setWhereConstraint
setWhereConstraint( String sparm, String op, String sval ) &rarr; void

allow constraint for where condition is true.  This doesn't 
 need the data to be interpreted for "eq", string equality is checked
 for nominal data.  Note sval is compared after trimming outside spaces.

### Parameters:
sparm - column name, such as "field4"
<br>op - constraint, one of eq gt ge lt le ne
<br>sval - String value.  For nominal columns, String equality is used.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setWhereConstraint&unscoped_q=setWhereConstraint">[search for examples]</a>

