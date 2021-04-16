# org.das2.qds.util.MultiFieldTimeParserParse the record by recombining the separated fields, then parsing
 the combined string.  This is to be used with AsciiParser.

 2010/03/11: Indeterminate field length is used when one field is in a record.
 2010/03/11: The last field, if just one digit type (%S), can contain fractional part.
MultiFieldTimeParser( int firstColumn, java.lang.String[] timeFormats, org.das2.datum.TimeParser parser, Units units )


***
<a name="create"></a>
# create
create( org.das2.qds.util.AsciiParser ap, int firstColumn, java.lang.String[] timeFormats ) &rarr; MultiFieldTimeParser

configure AsciiParser ap to use this field parser.  The parser is
 registered with each column and the units are set.

### Parameters:
ap - an AsciiParser
<br>firstColumn - an int
<br>timeFormats - a java.lang.String[]

### Returns:
org.das2.qds.util.MultiFieldTimeParser


<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

***
<a name="getUnits"></a>
# getUnits
getUnits(  ) &rarr; Units

suggest units for unpacking.

### Returns:
an Units


<a href="https://github.com/autoplot/dev/search?q=getUnits&unscoped_q=getUnits">[search for examples]</a>

***
<a name="parseField"></a>
# parseField
parseField( String field, int columnIndex ) &rarr; double

Either the field is accumulated in a string, and the entire string is parsed for the last field.

### Parameters:
field - the contents of the field.
<br>columnIndex - the index of the column in the table.

### Returns:
0 or the value for the time unit if it's the last field.

<a href="https://github.com/autoplot/dev/search?q=parseField&unscoped_q=parseField">[search for examples]</a>

***
<a name="unpack"></a>
# unpack
unpack( QDataSet rank2, Units u ) &rarr; QDataSet



### Parameters:
rank2 - a QDataSet
<br>u - an Units

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=unpack&unscoped_q=unpack">[search for examples]</a>

