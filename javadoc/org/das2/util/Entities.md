# org.das2.util.Entities
Entities( )


***
<a name="decode"></a>
# decode
decode( String entity ) &rarr; String

decode one entity.

### Parameters:
entity - like &amp;rho;

### Returns:
string with unicode like "&rho;"

<a href="https://github.com/autoplot/dev/search?q=decode&unscoped_q=decode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="decodeEntities"></a>
# decodeEntities
decodeEntities( String str ) &rarr; String

utility method for decoding entities like &amp;rho; into unicode.
 Malformed entities (like &#03B1; instead of &#x03B1;) are formatted as "???"

### Parameters:
str - string e.g. "&rho; degrees"

### Returns:
string with unicode characters for entities.

<a href="https://github.com/autoplot/dev/search?q=decodeEntities&unscoped_q=decodeEntities">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="encode"></a>
# encode
encode( String s ) &rarr; String

encode one entity.

### Parameters:
s - string with unicode like "&rho;"

### Returns:
like &amp;rho;

<a href="https://github.com/autoplot/dev/search?q=encode&unscoped_q=encode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

