# org.autoplot.csv.TableOpsI'd still like to refactor all the table-type sources to get the common codes.
 These include:<ul>
   <li> html tables
   <li> xls, csv
   <li> dat
 </ul>
TableOps( )


***
<a name="columnIndex"></a>
# columnIndex
columnIndex( String name, java.lang.String[] fieldNames ) &rarr; int

returns the field index of the name, which can be:<ul>
   <li>a column name
   <li>an implicit column name "field1"
   <li>a column index (0 is the first column)
   <li>a negative column index (-1 is the last column)
 </ul>

### Parameters:
name - a String
<br>fieldNames - the field names for each column.

### Returns:
the index of the field, or -1 if the column doesn't exist.

<a href="https://github.com/autoplot/dev/search?q=columnIndex&unscoped_q=columnIndex">[search for examples]</a>

***
<a name="getDelim"></a>
# getDelim
getDelim( java.io.PushbackInputStream thein ) &rarr; char

get the delimiter, either a comma or semicolon, by looking at the first
 few lines of the file.  The pushbackInputStream should be returned at 
 the zeroth byte.

### Parameters:
thein - the PushbackInputStream, which will be at the zeroth byte to start and the zeroth byte when this is done.

### Returns:
the delimiter.

<a href="https://github.com/autoplot/dev/search?q=getDelim&unscoped_q=getDelim">[search for examples]</a>

***
<a name="getFieldIndex"></a>
# getFieldIndex
getFieldIndex( String string, java.lang.String[] fieldNames ) &rarr; int

returns the index of the field.  Supports the name, or field0, or 0, etc.

### Parameters:
string - the field for which we want to identify the index
<br>fieldNames - the field names for each column.

### Returns:
the field index, or -1 if the column doesn't exist.

<a href="https://github.com/autoplot/dev/search?q=getFieldIndex&unscoped_q=getFieldIndex">[search for examples]</a>

***
<a name="parseRangeStr"></a>
# parseRangeStr
parseRangeStr( String o, java.lang.String[] fieldNames ) &rarr; int

parse range strings like "3:6", "3:-5", and "Bx_gsm-Bz_gsm"
 if the delimiter is colon, then the end is exclusive.  If it is "-",
 then it is inclusive.  For example,<ul>
 <li>3:6 -> [3,6]
 <li>3-5 -> [3,6]
 </ul>

### Parameters:
o - the range string or field names, etc.
<br>fieldNames - the field names for each column.

### Returns:
the two-element range, where first index is inclusive, second is exclusive.

<a href="https://github.com/autoplot/dev/search?q=parseRangeStr&unscoped_q=parseRangeStr">[search for examples]</a>

