# org.das2.datum.TimeUtilVarious time utilities
***
<a name="YEAR"></a>
# YEAR



***
<a name="MONTH"></a>
# MONTH



***
<a name="DAY"></a>
# DAY



***
<a name="HOUR"></a>
# HOUR



***
<a name="MINUTE"></a>
# MINUTE



***
<a name="SECOND"></a>
# SECOND



***
<a name="MILLI"></a>
# MILLI



***
<a name="MICRO"></a>
# MICRO



***
<a name="NANO"></a>
# NANO



***
<a name="WEEK"></a>
# WEEK



***
<a name="QUARTER"></a>
# QUARTER



***
<a name="HALF_YEAR"></a>
# HALF_YEAR



***
<a name="TD_YEAR"></a>
# TD_YEAR



***
<a name="TD_MONTH"></a>
# TD_MONTH



***
<a name="TD_DAY"></a>
# TD_DAY



***
<a name="TD_HOUR"></a>
# TD_HOUR



***
<a name="TD_MINUTE"></a>
# TD_MINUTE



***
<a name="TD_SECOND"></a>
# TD_SECOND



***
<a name="TD_MILLI"></a>
# TD_MILLI



***
<a name="TD_MICRO"></a>
# TD_MICRO



***
<a name="TD_NANO"></a>
# TD_NANO



***
<a name="add"></a>
# add
add( org.das2.datum.TimeUtil.TimeStruct a, org.das2.datum.TimeUtil.TimeStruct b ) &rarr; TimeStruct



### Parameters:
a - a TimeUtil.TimeStruct
<br>b - a TimeUtil.TimeStruct

### Returns:
org.das2.datum.TimeUtil.TimeStruct


<a href="https://github.com/autoplot/dev/search?q=add&unscoped_q=add">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="borrow"></a>
# borrow
borrow( org.das2.datum.TimeUtil.TimeStruct t ) &rarr; TimeStruct

Normalize the TimeStruct by decrementing higher digits.

### Parameters:
t - the time.

### Returns:
the normalized TimeStruct
### See Also:
<a href='#normalize'>normalize(org.das2.datum.TimeUtil.TimeStruct)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=borrow&unscoped_q=borrow">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="carry"></a>
# carry
carry( org.das2.datum.TimeUtil.TimeStruct t ) &rarr; TimeStruct

Normalize the TimeStruct by incrementing higher digits.  For
 example, 2002-01-01T24:00 &rarr;  2002-01-02T00:00.
 This will only carry one to the next higher place, so 70 seconds is handled but not 130.
 2015-09-08: this now supports leap seconds.

### Parameters:
t - a time structure

### Returns:
a time structure where extra minutes are moved into hours, etc.

<a href="https://github.com/autoplot/dev/search?q=carry&unscoped_q=carry">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="ceil"></a>
# ceil
ceil( int step, Datum datum ) &rarr; Datum

return the next ordinal boundary if we aren't at one already.

### Parameters:
step - the ordinal location, such as TimeUtil.DAY or TimeUtil.HALF_YEAR
<br>datum - the location.

### Returns:
the next ordinal boundary if we aren't at one already.

<a href="https://github.com/autoplot/dev/search?q=ceil&unscoped_q=ceil">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="convert"></a>
# convert
convert( int year, int month, int day, int hour, int minute, double second, org.das2.datum.TimeLocationUnits units ) &rarr; double

convert the month components to a double in the given units.

### Parameters:
year - the year, which must be greater than 1582
<br>month - the month
<br>day - the day of month, unless month==0, then day is day of year.
<br>hour - additional hours
<br>minute - additional minutes
<br>second - additional seconds
<br>units - the Units in which to return the result.

### Returns:
a double in the given units.

<a href="https://github.com/autoplot/dev/search?q=convert&unscoped_q=convert">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="create"></a>
# create
create( String s ) &rarr; Datum

Creates a datum from a string

### Parameters:
s - a String

### Returns:
a Datum


<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createTimeDatum"></a>
# createTimeDatum
createTimeDatum( int year, int month, int day, int hour, int minute, int second, int nano ) &rarr; Datum

creates a Datum representing the time given in integer years, months, ..., seconds, nanoseconds.  The year
 must be at least 1000, and must be a four-digit year.  A double in Units.us2000 is used to represent the
 Datum, so resolution will drop as the year drops away from 2000.

### Parameters:
year - four digit year &gt;= 1060.
<br>month - integer month, 1..12.
<br>day - integer day of month.
<br>hour - additional hours
<br>minute - additional minutes
<br>second - additional seconds
<br>nano - additional nanoseconds

### Returns:
a Datum with units Units.us2000.

<a href="https://github.com/autoplot/dev/search?q=createTimeDatum&unscoped_q=createTimeDatum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createValid"></a>
# createValid
createValid( String validString ) &rarr; Datum

creates a Datum from a string which is known to contain
 a valid time format.  Throws a RuntimeException if the
 string is not valid.

### Parameters:
validString - a String

### Returns:
a Datum


<a href="https://github.com/autoplot/dev/search?q=createValid&unscoped_q=createValid">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="dayContaining"></a>
# dayContaining
dayContaining( Datum t ) &rarr; DatumRange

return a DatumRange for the day containing the given time.  Midnight
 is contained within the following day.

### Parameters:
t - a time.

### Returns:
the day containing the time.

<a href="https://github.com/autoplot/dev/search?q=dayContaining&unscoped_q=dayContaining">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="dayOfYear"></a>
# dayOfYear
dayOfYear( int month, int day, int year ) &rarr; int

return the day of year for the month and day, for the given year

### Parameters:
month - the month, january=1, february=2, etc.
<br>day - day of month
<br>year - four-digit year

### Returns:
the day of year

<a href="https://github.com/autoplot/dev/search?q=dayOfYear&unscoped_q=dayOfYear">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="daysInMonth"></a>
# daysInMonth
daysInMonth( int month, int year ) &rarr; int



### Parameters:
month - an int
<br>year - an int

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=daysInMonth&unscoped_q=daysInMonth">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="floor"></a>
# floor
floor( int step, Datum datum ) &rarr; Datum

return the previous ordinal boundary if we aren't at one already.

### Parameters:
step - the ordinal location, such as TimeUtil.DAY or TimeUtil.HALF_YEAR
<br>datum - the location.

### Returns:
the previous ordinal boundary if we aren't at one already.

<a href="https://github.com/autoplot/dev/search?q=floor&unscoped_q=floor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="fromDatum"></a>
# fromDatum
fromDatum( Datum time ) &rarr; int

returns the 7-element array of components from the time location datum:
 0:year, 1:month, 2:day, 3:hour, 4:minute, 5:second, 6:nanoseconds

### Parameters:
time - a Datum

### Returns:
seven-element int array.

<a href="https://github.com/autoplot/dev/search?q=fromDatum&unscoped_q=fromDatum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getJulianDay"></a>
# getJulianDay
getJulianDay( Datum datum ) &rarr; int

return the the integer number of days that have elapsed since roughly Monday, January 1, 4713 BC.  Julian Day
 is defined as starting at noon UT, here is is defined starting at midnight.

### Parameters:
datum - a Datum

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=getJulianDay&unscoped_q=getJulianDay">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getJulianDay( long val, Units units ) &rarr; int<br>
***
<a name="getMicroSecondsSinceMidnight"></a>
# getMicroSecondsSinceMidnight
getMicroSecondsSinceMidnight( Datum datum ) &rarr; double

return the number of microseconds elapsed since the last midnight.

### Parameters:
datum - a Datum

### Returns:
a double


<a href="https://github.com/autoplot/dev/search?q=getMicroSecondsSinceMidnight&unscoped_q=getMicroSecondsSinceMidnight">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSecondsSinceMidnight"></a>
# getSecondsSinceMidnight
getSecondsSinceMidnight( Datum datum ) &rarr; double

return the number of seconds elapsed since the last midnight.

### Parameters:
datum - a Datum

### Returns:
a double


<a href="https://github.com/autoplot/dev/search?q=getSecondsSinceMidnight&unscoped_q=getSecondsSinceMidnight">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isLeapYear"></a>
# isLeapYear
isLeapYear( int year ) &rarr; boolean

return the leap year for years 1901-2099.

### Parameters:
year - an int

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isLeapYear&unscoped_q=isLeapYear">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isValidTime"></a>
# isValidTime
isValidTime( String string ) &rarr; boolean



### Parameters:
string - a String

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isValidTime&unscoped_q=isValidTime">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="julianDay"></a>
# julianDay
julianDay( int year, int month, int day ) &rarr; int

return the julianDay for the year month and day.  This was verified
 against another calculation (julianDayWP, commented out above) from 
 http://en.wikipedia.org/wiki/Julian_day.  Both calculations have 20 operations.
 Note this does not match

### Parameters:
year - calendar year greater than 1582.
<br>month - an int
<br>day - day of month. For day of year, use month=1 and doy for day.

### Returns:
the Julian day
### See Also:
<a href='julianToGregorian.md'>julianToGregorian</a> <br>

<a href="https://github.com/autoplot/dev/search?q=julianDay&unscoped_q=julianDay">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="julianDayIMCCE"></a>
# julianDayIMCCE
julianDayIMCCE( int YY, int MM, int DD ) &rarr; int

calculation of julianDay based on http://www.imcce.fr/en/grandpublic/temps/jour_julien.php
 This is slightly slower because of a cusp at 1582, but is accurate
 before these times.

### Parameters:
YY - Gregorian year
<br>MM - Gregorian month
<br>DD - Gregorian day

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=julianDayIMCCE&unscoped_q=julianDayIMCCE">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="julianToGregorian"></a>
# julianToGregorian
julianToGregorian( int julian ) &rarr; TimeStruct

Break the Julian day apart into month, day year.  This is based on
http://en.wikipedia.org/wiki/Julian_day (GNU Public License), and 
was introduced when toTimeStruct failed when the year was 1886.

### Parameters:
julian - the (integer) number of days that have elapsed since the initial epoch at noon Universal Time (UT) Monday, January 1, 4713 BC

### Returns:
a TimeStruct with the month, day and year fields set.
### See Also:
<a href='julianDay.md'>julianDay( int year, int mon, int day )</a> <br>

<a href="https://github.com/autoplot/dev/search?q=julianToGregorian&unscoped_q=julianToGregorian">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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
<a name="monthNameAbbrev"></a>
# monthNameAbbrev
monthNameAbbrev( int mon ) &rarr; String

returns "Jan", "Feb", ... for month number (1..12).

### Parameters:
mon - integer from 1 to 12.

### Returns:
three character English month name.

<a href="https://github.com/autoplot/dev/search?q=monthNameAbbrev&unscoped_q=monthNameAbbrev">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="monthNumber"></a>
# monthNumber
monthNumber( String s ) &rarr; int

returns 1..12 for the English month name.  (Sorry, rest of world...)

### Parameters:
s - the three-letter month name, jan,feb,...,nov,dec

### Returns:
1,2,...,11,12 for the English month name

<a href="https://github.com/autoplot/dev/search?q=monthNumber&unscoped_q=monthNumber">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="next"></a>
# next
next( org.das2.datum.TimeUtil.TimeDigit td, int count, Datum datum ) &rarr; Datum

return the next boundary

### Parameters:
td - the boundary, e.g. TimeUtil.TD_HALF_YEAR
<br>count - the number of boundaries
<br>datum - the starting point.

### Returns:
the boundary

<a href="https://github.com/autoplot/dev/search?q=next&unscoped_q=next">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

next( int step, Datum datum ) &rarr; Datum<br>
***
<a name="nextMidnight"></a>
# nextMidnight
nextMidnight( Datum datum ) &rarr; Datum

provide the next midnight, similar to the ceil function, noting that
 if the datum provided is midnight already then it is simply returned.

### Parameters:
datum - a Datum

### Returns:
the Datum for the next day boundary.

<a href="https://github.com/autoplot/dev/search?q=nextMidnight&unscoped_q=nextMidnight">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="nextMonth"></a>
# <del>nextMonth</del>
Deprecated: Use next(MONTH,datum) instead
***
<a name="normalize"></a>
# normalize
normalize( org.das2.datum.TimeUtil.TimeStruct t ) &rarr; TimeStruct

convert times like "2000-01-01T24:00" to "2000-01-02T00:00" and
 "2000-002T00:00" to "2000-01-02T00:00".
 This will only carry one to the next higher place, so 70 seconds is handled but not 130.

### Parameters:
t - a TimeUtil.TimeStruct

### Returns:
an org.das2.datum.TimeUtil.TimeStruct

### See Also:
<a href='#borrow'>borrow(org.das2.datum.TimeUtil.TimeStruct)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=normalize&unscoped_q=normalize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="now"></a>
# now
now(  ) &rarr; Datum

return the current time as a Datum.

### Returns:
the current time as a Datum.

<a href="https://github.com/autoplot/dev/search?q=now&unscoped_q=now">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parseTime"></a>
# parseTime
parseTime( String s ) &rarr; TimeStruct

parse the time into a timestruct.

### Parameters:
s - a String

### Returns:
an org.das2.datum.TimeUtil.TimeStruct

### See Also:
<a href='#createValid'>createValid(java.lang.String)</a> createValid which creates a Datum.<br>

<a href="https://github.com/autoplot/dev/search?q=parseTime&unscoped_q=parseTime">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="prev"></a>
# prev
prev( int step, Datum datum ) &rarr; Datum

step down the previous ordinal.  If the datum is already at an ordinal
 boundary, then step down by one ordinal.

### Parameters:
step - the ordinal location, such as TimeUtil.DAY or TimeUtil.HALF_YEAR
<br>datum - the location.

### Returns:
the prev boundary location.

<a href="https://github.com/autoplot/dev/search?q=prev&unscoped_q=prev">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="prevMidnight"></a>
# prevMidnight
prevMidnight( Datum datum ) &rarr; Datum

provide the previous midnight, similar to the floor function, noting that
 if the datum provided is midnight exactly then it is simply returned.

### Parameters:
datum - a Datum

### Returns:
the Datum for the next day boundary.

<a href="https://github.com/autoplot/dev/search?q=prevMidnight&unscoped_q=prevMidnight">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="prevWeek"></a>
# prevWeek
prevWeek( Datum datum ) &rarr; Datum

decrement by 7 days.

### Parameters:
datum - a Datum

### Returns:
the datum

<a href="https://github.com/autoplot/dev/search?q=prevWeek&unscoped_q=prevWeek">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="roundNDigits"></a>
# roundNDigits
roundNDigits( org.das2.datum.TimeUtil.TimeStruct ts, int n ) &rarr; TimeStruct

round seconds to N decimal places.  For example, n=3 means round to the 
 millisecond.

### Parameters:
ts - a time structure
<br>n - number of digits, 3 is millis, 6 is micros.

### Returns:
rounded and normalized TimeStruct.

<a href="https://github.com/autoplot/dev/search?q=roundNDigits&unscoped_q=roundNDigits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="subtract"></a>
# subtract
subtract( org.das2.datum.TimeUtil.TimeStruct a, org.das2.datum.TimeUtil.TimeStruct b ) &rarr; TimeStruct



### Parameters:
a - a TimeUtil.TimeStruct
<br>b - a TimeUtil.TimeStruct

### Returns:
org.das2.datum.TimeUtil.TimeStruct


<a href="https://github.com/autoplot/dev/search?q=subtract&unscoped_q=subtract">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toDatum"></a>
# toDatum
toDatum( org.das2.datum.TimeUtil.TimeStruct d ) &rarr; Datum

convert to Datum without regard to the type of unit used to represent time.
 This will use the canonical Units.us2000 for time locations, which does 
 not represent leap seconds.

### Parameters:
d - the decomposed time or time width.

### Returns:
the Datum.

<a href="https://github.com/autoplot/dev/search?q=toDatum&unscoped_q=toDatum">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

toDatum( org.das2.datum.TimeUtil.TimeStruct d, Units u ) &rarr; Datum<br>
toDatum( int[] timeArray ) &rarr; Datum<br>
toDatum( int[] timeArray, Units u ) &rarr; Datum<br>
***
<a name="toDatumDuration"></a>
# toDatumDuration
toDatumDuration( int[] timeArray ) &rarr; Datum

return approximate duration in Units.seconds or in Units.days.
 This is assuming a year is 365 days, a month is 30 days, and a day 
 is 86400 seconds.

### Parameters:
timeArray - 6 or 7 element array [ yrs, months, days, hours, minutes, seconds, nanos ]

### Returns:
a Datum

### See Also:
<a href='DatumRangeUtil.md#parseISO8601Duration'>DatumRangeUtil#parseISO8601Duration(java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=toDatumDuration&unscoped_q=toDatumDuration">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toTimeArray"></a>
# <del>toTimeArray</del>
Deprecated: use 7-element fromDatum instead, which is consistent with toDatum.  Note the array elements are different!
***
<a name="toTimeStruct"></a>
# toTimeStruct
toTimeStruct( org.das2.datum.Datum.Long datum ) &rarr; TimeStruct

splits the time location datum into y,m,d,etc components, using the full
 precision of the Long backing the Datum.  The datum can have the units
 of ms1970 or cdf_tt2000, and

### Parameters:
datum - with time location units.

### Returns:
TimeStruct containing the time components.

<a href="https://github.com/autoplot/dev/search?q=toTimeStruct&unscoped_q=toTimeStruct">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

toTimeStruct( Datum datum ) &rarr; TimeStruct<br>
