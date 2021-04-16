# org.das2.util.FileUtilstatic utility methods.
 
 introduced Jul 28, 2008.
***
<a name="deleteFileTree"></a>
# deleteFileTree
deleteFileTree( java.io.File root ) &rarr; boolean

deletes all files and folders below root, and root, just as "rm -r" would.
 TODO: check links

### Parameters:
root - the root where we start deleting.

### Returns:
true if the operation was successful.

<a href="https://github.com/autoplot/dev/search?q=deleteFileTree&unscoped_q=deleteFileTree">[search for examples]</a>

deleteFileTree( java.io.File root, java.util.Set exclude ) &rarr; boolean<br>
***
<a name="deleteWithinFileTree"></a>
# deleteWithinFileTree
deleteWithinFileTree( java.io.File root, String name ) &rarr; boolean

deletes all files with the given name, and root, just as "find . -name name -exec rm {} \;" would.
 TODO: check links.  For example deleteWithinFileTree( root, ".listing" )

### Parameters:
root - the root directory of the tree.
<br>name - the file name.

### Returns:
true if the operation was successful.

<a href="https://github.com/autoplot/dev/search?q=deleteWithinFileTree&unscoped_q=deleteWithinFileTree">[search for examples]</a>

***
<a name="fileCompare"></a>
# fileCompare
fileCompare( java.io.File file1, java.io.File file2 ) &rarr; boolean

returns True if the file contents are equal.

### Parameters:
file1 - a File
<br>file2 - a File

### Returns:
true if the two files have identical

<a href="https://github.com/autoplot/dev/search?q=fileCompare&unscoped_q=fileCompare">[search for examples]</a>

***
<a name="fileCopy"></a>
# fileCopy
fileCopy( java.io.File src, java.io.File dst ) &rarr; void

copies the file or folder from src to dst.

### Parameters:
src - the source file or folder.
<br>dst - the location for the new file or folder.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=fileCopy&unscoped_q=fileCopy">[search for examples]</a>

***
<a name="find"></a>
# find
find( java.io.File root, String name ) &rarr; File

find a files with the given name within the given root, just as "find . -name name -print \;" would.
 TODO: check links.  For example, find( "/usr/share/fonts/truetype", "FreeMono.ttf" )

### Parameters:
root - the root to start
<br>name - name to look for.

### Returns:
the File found, or null if it does not exist.

<a href="https://github.com/autoplot/dev/search?q=find&unscoped_q=find">[search for examples]</a>

find( java.io.File root, java.util.regex.Pattern pattern, java.util.List result ) &rarr; int<br>
find( java.io.File[] roots, String name ) &rarr; File<br>
***
<a name="getMagic"></a>
# getMagic
getMagic( java.io.File src ) &rarr; String

return the first four bytes of the file as a string.  Some magic
 numbers we care about:
  <li> '\x89HDF'  HDF (and new NetCDF) files

### Parameters:
src - a File

### Returns:
a four byte string

<a href="https://github.com/autoplot/dev/search?q=getMagic&unscoped_q=getMagic">[search for examples]</a>

***
<a name="isParent"></a>
# isParent
isParent( java.io.File possibleParent, java.io.File maybeChild ) &rarr; boolean

return true of the maybeChild parent is a child of possibleParent.  Note either
 can be null, and this will not throw an exception, but will return false.

### Parameters:
possibleParent - parent file.
<br>maybeChild - a file or folder which may exist within possibleParent.

### Returns:
true if the possibleParent is actually a parent of maybeChild.

<a href="https://github.com/autoplot/dev/search?q=isParent&unscoped_q=isParent">[search for examples]</a>

***
<a name="lineCount"></a>
# lineCount
lineCount( java.io.File f ) &rarr; int

return the number of lines in the text file.  Breaking the file into
 lines is handled by Java's BufferedReader.

### Parameters:
f - the file

### Returns:
the number of lines.
### See Also:
<a href='BufferedReader.md'>BufferedReader</a> <br>

<a href="https://github.com/autoplot/dev/search?q=lineCount&unscoped_q=lineCount">[search for examples]</a>

***
<a name="listRecursively"></a>
# listRecursively
listRecursively( java.io.File root, java.util.regex.Pattern name, java.util.List matches ) &rarr; List

find all files under the root matching the spec.

### Parameters:
root - the root of the search (e.g. /fonts/)
<br>name - the pattern to match
<br>matches - list that will accept the matches, or null if one should be created.

### Returns:
the list.

<a href="https://github.com/autoplot/dev/search?q=listRecursively&unscoped_q=listRecursively">[search for examples]</a>

listRecursively( java.io.File root, String glob ) &rarr; File<br>
***
<a name="readFileToString"></a>
# readFileToString
readFileToString( java.io.File f ) &rarr; String

read all the bytes in the UTF-8 encoded file into a string.

### Parameters:
f - the file, which presumed to be UTF-8 (or ASCII) encoded.

### Returns:
string containing the contents of the file.

<a href="https://github.com/autoplot/dev/search?q=readFileToString&unscoped_q=readFileToString">[search for examples]</a>

***
<a name="writeStringToFile"></a>
# writeStringToFile
writeStringToFile( java.io.File f, String src ) &rarr; void

write all the bytes in the string to a file using UTF-8 encoding.

### Parameters:
f - the file name.
<br>src - the string to write to the file.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeStringToFile&unscoped_q=writeStringToFile">[search for examples]</a>

