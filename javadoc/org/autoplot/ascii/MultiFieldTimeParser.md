# org.autoplot.ascii.MultiFieldTimeParser

Parse the record by recombining the separated fields, then parsing
 the combined string.

 2010/03/11: Indeterminate field length is used when one field is in a record.
 2010/03/11: The last field, if just one digit type (%S), can contain fractional part.

# MultiFieldTimeParser( int firstColumn, java.lang.String[] timeFormats, org.das2.datum.TimeParser parser, Units units )


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
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

