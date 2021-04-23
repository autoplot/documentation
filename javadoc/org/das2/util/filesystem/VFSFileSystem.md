# org.das2.util.filesystem.VFSFileSystem

FileSystem provides additional abstraction to Apache VFS to implement das2 FileSystems, and provide
 SFTP access.

***
<a name="close"></a>
# close
close(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=close&unscoped_q=close">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createVFSFileSystem"></a>
# createVFSFileSystem
createVFSFileSystem( java.net.URI root ) &rarr; VFSFileSystem



### Parameters:
root - an URI

### Returns:
org.das2.util.filesystem.VFSFileSystem


<a href="https://github.com/autoplot/dev/search?q=createVFSFileSystem&unscoped_q=createVFSFileSystem">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

createVFSFileSystem( java.net.URI root, boolean createFolder ) &rarr; VFSFileSystem<br>
***
<a name="getFileObject"></a>
# getFileObject
getFileObject( String filename ) &rarr; FileObject



### Parameters:
filename - a String

### Returns:
org.das2.util.filesystem.FileObject


<a href="https://github.com/autoplot/dev/search?q=getFileObject&unscoped_q=getFileObject">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLocalRoot"></a>
# getLocalRoot
getLocalRoot(  ) &rarr; File



### Returns:
java.io.File


<a href="https://github.com/autoplot/dev/search?q=getLocalRoot&unscoped_q=getLocalRoot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDirectory"></a>
# isDirectory
isDirectory( String filename ) &rarr; boolean



### Parameters:
filename - a String

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isDirectory&unscoped_q=isDirectory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isLocal"></a>
# isLocal
isLocal(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isLocal&unscoped_q=isLocal">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="listDirectory"></a>
# listDirectory
listDirectory( String directory ) &rarr; String

return a list of files and folders in the directory.
 Conventionally, folders are identified with a trailing slash.

### Parameters:
directory - a String

### Returns:
a java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=listDirectory&unscoped_q=listDirectory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

listDirectory( String directory, String regex ) &rarr; String<br>
