# org.das2.qds.util.AsciiParser.DelimParser

DelimParser splits the line on a regex (like "," or "\\s+") to create the fields.
 Trailing and leading whitespace is ignored.

# DelimParser( int fieldCount, String delim )


***
<a name="header"></a>
# header



***
<a name="fieldCount"></a>
# fieldCount
fieldCount(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=fieldCount&unscoped_q=fieldCount">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

fieldCount( String line ) &rarr; int<br>
***
<a name="getDelim"></a>
# getDelim
getDelim(  ) &rarr; String

returns the delimiter, which is a regex.  Examples include "," "\t", and "\s+"

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getDelim&unscoped_q=getDelim">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readNextRecord"></a>
# readNextRecord
readNextRecord( java.io.BufferedReader reader ) &rarr; String



### Parameters:
reader - a BufferedReader

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=readNextRecord&unscoped_q=readNextRecord">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setGuessUnits"></a>
# setGuessUnits
setGuessUnits( boolean guess ) &rarr; void

if true, then try to guess the units of the data coming in.  If most
 fields will be non-enumeration, then the flag is cleared.

### Parameters:
guess - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setGuessUnits&unscoped_q=setGuessUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setShowException"></a>
# setShowException
setShowException( boolean s ) &rarr; void



### Parameters:
s - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setShowException&unscoped_q=setShowException">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSkipField"></a>
# setSkipField
setSkipField( int ifield, boolean skip ) &rarr; void



### Parameters:
ifield - an int
<br>skip - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSkipField&unscoped_q=setSkipField">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="splitRecord"></a>
# splitRecord
splitRecord( String input, java.lang.String[] fields ) &rarr; boolean



### Parameters:
input - a String
<br>fields - a java.lang.String[]

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=splitRecord&unscoped_q=splitRecord">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="tryParseRecord"></a>
# tryParseRecord
tryParseRecord( String line, int irec, org.das2.qds.util.DataSetBuilder builder ) &rarr; boolean



### Parameters:
line - a String
<br>irec - an int
<br>builder - a DataSetBuilder

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=tryParseRecord&unscoped_q=tryParseRecord">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

