# org.das2.util.filesystem.ExpensiveOpCacheThis simply reduces invocations of an expensive operation by
 caching the result for a given number of milliseconds.  This was
 introduced to remove the number of HEAD requests to the server for
 a given file.
ExpensiveOpCache( org.das2.util.filesystem.ExpensiveOpCache.Op op, int limitMs )
Cache the result of op for no more than limitMs milliseconds.

***
<a name="doOp"></a>
# doOp
doOp( String key ) &rarr; Object

Do the operation if it has not been done, or if it has not been
 done recently.

### Parameters:
key - a String

### Returns:
the result of the operation

<a href="https://github.com/autoplot/dev/search?q=doOp&unscoped_q=doOp">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reset"></a>
# reset
reset(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reset&unscoped_q=reset">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

