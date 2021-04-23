# org.das2.jythoncompletion.nbadapt.CharSequenceUtilities

Utility methods related to character sequences.

***
<a name="append"></a>
# append
append( java.lang.StringBuffer sb, java.lang.CharSequence text ) &rarr; void

Append character sequence to the given string buffer.
 <br/>
 This method is no longer needed in JDK 1.5 where the implementation
 does not create an extra java.lang.String instance.

### Parameters:
sb - a StringBuffer
<br>text - a CharSequence

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=append&unscoped_q=append">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

append( java.lang.StringBuffer sb, java.lang.CharSequence text, int start, int end ) &rarr; void<br>
***
<a name="checkIndexNonNegative"></a>
# checkIndexNonNegative
checkIndexNonNegative( int index ) &rarr; void

Ensure that the given index is &gt;=0 and lower than the given length.

### Parameters:
index - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=checkIndexNonNegative&unscoped_q=checkIndexNonNegative">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="checkIndexValid"></a>
# checkIndexValid
checkIndexValid( int index, int length ) &rarr; void

Ensure that the given index is &gt;=0 and lower than the given length.

### Parameters:
index - an int
<br>length - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=checkIndexValid&unscoped_q=checkIndexValid">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="checkIndexesValid"></a>
# checkIndexesValid
checkIndexesValid( java.lang.CharSequence text, int start, int end ) &rarr; void

Ensure that the given start and end parameters are valid indices
 of the given text.

### Parameters:
text - a CharSequence
<br>start - an int
<br>end - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=checkIndexesValid&unscoped_q=checkIndexesValid">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="debugChar"></a>
# debugChar
debugChar( java.lang.StringBuffer sb, char ch ) &rarr; void

Append the character description to the given string buffer
 translating the special characters (and '\') into escape sequences.

### Parameters:
sb - non-null string buffer to append to.
<br>ch - character to be debugged.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=debugChar&unscoped_q=debugChar">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

debugChar( java.lang.StringBuilder sb, char ch ) &rarr; void<br>
debugChar( char ch ) &rarr; String<br>
***
<a name="debugText"></a>
# debugText
debugText( java.lang.StringBuffer sb, java.lang.CharSequence text ) &rarr; void

Append the text description to the given string buffer
 translating the special characters (and '\') into escape sequences.

### Parameters:
sb - non-null string buffer to append to.
<br>text - non-null text to be debugged.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=debugText&unscoped_q=debugText">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

debugText( java.lang.StringBuilder sb, java.lang.CharSequence text ) &rarr; void<br>
debugText( java.lang.CharSequence text ) &rarr; String<br>
***
<a name="endsWith"></a>
# endsWith
endsWith( java.lang.CharSequence text, java.lang.CharSequence suffix ) &rarr; boolean

Implementation of {@link String#endsWith(String)} for character sequences.

### Parameters:
text - a CharSequence
<br>suffix - a CharSequence

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=endsWith&unscoped_q=endsWith">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="equals"></a>
# equals
equals( java.lang.CharSequence text, Object o ) &rarr; boolean

Compare character sequence to another object.
 The match is successful if the second object is a character sequence as well
 and both character sequences contain the same characters (or if both objects are null).

### Parameters:
text - character sequence being compared to the given object.
  It may be <code>null</code>.
<br>o - object to be compared to the character sequence.
  It may be <code>null</code>.

### Returns:
true if both parameters are null or both are non-null
  and they contain the same text.

<a href="https://github.com/autoplot/dev/search?q=equals&unscoped_q=equals">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="indexOf"></a>
# indexOf
indexOf( java.lang.CharSequence text, int ch ) &rarr; int

Implementation of {@link String#indexOf(int)} for character sequences.

### Parameters:
text - a CharSequence
<br>ch - an int

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=indexOf&unscoped_q=indexOf">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

indexOf( java.lang.CharSequence text, int ch, int fromIndex ) &rarr; int<br>
indexOf( java.lang.CharSequence text, java.lang.CharSequence seq ) &rarr; int<br>
indexOf( java.lang.CharSequence text, java.lang.CharSequence seq, int fromIndex ) &rarr; int<br>
***
<a name="lastIndexOf"></a>
# lastIndexOf
lastIndexOf( java.lang.CharSequence text, java.lang.CharSequence seq ) &rarr; int

Implementation of {@link String#lastIndexOf(String)} for character sequences.

### Parameters:
text - a CharSequence
<br>seq - a CharSequence

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=lastIndexOf&unscoped_q=lastIndexOf">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

lastIndexOf( java.lang.CharSequence text, java.lang.CharSequence seq, int fromIndex ) &rarr; int<br>
lastIndexOf( java.lang.CharSequence text, int ch ) &rarr; int<br>
lastIndexOf( java.lang.CharSequence text, int ch, int fromIndex ) &rarr; int<br>
***
<a name="startsWith"></a>
# startsWith
startsWith( java.lang.CharSequence text, java.lang.CharSequence prefix ) &rarr; boolean

Implementation of {@link String#startsWith(String)} for character sequences.

### Parameters:
text - a CharSequence
<br>prefix - a CharSequence

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=startsWith&unscoped_q=startsWith">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="stringLikeHashCode"></a>
# stringLikeHashCode
stringLikeHashCode( java.lang.CharSequence text ) &rarr; int

Compute {@link String}-like hashcode over given {@link CharSequence}.

### Parameters:
text - character sequence for which the hashcode is being computed.

### Returns:
hashcode of the given character sequence.

<a href="https://github.com/autoplot/dev/search?q=stringLikeHashCode&unscoped_q=stringLikeHashCode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="textEquals"></a>
# textEquals
textEquals( java.lang.CharSequence text1, java.lang.CharSequence text2 ) &rarr; boolean

Test whether whether the given character sequences
 represent the same text.
 <br>
 The match is successful if the contained characters
 of the two character sequences are the same.

### Parameters:
text1 - first character sequence being compared.
  It must not be <code>null</code>.
<br>text2 - second character sequence being compared.
  It must not be <code>null</code>.

### Returns:
true if both parameters are equal in String-like manner.

<a href="https://github.com/autoplot/dev/search?q=textEquals&unscoped_q=textEquals">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString( java.lang.CharSequence text ) &rarr; String

Create a string from the given character sequence by first creating
 a <code>StringBuilder</code> and appending the whole character sequence
 to it.
 <br>
 The method does not call <code>toString()</code> on the given character
 sequence.

### Parameters:
text - character sequence for which the <code>String</code> form
  should be created.

### Returns:
string representation of the character sequence.

<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

toString( java.lang.CharSequence text, int start, int end ) &rarr; String<br>
***
<a name="trim"></a>
# trim
trim( java.lang.CharSequence text ) &rarr; CharSequence

Implementation of {@link String#trim()} for character sequences.

### Parameters:
text - a CharSequence

### Returns:
java.lang.CharSequence


<a href="https://github.com/autoplot/dev/search?q=trim&unscoped_q=trim">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

