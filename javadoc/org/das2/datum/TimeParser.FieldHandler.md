# org.das2.datum.TimeParser.FieldHandler

Interface to add custom handlers for strings with unique formats.  For example, the RPWS group had files with
 two-hex digits indicating the ten-minute interval covered by the file name.  This is also used for orbits.
 TODO: FieldHandler needs to report its affect on the LSD.  (Autoplot gets versioning).

***
<a name="configure"></a>
# configure
configure( java.util.Map args ) &rarr; String

arguments for the parser are passed in.

### Parameters:
args - map of arguments.  $(t,a1=v1,a2=v2,a3=v3)

### Returns:
null if the string is parseable, an error message otherwise.

<a href="https://github.com/autoplot/dev/search?q=configure&unscoped_q=configure">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="format"></a>
# format
format( org.das2.datum.TimeUtil.TimeStruct startTime, org.das2.datum.TimeUtil.TimeStruct timeWidth, int length, java.util.Map extra ) &rarr; String

create a string given the times, when this is possible.  An IllegalArgumentException should be thrown when this is 
 not possible, but be loose so this can be composed with other field handlers.  For example, imagine the $Y field handler.
 This should not throw an exception when 2012-03-29 is passed in because it's not 2012-01-01, because the $m and $d might
 be used later.  However if a time is specified for a year before the first orbit of a spacecraft, then an exception
 should be thrown because there is an error that the developer is going to have to deal with.

### Parameters:
startTime - a TimeUtil.TimeStruct
<br>timeWidth - a TimeUtil.TimeStruct
<br>length - an int
<br>extra - extra data, such as version numbers, are passed in here.

### Returns:
the string representing the time range specified.

<a href="https://github.com/autoplot/dev/search?q=format&unscoped_q=format">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRegex"></a>
# getRegex
getRegex(  ) &rarr; String

return a regular expression that matches valid field entries.  ".*" can be used to match anything, but this limits use.
 TODO: where is this used?  I added it because it's easy and I saw a TODO to add it.

### Returns:
null to match anything, or a regular expression matching valid entries.

<a href="https://github.com/autoplot/dev/search?q=getRegex&unscoped_q=getRegex">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parse"></a>
# parse
parse( String fieldContent, org.das2.datum.TimeUtil.TimeStruct startTime, org.das2.datum.TimeUtil.TimeStruct timeWidth, java.util.Map extra ) &rarr; void

parse the field to interpret as a time range.

### Parameters:
fieldContent - the field to parse, for example "2014" for $Y
<br>startTime - the current startTime
<br>timeWidth - the current timeWidth
<br>extra - extra data, such as version numbers, are passed out here.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=parse&unscoped_q=parse">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

