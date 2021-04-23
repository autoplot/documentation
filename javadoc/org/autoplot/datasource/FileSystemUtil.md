# org.autoplot.datasource.FileSystemUtil

More abstract filesystem functions.

# FileSystemUtil( )


***
<a name="copyFile"></a>
# copyFile
copyFile( java.io.File partFile, java.io.File targetFile ) &rarr; boolean

copy the file to a new name.

### Parameters:
partFile - a File
<br>targetFile - a File

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=copyFile&unscoped_q=copyFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="deleteFilesInTree"></a>
# deleteFilesInTree
deleteFilesInTree( java.io.File root, org.autoplot.datasource.FileSystemUtil.Check shouldDelete ) &rarr; boolean

deletes all files where shouldDelete returns true and empty 
 folders below root, and root.  If a directory is left empty, then it is also deleted.

### Parameters:
root - the root of the tree to start searching.  If root does not exist, return true!
<br>shouldDelete - an object which returns true if the file should be deleted, or if null is used, then any file is deleted.

### Returns:
true if the operation was successful.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/util/filesystem/FileSystemUtil.md#deleteAllFiles'>org.das2.util.filesystem.FileSystemUtil#deleteAllFiles(java.io.File, java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=deleteFilesInTree&unscoped_q=deleteFilesInTree">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="doDownload"></a>
# <del>doDownload</del>
Deprecated: use DataSetURI.getFile instead
***
<a name="getNameRelativeTo"></a>
# getNameRelativeTo
getNameRelativeTo( org.das2.util.filesystem.FileSystem fs, String resource ) &rarr; String



### Parameters:
fs - a FileSystem
<br>resource - a String

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getNameRelativeTo&unscoped_q=getNameRelativeTo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPresentWorkingDirectory"></a>
# getPresentWorkingDirectory
getPresentWorkingDirectory(  ) &rarr; File

get the current working directory (pwd)

### Returns:
the current working directory.

<a href="https://github.com/autoplot/dev/search?q=getPresentWorkingDirectory&unscoped_q=getPresentWorkingDirectory">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasParent"></a>
# hasParent
hasParent( java.net.URL url ) &rarr; boolean

return true if the file has a parent which is resolvable.

### Parameters:
url - an URL

### Returns:
<pre>
 {@code
 from org.autoplot.datasource import FileSystemUtil
 print FileSystemUtil.hasParent(URL('http://autoplot.org/data/2016/ace_mag_2016_001.cdf'))  # True
 print FileSystemUtil.hasParent(URL('http://autoplot.org/Image:tabs.png'))  # False
 }
 </pre>

<a href="https://github.com/autoplot/dev/search?q=hasParent&unscoped_q=hasParent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isChildOf"></a>
# isChildOf
isChildOf( java.io.File possibleParent, java.io.File maybeChild ) &rarr; boolean

return true if the possibleParent is a valid folder tree root, and maybeChild exists within tree.

### Parameters:
possibleParent - parent file.
<br>maybeChild - a file or folder which may exist within possibleParent.

### Returns:
true if possibleParent is a folder containing

<a href="https://github.com/autoplot/dev/search?q=isChildOf&unscoped_q=isChildOf">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isLocalResource"></a>
# isLocalResource
isLocalResource( String file ) &rarr; boolean

return true if the resource is local, and can therefore be trusted.  
 This was introduced to secure the server, where an Autoplot there could be 
 used to access local resources.  This returns true for file:/ references.
 Note this will also return true for sftp since the reference 
 may utilize keys private to the server.  Note too that a .jyds script
 that is not local could attempt to use local resources.  For this reason
 there is JythonDataSourceFactory.hasLocalReferences.
 
 "upload" is another magic element.  Paths containing "upload" are considered 
 remote.  This is to allow areas where content is uploaded.

### Parameters:
file - an Autoplot URI.

### Returns:
true if the uri is a reference to a local resource.

<a href="https://github.com/autoplot/dev/search?q=isLocalResource&unscoped_q=isLocalResource">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resourceExists"></a>
# resourceExists
resourceExists( String suri ) &rarr; boolean

checks to see if the resource uri appears to represent an existing
 data source.  false indicates that the resource is known to not exist.
 true indicates that the resource does exist.

### Parameters:
suri - URI, such as http://server.org/data/asciitable.dat

### Returns:
true of the resource exists and can be downloaded.

<a href="https://github.com/autoplot/dev/search?q=resourceExists&unscoped_q=resourceExists">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resourceIsLocal"></a>
# resourceIsLocal
resourceIsLocal( String suri ) &rarr; boolean

returns true if the resource is already in a local cache.

### Parameters:
suri - the URI containing a file resource.

### Returns:
true if the resource is already in a local cache.

<a href="https://github.com/autoplot/dev/search?q=resourceIsLocal&unscoped_q=resourceIsLocal">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

