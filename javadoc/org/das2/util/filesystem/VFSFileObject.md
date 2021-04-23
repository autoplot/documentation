# org.das2.util.filesystem.VFSFileObject

This class is part of a wrapper for the Apache Commons VFS.

 NOTE: At the moment, many situations where the Commons VFS throws a FileSystemException
 will result in a RuntimeException from this code.  A better way of handling these
 exceptions should probably be found.

***
<a name="canRead"></a>
# canRead
canRead(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=canRead&unscoped_q=canRead">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="canWrite"></a>
# canWrite
canWrite(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=canWrite&unscoped_q=canWrite">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="close"></a>
# close
close(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=close&unscoped_q=close">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createFile"></a>
# createFile
createFile(  ) &rarr; void

Create the file named by this VFSFileObject. Also creates any necessary
 ancestor folders.  Does nothing if file already exists and is a file (not a folder).

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=createFile&unscoped_q=createFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createFolder"></a>
# createFolder
createFolder(  ) &rarr; void

Create a folder named by this VFSFileObject.  This method will also create
 any necessary ancestor folders.  Does nothing if the folder already exists.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=createFolder&unscoped_q=createFolder">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="delete"></a>
# delete
delete(  ) &rarr; void

Deletes the file.  Does nothing if the file doesn't exist or is a non-empty folder.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=delete&unscoped_q=delete">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="exists"></a>
# exists
exists(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=exists&unscoped_q=exists">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getChannel"></a>
# getChannel
getChannel( ProgressMonitor monitor ) &rarr; ReadableByteChannel



### Parameters:
monitor - a ProgressMonitor

### Returns:
java.nio.channels.ReadableByteChannel


<a href="https://github.com/autoplot/dev/search?q=getChannel&unscoped_q=getChannel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getChildren"></a>
# getChildren
getChildren(  ) &rarr; FileObject



### Returns:
org.das2.util.filesystem.FileObject[]


<a href="https://github.com/autoplot/dev/search?q=getChildren&unscoped_q=getChildren">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFile"></a>
# getFile
getFile( ProgressMonitor monitor ) &rarr; File



### Parameters:
monitor - a ProgressMonitor

### Returns:
java.io.File


<a href="https://github.com/autoplot/dev/search?q=getFile&unscoped_q=getFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInputStream"></a>
# getInputStream
getInputStream( ProgressMonitor monitor ) &rarr; InputStream



### Parameters:
monitor - a ProgressMonitor

### Returns:
java.io.InputStream


<a href="https://github.com/autoplot/dev/search?q=getInputStream&unscoped_q=getInputStream">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNameExt"></a>
# getNameExt
getNameExt(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getNameExt&unscoped_q=getNameExt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getOutputStream"></a>
# getOutputStream
getOutputStream( boolean append ) &rarr; OutputStream



### Parameters:
append - a boolean

### Returns:
java.io.OutputStream


<a href="https://github.com/autoplot/dev/search?q=getOutputStream&unscoped_q=getOutputStream">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getParent"></a>
# getParent
getParent(  ) &rarr; FileObject



### Returns:
org.das2.util.filesystem.FileObject


<a href="https://github.com/autoplot/dev/search?q=getParent&unscoped_q=getParent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSize"></a>
# getSize
getSize(  ) &rarr; long



### Returns:
long


<a href="https://github.com/autoplot/dev/search?q=getSize&unscoped_q=getSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isData"></a>
# isData
isData(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isData&unscoped_q=isData">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isFolder"></a>
# isFolder
isFolder(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isFolder&unscoped_q=isFolder">[search for examples]</a>

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
<a name="isReadOnly"></a>
# isReadOnly
isReadOnly(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isReadOnly&unscoped_q=isReadOnly">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isRoot"></a>
# isRoot
isRoot(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isRoot&unscoped_q=isRoot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="lastModified"></a>
# lastModified
lastModified(  ) &rarr; Date



### Returns:
java.util.Date


<a href="https://github.com/autoplot/dev/search?q=lastModified&unscoped_q=lastModified">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

