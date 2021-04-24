# org.das2.qds.util.dd.SimpleExpTokenManager

Token Manager.

# SimpleExpTokenManager( org.das2.qds.util.dd.SimpleCharStream stream )
Constructor.

# SimpleExpTokenManager( org.das2.qds.util.dd.SimpleCharStream stream, int lexState )
Constructor.

***
<a name="debugStream"></a>
# debugStream

Debug output.

***
<a name="jjstrLiteralImages"></a>
# jjstrLiteralImages

Token literal values.

***
<a name="lexStateNames"></a>
# lexStateNames

Lexer state names.

***
<a name="ReInit"></a>
# ReInit
ReInit( org.das2.qds.util.dd.SimpleCharStream stream ) &rarr; void

Reinitialise parser.

### Parameters:
stream - a SimpleCharStream

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=ReInit&unscoped_q=ReInit">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

ReInit( org.das2.qds.util.dd.SimpleCharStream stream, int lexState ) &rarr; void<br>
***
<a name="SwitchTo"></a>
# SwitchTo
SwitchTo( int lexState ) &rarr; void

Switch to specified lex state.

### Parameters:
lexState - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=SwitchTo&unscoped_q=SwitchTo">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNextToken"></a>
# getNextToken
getNextToken(  ) &rarr; Token

Get the next Token.

### Returns:
org.das2.qds.util.dd.Token


<a href="https://github.com/autoplot/dev/search?q=getNextToken&unscoped_q=getNextToken">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDebugStream"></a>
# setDebugStream
setDebugStream( java.io.PrintStream ds ) &rarr; void

Set debug output.

### Parameters:
ds - a PrintStream

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDebugStream&unscoped_q=setDebugStream">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

