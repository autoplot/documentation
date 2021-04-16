# org.das2.qds.util.dd.ParseExceptionThis exception is thrown when parse errors are encountered.
 You can explicitly create objects of this exception type by
 calling the method generateParseException in the generated
 parser.

 You can modify this class to customize your error reporting
 mechanisms so long as you retain the public fields.
ParseException( org.das2.qds.util.dd.Token currentTokenVal, int[][] expectedTokenSequencesVal, java.lang.String[] tokenImageVal )
This constructor is used by the method "generateParseException"
 in the generated parser.  Calling this constructor generates
 a new object of this type with the fields "currentToken",
 "expectedTokenSequences", and "tokenImage" set.

ParseException( )
The following constructors are for use by you for whatever
 purpose you can think of.  Constructing the exception in this
 manner makes the exception behave in the normal way - i.e., as
 documented in the class "Throwable".  The fields "errorToken",
 "expectedTokenSequences", and "tokenImage" do not contain
 relevant information.  The JavaCC generated code does not use
 these constructors.

ParseException( String message )
Constructor with message.

***
<a name="currentToken"></a>
# currentToken

This is the last token that has been consumed successfully.  If
 this object has been created due to a parse error, the token
 followng this token will (therefore) be the first error token.

***
<a name="expectedTokenSequences"></a>
# expectedTokenSequences

Each entry in this array is an array of integers.  Each array
 of integers represents a sequence of tokens (by their ordinal
 values) that is expected at this point of the parse.

***
<a name="tokenImage"></a>
# tokenImage

This is a reference to the "tokenImage" array of the generated
 parser within which the parse error occurred.  This array is
 defined in the generated ...Constants interface.

