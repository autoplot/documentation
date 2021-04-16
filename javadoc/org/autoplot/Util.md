# org.autoplot.Util
Util( )


***
<a name="logger"></a>
# logger



***
<a name="addFonts"></a>
# addFonts
addFonts(  ) &rarr; void

this will add the Scheme and other named fonts found in the /resources/ folder.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addFonts&unscoped_q=addFonts">[search for examples]</a>

***
<a name="copyFile"></a>
# copyFile
copyFile( java.io.File srcf, java.io.File dstf ) &rarr; boolean

copy a file.  This will probably always returns true or an exception, but check the status to be sure.

### Parameters:
srcf - the source file
<br>dstf - the destination file

### Returns:
true if successful.

<a href="https://github.com/autoplot/dev/search?q=copyFile&unscoped_q=copyFile">[search for examples]</a>

***
<a name="copyFileTree"></a>
# copyFileTree
copyFileTree( java.io.File root, java.io.File dst ) &rarr; boolean

copy a branch of files and folders.

### Parameters:
root - root folder.
<br>dst - destination folder.

### Returns:
true if successful.

<a href="https://github.com/autoplot/dev/search?q=copyFileTree&unscoped_q=copyFileTree">[search for examples]</a>

copyFileTree( java.io.File root, java.io.File dst, ProgressMonitor mon ) &rarr; boolean<br>
copyFileTree( java.io.File root, java.io.File dst, int depth, ProgressMonitor mon ) &rarr; boolean<br>
***
<a name="deleteFileTree"></a>
# deleteFileTree
deleteFileTree( java.io.File root ) &rarr; boolean

deletes all files and folders below root, and root, just as "rm -r" would.
 TODO: check links

### Parameters:
root - the root of the tree.

### Returns:
true if the operation was successful.
### See Also:
<a href='#pruneFileTree'>pruneFileTree(java.io.File, java.util.List)</a> which probably does the same thing.<br>

<a href="https://github.com/autoplot/dev/search?q=deleteFileTree&unscoped_q=deleteFileTree">[search for examples]</a>

***
<a name="getBuildInfos"></a>
# getBuildInfos
getBuildInfos(  ) &rarr; List

searches class path for META-INF/version.txt, returns nice strings

### Returns:
one line per jar

<a href="https://github.com/autoplot/dev/search?q=getBuildInfos&unscoped_q=getBuildInfos">[search for examples]</a>

***
<a name="getBuildTime"></a>
# getBuildTime
getBuildTime(  ) &rarr; String

return the build time an an ISO8601 time, or "????" if it is unknown.
 Note question marks are used intentionally so sloppy codes can assume
 that ???? means the current version of the code built in a debugger.

### Returns:
ISO8601 time or "????"

<a href="https://github.com/autoplot/dev/search?q=getBuildTime&unscoped_q=getBuildTime">[search for examples]</a>

***
<a name="pruneFileTree"></a>
# pruneFileTree
pruneFileTree( java.io.File root, java.util.List problems ) &rarr; boolean

remove empty branches from file tree.  This is like "rm -r $root"

### Parameters:
root - the root directory from which to start a search.
<br>problems - any files which could not be deleted are listed here.

### Returns:
true if successful.
### See Also:
<a href='#deleteFileTree'>deleteFileTree(java.io.File)</a> which probably does the same thing.<br>

<a href="https://github.com/autoplot/dev/search?q=pruneFileTree&unscoped_q=pruneFileTree">[search for examples]</a>

***
<a name="strjoin"></a>
# strjoin
strjoin( java.util.Collection c, String delim ) &rarr; String

this will be replaced in Java 8.

### Parameters:
c - a java.util.Collection
<br>delim - a String

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=strjoin&unscoped_q=strjoin">[search for examples]</a>

