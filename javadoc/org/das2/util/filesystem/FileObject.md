# org.das2.util.filesystem.FileObject<p>Class for describing and accessing files in file systems.  This 
 is similar to java.io.File, except that it can describe files on remote
 file systems like an ftp site.</p>

 <p>Note: this is modelled after the NetBeans fileSystem FileObject, with the
 thought that we might use it later. </p>
FileObject( )


***
<a name="canRead"></a>
# canRead
canRead(  ) &rarr; boolean

returns true if the file can be read by the client.

### Returns:
true if the file can be read (see getInputStream)

<a href="https://github.com/autoplot/dev/search?q=canRead&unscoped_q=canRead">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="exists"></a>
# exists
exists(  ) &rarr; boolean

returns true if the file exists.  This may have the side effect of 
 downloading the file.

### Returns:
true if the file exists

<a href="https://github.com/autoplot/dev/search?q=exists&unscoped_q=exists">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCapability"></a>
# getCapability
getCapability( java.lang.Class clazz ) &rarr; Object

returns extra capabilities, such as writing to the filesystem.

### Parameters:
clazz - a java.lang.Class

### Returns:
an Object


<a href="https://github.com/autoplot/dev/search?q=getCapability&unscoped_q=getCapability">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getChannel"></a>
# getChannel
getChannel( ProgressMonitor monitor ) &rarr; ReadableByteChannel

opens a Channel, perhaps transferring the file to a local cache first.  monitor
 is used to monitor the download.

### Parameters:
monitor - for monitoring the download.  The monitor won't be used when the access
   is immediate, for example with local FileObjects.

### Returns:
a java.nio.channels.Channel for fast IO reads.

<a href="https://github.com/autoplot/dev/search?q=getChannel&unscoped_q=getChannel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getChannel(  ) &rarr; ReadableByteChannel<br>
***
<a name="getChildren"></a>
# getChildren
getChildren(  ) &rarr; FileObject

returns objects within a folder.

### Returns:
an array of all FileObjects with the folder.

<a href="https://github.com/autoplot/dev/search?q=getChildren&unscoped_q=getChildren">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFile"></a>
# getFile
getFile( ProgressMonitor monitor ) &rarr; File

gets a File object that can be opened by the client.  This may download a remote file, so
 a progress monitor can be used to monitor the download.

### Parameters:
monitor - for monitoring the download.  The monitor won't be used when the access
   is immediate, for example with local FileObjects.

### Returns:
a reference to a File that can be opened.

<a href="https://github.com/autoplot/dev/search?q=getFile&unscoped_q=getFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getFile(  ) &rarr; File<br>
***
<a name="getInputStream"></a>
# getInputStream
getInputStream( ProgressMonitor monitor ) &rarr; InputStream

opens an inputStream, perhaps transferring the file to a
  cache first.

### Parameters:
monitor - for monitoring the download.  The monitor won't be used when the access
   is immediate, for example with local FileObjects.

### Returns:
an InputStream

<a href="https://github.com/autoplot/dev/search?q=getInputStream&unscoped_q=getInputStream">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getInputStream(  ) &rarr; InputStream<br>
***
<a name="getNameExt"></a>
# getNameExt
getNameExt(  ) &rarr; String

returns the canonical name of the file within the filesystem.  For example,
 in the local filesystem /mnt/data/steven/, /mnt/data/steven/jan/01.dat
 would be /jan/01.dat.

 For example, /a/b/c.dat.

### Returns:
the name of the file within the FileSystem.

<a href="https://github.com/autoplot/dev/search?q=getNameExt&unscoped_q=getNameExt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getParent"></a>
# getParent
getParent(  ) &rarr; FileObject

returns the parent FileObject (a folder).
 If the fileObject is root, then null should be returned.

### Returns:
the parent folder of this object.

<a href="https://github.com/autoplot/dev/search?q=getParent&unscoped_q=getParent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSize"></a>
# getSize
getSize(  ) &rarr; long

returns the size of the file.

### Returns:
the size in bytes of the file, and -1 if the size is unknown.

<a href="https://github.com/autoplot/dev/search?q=getSize&unscoped_q=getSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isData"></a>
# isData
isData(  ) &rarr; boolean

returns true if the file is a data file that to be used
  reading or writing data. (And not a folder.)

### Returns:
true if the file is a data file

<a href="https://github.com/autoplot/dev/search?q=isData&unscoped_q=isData">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isFolder"></a>
# isFolder
isFolder(  ) &rarr; boolean

indicates the type of FileObject

### Returns:
true if the object is a folder (directory).

<a href="https://github.com/autoplot/dev/search?q=isFolder&unscoped_q=isFolder">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isLocal"></a>
# isLocal
isLocal(  ) &rarr; boolean

returns true if the file is locally available, meaning clients can 
 call getFile() and the readable File reference will be available in
 interactive time.  Note that isLocal does not imply exists().  Also,
 This may result in side effects such as a website hit.

### Returns:
true if the file is locally available and fresh

<a href="https://github.com/autoplot/dev/search?q=isLocal&unscoped_q=isLocal">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isReadOnly"></a>
# isReadOnly
isReadOnly(  ) &rarr; boolean

true is the file is read-only.

### Returns:
true if the file is read-only

<a href="https://github.com/autoplot/dev/search?q=isReadOnly&unscoped_q=isReadOnly">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isRoot"></a>
# isRoot
isRoot(  ) &rarr; boolean

returns true if this is the root of the filesystem it came from.

### Returns:
true if this is the root of the filesystem it came from.

<a href="https://github.com/autoplot/dev/search?q=isRoot&unscoped_q=isRoot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="lastModified"></a>
# lastModified
lastModified(  ) &rarr; Date

returns the Date when the file was last modified.  or new Date(0L) if the date is
 not available.

### Returns:
the last modified Date, or new Date(0) if it is not available.

<a href="https://github.com/autoplot/dev/search?q=lastModified&unscoped_q=lastModified">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeLocalFile"></a>
# removeLocalFile
removeLocalFile(  ) &rarr; boolean

remove the local file in the cache, if any.  This can/will be overriden by other 
 filesystems.

### Returns:
true if the action was handled.  (Local files are not deleted.)

<a href="https://github.com/autoplot/dev/search?q=removeLocalFile&unscoped_q=removeLocalFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

