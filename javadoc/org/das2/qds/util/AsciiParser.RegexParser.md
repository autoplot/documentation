# org.das2.qds.util.AsciiParser.RegexParser

parser uses a regular expression to match each record.

# RegexParser( org.das2.qds.util.AsciiParser parser, String regex )


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
<a name="fields"></a>
# fields
fields( String line ) &rarr; String

show the fields found in the line.  This assumes the line 
 will match.

### Parameters:
line - a String

### Returns:
the groups.

<a href="https://github.com/autoplot/dev/search?q=fields&unscoped_q=fields">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNamedGroups"></a>
# getNamedGroups
getNamedGroups( String regex ) &rarr; String



### Parameters:
regex - a String

### Returns:
java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=getNamedGroups&unscoped_q=getNamedGroups">[search for examples]</a>
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
<a name="splitRecord"></a>
# splitRecord
splitRecord( String line, java.lang.String[] fields ) &rarr; boolean



### Parameters:
line - a String
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

