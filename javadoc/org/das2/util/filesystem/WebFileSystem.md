# org.das2.util.filesystem.WebFileSystemBase class for HTTP and FTP-based filesystems.  A local cache is kept of
 the files.
***
<a name="LISTING_TIMEOUT_MS"></a>
# LISTING_TIMEOUT_MS

we keep a cached listing in on disk.  This is backed by the website.

***
<a name="MEMORY_LISTING_TIMEOUT_MS"></a>
# MEMORY_LISTING_TIMEOUT_MS

we keep a cached listing in memory for performance.  This is backed by the .listing file.

***
<a name="HTTP_CHECK_TIMESTAMP_LIMIT_MS"></a>
# HTTP_CHECK_TIMESTAMP_LIMIT_MS

timestamp checks will occur no more often than this.

***
<a name="PROP_OFFLINE"></a>
# PROP_OFFLINE

if true, then the remote filesystem is not accessible, but local cache
 copies may be accessed.  See FileSystemSettings.allowOffline

***
<a name="PROP_READ_ONLY_CACHE"></a>
# PROP_READ_ONLY_CACHE

alternate location to check for file before downloading.

***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="cacheListing"></a>
# cacheListing
cacheListing( String directory, org.das2.util.filesystem.FileSystem.DirectoryEntry[] listing ) &rarr; void



### Parameters:
directory - a String
<br>listing - an org.das2.util.filesystem.FileSystem.DirectoryEntry[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=cacheListing&unscoped_q=cacheListing">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="consumeStream"></a>
# <del>consumeStream</del>
Deprecated: see HtmlUtil.consumeStream.
***
<a name="getDownloadDirectory"></a>
# getDownloadDirectory
getDownloadDirectory(  ) &rarr; File



### Returns:
java.io.File


<a href="https://github.com/autoplot/dev/search?q=getDownloadDirectory&unscoped_q=getDownloadDirectory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFileObject"></a>
# getFileObject
getFileObject( String filename ) &rarr; FileObject

Return the handle for this file.  This is not the file itself, and 
 accessing this object does not necessarily download the resource.  This will be a 
 container for file metadata, in addition to providing access to the data
 file itself.

### Parameters:
filename - the name of the file within the filesystem.

### Returns:
a FileObject for the file

<a href="https://github.com/autoplot/dev/search?q=getFileObject&unscoped_q=getFileObject">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLocalName"></a>
# getLocalName
getLocalName( java.io.File file ) &rarr; String

return the name of the File within the FileSystem, where File is a local
 file within the local copy of the filesystem.

### Parameters:
file - a File

### Returns:
the name within the filesystem

<a href="https://github.com/autoplot/dev/search?q=getLocalName&unscoped_q=getLocalName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getLocalName( java.net.URL url ) &rarr; String<br>
***
<a name="getLocalRoot"></a>
# getLocalRoot
getLocalRoot(  ) &rarr; File



### Returns:
java.io.File


<a href="https://github.com/autoplot/dev/search?q=getLocalRoot&unscoped_q=getLocalRoot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLocalRootAbsPath"></a>
# <del>getLocalRootAbsPath</del>
Deprecated: use getLocalRoot().getAbsolutePath()
***
<a name="getOfflineMessage"></a>
# getOfflineMessage
getOfflineMessage(  ) &rarr; String

return the reason (if any provided) why the filesystem is offline,

### Returns:
the message for the response code

<a href="https://github.com/autoplot/dev/search?q=getOfflineMessage&unscoped_q=getOfflineMessage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getOfflineResponseCode"></a>
# getOfflineResponseCode
getOfflineResponseCode(  ) &rarr; int

if non-zero, the response code (e.g. 403) why the filesystem is offline.

### Returns:
the response code.

<a href="https://github.com/autoplot/dev/search?q=getOfflineResponseCode&unscoped_q=getOfflineResponseCode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPartFile"></a>
# getPartFile
getPartFile( java.io.File localFile ) &rarr; File

return a name where the download is to be staged.  This will
 be unique for any process.  We make the following assumptions:
 <ul>
 <li> multiple Java processes will be using and modifying the file database.
 <li> java processes may be on different machines
 <li> an ID conflict may occur should two processes have the same UID, hostname, and are started at the same clock time millisecond.
 </ul>
 See https://sourceforge.net/p/autoplot/bugs/1301/

### Parameters:
localFile - a File

### Returns:
the temporary filename to use.

<a href="https://github.com/autoplot/dev/search?q=getPartFile&unscoped_q=getPartFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getProtocol"></a>
# getProtocol
getProtocol(  ) &rarr; WebProtocol

return the protocol object, which allows access to the metadata.  This
 may go away, so do not depend on this for production code.

### Returns:
the protocol object.

<a href="https://github.com/autoplot/dev/search?q=getProtocol&unscoped_q=getProtocol">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getReadOnlyCache"></a>
# getReadOnlyCache
getReadOnlyCache(  ) &rarr; File



### Returns:
java.io.File


<a href="https://github.com/autoplot/dev/search?q=getReadOnlyCache&unscoped_q=getReadOnlyCache">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRootURL"></a>
# getRootURL
getRootURL(  ) &rarr; URL

return the root of the filesystem as a URL.
 Since the root is stored as a URI and "ftp://jbf@mysite.com:@ftpproxy.net/temp/" is a legal address, check for this case.

### Returns:
the root of the filesystem as a URL.

<a href="https://github.com/autoplot/dev/search?q=getRootURL&unscoped_q=getRootURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getURI"></a>
# getURI
getURI( String filename ) &rarr; URI

return the URI for the internal filename

### Parameters:
filename - internal filename

### Returns:
a java.net.URI


<a href="https://github.com/autoplot/dev/search?q=getURI&unscoped_q=getURI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getURL"></a>
# getURL
getURL( String filename ) &rarr; URL

return the URL for the internal filename

### Parameters:
filename - internal filename

### Returns:
a java.net.URL


<a href="https://github.com/autoplot/dev/search?q=getURL&unscoped_q=getURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isAppletMode"></a>
# isAppletMode
isAppletMode(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isAppletMode&unscoped_q=isAppletMode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDirectory"></a>
# isDirectory
isDirectory( String filename ) &rarr; boolean

return true if the name refers to a directory, not a file.

### Parameters:
filename - a String

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isDirectory&unscoped_q=isDirectory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isListingCached"></a>
# isListingCached
isListingCached( String directory ) &rarr; boolean

return true if the listing file (.listing) is available in the 
 file system cache, and is still fresh.  LISTING_TIMEOUT_MS controls
 the freshness, where files older than LISTING_TIMEOUT_MS milliseconds
 will not be used.  Note the timestamp on the file comes from the server
 providing the listing, so the age may be negative when clocks are not
 synchronized.

### Parameters:
directory - a String

### Returns:
true if the listing is cached.

<a href="https://github.com/autoplot/dev/search?q=isListingCached&unscoped_q=isListingCached">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isOffline"></a>
# isOffline
isOffline(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isOffline&unscoped_q=isOffline">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="listDirectory"></a>
# listDirectory
listDirectory( String directory ) &rarr; String

return the directory listing for the name.

### Parameters:
directory - a String

### Returns:
a java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=listDirectory&unscoped_q=listDirectory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

listDirectory( String directory, String regex ) &rarr; String<br>
***
<a name="localRoot"></a>
# localRoot
localRoot( java.net.URI root ) &rarr; File

return the local root for the URI.

### Parameters:
root - the URI such as http://das2.org/data/

### Returns:
/home/jbf/autoplot_data/fscache/http/das2.org/data/

<a href="https://github.com/autoplot/dev/search?q=localRoot&unscoped_q=localRoot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="maybeUpdateDirectoryEntry"></a>
# maybeUpdateDirectoryEntry
maybeUpdateDirectoryEntry( String filename, boolean force ) &rarr; DirectoryEntry

trigger an update of the in-memory listing, or check to see if it is in memory.

### Parameters:
filename - the particular file for which we need a listing.
<br>force - if true, then list if it isn't available.

### Returns:
null if the listing is not available, or if the element is not in the folder, the DirectoryEntry otherwise.

<a href="https://github.com/autoplot/dev/search?q=maybeUpdateDirectoryEntry&unscoped_q=maybeUpdateDirectoryEntry">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resetListCache"></a>
# resetListCache
resetListCache( String directory ) &rarr; void

From FTPBeanFileSystem.

### Parameters:
directory - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resetListCache&unscoped_q=resetListCache">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resetListingCache"></a>
# resetListingCache
resetListingCache(  ) &rarr; void

reset the .listing files and the ram-memory caches.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resetListingCache&unscoped_q=resetListingCache">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAppletMode"></a>
# setAppletMode
setAppletMode( boolean applet ) &rarr; void



### Parameters:
applet - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAppletMode&unscoped_q=setAppletMode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setOffline"></a>
# setOffline
setOffline( boolean offline ) &rarr; void



### Parameters:
offline - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setOffline&unscoped_q=setOffline">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setReadOnlyCache"></a>
# setReadOnlyCache
setReadOnlyCache( java.io.File f ) &rarr; void



### Parameters:
f - a File

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setReadOnlyCache&unscoped_q=setReadOnlyCache">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

