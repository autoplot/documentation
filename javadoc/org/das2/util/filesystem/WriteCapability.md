# org.das2.util.filesystem.WriteCapability

The FileObject can be written.

***
<a name="canWrite"></a>
# canWrite
canWrite(  ) &rarr; boolean

Test to see if we can write to this file.  This should not
 create a file, only getOutputStream should do this.  
 TODO: someday we'll want a locking mechanism.

### Returns:
true if the file can be created.

<a href="https://github.com/autoplot/dev/search?q=canWrite&unscoped_q=canWrite">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="delete"></a>
# delete
delete(  ) &rarr; boolean

delete the file

### Returns:
true if the file was deleted.

<a href="https://github.com/autoplot/dev/search?q=delete&unscoped_q=delete">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getOutputStream"></a>
# getOutputStream
getOutputStream(  ) &rarr; OutputStream

Get the output stream.  The client who has requested the stream must close the stream.

### Returns:
a java.io.OutputStream


<a href="https://github.com/autoplot/dev/search?q=getOutputStream&unscoped_q=getOutputStream">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

