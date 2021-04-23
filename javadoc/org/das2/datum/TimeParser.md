# org.das2.datum.TimeParserTimeParser designed to quickly parse strings with a known format.  This parser has been
 shown to perform around 20 times faster than the discovery parser.
 
 This class is not thread-safe, so clients must make sure that only one thread accesses the class at a time.
***
<a name="TIMEFORMAT_Z"></a>
# TIMEFORMAT_Z

$Y-$m-$dT$H:$M:$S.$(subsec;places=3)Z

***
<a name="IGNORE_FIELD_HANDLER"></a>
# IGNORE_FIELD_HANDLER

handy FieldHandler that ignores the contents.  For example,
 <pre>tp= TimeParser.create(sagg,"v", TimeParser.IGNORE_FIELD_HANDLER );</pre>

***
<a name="create"></a>
# create
create( String formatString ) &rarr; TimeParser

Create a TimeParser object, which is the fast time parser for use when a known format specification is used to
 parse many instances of a formatted string.  For example, this would be used to interpret the times in an text file,
 but not times entered in a time range GUI to control an axis.  This can also be and is used for filenames,
 for example omni2_h0_mrg1hr_$Y$(m,span=6)01_v01.cdf.

 Note field lengths are used when formatting the data, but when parsing often fractional components are accepted.  For
 example, the format might be "%Y %j %H", and "2012 365 12.003" is accepted.

 Note also that often $(Y) is used where %{Y} is used.  These are equivalent, and useful when $() interferes with parsing
 elsewhere.

 An effort has begun to try and unify to an agreeable specification for this.  See http://tsds.org/uri_templates
 <pre>
  $[fieldLength]<1-char code>  or
  $[fieldLength](<code>)
  $[fieldLength](<code>;qualifiers)

  fieldLength=0 --> makes field length indeterminate, deliminator must follow.

  $Y   4-digit year
  $y   2-digit year
  $j   3-digit day of year
  $m   2-digit month
  $b   3-char month name (jan,feb,mar,apr,may,jun,jul,aug,sep,oct,nov,dec.  Sorry, rest of world...)
  $d   2-digit day
  $H   2-digit hour
  $M   2-digit minute
  $S   2-digit second
  $(milli)  3-digit milliseconds
  $(ignore) skip this field
  $x   skip this field
  $(enum)  skip this field.  If id is specified, then id can be retrieved.
  $v   skip this field
  $(hrinterval;values=0,1,2,3)  enumeration of part of day
  $(subsec;places=6)  fractional seconds (6->microseconds)
  $(periodic;offset=0;start=2000-001;period=P1D)

 Qualifiers:
    span=<int>
    delta=<int>
    Y=2004  Also for Y,m,d,H,M,S

   For example:
      $(j;Y=2004) means the day-of-year, within the year 2004.
      $(H;Y=2004;j=117) means the hour of day 2004-117
      $(m;span=6) means the 6-month interval starting at the given month.

  </pre>

### Parameters:
formatString - the format string.

### Returns:
the time parser.

<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

create( String formatString, String fieldName, org.das2.datum.TimeParser.FieldHandler handler, java.lang.Object[] moreHandler ) &rarr; TimeParser<br>
***
<a name="format"></a>
# format
format( DatumRange range ) &rarr; String

return the formatted range.  This actually returns the range that contains the min
 of the given range.

### Parameters:
range - a DatumRange

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=format&unscoped_q=format">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

format( Datum start ) &rarr; String<br>
format( Datum start, Datum stop ) &rarr; String<br>
format( Datum start, Datum stop, java.util.Map extra ) &rarr; String<br>
***
<a name="getEndTime"></a>
# getEndTime
getEndTime( Units units ) &rarr; double

return the end time of the range in units, e.g. Units.us2000

### Parameters:
units - an Units

### Returns:
a double


<a href="https://github.com/autoplot/dev/search?q=getEndTime&unscoped_q=getEndTime">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFieldHandlerByCode"></a>
# getFieldHandlerByCode
getFieldHandlerByCode( String code ) &rarr; FieldHandler

return the field handler for the id.  For example, enum
 returns the field handler handling enumerations.  Note there 
 is currently only one field handler for each type, so for example
 two enumerations are not allowed.

### Parameters:
code - a String

### Returns:
the field handler.

<a href="https://github.com/autoplot/dev/search?q=getFieldHandlerByCode&unscoped_q=getFieldHandlerByCode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFieldHandlerById"></a>
# getFieldHandlerById
getFieldHandlerById( String id ) &rarr; FieldHandler

return the field handler for the id.  For example, enum
 returns the field handler handling enumerations.  Note there 
 is currently only one field handler for each type, so for example
 two enumerations are not allowed.

### Parameters:
id - the field handler id

### Returns:
the field handler.

<a href="https://github.com/autoplot/dev/search?q=getFieldHandlerById&unscoped_q=getFieldHandlerById">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPad"></a>
# getPad
getPad( java.util.Map args ) &rarr; char

return the pad for the spec, like "underscore" "space" "zero" or "none"
 For "none", space is returned, and clients allowing special behavior should check for this.

### Parameters:
args - a java.util.Map

### Returns:
the char, or (char)0.

<a href="https://github.com/autoplot/dev/search?q=getPad&unscoped_q=getPad">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRegex"></a>
# getRegex
getRegex(  ) &rarr; String

peek at the regular expression used.

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getRegex&unscoped_q=getRegex">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTime"></a>
# getTime
getTime( Units units ) &rarr; double

return the parsed time in the given units. Here Autoplot
 Jython code shows how this is used:
 <code>
  from org.virbo.dataset import SemanticOps
  tp= TimeParser.create("$Y-$m-$dT$H")
  u= SemanticOps.lookupTimeUnits("seconds since 2014-01-01T00:00")
  print tp.parse("2014-01-06T02").getTime( u )
 </code>

### Parameters:
units - as in Units.us2000

### Returns:
the value in the given units.

<a href="https://github.com/autoplot/dev/search?q=getTime&unscoped_q=getTime">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTimeDatum"></a>
# getTimeDatum
getTimeDatum(  ) &rarr; Datum

return the parsed time as a Datum.  For years less than 1990, 
 Units.us1980 is used, otherwise Units.us2000 is used.

### Returns:
a datum representing the parsed time.

<a href="https://github.com/autoplot/dev/search?q=getTimeDatum&unscoped_q=getTimeDatum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTimeRange"></a>
# getTimeRange
getTimeRange(  ) &rarr; DatumRange

Returns the implicit interval as a DatumRange.
 For example, "Jan 1, 2003" would have a getTimeDatum of "Jan 1, 2003 00:00:00",
 and getDatumRange() would go from midnight to midnight.
 This will try to create MonthDatumRanges when possible, to keep it abstract,
 so for example, 
 <blockquote><pre>
tr= tp.getTimeRange()  // "Jan 2015"
tr= tr.next()          // "Feb 2015", not 31 days starting Feb 1
</pre></blockquote>
 
 This accesses time, timeWidth, orbitDatumRange, startTime.

### Returns:
the DatumRange

<a href="https://github.com/autoplot/dev/search?q=getTimeRange&unscoped_q=getTimeRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getValidRange"></a>
# getValidRange
getValidRange(  ) &rarr; DatumRange

return the limits of the range we can parse.  These limits come from
 orbit files like "$(o,sc=rbspa-pp)"
 or from explicit fields like "$(M,Y=1999)"

### Returns:
a DatumRange


<a href="https://github.com/autoplot/dev/search?q=getValidRange&unscoped_q=getValidRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasField"></a>
# hasField
hasField( String field ) &rarr; boolean

return true if the parser has a field.

### Parameters:
field - e.g. "x"

### Returns:
true if the parser has a field.

<a href="https://github.com/autoplot/dev/search?q=hasField&unscoped_q=hasField">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isIso8601String"></a>
# isIso8601String
isIso8601String( String exampleTime ) &rarr; boolean

return true if the string appears to be an ISO8601 time.  This
 requires that the string contain a "T" or space and the hours and
 minutes components.

### Parameters:
exampleTime - string like "1992-353T02:00"

### Returns:
true if the string appears to be an ISO8601 time.

<a href="https://github.com/autoplot/dev/search?q=isIso8601String&unscoped_q=isIso8601String">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isNested"></a>
# isNested
isNested(  ) &rarr; boolean

return true if each successive field is nested within the previous,
 e.g.  $Y$m/$d is nested, but $Y$m/$Y$m$d is not because of the second $Y.

### Returns:
true if the spec is nested.

<a href="https://github.com/autoplot/dev/search?q=isNested&unscoped_q=isNested">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isSpec"></a>
# isSpec
isSpec( String spec ) &rarr; boolean

Provide standard means of indicating this appears to be a spec by
 looking for something that would assert the year.

### Parameters:
spec - a String

### Returns:
true if the string appears to be a spec.

<a href="https://github.com/autoplot/dev/search?q=isSpec&unscoped_q=isSpec">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isStartTimeOnly"></a>
# isStartTimeOnly
isStartTimeOnly(  ) &rarr; boolean

true if the flag (startTimeOnly) was set in the spec. This is a hint to clients (FileStorageModel) using the time that
 it shouldn't infer that the time is bounded.

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isStartTimeOnly&unscoped_q=isStartTimeOnly">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="iso8601String"></a>
# iso8601String
iso8601String( String exampleTime ) &rarr; String

must contain T or space to delimit date and time.

### Parameters:
exampleTime - "1992-353T02:00"

### Returns:
"$Y-$jT$H$M" etc.

<a href="https://github.com/autoplot/dev/search?q=iso8601String&unscoped_q=iso8601String">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] aa ) &rarr; void



### Parameters:
aa - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parse"></a>
# parse
parse( String timeString ) &rarr; TimeParser

parse the string, which presumably contains a time matching the
 spec.  A reference to the TimeParser is returned so operations can be
 chained together:<code>
   tp.parse("2014-01-06T02").getTime( Units.us2000 )
 </code>
 Since this the TimeParser has a state, it is not safe to use simultaneously
 by multiple threads.   Each thread should create its own parser.

### Parameters:
timeString - string containing a time

### Returns:
a reference to this TimeParser object, which now contains the time.

<a href="https://github.com/autoplot/dev/search?q=parse&unscoped_q=parse">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

parse( String timeString, java.util.Map extra ) &rarr; TimeParser<br>
***
<a name="setContext"></a>
# setContext
setContext( DatumRange tr ) &rarr; void

explicitly set the context for time parsing.  For example,
 filenames are just $H$M$S.dat, and the context is "Jan 17th, 2015"
 Note that the context is stored internally as just a start time, so
 spans (e.g. 3-day) are not supported.

### Parameters:
tr - the range

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setContext&unscoped_q=setContext">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDigit"></a>
# setDigit
setDigit( String format, double value ) &rarr; void

set the digit with the integer part, and move the fractional part to the
 less significant digits.  Format should contain just one field,
 see setDigit( String format, int value ) to break up fields.

### Parameters:
format - like "Y"
<br>value - like 2014

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDigit&unscoped_q=setDigit">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

setDigit( String format, int value ) &rarr; TimeParser<br>
setDigit( int digitNumber, int digit ) &rarr; TimeParser<br>
***
<a name="sloppyColumns"></a>
# sloppyColumns
sloppyColumns(  ) &rarr; void

force the parser to look for delimiters.  This should be called immediately after

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=sloppyColumns&unscoped_q=sloppyColumns">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="testTimeParser"></a>
# testTimeParser
testTimeParser(  ) &rarr; void

test time parsing when the format is known.  This time parser is much faster than the time parser of Test009, which must
 infer the format as it parses.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=testTimeParser&unscoped_q=testTimeParser">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

