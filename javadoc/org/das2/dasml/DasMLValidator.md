# org.das2.dasml.DasMLValidatorA validator for the dasML language developed for the University of
 Iowa Space Plasma Wave Group.  This class is used as a pre-processor
 to (hopefully) provide clear and helpful error messages.

 Warning:  This class is not thread-safe.  Unexpected results can occur
    if multiple threads use an instance of this class concurrently.
DasMLValidator( )
Creates a new instance of DasMLValidator

***
<a name="INTEGER_PATTERN"></a>
# INTEGER_PATTERN



***
<a name="WINDOW_POSITION_PATTERN"></a>
# WINDOW_POSITION_PATTERN



***
<a name="FLOAT_PATTERN"></a>
# FLOAT_PATTERN



***
<a name="endDocument"></a>
# endDocument
endDocument(  ) &rarr; void

Receive notification of the end of the document.

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/xml/sax/ContentHandler.md#endDocument'>org.xml.sax.ContentHandler#endDocument</a> <br>

<a href="https://github.com/autoplot/dev/search?q=endDocument&unscoped_q=endDocument">[search for examples]</a>

***
<a name="endElement"></a>
# endElement
endElement( String uri, String localName, String qName ) &rarr; void



### Parameters:
uri - a String
<br>localName - a String
<br>qName - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=endElement&unscoped_q=endElement">[search for examples]</a>

***
<a name="error"></a>
# error
error( org.xml.sax.SAXParseException e ) &rarr; void

Receive notification of a recoverable parser error.

### Parameters:
e - The warning information encoded as an exception.

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/xml/sax/ErrorHandler.md#warning'>org.xml.sax.ErrorHandler#warning</a> <br>
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/xml/sax/SAXParseException.md'>org.xml.sax.SAXParseException</a> <br>

<a href="https://github.com/autoplot/dev/search?q=error&unscoped_q=error">[search for examples]</a>

***
<a name="fatalError"></a>
# fatalError
fatalError( org.xml.sax.SAXParseException e ) &rarr; void

Report a fatal XML parsing error.

### Parameters:
e - The error information encoded as an exception.

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/xml/sax/ErrorHandler.md#fatalError'>org.xml.sax.ErrorHandler#fatalError</a> <br>
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/xml/sax/SAXParseException.md'>org.xml.sax.SAXParseException</a> <br>

<a href="https://github.com/autoplot/dev/search?q=fatalError&unscoped_q=fatalError">[search for examples]</a>

***
<a name="getLastError"></a>
# getLastError
getLastError(  ) &rarr; SAXException

Returns the last error encountered by this validator
 or null if no error has been found.  This method
 will only return an error if the last call to
 validate(InputSource, ErrorHandler) returned false.
 If an application wishes to have access to warnings
 and non-fatal errors then an ErrorHandler must be provided.

### Returns:
the last error.

<a href="https://github.com/autoplot/dev/search?q=getLastError&unscoped_q=getLastError">[search for examples]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

***
<a name="setDocumentLocator"></a>
# setDocumentLocator
setDocumentLocator( org.xml.sax.Locator locator ) &rarr; void

Receive a Locator object for document events.

### Parameters:
locator - A locator for all SAX document events.

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/xml/sax/ContentHandler.md#setDocumentLocator'>org.xml.sax.ContentHandler#setDocumentLocator</a> <br>
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/xml/sax/Locator.md'>org.xml.sax.Locator</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setDocumentLocator&unscoped_q=setDocumentLocator">[search for examples]</a>

***
<a name="startDocument"></a>
# startDocument
startDocument(  ) &rarr; void

Receive notification of the beginning of the document.

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/xml/sax/ContentHandler.md#startDocument'>org.xml.sax.ContentHandler#startDocument</a> <br>

<a href="https://github.com/autoplot/dev/search?q=startDocument&unscoped_q=startDocument">[search for examples]</a>

***
<a name="startElement"></a>
# startElement
startElement( String uri, String localName, String qName, org.xml.sax.Attributes attributes ) &rarr; void

Receive notification of the start of an element.

### Parameters:
uri - a String
<br>localName - a String
<br>qName - The element type name.
<br>attributes - The specified or defaulted attributes.

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/xml/sax/ContentHandler.md#startElement'>org.xml.sax.ContentHandler#startElement</a> <br>

<a href="https://github.com/autoplot/dev/search?q=startElement&unscoped_q=startElement">[search for examples]</a>

***
<a name="validate"></a>
# validate
validate( org.xml.sax.InputSource source, org.xml.sax.ErrorHandler errorHandler ) &rarr; boolean

Parses and validates a dasML document.  All errors are
 passed to the ErrorHandler instance specified.  SAXExceptions
 thrown by the underlying parser are caught and suppressed by
 this method.  If an application needs access to the errors,
 an ErrorHandler must be provided.

### Parameters:
source - The source of the XML document
<br>errorHandler - The ErrorHandler instance that will receive
    error messages from the parser.  This can be null

### Returns:
true if the document is a valid dasML document.

<a href="https://github.com/autoplot/dev/search?q=validate&unscoped_q=validate">[search for examples]</a>

***
<a name="warning"></a>
# warning
warning( org.xml.sax.SAXParseException e ) &rarr; void

Receive notification of a parser warning.

### Parameters:
e - The warning information encoded as an exception.

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/xml/sax/ErrorHandler.md#warning'>org.xml.sax.ErrorHandler#warning</a> <br>
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/xml/sax/SAXParseException.md'>org.xml.sax.SAXParseException</a> <br>

<a href="https://github.com/autoplot/dev/search?q=warning&unscoped_q=warning">[search for examples]</a>

