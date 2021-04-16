# org.das2.fsm.FileStorageModelRepresents a method for storing data sets in a set of files by time.  The
 client provides a regex for the files and how each group of the regex is
 interpreted as a time digit.  The model can then be used to provide the set
 of files that cover a time range, etc.

 This new implementation uses a TimeParser object to more quickly process 
 file names.
***
<a name="cacheCleanup"></a>
# cacheCleanup
cacheCleanup(  ) &rarr; void

remove files that have been identified as old versions.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=cacheCleanup&unscoped_q=cacheCleanup">[search for examples]</a>

***
<a name="containsFile"></a>
# containsFile
containsFile( java.io.File file ) &rarr; boolean

return true if the file came (or could come) from this FileStorageModel.

### Parameters:
file - the file

### Returns:
true if the file came (or could come) from this FileStorageModel.

<a href="https://github.com/autoplot/dev/search?q=containsFile&unscoped_q=containsFile">[search for examples]</a>

***
<a name="create"></a>
# create
create( org.das2.util.filesystem.FileSystem root, String template ) &rarr; FileStorageModel

creates a FileStorageModel for the given template, which uses:
 <pre>%Y-%m-%dT%H:%M:%S.%{milli}Z";
    %Y  4-digit year
    %m  2-digit month
    %d  2-digit day of month
    %j  3-digit day of year
    %H  2-digit Hour
    %M  2-digit Minute
    %S  2-digit second
    %v  best version by number  Also %(v,sep) for 4.3.2  or %(v,alpha)
    %{milli}  3-digit milliseconds </pre>
 product_$(o,id=ftp://stevens.lanl.gov/pub/projects/rbsp/autoplot/orbits/rbspa_pp).png

### Parameters:
root - FileSystem source of the files.
<br>template - describes how filenames are constructed.  This is converted to a regular expression and may contain regex elements without groups.  The
   string may contain $ instead of percents as long as there are no percents in the string.

### Returns:
a newly-created FileStorageModel.

<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

create( org.das2.util.filesystem.FileSystem root, String template, String fieldName, org.das2.datum.TimeParser.FieldHandler fieldHandler ) &rarr; FileStorageModel<br>
***
<a name="generateNamesFor"></a>
# generateNamesFor
generateNamesFor( DatumRange range ) &rarr; String

generate the names of the files that would cover this range.  This was
 taken from Autoplot's org.virbo.jythonsupport.Util.  
 TODO: versioning, etc.

### Parameters:
range - the time range to cover.

### Returns:
the string names, each in the context of the filesystem.

<a href="https://github.com/autoplot/dev/search?q=generateNamesFor&unscoped_q=generateNamesFor">[search for examples]</a>

***
<a name="getBestFilesFor"></a>
# getBestFilesFor
getBestFilesFor( DatumRange targetRange ) &rarr; File

return the best files found for the range, without progress feedback.

### Parameters:
targetRange - a DatumRange

### Returns:
a java.io.File[]


<a href="https://github.com/autoplot/dev/search?q=getBestFilesFor&unscoped_q=getBestFilesFor">[search for examples]</a>

getBestFilesFor( DatumRange targetRange, ProgressMonitor monitor ) &rarr; File<br>
***
<a name="getBestNamesFor"></a>
# getBestNamesFor
getBestNamesFor( DatumRange targetRange, ProgressMonitor monitor ) &rarr; String

return the names in the range, minding version numbers, or all available 
 names if the range is null.  This will list directories.

### Parameters:
targetRange - range limit, or null.
<br>monitor - a ProgressMonitor

### Returns:
array of names within the system.

<a href="https://github.com/autoplot/dev/search?q=getBestNamesFor&unscoped_q=getBestNamesFor">[search for examples]</a>

getBestNamesFor( DatumRange targetRange ) &rarr; String<br>
***
<a name="getCacheTagFor"></a>
# getCacheTagFor
getCacheTagFor( org.das2.fsm.FileStorageModel fsm, DatumRange range, java.lang.String[] names ) &rarr; CacheTag



### Parameters:
fsm - a FileStorageModel
<br>range - a DatumRange
<br>names - a java.lang.String[]

### Returns:
org.das2.datum.CacheTag


<a href="https://github.com/autoplot/dev/search?q=getCacheTagFor&unscoped_q=getCacheTagFor">[search for examples]</a>

getCacheTagFor( org.das2.fsm.FileStorageModel fsm, DatumRange range, java.io.File[] files ) &rarr; CacheTag<br>
***
<a name="getChildFileSystem"></a>
# getChildFileSystem
getChildFileSystem( org.das2.util.filesystem.FileSystem root, String child, ProgressMonitor monitor ) &rarr; FileSystem

return a child filesystem, with special code for LocalFileSystems to support
 Windows.  TODO: look into .zip child.

### Parameters:
root - a FileSystem
<br>child - a String
<br>monitor - a ProgressMonitor

### Returns:
the FileSystem
### See Also:
<a href='https://sourceforge.net/p/autoplot/bugs/2132'>https://sourceforge.net/p/autoplot/bugs/2132</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getChildFileSystem&unscoped_q=getChildFileSystem">[search for examples]</a>

***
<a name="getField"></a>
# getField
getField( String field, String name ) &rarr; String

return the field value for the given name.  For example, if the spec
 is $Y/$m/$d/$Y$m$d_v$(v,sep).dat and the name matched is 2014/04/04/20140404_v2.3.dat
 then calling this for the field "v" would result in "2.3"  This should not
 be used to retrieve fields that are components of the time range, such as 
 $Y or $m.

### Parameters:
field - field, for example "v"
<br>name - name, for example 2014/04/04/20140404_v2.3.dat

### Returns:
the field value, for example, "2.3" when the spec is $Y/$m/$d/$Y$m$d_v$v.dat

<a href="https://github.com/autoplot/dev/search?q=getField&unscoped_q=getField">[search for examples]</a>

***
<a name="getFileFor"></a>
# getFileFor
getFileFor( String name ) &rarr; File

download the file for the given name within the filesystem.

### Parameters:
name - the name within the filesystem.

### Returns:
null or a local file which can be opened.

<a href="https://github.com/autoplot/dev/search?q=getFileFor&unscoped_q=getFileFor">[search for examples]</a>

getFileFor( String name, ProgressMonitor monitor ) &rarr; File<br>
***
<a name="getFileSystem"></a>
# getFileSystem
getFileSystem(  ) &rarr; FileSystem

return the filesystem used to implement this.

### Returns:
filesystem

<a href="https://github.com/autoplot/dev/search?q=getFileSystem&unscoped_q=getFileSystem">[search for examples]</a>

***
<a name="getFilenameFor"></a>
# getFilenameFor
getFilenameFor( Datum start, Datum end ) &rarr; String

return a filename that would intersect the range.  Note this file
 may not actually exist.  This may be used to quantize the range.
 The template may not contain versions.

### Parameters:
start - a Datum
<br>end - a Datum

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getFilenameFor&unscoped_q=getFilenameFor">[search for examples]</a>

***
<a name="getFilesFor"></a>
# getFilesFor
getFilesFor( DatumRange targetRange ) &rarr; File



### Parameters:
targetRange - a DatumRange

### Returns:
java.io.File[]


<a href="https://github.com/autoplot/dev/search?q=getFilesFor&unscoped_q=getFilesFor">[search for examples]</a>

getFilesFor( java.lang.String[] names, ProgressMonitor monitor ) &rarr; File<br>
getFilesFor( DatumRange targetRange, ProgressMonitor monitor ) &rarr; File<br>
***
<a name="getNameFor"></a>
# getNameFor
getNameFor( java.io.File file ) &rarr; String

Provides a way to recover the model name of a file.  The returned File from getFilesFor can be anywhere,
 so it would be good to provide a way to get it back into a FSM name.  For example, a filesystem
 might download the remote file to a cache directory, which is the File that is provided to the
 client, sometimes the client will need to recover the name of the corresponding FileObject, so
 this maps the File back to the name.

### Parameters:
file - the file

### Returns:
the canonical name of the file.

<a href="https://github.com/autoplot/dev/search?q=getNameFor&unscoped_q=getNameFor">[search for examples]</a>

***
<a name="getNamesFor"></a>
# getNamesFor
getNamesFor( DatumRange targetRange ) &rarr; String

return the names in the range, or all names if the range is null.

### Parameters:
targetRange - range limit, or null.

### Returns:
array of names within the system.

<a href="https://github.com/autoplot/dev/search?q=getNamesFor&unscoped_q=getNamesFor">[search for examples]</a>

getNamesFor( DatumRange targetRange, ProgressMonitor monitor ) &rarr; String<br>
***
<a name="getParent"></a>
# getParent
getParent(  ) &rarr; FileStorageModel

returns the parent or null if none exists.  None will exist when there
 are no more wildcards. (/home/foo/$Y/$m-$d.dat has parent /home/foo/$Y
 which has parent null.)

### Returns:
parent or null.

<a href="https://github.com/autoplot/dev/search?q=getParent&unscoped_q=getParent">[search for examples]</a>

***
<a name="getRangeFor"></a>
# getRangeFor
getRangeFor( String name ) &rarr; DatumRange

return the time range represented by this name.

### Parameters:
name - like 2013-10-31

### Returns:
the timerange representing the day 2013-10-31

<a href="https://github.com/autoplot/dev/search?q=getRangeFor&unscoped_q=getRangeFor">[search for examples]</a>

***
<a name="getRepresentativeFile"></a>
# getRepresentativeFile
getRepresentativeFile( ProgressMonitor monitor ) &rarr; String

return a random file from the FSM, which can be used to represent a typical file.  For
 example, we need to look at metadata to see what is available.

### Parameters:
monitor - progress monitor in case a file must be downloaded.

### Returns:
a reference to the file within the FileSystem, or null if one is not found.

<a href="https://github.com/autoplot/dev/search?q=getRepresentativeFile&unscoped_q=getRepresentativeFile">[search for examples]</a>

getRepresentativeFile( ProgressMonitor monitor, String childRegex ) &rarr; String<br>
getRepresentativeFile( ProgressMonitor monitor, String childRegex, DatumRange range ) &rarr; String<br>
getRepresentativeFile( org.das2.fsm.FileStorageModel ths, ProgressMonitor monitor, String childRegex, DatumRange range, int depth ) &rarr; String<br>
***
<a name="getRoot"></a>
# getRoot
getRoot(  ) &rarr; String

return the root of the filesystem as a string.

### Returns:
the root of the filesystem as a string.

<a href="https://github.com/autoplot/dev/search?q=getRoot&unscoped_q=getRoot">[search for examples]</a>

***
<a name="hasField"></a>
# hasField
hasField( String field ) &rarr; boolean

returns true if the parser has the field.

### Parameters:
field - e.g. "x"

### Returns:
true if the parser has the field.

<a href="https://github.com/autoplot/dev/search?q=hasField&unscoped_q=hasField">[search for examples]</a>

***
<a name="quantize"></a>
# quantize
quantize( DatumRange timeRange ) &rarr; DatumRange

return the timerange that contains the given timerange and
 exactly contains a set of granules.
 
 This needs to be synchronized because the timeParser.

### Parameters:
timeRange - arbitrary time range

### Returns:
list of file timeranges covering file input timeRange.

<a href="https://github.com/autoplot/dev/search?q=quantize&unscoped_q=quantize">[search for examples]</a>

***
<a name="setContext"></a>
# setContext
setContext( DatumRange trdr ) &rarr; void

set the datum range giving context to the files.  For example,
 filenames are just $H$M$S.dat, and the context is "Jan 17th, 2015"

### Parameters:
trdr - the context

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setContext&unscoped_q=setContext">[search for examples]</a>

***
<a name="splitIndex"></a>
# splitIndex
splitIndex( String surl ) &rarr; int

This returns the index splitting the static part of the filename from the templated part.
 For example, http://autoplot.org/data/C1_CP_EDI_EGD__$Y$m$d_V$v.cef is split into:<br>
 <pre>http://autoplot.org/data/
C1_CP_EDI_EGD__$Y$m$d_V$v.cef</pre> and
 http://emfisis.physics.uiowa.edu/Flight/RBSP-A/Quick-Look/$Y/$m/$d/rbsp-a_magnetometer_4sec-gsm_emfisis-Quick-Look_$Y$m$d_v$(v,sep).cdf:<br>
 <pre>http://emfisis.physics.uiowa.edu/Flight/RBSP-A/Quick-Look/
$Y/$m/$d/rbsp-a_magnetometer_4sec-gsm_emfisis-Quick-Look_$Y$m$d_v$(v,sep).cdf</pre>
 <tt></tt><br>

 <p>
 This new version uses regexs and is more complete than versions found in Autoplot, and they should
 eventually use this instead.  Note the Autoplot one returns the index of the last /, whereas this
 returns that index plus one.
 </p>
 
 <p>Taken from Autoplot's AggregatingDataSourceFactory, where Autoplot just has a URI and needs to get a file list.
 See also org/autoplot/pngwalk/WalkUtil.java splitIndex, which also allows wildcards like *.</p>

### Parameters:
surl - a string like http://autoplot.org/data/C1_CP_EDI_EGD__$Y$m$d_V$v.cef

### Returns:
an integer indicating the split index, so that surl.substring(0,i) includes the slash.

<a href="https://github.com/autoplot/dev/search?q=splitIndex&unscoped_q=splitIndex">[search for examples]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

