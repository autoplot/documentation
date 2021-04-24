# org.das2.util.filesystem.FileSystemSettings.Persistence



***
<a name="NONE"></a>
# NONE

No persistence.  No files are cached locally.

***
<a name="SESSION"></a>
# SESSION

Within a session, files are cached locally.  This is the default.

***
<a name="EXPIRES"></a>
# EXPIRES

Files persist until a new version is available on the remote cache.

***
<a name="ALWAYS"></a>
# ALWAYS

Files persist indefinitely, and the server is only contacted when a file
 is not available locally.

***
<a name="valueOf"></a>
# valueOf
valueOf( String name ) &rarr; Persistence



### Parameters:
name - a String

### Returns:
org.das2.util.filesystem.FileSystemSettings.Persistence


<a href="https://github.com/autoplot/dev/search?q=valueOf&unscoped_q=valueOf">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="values"></a>
# values
values(  ) &rarr; Persistence



### Returns:
org.das2.util.filesystem.FileSystemSettings.Persistence[]


<a href="https://github.com/autoplot/dev/search?q=values&unscoped_q=values">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

