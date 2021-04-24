# org.das2.qstream.DatumRangeSerializeDelegate

This serialize delegate assumes the formatted object is a time range,
 and if it doesn't parse then it's a datum range.  Time Ranges
 may be explicitly declared with "time:" prefix.

# DatumRangeSerializeDelegate( )


***
<a name="format"></a>
# format
format( Object o ) &rarr; String



### Parameters:
o - an Object

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=format&unscoped_q=format">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parse"></a>
# parse
parse( String typeId, String s ) &rarr; Object



### Parameters:
typeId - a String
<br>s - a String

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=parse&unscoped_q=parse">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="typeId"></a>
# typeId
typeId( java.lang.Class clas ) &rarr; String



### Parameters:
clas - a java.lang.Class

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=typeId&unscoped_q=typeId">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="xmlFormat"></a>
# xmlFormat
xmlFormat( org.w3c.dom.Document doc, Object o ) &rarr; Element



### Parameters:
doc - a Document
<br>o - an Object

### Returns:
org.w3c.dom.Element


<a href="https://github.com/autoplot/dev/search?q=xmlFormat&unscoped_q=xmlFormat">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="xmlParse"></a>
# xmlParse
xmlParse( org.w3c.dom.Element e ) &rarr; Object



### Parameters:
e - an Element

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=xmlParse&unscoped_q=xmlParse">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

