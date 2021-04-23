# org.das2.qds.util.dd.SimpleCharStream

An implementation of interface CharStream, where the stream is assumed to
 contain only ASCII characters (without unicode processing).

# SimpleCharStream( java.io.Reader dstream, int startline, int startcolumn, int buffersize )
Constructor.

# SimpleCharStream( java.io.Reader dstream, int startline, int startcolumn )
Constructor.

# SimpleCharStream( java.io.Reader dstream )
Constructor.

# SimpleCharStream( java.io.InputStream dstream, String encoding, int startline, int startcolumn, int buffersize )
Constructor.

# SimpleCharStream( java.io.InputStream dstream, int startline, int startcolumn, int buffersize )
Constructor.

# SimpleCharStream( java.io.InputStream dstream, String encoding, int startline, int startcolumn )
Constructor.

# SimpleCharStream( java.io.InputStream dstream, int startline, int startcolumn )
Constructor.

# SimpleCharStream( java.io.InputStream dstream, String encoding )
Constructor.

# SimpleCharStream( java.io.InputStream dstream )
Constructor.

***
<a name="staticFlag"></a>
# staticFlag

Whether parser is static.

***
<a name="bufpos"></a>
# bufpos

Position in buffer.

***
<a name="BeginToken"></a>
# BeginToken
BeginToken(  ) &rarr; char

Start.

### Returns:
char


<a href="https://github.com/autoplot/dev/search?q=BeginToken&unscoped_q=BeginToken">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="Done"></a>
# Done
Done(  ) &rarr; void

Reset buffer when finished.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=Done&unscoped_q=Done">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="GetImage"></a>
# GetImage
GetImage(  ) &rarr; String

Get token literal value.

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=GetImage&unscoped_q=GetImage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="GetSuffix"></a>
# GetSuffix
GetSuffix( int len ) &rarr; char

Get the suffix.

### Parameters:
len - an int

### Returns:
char[]


<a href="https://github.com/autoplot/dev/search?q=GetSuffix&unscoped_q=GetSuffix">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="ReInit"></a>
# ReInit
ReInit( java.io.Reader dstream, int startline, int startcolumn, int buffersize ) &rarr; void

Reinitialise.

### Parameters:
dstream - a Reader
<br>startline - an int
<br>startcolumn - an int
<br>buffersize - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=ReInit&unscoped_q=ReInit">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

ReInit( java.io.Reader dstream, int startline, int startcolumn ) &rarr; void<br>
ReInit( java.io.Reader dstream ) &rarr; void<br>
ReInit( java.io.InputStream dstream, String encoding, int startline, int startcolumn, int buffersize ) &rarr; void<br>
ReInit( java.io.InputStream dstream, int startline, int startcolumn, int buffersize ) &rarr; void<br>
ReInit( java.io.InputStream dstream, String encoding ) &rarr; void<br>
ReInit( java.io.InputStream dstream ) &rarr; void<br>
ReInit( java.io.InputStream dstream, String encoding, int startline, int startcolumn ) &rarr; void<br>
ReInit( java.io.InputStream dstream, int startline, int startcolumn ) &rarr; void<br>
***
<a name="adjustBeginLineColumn"></a>
# adjustBeginLineColumn
adjustBeginLineColumn( int newLine, int newCol ) &rarr; void

Method to adjust line and column numbers for the start of a token.

### Parameters:
newLine - an int
<br>newCol - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=adjustBeginLineColumn&unscoped_q=adjustBeginLineColumn">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="backup"></a>
# backup
backup( int amount ) &rarr; void

Backup a number of characters.

### Parameters:
amount - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=backup&unscoped_q=backup">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBeginColumn"></a>
# getBeginColumn
getBeginColumn(  ) &rarr; int

Get token beginning column number.

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getBeginColumn&unscoped_q=getBeginColumn">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBeginLine"></a>
# getBeginLine
getBeginLine(  ) &rarr; int

Get token beginning line number.

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getBeginLine&unscoped_q=getBeginLine">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getColumn"></a>
# getColumn
getColumn(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getColumn&unscoped_q=getColumn">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getEndColumn"></a>
# getEndColumn
getEndColumn(  ) &rarr; int

Get token end column number.

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getEndColumn&unscoped_q=getEndColumn">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getEndLine"></a>
# getEndLine
getEndLine(  ) &rarr; int

Get token end line number.

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getEndLine&unscoped_q=getEndLine">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLine"></a>
# getLine
getLine(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getLine&unscoped_q=getLine">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readChar"></a>
# readChar
readChar(  ) &rarr; char

Read a character.

### Returns:
char


<a href="https://github.com/autoplot/dev/search?q=readChar&unscoped_q=readChar">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

