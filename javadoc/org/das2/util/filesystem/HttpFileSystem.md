# org.das2.util.filesystem.HttpFileSystemMake a web folder accessible.  This assumes listings are provided in html form by requesting links ending in a slash.
 For example, http://autoplot.org/data/pngwalk/.  Links to resources "outside" of the filesystem are not considered part of
 the filesystem.  Again, this assumes listings are HTML content, and I suspect this will be changing (xml+client-side-xslt)...
***
<a name="createHttpFileSystem"></a>
# createHttpFileSystem
createHttpFileSystem( java.net.URI rooturi ) &rarr; HttpFileSystem

Create a filesystem from the URI.  Note "user@" will be added to the 
 URI if credentials are needed and added automatically.

### Parameters:
rooturi - an URI

### Returns:
the filesystem.

<a href="https://github.com/autoplot/dev/search?q=createHttpFileSystem&unscoped_q=createHttpFileSystem">[search for examples]</a>

***
<a name="isDirectory"></a>
# isDirectory
isDirectory( String filename ) &rarr; boolean

dumb method looks for / in parent directory's listing.  Since we have
 to list the parent, then IOException can be thrown.

### Parameters:
filename - a String

### Returns:
true if the name appears to be a directory (folder).

<a href="https://github.com/autoplot/dev/search?q=isDirectory&unscoped_q=isDirectory">[search for examples]</a>

***
<a name="isRegexNoWild"></a>
# isRegexNoWild
isRegexNoWild( String regex ) &rarr; boolean

return true if the regular expression for the file is actually a single
 file with no wildcards.  This is tricky because for years a single period
 (".") has been left in the name, so that "." matches ".", and really 
 screen.png would match screen_png.  To contain this logic, this routine
 is introduced.  Presently it just checks for "screen.png" so that a 
 pngwalk of each screenshot (http://autoplot.org/jnlp/v$x/screen.png) can
 be made, which is useful when looking for old versions.

### Parameters:
regex - a String

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isRegexNoWild&unscoped_q=isRegexNoWild">[search for examples]</a>

***
<a name="listDirectory"></a>
# listDirectory
listDirectory( String directory ) &rarr; String

list the directory, using the cached entry from listDirectoryFromMemory, or
 by HtmlUtil.getDirectoryListing.  If there is a ro_cache, then add extra entries from here as well.
 Note the following extentions are hidden: .css, .php, .jnlp, .part.

### Parameters:
directory - name within the filesystem

### Returns:
names within the directory

<a href="https://github.com/autoplot/dev/search?q=listDirectory&unscoped_q=listDirectory">[search for examples]</a>

listDirectory( String directory, String regex ) &rarr; String<br>
***
<a name="maybeUpdateDirectoryEntry"></a>
# maybeUpdateDirectoryEntry
maybeUpdateDirectoryEntry( String filename, boolean force ) &rarr; DirectoryEntry

HTTP listings are really done by querying the single file, so support this by issuing a head request

### Parameters:
filename - filename within the system
<br>force - if true, then guarantee a listing and throw an IOException if it cannot be done.

### Returns:
the DirectoryEntry showing size and date.

<a href="https://github.com/autoplot/dev/search?q=maybeUpdateDirectoryEntry&unscoped_q=maybeUpdateDirectoryEntry">[search for examples]</a>

