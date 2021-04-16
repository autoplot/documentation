# org.autoplot.ascii.AsciiTableDataSourceFormatFormat the QDataSet into Ascii tables.  
 <ul>
 <li>header=rich include "rich ascii" metadata.
 <li>header=none don't include any headers.
 <li>tformat=iso8601 use ISO8601 times (like 2015-01-01T00:00Z)
 <li>tformat=hours+since+2015-01-01T00:00 use offsets. (timeformat and tformat are aliases)
 <li>tformat=$Y+$J+$H+$M+$S. (separate into columns for each component)
 <li>tformat=day
 <li>format=%5.2f use this formatter for data.
 </ul>
AsciiTableDataSourceFormat( )


***
<a name="canFormat"></a>
# canFormat
canFormat( QDataSet ds ) &rarr; boolean



### Parameters:
ds - a QDataSet

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=canFormat&unscoped_q=canFormat">[search for examples]</a>

***
<a name="formatData"></a>
# formatData
formatData( String uri, QDataSet data, ProgressMonitor mon ) &rarr; void

format the data to an ASCII table file.  No controls are provided presently, but this
 may change.

### Parameters:
uri - a String
<br>data - a QDataSet
<br>mon - a ProgressMonitor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=formatData&unscoped_q=formatData">[search for examples]</a>

***
<a name="getDescription"></a>
# getDescription
getDescription(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getDescription&unscoped_q=getDescription">[search for examples]</a>

