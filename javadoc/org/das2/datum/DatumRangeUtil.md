# org.das2.datum.DatumRangeUtil
DatumRangeUtil( )


***
<a name="iso8601duration"></a>
# iso8601duration



***
<a name="iso8601DurationPattern"></a>
# iso8601DurationPattern



***
<a name="createCentered"></a>
# createCentered
createCentered( Datum middle, Datum width ) &rarr; DatumRange

create a DatumRange with the value for the center, and the width.

### Parameters:
middle - a Datum
<br>width - a Datum

### Returns:
datumRange centered at middle with the given width.

<a href="https://github.com/autoplot/dev/search?q=createCentered&unscoped_q=createCentered">[search for examples]</a>

***
<a name="formatISO8601Datum"></a>
# formatISO8601Datum
formatISO8601Datum( int[] result ) &rarr; String

for convenience, this formats the decomposed time.

### Parameters:
result - seven-element time [ Y,m,d,H,M,S,nanos ]

### Returns:
formatted time

<a href="https://github.com/autoplot/dev/search?q=formatISO8601Datum&unscoped_q=formatISO8601Datum">[search for examples]</a>

***
<a name="formatISO8601Duration"></a>
# formatISO8601Duration
formatISO8601Duration( int[] t ) &rarr; String

format ISO8601 duration string, for example [1,0,0,1,0,0,0] &rarr; P1YT1H

### Parameters:
t - 6 or 7-element array with [year,mon,day,hour,min,sec,nanos]

### Returns:
the formatted ISO8601 duration

<a href="https://github.com/autoplot/dev/search?q=formatISO8601Duration&unscoped_q=formatISO8601Duration">[search for examples]</a>

***
<a name="formatTimeRange"></a>
# formatTimeRange
formatTimeRange( DatumRange self ) &rarr; String



### Parameters:
self - a DatumRange

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=formatTimeRange&unscoped_q=formatTimeRange">[search for examples]</a>

formatTimeRange( DatumRange self, boolean bothDoyYMD ) &rarr; String<br>
***
<a name="fuzzyEqual"></a>
# fuzzyEqual
fuzzyEqual( DatumRange timeRange1, DatumRange timeRange2, double percent ) &rarr; boolean

return true if the time ranges are overlapping with bounds within

### Parameters:
timeRange1 - a DatumRange
<br>timeRange2 - a DatumRange
<br>percent - double from 0 to 100.

### Returns:
true if the two ranges are sufficiently close.

<a href="https://github.com/autoplot/dev/search?q=fuzzyEqual&unscoped_q=fuzzyEqual">[search for examples]</a>

***
<a name="generateList"></a>
# generateList
generateList( DatumRange bounds, DatumRange element ) &rarr; List

return a list of DatumRanges that together cover the space identified
 by bounds.  The list should contain one DatumRange that is equal to
 element, which should define the phase and period of the list elements.
 For example,
 <pre> DatumRange bounds= DatumRangeUtil.parseTimeRangeValid( '2006' );
 DatumRange first= DatumRangeUtil.parseTimeRangeValid( 'Jan 2006' );
 List list= generateList( bounds, first );</pre>
 Note the procedure calls element.previous until bound.min() is contained,
 then calls bound.max until bound.max() is contained.

### Parameters:
bounds - range to be covered.
<br>element - range defining the width and phase of each list DatumRange.

### Returns:
the ranges covering the range.

<a href="https://github.com/autoplot/dev/search?q=generateList&unscoped_q=generateList">[search for examples]</a>

***
<a name="intersection"></a>
# intersection
intersection( java.util.List bounds, java.util.List elements, boolean remove ) &rarr; List

return the elements of src that intersect with elements of the list contains.
 Both src and dst should be sorted lists that do not contain overlaps.

### Parameters:
bounds - sorted list of non-overlapping ranges.
<br>elements - sorted list of non-overlapping ranges.  If remove is true, then
   the elements intersecting are removed and the result will contain non-overlapping elements.
<br>remove - if true, remove intersecting elements from the elements list, leaving the elements that
   did not intersect with any of the ranges in bounds.

### Returns:
list of elements of src that overlap with elements of contains.

<a href="https://github.com/autoplot/dev/search?q=intersection&unscoped_q=intersection">[search for examples]</a>

***
<a name="isAcceptable"></a>
# isAcceptable
isAcceptable( DatumRange dr, boolean log ) &rarr; boolean

put limits on the typical use when looking at data:
   * both min and max are finite numbers
   * time range is between year 1000 and year 3000.
   * log ranges span no more than 1e100 cycles.

### Parameters:
dr - the DatumRange, which can contain infinite values that would make is inacceptable.
<br>log - if true, then only allow 1e100 cycles.

### Returns:
true if the range is valid.

<a href="https://github.com/autoplot/dev/search?q=isAcceptable&unscoped_q=isAcceptable">[search for examples]</a>

***
<a name="isISO8601Range"></a>
# isISO8601Range
isISO8601Range( String stringIn ) &rarr; boolean

true true for parseable ISO8601 time ranges.

### Parameters:
stringIn - a String

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isISO8601Range&unscoped_q=isISO8601Range">[search for examples]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] ss ) &rarr; void



### Parameters:
ss - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

***
<a name="newDimensionless"></a>
# newDimensionless
newDimensionless( double lower, double upper ) &rarr; DatumRange



### Parameters:
lower - a double
<br>upper - a double

### Returns:
org.das2.datum.DatumRange


<a href="https://github.com/autoplot/dev/search?q=newDimensionless&unscoped_q=newDimensionless">[search for examples]</a>

***
<a name="normalize"></a>
# normalize
normalize( DatumRange dr, Datum d ) &rarr; double

returns the position within dr, where 0. is the dr.min(), and 1. is dr.max()

### Parameters:
dr - a datum range with non-zero width.
<br>d - a datum to normalize with respect to the range.

### Returns:
a double indicating the normalized datum.
### See Also:
<a href='#rescale'>rescale(org.das2.datum.DatumRange, double, double)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=normalize&unscoped_q=normalize">[search for examples]</a>

normalize( DatumRange dr, Datum d, boolean log ) &rarr; double<br>
***
<a name="normalizeLog"></a>
# normalizeLog
normalizeLog( DatumRange dr, Datum d ) &rarr; double

returns the position within dr, where 0. is the dr.min(), and 1. is dr.max()

### Parameters:
dr - a datum range with non-zero width.
<br>d - a datum to normalize with respect to the range.

### Returns:
a double indicating the normalized datum.

<a href="https://github.com/autoplot/dev/search?q=normalizeLog&unscoped_q=normalizeLog">[search for examples]</a>

***
<a name="normalizeTimeComponents"></a>
# normalizeTimeComponents
normalizeTimeComponents( int[] components ) &rarr; int

Normalize all the components, so no component is 
 greater than its expected range or less than zero.
 
 Note that leap seconds are not accounted for.  TODO: account for them.

### Parameters:
components - int[7]: [ Y, m, d, H, M, S, nano ]

### Returns:
the same array

<a href="https://github.com/autoplot/dev/search?q=normalizeTimeComponents&unscoped_q=normalizeTimeComponents">[search for examples]</a>

***
<a name="parseDatumRange"></a>
# parseDatumRange
parseDatumRange( String str, Units units ) &rarr; DatumRange

Parse the datum range in the context of units.

### Parameters:
str - input like "5 to 15 cm"
<br>units - unit like Units.km

### Returns:
the DatumRange

<a href="https://github.com/autoplot/dev/search?q=parseDatumRange&unscoped_q=parseDatumRange">[search for examples]</a>

parseDatumRange( String str, DatumRange orig ) &rarr; DatumRange<br>
parseDatumRange( String str ) &rarr; DatumRange<br>
***
<a name="parseISO8601"></a>
# parseISO8601
parseISO8601( String str ) &rarr; int

Parser for ISO8601 formatted times.
 returns null or int[7]: [ Y, m, d, H, M, S, nano ]
 The code cannot parse any iso8601 string, but this code should.  Right now it parses:
 "2012-03-27T12:22:36.786Z"
 "2012-03-27T12:22:36"
 (and some others) TODO: enumerate and test.
 TODO: this should use parseISO8601Datum.

### Parameters:
str - iso8601 string.

### Returns:
null or int[7]: [ Y, m, d, H, M, S, nano ]

<a href="https://github.com/autoplot/dev/search?q=parseISO8601&unscoped_q=parseISO8601">[search for examples]</a>

***
<a name="parseISO8601Datum"></a>
# parseISO8601Datum
parseISO8601Datum( String str, int[] result, int lsd ) &rarr; int

new attempt to write a clean ISO8601 parser.  This should also parse 02:00
 in the context of 2010-002T00:00/02:00.  This does not support 2-digit years, which
 were removed in ISO 8601:2004.

### Parameters:
str - the ISO8601 string
<br>result - the datum, decomposed into [year,month,day,hour,minute,second,nano]
<br>lsd - -1 or the current position ???

### Returns:
the lsd least significant digit

<a href="https://github.com/autoplot/dev/search?q=parseISO8601Datum&unscoped_q=parseISO8601Datum">[search for examples]</a>

***
<a name="parseISO8601Duration"></a>
# parseISO8601Duration
parseISO8601Duration( String stringIn ) &rarr; int

returns a 7 element array with [year,mon,day,hour,min,sec,nanos].

### Parameters:
stringIn - a String

### Returns:
7-element array with [year,mon,day,hour,min,sec,nanos]

<a href="https://github.com/autoplot/dev/search?q=parseISO8601Duration&unscoped_q=parseISO8601Duration">[search for examples]</a>

***
<a name="parseISO8601Range"></a>
# parseISO8601Range
parseISO8601Range( String stringIn ) &rarr; DatumRange

returns the time found in an iso8601 string, or null.  This supports
 periods (durations) as in: 2007-03-01T13:00:00Z/P1Y2M10DT2H30M
 Other examples:<ul>
   <li>2007-03-01T13:00:00Z/2008-05-11T15:30:00Z
   <li>2007-03-01T13:00:00Z/P1Y2M10DT2H30M
   <li>P1Y2M10DT2H30M/2008-05-11T15:30:00Z
   <li>2007-03-01T00:00Z/P1D
   <li>2012-100T02:00/03:45
   <li>2001-01-01T06:08-0600/P1D Time zones (-0600) are supported though discouraged.
 </ul>
 http://en.wikipedia.org/wiki/ISO_8601#Time_intervals

### Parameters:
stringIn - a String

### Returns:
null or a DatumRange

<a href="https://github.com/autoplot/dev/search?q=parseISO8601Range&unscoped_q=parseISO8601Range">[search for examples]</a>

***
<a name="parseRescaleStr"></a>
# parseRescaleStr
parseRescaleStr( String s, org.das2.datum.Datum[] result ) &rarr; Datum

parse position strings like "100%-5hr" into [ npos, datum ].
 Note px is acceptable, but pt is proper.
 Ems are rounded to the nearest hundredth.
 Percents are returned as normal (0-1) and rounded to the nearest thousandth.

### Parameters:
s - the string, like "100%-5hr"
<br>result - a two-element Datum array with [npos,datum] result[1] provides the units.

### Returns:
a two-element Datum array with [npos,datum]

<a href="https://github.com/autoplot/dev/search?q=parseRescaleStr&unscoped_q=parseRescaleStr">[search for examples]</a>

***
<a name="parseTimeRange"></a>
# parseTimeRange
parseTimeRange( String string ) &rarr; DatumRange

parse the string into a DatumRange with time location units.
 This parse allows several different forms of time ranges, such as:
 <ul>
 <li> orbit:rbspa-pp:3  S/C orbits
 <li> orbit:rbspa-pp:3-6  S/C orbits, three orbits.
 <li> P10D  the last 10 days, immediately resolved into static time range.
 <li> 1972/now-P10D, immediately resolved into static time range.
 <li> 1972/2002  ISO8601 time ranges
 <li> 1972 to 2002  legacy das2 colloquial time ranges.
 <li> lasthour/lasthour+P1H  the hour we are within. 
 </ul>

### Parameters:
string - a String

### Returns:
the range interpreted.

<a href="https://github.com/autoplot/dev/search?q=parseTimeRange&unscoped_q=parseTimeRange">[search for examples]</a>

***
<a name="parseTimeRangeValid"></a>
# parseTimeRangeValid
parseTimeRangeValid( String s ) &rarr; DatumRange

parse the string into a DatumRange with time location units.

### Parameters:
s - a String

### Returns:
a DatumRange


<a href="https://github.com/autoplot/dev/search?q=parseTimeRangeValid&unscoped_q=parseTimeRangeValid">[search for examples]</a>

***
<a name="parseValidISO8601Range"></a>
# parseValidISO8601Range
parseValidISO8601Range( String stringIn ) &rarr; DatumRange

returns the time found in an iso8601 string, or throws a 
 runtime exception.

### Parameters:
stringIn - a String

### Returns:
a DatumRange


<a href="https://github.com/autoplot/dev/search?q=parseValidISO8601Range&unscoped_q=parseValidISO8601Range">[search for examples]</a>

***
<a name="rescale"></a>
# rescale
rescale( DatumRange dr, String rescale ) &rarr; DatumRange

rescale the DatumRange with a specification like "50%,150%" or "0%-1hr,100%+1hr".  The string is spit on the comma
 the each is split on the % sign.  This was originally introduced to support CreatePngWalk in Autoplot.

### Parameters:
dr - a DatumRange
<br>rescale - a String

### Returns:
a DatumRange


<a href="https://github.com/autoplot/dev/search?q=rescale&unscoped_q=rescale">[search for examples]</a>

rescale( DatumRange dr, double min, double max ) &rarr; DatumRange<br>
rescale( DatumRange dr, double n ) &rarr; Datum<br>
***
<a name="rescaleInverse"></a>
# rescaleInverse
rescaleInverse( DatumRange dr, String rescale ) &rarr; DatumRange

rescale the DatumRange with a specification like "50%,150%" or
 "0%-1hr,100%+1hr".  The string is split on the comma the each is split on
 the % sign.  This was originally introduced to support CreatePngWalk in 
 Autoplot.

### Parameters:
dr - a DatumRange
<br>rescale - a String

### Returns:
a DatumRange


<a href="https://github.com/autoplot/dev/search?q=rescaleInverse&unscoped_q=rescaleInverse">[search for examples]</a>

rescaleInverse( DatumRange dr, double min, double max ) &rarr; DatumRange<br>
***
<a name="rescaleLog"></a>
# rescaleLog
rescaleLog( DatumRange dr, double min, double max ) &rarr; DatumRange

returns DatumRange relative to this, where 0. is the minimum, and 1. is the maximum, but the
 scaling is done in the log space.
 For example, rescaleLog( [0.1,1.0], -1, 2 ) &rarr; [ 0.01, 10.0 ]

### Parameters:
dr - a DatumRange with nonzero width.
<br>min - the new min normalized with respect to this range.  0. is this range's min, 1 is this range's max, 0 is
 min-width.
<br>max - the new max with normalized wrt this range.  0. is this range's min, 1 is this range's max, 0 is
 min-width.

### Returns:
new DatumRange.

<a href="https://github.com/autoplot/dev/search?q=rescaleLog&unscoped_q=rescaleLog">[search for examples]</a>

***
<a name="roundSections"></a>
# roundSections
roundSections( DatumRange dr, int n ) &rarr; DatumRange

round to a nice interval with very roughly n divisions.  For example,
 <pre>
   -0.048094730687625806 to 0.047568, 100  &rarr; -0.048 to 0.048
   2012-04-18 0:00:00 to 23:59:40, 24 &rarr; 2012-04-18  
   2014-08-10 0:00:00 to 2014-08-11T00:00:59, 24 &rarr; 2014-08-10
 </pre>

### Parameters:
dr - a DatumRange
<br>n - an int

### Returns:
dr when its width is zero, or a rounded range.

<a href="https://github.com/autoplot/dev/search?q=roundSections&unscoped_q=roundSections">[search for examples]</a>

***
<a name="setUseDoy"></a>
# setUseDoy
setUseDoy( boolean v ) &rarr; void



### Parameters:
v - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUseDoy&unscoped_q=setUseDoy">[search for examples]</a>

***
<a name="sloppyContains"></a>
# sloppyContains
sloppyContains( DatumRange context, Datum datum ) &rarr; boolean

Like DatumRange.contains, but includes the end point.  Often this allows for simpler code.

### Parameters:
context - the datum range.
<br>datum - the data point

### Returns:
true if the range contains the datum.
### See Also:
<a href='DatumRange.md#contains'>DatumRange#contains(org.das2.datum.DatumRange)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=sloppyContains&unscoped_q=sloppyContains">[search for examples]</a>

***
<a name="sloppyIntersection"></a>
# sloppyIntersection
sloppyIntersection( DatumRange range, DatumRange include ) &rarr; DatumRange

Like DatumRange.intersects, but returns a zero-width range when the two do
 not intersect.  When they do not intersect, the min or max of the first range
 is returned, depending on whether or not the second range is above or below
 the first range.  Often this allows for simpler code.

### Parameters:
range - the first DatumRange
<br>include - the second DatumRange

### Returns:
a DatumRange that contains parts of both ranges, or is zero-width.
### See Also:
<a href='DatumRange.md#intersection'>DatumRange#intersection(org.das2.datum.DatumRange)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=sloppyIntersection&unscoped_q=sloppyIntersection">[search for examples]</a>

***
<a name="union"></a>
# union
union( Datum d1, Datum d2 ) &rarr; DatumRange

return a datum range that sloppily covers the d1 and d2.
 (The bigger of the two will be the exclusive max.)

### Parameters:
d1 - a Datum
<br>d2 - a Datum

### Returns:
a DatumRange


<a href="https://github.com/autoplot/dev/search?q=union&unscoped_q=union">[search for examples]</a>

union( DatumRange range, Datum include ) &rarr; DatumRange<br>
union( DatumRange range, DatumRange include ) &rarr; DatumRange<br>
