# org.das2.util.OsUtil

Utility methods for operating system functions.

# OsUtil( )


***
<a name="closeQuietly"></a>
# closeQuietly
closeQuietly( java.io.InputStream input ) &rarr; void

Unconditionally close an <code>Reader</code>.
 <p>
 Equivalent to {@link Reader#close()}, except any exceptions will be ignored.
 This is typically used in finally blocks.
 
 From apache commons. http://grepcode.com/file_/repo1.maven.org/maven2/commons-io/commons-io/1.2/org/apache/commons/io/IOUtils.java/?v=source

### Parameters:
input - the Reader to close, may be null or already closed

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=closeQuietly&unscoped_q=closeQuietly">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="contentEquals"></a>
# contentEquals
contentEquals( java.io.InputStream input1, java.io.InputStream input2 ) &rarr; boolean

Compare the contents of two Streams to determine if they are equal or
 not.
 <p>
 This method buffers the input internally using
 <code>BufferedInputStream</code> if they are not already buffered.

### Parameters:
input1 - the first stream
<br>input2 - the second stream

### Returns:
true if the content of the streams are equal or they both don't
 exist, false otherwise

<a href="https://github.com/autoplot/dev/search?q=contentEquals&unscoped_q=contentEquals">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

contentEquals( java.io.File file1, java.io.File file2 ) &rarr; boolean<br>
***
<a name="getProcessId"></a>
# getProcessId
getProcessId( String fallback ) &rarr; String

return the processID (pid), or the fallback if the pid cannot be found.

### Parameters:
fallback - the string (null is okay) to return when the pid cannot be found.

### Returns:
the process id or the fallback provided by the caller.

<a href="https://github.com/autoplot/dev/search?q=getProcessId&unscoped_q=getProcessId">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

