# org.das2.util.filesystem.WebFileObject



***
<a name="METADATA_FRESH_TIMEOUT_MS"></a>
# METADATA_FRESH_TIMEOUT_MS



***
<a name="canRead"></a>
# canRead
canRead(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=canRead&unscoped_q=canRead">[search for examples]</a>

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

return a Channel for the resource.  If the resource can be made locally available, a FileChannel is returned.

### Parameters:
monitor - a ProgressMonitor

### Returns:
a java.nio.channels.ReadableByteChannel


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

return the file for the WebFileObject.

### Parameters:
monitor - a ProgressMonitor

### Returns:
a java.io.File


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
<a name="getParent"></a>
# getParent
getParent(  ) &rarr; FileObject



### Returns:
a WebFileObject referencing the parent directory.

<a href="https://github.com/autoplot/dev/search?q=getParent&unscoped_q=getParent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSize"></a>
# getSize
getSize(  ) &rarr; long

return the fileObject size in bytes.  This may contact the server to get the size, and this
 caches the size.

### Returns:
a long


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

returns true is the file is locally available, meaning clients can 
 call getFile() and the readable File reference will be available in
 interactive time.  For FileObjects from HttpFileSystem, a HEAD request
 is made to ensure that the local file is as new as the website one (when offline=false).

### Returns:
true if the file is local and can be used without web access.

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

***
<a name="removeLocalFile"></a>
# removeLocalFile
removeLocalFile(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=removeLocalFile&unscoped_q=removeLocalFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

