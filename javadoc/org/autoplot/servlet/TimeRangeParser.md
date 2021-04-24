# org.autoplot.servlet.TimeRangeParser

Extract a clean Java code for parsing ISO8601 strings.

# TimeRangeParser( )


***
<a name="iso8601duration"></a>
# iso8601duration



***
<a name="iso8601DurationPattern"></a>
# iso8601DurationPattern



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
<a name="parseISO8601Datum"></a>
# parseISO8601Datum
parseISO8601Datum( String str, int[] result, int lsd ) &rarr; int

ISO8601 datum parser.  This does not support 2-digit years, which
 were removed in ISO 8601:2004.

### Parameters:
str - a String
<br>result - an int[]
<br>lsd - an int

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=parseISO8601Datum&unscoped_q=parseISO8601Datum">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parseISO8601Duration"></a>
# parseISO8601Duration
parseISO8601Duration( String stringIn ) &rarr; int

returns a 7 element array with [year,mon,day,hour,min,sec,nanos] or [-9999].

### Parameters:
stringIn - a String

### Returns:
[year,mon,day,hour,min,sec,nanos]

<a href="https://github.com/autoplot/dev/search?q=parseISO8601Duration&unscoped_q=parseISO8601Duration">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parseISO8601Range"></a>
# parseISO8601Range
parseISO8601Range( String stringIn, int[] result ) &rarr; int

returns the time found in an iso8601 string, or null.  This supports
 periods (durations) as in: 2007-03-01T13:00:00Z/P1Y2M10DT2H30M
 Other examples:
   2007-03-01T13:00:00Z/2008-05-11T15:30:00Z
   2007-03-01T13:00:00Z/P1Y2M10DT2H30M
   P1Y2M10DT2H30M/2008-05-11T15:30:00Z
   2007-03-01T00:00Z/P1D
   2012-100T02:00/03:45
 http://en.wikipedia.org/wiki/ISO_8601#Time_intervals

### Parameters:
stringIn - a String
<br>result - an int[]

### Returns:
int[14] with [Y,M,D,H,M,S,NS,Y,M,D,H,M,S,NS]

<a href="https://github.com/autoplot/dev/search?q=parseISO8601Range&unscoped_q=parseISO8601Range">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

