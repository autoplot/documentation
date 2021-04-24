# org.das2.qstream.AsciiTimeTransferType

ISO-8601 encoded times.

# AsciiTimeTransferType( int sizeBytes, Units units )
create the ISO8601 transfer type.

***
<a name="getByName"></a>
# getByName
getByName( String name, java.util.Map properties ) &rarr; TransferType



### Parameters:
name - a String
<br>properties - a java.util.Map

### Returns:
org.das2.qstream.TransferType


<a href="https://github.com/autoplot/dev/search?q=getByName&unscoped_q=getByName">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="name"></a>
# name
name(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=name&unscoped_q=name">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="read"></a>
# read
read( java.nio.ByteBuffer buffer ) &rarr; double



### Parameters:
buffer - a ByteBuffer

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=read&unscoped_q=read">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="write"></a>
# write
write( double d, java.nio.ByteBuffer buffer ) &rarr; void



### Parameters:
d - a double
<br>buffer - a ByteBuffer

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=write&unscoped_q=write">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

