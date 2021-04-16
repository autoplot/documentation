# org.das2.qstream.SerializeDelegateinterface for serializing (formatting) and parsing objects.
***
<a name="format"></a>
# format
format( Object o ) &rarr; String

format the object.

### Parameters:
o - the object

### Returns:
the string representation of the object.

<a href="https://github.com/autoplot/dev/search?q=format&unscoped_q=format">[search for examples]</a>

***
<a name="parse"></a>
# parse
parse( String typeId, String s ) &rarr; Object

parse the object from the string

### Parameters:
typeId - the type ID
<br>s - the string, e.g. "royalBlue"

### Returns:
the object, e.g. Color.decode("#4169E1")

<a href="https://github.com/autoplot/dev/search?q=parse&unscoped_q=parse">[search for examples]</a>

***
<a name="typeId"></a>
# typeId
typeId( java.lang.Class clas ) &rarr; String

identifier for the delegate, that is used to qualify the name of the thing formatted.

### Parameters:
clas - the class

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=typeId&unscoped_q=typeId">[search for examples]</a>

