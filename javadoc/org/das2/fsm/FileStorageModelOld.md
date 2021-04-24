# org.das2.fsm.FileStorageModelOld

Represents a method for storing data sets in a set of files by time.  The
 client provides a regex for the files and how each group of the regex is
 interpreted as a time digit.  The model can then be used to provide the set
 of files that cover a time range, etc.

# FileStorageModelOld( org.das2.fsm.FileStorageModelOld parent, org.das2.util.filesystem.FileSystem root, String regex, org.das2.fsm.FileStorageModelOld.FieldHandler[] handlers )


***
<a name="StartYear4"></a>
# StartYear4



***
<a name="StartYear2"></a>
# StartYear2



***
<a name="StartMonth"></a>
# StartMonth



***
<a name="StartMonthName"></a>
# StartMonthName



***
<a name="StartDay"></a>
# StartDay



***
<a name="StartDoy"></a>
# StartDoy



***
<a name="StartHour"></a>
# StartHour



***
<a name="StartMinute"></a>
# StartMinute



***
<a name="StartSecond"></a>
# StartSecond



***
<a name="EndYear4"></a>
# EndYear4



***
<a name="EndYear2"></a>
# EndYear2



***
<a name="EndMonth"></a>
# EndMonth



***
<a name="EndMonthName"></a>
# EndMonthName



***
<a name="EndDay"></a>
# EndDay



***
<a name="EndDoy"></a>
# EndDoy



***
<a name="EndHour"></a>
# EndHour



***
<a name="EndMinute"></a>
# EndMinute



***
<a name="EndSecond"></a>
# EndSecond



***
<a name="Ignore"></a>
# Ignore



***
<a name="calculateNameFor"></a>
# calculateNameFor
calculateNameFor( Datum start ) &rarr; String

return the name that this time will fall into.

### Parameters:
start - a Datum

### Returns:
the internal name of the file.

<a href="https://github.com/autoplot/dev/search?q=calculateNameFor&unscoped_q=calculateNameFor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="containsFile"></a>
# containsFile
containsFile( java.io.File file ) &rarr; boolean

returns true if the file came (or could come) from this FileStorageModel.

### Parameters:
file - a File

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=containsFile&unscoped_q=containsFile">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="create"></a>
# create
create( org.das2.util.filesystem.FileSystem root, String regex, int[] digitList ) &rarr; FileStorageModelOld



### Parameters:
root - a FileSystem
<br>regex - a String
<br>digitList - an int[]

### Returns:
org.das2.fsm.FileStorageModelOld


<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

create( org.das2.util.filesystem.FileSystem root, String template ) &rarr; FileStorageModelOld<br>
***
<a name="getFileFor"></a>
# getFileFor
getFileFor( String name, ProgressMonitor monitor ) &rarr; File

retrieve the file for the name.

### Parameters:
name - a String
<br>monitor - a ProgressMonitor

### Returns:
java.io.File


<a href="https://github.com/autoplot/dev/search?q=getFileFor&unscoped_q=getFileFor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFileSystem"></a>
# getFileSystem
getFileSystem(  ) &rarr; FileSystem



### Returns:
org.das2.util.filesystem.FileSystem


<a href="https://github.com/autoplot/dev/search?q=getFileSystem&unscoped_q=getFileSystem">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFilenameFor"></a>
# getFilenameFor
getFilenameFor( Datum start, Datum end ) &rarr; String



### Parameters:
start - a Datum
<br>end - a Datum

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getFilenameFor&unscoped_q=getFilenameFor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFilesFor"></a>
# getFilesFor
getFilesFor( DatumRange targetRange ) &rarr; File



### Parameters:
targetRange - a DatumRange

### Returns:
java.io.File[]


<a href="https://github.com/autoplot/dev/search?q=getFilesFor&unscoped_q=getFilesFor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getFilesFor( DatumRange targetRange, ProgressMonitor monitor ) &rarr; File<br>
***
<a name="getNameFor"></a>
# getNameFor
getNameFor( java.io.File file ) &rarr; String

Need a way to recover the model name of a file.  The returned File from getFilesFor can be anywhere,
 so it would be good to provide a way to get it back into a FSM name.

### Parameters:
file - a File

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getNameFor&unscoped_q=getNameFor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNamesFor"></a>
# getNamesFor
getNamesFor( DatumRange targetRange ) &rarr; String



### Parameters:
targetRange - restrict search to range.  May be null, in which case all names are returned.

### Returns:
java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=getNamesFor&unscoped_q=getNamesFor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getNamesFor( DatumRange targetRange, ProgressMonitor monitor ) &rarr; String<br>
***
<a name="getParentRegex"></a>
# getParentRegex
getParentRegex( String regex ) &rarr; String



### Parameters:
regex - a String

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getParentRegex&unscoped_q=getParentRegex">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRangeFor"></a>
# getRangeFor
getRangeFor( String name ) &rarr; DatumRange



### Parameters:
name - a String

### Returns:
org.das2.datum.DatumRange


<a href="https://github.com/autoplot/dev/search?q=getRangeFor&unscoped_q=getRangeFor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRepresentativeFile"></a>
# getRepresentativeFile
getRepresentativeFile( ProgressMonitor monitor ) &rarr; String

this is introduced to support discovery, where we just need one file to
 get started.  Before, there was code that would list all files, then use
 just the first one.  This may return a skeleton file, but getFileFor() must
 return a result.
 This implementation does the same as getNames(), but stops after finding a file.

### Parameters:
monitor - a ProgressMonitor

### Returns:
null if no file is found

<a href="https://github.com/autoplot/dev/search?q=getRepresentativeFile&unscoped_q=getRepresentativeFile">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFileWidth"></a>
# setFileWidth
setFileWidth( int multiplier, char digitCode ) &rarr; void

specify each file's width when the implicit width is not correct.  For
 example, files are stored with a tag for the starting day, but actually
 span a week.  The width must be an integer multiple of one year, month,
 day, hour, minute, or second.

### Parameters:
multiplier - an int
<br>digitCode - 'Y', 'm', 'd', 'H', etc.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFileWidth&unscoped_q=setFileWidth">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

