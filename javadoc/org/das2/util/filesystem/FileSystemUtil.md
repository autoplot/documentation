# org.das2.util.filesystem.FileSystemUtil



# FileSystemUtil( )


***
<a name="copyStream"></a>
# copyStream
copyStream( java.io.InputStream is, java.io.OutputStream out, ProgressMonitor monitor ) &rarr; void

copies data from in to out, sending the number of bytesTransferred to the monitor.
 The input and output are not closed.

### Parameters:
is - the input stream, which will not be closed.
<br>out - the output stream, which will not be closed.
<br>monitor - a monitor, or null.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=copyStream&unscoped_q=copyStream">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createTempFile"></a>
# createTempFile
createTempFile( java.io.File localFile, int timeoutSeconds ) &rarr; File

create a temporary file, based on the name of the localFile.  This will
 be a different name, and may exist already.  The problem with using 
 deleteOnExit, is that Autoplot may be running within a webserver that
 doesn't exit.  Java7 nio2 introduces more methods for cleaning up temporary
 files, but even delete-on-close doesn't work because often a file is opened
 and closed several times.

### Parameters:
localFile - which need not exist.
<br>timeoutSeconds - the minimum number of seconds this file will exist.

### Returns:
a new file that is a different but predictable name.

<a href="https://github.com/autoplot/dev/search?q=createTempFile&unscoped_q=createTempFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="deleteAllFiles"></a>
# deleteAllFiles
deleteAllFiles( java.io.File dir, String regex ) &rarr; void

delete all files under the directory, with names matching the regex.

### Parameters:
dir - the directory
<br>regex - the regular expression, like ".*\.png"

### Returns:
void (returns nothing)

### See Also:
<a href='Glob.md#getRegex'>Glob#getRegex(java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=deleteAllFiles&unscoped_q=deleteAllFiles">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="dumpToFile"></a>
# dumpToFile
dumpToFile( java.io.InputStream in, java.io.File f ) &rarr; void

Dump the contents of the InputStream into a file.  If the inputStream comes
 from a file, then java.nio is used to transfer the data quickly.

### Parameters:
in - an InputStream
<br>f - a File

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dumpToFile&unscoped_q=dumpToFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="fromUri"></a>
# fromUri
fromUri( java.net.URI uri ) &rarr; String

canonical method for converting URI to human-readable string, containing
 spaces and other illegal characters.  Note pluses in the query part
 are interpreted as spaces.
 This was borrowed from Autoplot's URISplit code.

### Parameters:
uri - URI like URI("file:/home/jbf/ct/autoplot/bugs/1830227625/%5BajbTest%5D/")

### Returns:
string representation of a path like file:/home/jbf/ct/autoplot/bugs/1830227625/[ajbTest]/

<a href="https://github.com/autoplot/dev/search?q=fromUri&unscoped_q=fromUri">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFileNameExtensionFilter"></a>
# getFileNameExtensionFilter
getFileNameExtensionFilter( String description, String ext ) &rarr; FileFilter

get simple filter based on extension for use with JFileChooser.

### Parameters:
description - descriptions, like "png image file"
<br>ext - file extension, like ".png"

### Returns:
the FileFilter

<a href="https://github.com/autoplot/dev/search?q=getFileNameExtensionFilter&unscoped_q=getFileNameExtensionFilter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getParentUri"></a>
# getParentUri
getParentUri( java.net.URI ruri ) &rarr; URI

return the parent of the URI, or null if this is not possible.

### Parameters:
ruri - an URI

### Returns:
a java.net.URI


<a href="https://github.com/autoplot/dev/search?q=getParentUri&unscoped_q=getParentUri">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="gunzip"></a>
# gunzip
gunzip( java.io.File fz, java.io.File file ) &rarr; void

un-gzip the file.  This is similar to the unix gunzip command.

### Parameters:
fz - zipped input file
<br>file - unzipped destination file

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=gunzip&unscoped_q=gunzip">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isCacheable"></a>
# isCacheable
isCacheable( java.net.URI ruri ) &rarr; URI

return null if the URI is not cacheable, or the URI of the parent if it is.

 For example,
 <pre>
 
 URI uri= new URL("http://autoplot.org/data/demos2011.xml").toURI();
 URI parentUri= FileSystemUtil.isCacheable( uri );
 if ( parentUri ) {
     FileSystem fd= FileSystem.create(parentUri);
     FileObject fo= fd.getFileObject( ruri.relativize(parentUri).toString() );
     in= fo.getInputStream();
 
 }
 </pre>

### Parameters:
ruri - an URI

### Returns:
the URI of the parent, or null.

<a href="https://github.com/autoplot/dev/search?q=isCacheable&unscoped_q=isCacheable">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="maybeMkdirs"></a>
# maybeMkdirs
maybeMkdirs( java.io.File file ) &rarr; void

create the file folder if it does not exist.  Throw an IOException if it failed.

### Parameters:
file - a File

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=maybeMkdirs&unscoped_q=maybeMkdirs">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toUri"></a>
# toUri
toUri( String s ) &rarr; URI

encode the string as a URI.  The following characters are encoded:
 " " % &lt; &gt; [ ]

### Parameters:
s - string representation of a path like file:/home/jbf/ct/autoplot/bugs/1830227625/[ajbTest]/

### Returns:
URI like URI("file:/home/jbf/ct/autoplot/bugs/1830227625/%5BajbTest%5D/")

<a href="https://github.com/autoplot/dev/search?q=toUri&unscoped_q=toUri">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="unzip"></a>
# <del>unzip</del>
Deprecated: use gunzip instead.
***
<a name="unzipFile"></a>
# unzipFile
unzipFile( java.io.File zipFilePath, java.io.File destDir ) &rarr; void

Extracts a zip file specified by the zipFilePath to a directory specified by
 destDirectory (will be created if does not exists).
 From http://www.codejava.net/java-se/file-io/programmatically-extract-a-zip-file-using-java

### Parameters:
zipFilePath - a File
<br>destDir - a File

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=unzipFile&unscoped_q=unzipFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="uriDecode"></a>
# uriDecode
uriDecode( String s ) &rarr; String

convert "%20" to " ", etc, by using URLDecoder and catching the UnsupportedEncodingException that will never occur.

### Parameters:
s - a String

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=uriDecode&unscoped_q=uriDecode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="uriEncode"></a>
# uriEncode
uriEncode( String surl ) &rarr; String

convert " " to "%20", etc, by looking for and encoding illegal characters.
 We can't just aggressively convert...

### Parameters:
surl - a String

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=uriEncode&unscoped_q=uriEncode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="zip"></a>
# zip
zip( java.io.File fz, java.io.File dir ) &rarr; void

create a zip file of everything with and under the directory.

### Parameters:
fz - the output
<br>dir - the root directory.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=zip&unscoped_q=zip">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

