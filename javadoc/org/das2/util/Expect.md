# org.das2.util.Expect

Provides similar functions as the Unix Expect tool.<br>
 There are two ways to create an Expect object: a constructor that takes an
 {@link InputStream} handle and {@link OutputStream} handle; or spawning a
 process by providing a command String. <br>
 <br>
 The API is loosely based on Perl Expect library:<br>
 <a href="http://search.cpan.org/~rgiersig/Expect-1.15/Expect.pod">
 http://search.cpan.org/~rgiersig/Expect-1.15/Expect.pod</a>
 
 <br>
 If you are not familiar with the Tcl version of Expect, take a look at:<br>
 <a href="http://oreilly.com/catalog/expect/chapter/ch03.html">
 http://oreilly.com/catalog/expect/chapter/ch03.html</a> <br>
 <br>
 Expect uses a thread to convert InputStream to a SelectableChannel; other
 than this, no multi-threading is used.<br>
 A call to expect() will block for at most timeout seconds. Expect is not
 designed to be thread-safe, in other words, do not call methods of the same
 Expect object in different threads.

# Expect( java.io.InputStream input, java.io.OutputStream output )


***
<a name="before"></a>
# before

String before the last match(if there was a match),
  updated after each expect() call

***
<a name="match"></a>
# match

String representing the last match(if there was a match),
  updated after each expect() call

***
<a name="isSuccess"></a>
# isSuccess

Whether the last match was successful,
  updated after each expect() call

***
<a name="RETV_TIMEOUT"></a>
# RETV_TIMEOUT



***
<a name="RETV_EOF"></a>
# RETV_EOF



***
<a name="RETV_IOEXCEPTION"></a>
# RETV_IOEXCEPTION



***
<a name="byteToPrintableString"></a>
# byteToPrintableString
byteToPrintableString( byte b ) &rarr; String



### Parameters:
b - a byte

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=byteToPrintableString&unscoped_q=byteToPrintableString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bytesToPrintableString"></a>
# bytesToPrintableString
bytesToPrintableString( byte[] bytes ) &rarr; String

Static method used for convert byte array to string, each byte is
 converted to an ASCII character, if the byte represents a control
 character, it is replaced by a printable caret notation <a
 href="http://en.wikipedia.org/wiki/ASCII">
 http://en.wikipedia.org/wiki/ASCII </a>, or an escape code if possible.

### Parameters:
bytes - bytes to be printed

### Returns:
String representation of the byte array

<a href="https://github.com/autoplot/dev/search?q=bytesToPrintableString&unscoped_q=bytesToPrintableString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="close"></a>
# close
close(  ) &rarr; void

The OutputStream passed to Expect constructor is closed; the InputStream
 is not closed (there is no need to close the InputStream).<br>
 It is suggested that this method be called after the InputStream has come
 to EOF. For example, when you connect through SSH, send an "exit" command
 first, and then call this method.<br>
 <br>
 
 When this method is called, the thread which write to the sink of the
 pipe will end.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=close&unscoped_q=close">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="expect"></a>
# expect
expect( java.lang.Object[] patterns ) &rarr; int

Convenience method, same as calling {@link #expect(int, Object...)
 expect(default_timeout, patterns)}

### Parameters:
patterns - a java.lang.Object[]

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=expect&unscoped_q=expect">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

expect( int timeout, java.lang.Object[] patterns ) &rarr; int<br>
expect( int timeout, java.util.List list ) &rarr; int<br>
***
<a name="expectEOF"></a>
# expectEOF
expectEOF( int timeout ) &rarr; int

Convenience method, internally it calls {@link #expect(int, List)
 expect(timeout, new ArrayList&lt;Pattern&gt;())}. Given an empty list,
 {@link #expect(int, List)} will not perform any regex matching, therefore
 the only conditions for it to return is EOF or timeout (or IOException).
 If EOF is detected, {@link #isSuccess} and {@link #before} are properly
 set.

### Parameters:
timeout - an int

### Returns:
same as return value of {@link #expect(int, List)}

<a href="https://github.com/autoplot/dev/search?q=expectEOF&unscoped_q=expectEOF">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

expectEOF(  ) &rarr; int<br>
***
<a name="expectEOFOrThrow"></a>
# expectEOFOrThrow
expectEOFOrThrow( int timeout ) &rarr; int

Throws checked exceptions when expectEOF was not successful.

### Parameters:
timeout - timeout in seconds

### Returns:
same as return value of {@link #expect(int, List)}

<a href="https://github.com/autoplot/dev/search?q=expectEOFOrThrow&unscoped_q=expectEOFOrThrow">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

expectEOFOrThrow(  ) &rarr; int<br>
***
<a name="expectOrThrow"></a>
# expectOrThrow
expectOrThrow( int timeout, java.lang.Object[] patterns ) &rarr; int

This method calls {@link #expect(int, Object...) expect(timeout,
 patterns)}, and throws checked exceptions when expect was not successful.
 Useful when you want to simplify error handling: for example, when you
 send a series of commands to an SSH server, you expect a prompt after
 each send, however the server may die or the prompt may take forever to
 appear, you would want to skip the following commands if those occurred.
 In such a case this method will be handy.

### Parameters:
timeout - an int
<br>patterns - a java.lang.Object[]

### Returns:
same as {@link #expect(int, Object...) expect(timeout, patterns)}

<a href="https://github.com/autoplot/dev/search?q=expectOrThrow&unscoped_q=expectOrThrow">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

expectOrThrow( java.lang.Object[] patterns ) &rarr; int<br>
***
<a name="forwardInputStreamTo"></a>
# forwardInputStreamTo
forwardInputStreamTo( java.io.PrintStream duplicatedTo ) &rarr; void

While performing expect operations on the InputStream provided, duplicate
 the contents obtained from InputStream to a PrintStream (you can use
 System.err or System.out). <b>DO NOT</b> call this function while there
 are live Expect objects as this may cause the piping thread to end due to
 unsynchronized code; if you need this feature, add the following to both
 {@link #inputStreamToSelectableChannel(InputStream)} and
 {@link #forwardInputStreamTo(PrintStream)}:
 <pre>
 
 	synchronized(Expect.duplicatedTo) {...
 }
 </pre>

### Parameters:
duplicatedTo - call with null if you want to turn off

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=forwardInputStreamTo&unscoped_q=forwardInputStreamTo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDefault_timeout"></a>
# getDefault_timeout
getDefault_timeout(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getDefault_timeout&unscoped_q=getDefault_timeout">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getProcess"></a>
# getProcess
getProcess(  ) &rarr; Process



### Returns:
the spawned process, if this {@link Expect} object is created by
         spawning a process

<a href="https://github.com/autoplot/dev/search?q=getProcess&unscoped_q=getProcess">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isNotransfer"></a>
# isNotransfer
isNotransfer(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isNotransfer&unscoped_q=isNotransfer">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isRestart_timeout_upon_receive"></a>
# isRestart_timeout_upon_receive
isRestart_timeout_upon_receive(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isRestart_timeout_upon_receive&unscoped_q=isRestart_timeout_upon_receive">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="printDebugInfo"></a>
# printDebugInfo
printDebugInfo(  ) &rarr; void

print internal debug information to stderr.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=printDebugInfo&unscoped_q=printDebugInfo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="send"></a>
# send
send( String str ) &rarr; void



### Parameters:
str - Convenience method to send a string to output handle

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=send&unscoped_q=send">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

send( byte[] toWrite ) &rarr; void<br>
***
<a name="setDefault_timeout"></a>
# setDefault_timeout
setDefault_timeout( int default_timeout ) &rarr; void



### Parameters:
default_timeout - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDefault_timeout&unscoped_q=setDefault_timeout">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setNotransfer"></a>
# setNotransfer
setNotransfer( boolean notransfer ) &rarr; void



### Parameters:
notransfer - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setNotransfer&unscoped_q=setNotransfer">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRestart_timeout_upon_receive"></a>
# setRestart_timeout_upon_receive
setRestart_timeout_upon_receive( boolean restart_timeout_upon_receive ) &rarr; void



### Parameters:
restart_timeout_upon_receive - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRestart_timeout_upon_receive&unscoped_q=setRestart_timeout_upon_receive">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="spawn"></a>
# spawn
spawn( String command ) &rarr; Expect

Creates an Expect object by spawning a command.<br>
 To Linux users, perhaps you need to use "bash -i" if you want to spawn
 Bash.<br>
 Note: error stream of the process is redirected to output stream.

### Parameters:
command - a String

### Returns:
Expect object created using the input and output handles from the
         spawned process

<a href="https://github.com/autoplot/dev/search?q=spawn&unscoped_q=spawn">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

