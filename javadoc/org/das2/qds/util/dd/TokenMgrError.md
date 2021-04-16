# org.das2.qds.util.dd.TokenMgrErrorToken Manager Error.
TokenMgrError( )
No arg constructor.

TokenMgrError( String message, int reason )
Constructor with message and reason.

TokenMgrError( boolean EOFSeen, int lexState, int errorLine, int errorColumn, String errorAfter, char curChar, int reason )
Full Constructor.

***
<a name="getMessage"></a>
# getMessage
getMessage(  ) &rarr; String

You can also modify the body of this method to customize your error messages.
 For example, cases like LOOP_DETECTED and INVALID_LEXICAL_STATE are not
 of end-users concern, so you can return something like :

     "Internal Error : Please file a bug report .... "

 from this method for such cases in the release version of your parser.

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getMessage&unscoped_q=getMessage">[search for examples]</a>

