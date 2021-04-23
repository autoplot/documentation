# org.das2.datum.format.TimeDatumFormatter

Formatter is configured with strings of SimpleDateFormat (yyyy-MM-DD)
 or % percent format (%Y-%m-%d) specifiers.  
 SimpleDateFormat is discouraged because most other parts of das2 use the
 shorter form.
 This does not support formats with seconds but no hours and minutes, like "$Y $j $S"

# TimeDatumFormatter( String formatString )
Creates a new instance of TimeDatumFormatter

***
<a name="DEFAULT"></a>
# DEFAULT

yyyy-MM-dd'T'HH:mm:ss.SSS'Z

***
<a name="DAYS"></a>
# DAYS

yyyy-MM-dd

***
<a name="DAY_OF_YEAR"></a>
# DAY_OF_YEAR

yyyy-JJJ

***
<a name="DOY_DAYS"></a>
# DOY_DAYS

yyyy-MM-dd (JJJ)

***
<a name="YEARS"></a>
# YEARS

yyyy

***
<a name="MONTHS"></a>
# MONTHS

yyyy-MM

***
<a name="HOURS"></a>
# HOURS

yyyy-MM-dd HH:'00'

***
<a name="MINUTES"></a>
# MINUTES

HH:mm

***
<a name="SECONDS"></a>
# SECONDS

HH:mm:ss

***
<a name="MILLISECONDS"></a>
# MILLISECONDS

HH:mm:ss.SSS

***
<a name="MICROSECONDS"></a>
# MICROSECONDS

HH:mm:ss.SSSSSS

***
<a name="NANOSECONDS"></a>
# NANOSECONDS

HH:mm:ss.SSSSSSSSS

***
<a name="format"></a>
# format
format( Datum datum ) &rarr; String



### Parameters:
datum - a Datum

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=format&unscoped_q=format">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="formatterForScale"></a>
# formatterForScale
formatterForScale( int scale, DatumRange context ) &rarr; TimeDatumFormatter

returns a TimeDatumFormatter suitable for the specified scale and context.
 Context may be null to indicate that the formatted string will be interpreted
 outside of any context.

### Parameters:
scale - the length we wish to represent, such as TimeUtil.HOUR
<br>context - the context for the formatter, or null if the formatted string
   will be interpreted outside of any context.

### Returns:
the formatter.

<a href="https://github.com/autoplot/dev/search?q=formatterForScale&unscoped_q=formatterForScale">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

formatterForScale( int scale, DatumRange context, boolean useDOY ) &rarr; TimeDatumFormatter<br>
***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

