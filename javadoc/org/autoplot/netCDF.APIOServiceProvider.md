# org.autoplot.netCDF.APIOServiceProvider

APIOServiceProvider adapts Autoplot's data model to NetCDF to allow Autoplot
 URIs to be read into NetCDF.  The property vapuri in the NCML file contains
 an Autoplot URI.  It's been a while since we've played with this (to prove
 the idea), and I'm not sure where example NCML files are found.

# APIOServiceProvider( )


***
<a name="close"></a>
# close
close(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=close&unscoped_q=close">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDetailInfo"></a>
# getDetailInfo
getDetailInfo(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getDetailInfo&unscoped_q=getDetailInfo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFileTypeDescription"></a>
# getFileTypeDescription
getFileTypeDescription(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getFileTypeDescription&unscoped_q=getFileTypeDescription">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFileTypeId"></a>
# getFileTypeId
getFileTypeId(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getFileTypeId&unscoped_q=getFileTypeId">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFileTypeVersion"></a>
# getFileTypeVersion
getFileTypeVersion(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getFileTypeVersion&unscoped_q=getFileTypeVersion">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isValidFile"></a>
# isValidFile
isValidFile( RandomAccessFile arg0 ) &rarr; boolean



### Parameters:
arg0 - a RandomAccessFile

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isValidFile&unscoped_q=isValidFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="open"></a>
# open
open( RandomAccessFile raf, NetcdfFile ncfile, CancelTask arg2 ) &rarr; void



### Parameters:
raf - a RandomAccessFile
<br>ncfile - a NetcdfFile
<br>arg2 - a CancelTask

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=open&unscoped_q=open">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readData"></a>
# readData
readData( Variable variable, Section section ) &rarr; Array



### Parameters:
variable - a Variable
<br>section - a Section

### Returns:
Array


<a href="https://github.com/autoplot/dev/search?q=readData&unscoped_q=readData">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readSection"></a>
# readSection
readSection( ParsedSectionSpec arg0 ) &rarr; Array



### Parameters:
arg0 - a ParsedSectionSpec

### Returns:
Array


<a href="https://github.com/autoplot/dev/search?q=readSection&unscoped_q=readSection">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readToByteChannel"></a>
# readToByteChannel
readToByteChannel( Variable arg0, Section arg1, java.nio.channels.WritableByteChannel arg2 ) &rarr; long



### Parameters:
arg0 - a Variable
<br>arg1 - a Section
<br>arg2 - a WritableByteChannel

### Returns:
long


<a href="https://github.com/autoplot/dev/search?q=readToByteChannel&unscoped_q=readToByteChannel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="sync"></a>
# sync
sync(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=sync&unscoped_q=sync">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="syncExtend"></a>
# syncExtend
syncExtend(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=syncExtend&unscoped_q=syncExtend">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toStringDebug"></a>
# toStringDebug
toStringDebug( Object arg0 ) &rarr; String



### Parameters:
arg0 - an Object

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toStringDebug&unscoped_q=toStringDebug">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

