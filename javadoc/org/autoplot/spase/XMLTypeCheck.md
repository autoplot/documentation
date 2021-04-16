# org.autoplot.spase.XMLTypeCheckChecks to see if this sort of XML file is handled.  This works with a SAX
 parser, and looks at the tags to see if a file appears to be of a given type.
XMLTypeCheck( )


***
<a name="TYPE_HELM"></a>
# TYPE_HELM



***
<a name="TYPE_SPASE"></a>
# TYPE_SPASE



***
<a name="TYPE_VOTABLE"></a>
# TYPE_VOTABLE



***
<a name="calculateType"></a>
# calculateType
calculateType( java.io.File f ) &rarr; Object

use a sax parser to get the type.  Return
 TYPE_VOTABLE, TYPE_HELM, TYPE_SPASE

### Parameters:
f - a File

### Returns:
an Object


<a href="https://github.com/autoplot/dev/search?q=calculateType&unscoped_q=calculateType">[search for examples]</a>

***
<a name="startDocument"></a>
# startDocument
startDocument(  ) &rarr; void

initialize the state to STATE_OPEN.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=startDocument&unscoped_q=startDocument">[search for examples]</a>

***
<a name="startElement"></a>
# startElement
startElement( String uri, String localName, String qName, org.xml.sax.Attributes attributes ) &rarr; void

As elements come in, we go through the state transitions to keep track of
 whether we are reading FIELDS, Rows of the dataset, Individual columns, etc.

### Parameters:
uri - a String
<br>localName - a String
<br>qName - a String
<br>attributes - an Attributes

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=startElement&unscoped_q=startElement">[search for examples]</a>

