# org.autoplot.cdf.CdfDataSource

CDF data source based on Nand Lal's pure-Java
 CDF reader.  CDF, or Common Data Format, is a NASA data format.

# CdfDataSource( java.net.URI uri )


***
<a name="timer"></a>
# timer

To resolve bug 1002 we unload the cache after 10 seconds.  Joe at Aerospace had a problem where
 he couldn't kill a lingering autoplot process and then couldn't get at the file because it held a reference to the
 file.  Now we automatically unload all the cached files.  I did look at just disabling the cache, but the file is
 open and closed three times during the load.  See http://sourceforge.net/p/autoplot/bugs/1002.

***
<a name="checkCdf"></a>
# checkCdf
checkCdf( java.io.File cdfFile ) &rarr; void

check if the file really is a CDF, and throw IllegalArgumentException if it is not.
 NetCDF files occasionally use the extension .cdf.

### Parameters:
cdfFile - a CDF file (or not)

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=checkCdf&unscoped_q=checkCdf">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCdfFile"></a>
# getCdfFile
getCdfFile( String fileName ) &rarr; CDFReader

get the abstract access object to the given CDF file.  This provides read-only access to the file, and a cache
 is used to limit the number of references managed.
 See bug http://sourceforge.net/p/autoplot/bugs/922/

 The result returns a CDF object which contains a read-only memory-mapped byte buffer.

### Parameters:
fileName - a String

### Returns:
the CDF reference used to access the file

<a href="https://github.com/autoplot/dev/search?q=getCdfFile&unscoped_q=getCdfFile">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSet"></a>
# getDataSet
getDataSet( ProgressMonitor mon ) &rarr; QDataSet



### Parameters:
mon - a ProgressMonitor

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getDataSet( ProgressMonitor mon, java.util.Map attr1 ) &rarr; QDataSet<br>
***
<a name="getMetadata"></a>
# getMetadata
getMetadata( ProgressMonitor mon ) &rarr; Map



### Parameters:
mon - a ProgressMonitor

### Returns:
java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getMetadata&unscoped_q=getMetadata">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMetadataModel"></a>
# getMetadataModel
getMetadataModel(  ) &rarr; MetadataModel

{@inheritDoc }

### Returns:
an IstpMetadataModel
### See Also:
<a href='IstpMetadataModel.md'>IstpMetadataModel</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getMetadataModel&unscoped_q=getMetadataModel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="printCacheReport"></a>
# printCacheReport
printCacheReport(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=printCacheReport&unscoped_q=printCacheReport">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

