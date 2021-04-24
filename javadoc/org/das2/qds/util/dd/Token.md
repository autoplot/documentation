# org.das2.qds.util.dd.Token

Describes the input token stream.

# Token( )
No-argument constructor

# Token( int kind )
Constructs a new token for the specified Image.

# Token( int kind, String image )
Constructs a new token for the specified Image and Kind.

***
<a name="kind"></a>
# kind

An integer that describes the kind of this token.  This numbering
 system is determined by JavaCCParser, and a table of these numbers is
 stored in the file ...Constants.java.

***
<a name="beginLine"></a>
# beginLine

The line number of the first character of this Token.

***
<a name="beginColumn"></a>
# beginColumn

The column number of the first character of this Token.

***
<a name="endLine"></a>
# endLine

The line number of the last character of this Token.

***
<a name="endColumn"></a>
# endColumn

The column number of the last character of this Token.

***
<a name="image"></a>
# image

The string image of the token.

***
<a name="next"></a>
# next

A reference to the next regular (non-special) token from the input
 stream.  If this is the last token from the input stream, or if the
 token manager has not read tokens beyond this one, this field is
 set to null.  This is true only if this token is also a regular
 token.  Otherwise, see below for a description of the contents of
 this field.

***
<a name="specialToken"></a>
# specialToken

This field is used to access special tokens that occur prior to this
 token, but after the immediately preceding regular (non-special) token.
 If there are no such special tokens, this field is set to null.
 When there are more than one such special token, this field refers
 to the last of these special tokens, which in turn refers to the next
 previous special token through its specialToken field, and so on
 until the first special token (whose specialToken field is null).
 The next fields of special tokens refer to other special tokens that
 immediately follow it (without an intervening regular token).  If there
 is no such token, this field is null.

***
<a name="getValue"></a>
# getValue
getValue(  ) &rarr; Object

An optional attribute value of the Token.
 Tokens which are not used as syntactic sugar will often contain
 meaningful values that will be used later on by the compiler or
 interpreter. This attribute value is often different from the image.
 Any subclass of Token that actually wants to return a non-null value can
 override this method as appropriate.

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=getValue&unscoped_q=getValue">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="newToken"></a>
# newToken
newToken( int ofKind, String image ) &rarr; Token

Returns a new Token object, by default. However, if you want, you
 can create and return subclass objects based on the value of ofKind.
 Simply add the cases to the switch for all those special cases.
 For example, if you have a subclass of Token called IDToken that
 you want to create if ofKind is ID, simply add something like :

    case MyParserConstants.ID : return new IDToken(ofKind, image);

 to the following switch statement. Then you can cast matchedToken
 variable to the appropriate type and use sit in your lexical actions.

### Parameters:
ofKind - an int
<br>image - a String

### Returns:
org.das2.qds.util.dd.Token


<a href="https://github.com/autoplot/dev/search?q=newToken&unscoped_q=newToken">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

newToken( int ofKind ) &rarr; Token<br>
***
<a name="toString"></a>
# toString
toString(  ) &rarr; String

Returns the image.

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

