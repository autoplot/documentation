# org.das2.util.filesystem.FileSystem

Filesystems provide an abstraction layer so that clients can access
 any hierarchy of files in a implementation-independent way.  For example,
 remote filesystems accessible via HTTP are accessible through the same
 interface as a local filesystem.

***
<a name="PROP_CASE_INSENSITIVE"></a>
# PROP_CASE_INSENSITIVE

Boolean.TRUE if the filesystem ignores case, such as Windows local filesystem.

***
<a name="NULL"></a>
# NULL

result from failed listing, etc.

***
<a name="create"></a>
# <del>create</del>
Deprecated: use create( URI root ) instead.
create( String s ) &rarr; FileSystem<br>
create( String s, ProgressMonitor mon ) &rarr; FileSystem<br>
create( java.net.URL root, ProgressMonitor mon ) &rarr; FileSystem<br>
create( java.net.URI root ) &rarr; FileSystem<br>
create( java.net.URI root, ProgressMonitor mon ) &rarr; FileSystem<br>
***
<a name="createFileSystem"></a>
# createFileSystem
createFileSystem( String directory ) &rarr; FileSystem

create a new filesystem that is a part of this filesystem, rooted at
 directory.

### Parameters:
directory - subdirectory within the filesystem.

### Returns:
the new FileSystem

<a href="https://github.com/autoplot/dev/search?q=createFileSystem&unscoped_q=createFileSystem">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getExceptionHandler"></a>
# getExceptionHandler
getExceptionHandler(  ) &rarr; ExceptionHandler

return the exception handler.

### Returns:
the exception handler.

<a href="https://github.com/autoplot/dev/search?q=getExceptionHandler&unscoped_q=getExceptionHandler">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFileObject"></a>
# getFileObject
getFileObject( String filename ) &rarr; FileObject

return the FileObject that corresponds to the name.

### Parameters:
filename - the file name within the filesystem

### Returns:
the FileObject

<a href="https://github.com/autoplot/dev/search?q=getFileObject&unscoped_q=getFileObject">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getListing"></a>
# getListing
getListing( org.das2.util.filesystem.FileSystem.DirectoryEntry[] des ) &rarr; String

part of the refactoring to cache time stamps as well, this convenience method returns the old string.
 This returns des.name, plus '/' if it's a directory.

### Parameters:
des - array of directory entries.

### Returns:
des.name, and

<a href="https://github.com/autoplot/dev/search?q=getListing&unscoped_q=getListing">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getListing( java.util.Map des ) &rarr; String<br>
***
<a name="getLocalRoot"></a>
# getLocalRoot
getLocalRoot(  ) &rarr; File

return the folder that is a local copy of the filesystem. 
 For LocalFilesystem, this is the same as the filesystem.  For remote
 filesystems, this is a folder within their home directory.  
 Note File.getAbsolutePath() returns the string representation of this root.

### Returns:
the folder that is a local copy of the filesystem.

<a href="https://github.com/autoplot/dev/search?q=getLocalRoot&unscoped_q=getLocalRoot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getProperty"></a>
# getProperty
getProperty( String name ) &rarr; Object

return a filesystem property, such as PROP_CASE_INSENSITIVE.

### Parameters:
name - property name, e.g. PROP_CASE_INSENSITIVE

### Returns:
the property value, e.g. Boolean.TRUE

<a href="https://github.com/autoplot/dev/search?q=getProperty&unscoped_q=getProperty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRootURI"></a>
# getRootURI
getRootURI(  ) &rarr; URI

return the URI identifying the root of the filesystem.

### Returns:
a java.net.URI


<a href="https://github.com/autoplot/dev/search?q=getRootURI&unscoped_q=getRootURI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDirectory"></a>
# isDirectory
isDirectory( String filename ) &rarr; boolean

return true if the name is a directory.

### Parameters:
filename - the name

### Returns:
true if the name is a directory.

<a href="https://github.com/autoplot/dev/search?q=isDirectory&unscoped_q=isDirectory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="listDirectory"></a>
# listDirectory
listDirectory( String directory ) &rarr; String

returns a list of the names of the files in a directory.  Names ending
 in "/" are themselves directories, and the "/" is not part of the name.
 This is optional, and a directory may or may not be tagged with the trailing
 slash.

### Parameters:
directory - the directory name within the filesystem.

### Returns:
list of files and folders within the filesystem.

<a href="https://github.com/autoplot/dev/search?q=listDirectory&unscoped_q=listDirectory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

listDirectory( String directory, ProgressMonitor monitor ) &rarr; String<br>
listDirectory( String directory, String regex ) &rarr; String<br>
listDirectory( String directory, String regex, ProgressMonitor monitor ) &rarr; String<br>
***
<a name="listDirectoryDeep"></a>
# listDirectoryDeep
listDirectoryDeep( String directory, String regex ) &rarr; String

do a deep listing of directories, resolving wildcards along the way.  Note this
 can be quite expensive, so be careful when levels are too deep.

### Parameters:
directory - location within the filesystem.
<br>regex - regular expression (.*\.dat) (not a glob like *.dat).

### Returns:
the entire path of each matching name, including the directory within the filesystem.

<a href="https://github.com/autoplot/dev/search?q=listDirectoryDeep&unscoped_q=listDirectoryDeep">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="peek"></a>
# peek
peek( java.net.URI root ) &rarr; FileSystem

allow factories to peek, so they can see if there is a parent that is offline.

### Parameters:
root - the URI

### Returns:
null if not existing, or the filesystem for the URI.

<a href="https://github.com/autoplot/dev/search?q=peek&unscoped_q=peek">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="peekInstances"></a>
# peekInstances
peekInstances(  ) &rarr; FileSystem

return a copy of all cached filesystems

### Returns:
an org.das2.util.filesystem.FileSystem[]


<a href="https://github.com/autoplot/dev/search?q=peekInstances&unscoped_q=peekInstances">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="recreate"></a>
# recreate
recreate( java.net.URI root ) &rarr; FileSystem

creates a FileSystem, removing and recreating it if it was in the cache.

### Parameters:
root - an URI

### Returns:
an org.das2.util.filesystem.FileSystem


<a href="https://github.com/autoplot/dev/search?q=recreate&unscoped_q=recreate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

recreate( java.net.URI root, ProgressMonitor mon ) &rarr; FileSystem<br>
***
<a name="registerFileSystemFactory"></a>
# registerFileSystemFactory
registerFileSystemFactory( String proto, org.das2.util.filesystem.FileSystemFactory factory ) &rarr; void

register a code for handling a filesystem type.  For example, an
 FTP implementation can be registered to handle URIs like "ftp://autoplot.org/"

### Parameters:
proto - protocol identifier, like "ftp" "http" or "sftp"
<br>factory - the factory which will handle the URI.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=registerFileSystemFactory&unscoped_q=registerFileSystemFactory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reset"></a>
# reset
reset(  ) &rarr; void

remove all the cached FileSystem instances.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reset&unscoped_q=reset">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

reset( org.das2.util.filesystem.FileSystem fs ) &rarr; void<br>
***
<a name="setExceptionHandler"></a>
# setExceptionHandler
setExceptionHandler( org.das2.util.ExceptionHandler eh ) &rarr; void

set the exception handler that is called when exceptions occur.

### Parameters:
eh - the exception handler.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setExceptionHandler&unscoped_q=setExceptionHandler">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="settings"></a>
# settings
settings(  ) &rarr; FileSystemSettings

access the file system settings.

### Returns:
the single settings object.

<a href="https://github.com/autoplot/dev/search?q=settings&unscoped_q=settings">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="splitUrl"></a>
# splitUrl
splitUrl( String surl ) &rarr; String

returns a String[5]:<code><pre>
   [0] is proto "http://"
   [1] will be the host
   [2] is proto + path
   [3] is proto + path + file
   [4] is file ext
   [5] is params, not including ?.
 </pre></code>
 The URL must start with one of file:, ftp://, http://, https://, sftp://
 and "c:" is interpreted as "file:///c:..."

### Parameters:
surl - a URL string to parse.

### Returns:
the parsed URL.

<a href="https://github.com/autoplot/dev/search?q=splitUrl&unscoped_q=splitUrl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toCanonicalFilename"></a>
# toCanonicalFilename
toCanonicalFilename( String filename ) &rarr; String

returns the canonical name /a/b/c.dat of a string that
 may contain backslashes and might not have the leading /
 and trailing slashes.  Also, double slashes (//) are
 removed.  Even for Windows files, forward slashes are used.

### Parameters:
filename - name

### Returns:
name with \ converted to /, etc.

<a href="https://github.com/autoplot/dev/search?q=toCanonicalFilename&unscoped_q=toCanonicalFilename">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toCanonicalFolderName"></a>
# toCanonicalFolderName
toCanonicalFolderName( String name ) &rarr; String

returns the canonical name (/a/b/) of a string that
 may contain backslashes and might not have the leading /
 and trailing slashes.  Also, double slashes (//) are
 removed.  Note this is the name of the FileObject
 within the FileSystem.

### Parameters:
name - folder name

### Returns:
name with \ converted to /, etc.

<a href="https://github.com/autoplot/dev/search?q=toCanonicalFolderName&unscoped_q=toCanonicalFolderName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

