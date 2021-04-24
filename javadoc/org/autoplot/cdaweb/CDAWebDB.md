# org.autoplot.cdaweb.CDAWebDB

Class for encapsulating the functions of the database

# CDAWebDB( )


***
<a name="CDAWeb"></a>
# CDAWeb



***
<a name="dbloc"></a>
# dbloc



***
<a name="getBaseUrl"></a>
# getBaseUrl
getBaseUrl( String spid ) &rarr; String

returns the base URL.  FTP urls in the all.xml file are converted to HTTP by replacing
 "ftp://cdaweb.gsfc.nasa.gov/pub/istp/" with  "https://cdaweb.gsfc.nasa.gov/sp_phys/data/"

### Parameters:
spid - the id like "AC_H2_CRIS"

### Returns:
the base URL like https://cdaweb.gsfc.nasa.gov/sp_phys/data/ace/cris/level_2_cdaweb/cris_h2

<a href="https://github.com/autoplot/dev/search?q=getBaseUrl&unscoped_q=getBaseUrl">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFiles"></a>
# getFiles
getFiles( String spid, DatumRange tr, String useWebServiceHint, ProgressMonitor mon ) &rarr; String

isolate the code that resolves which files need to be accessed, so that
 we can use the web service when it is available.

### Parameters:
spid - the service provider id, like "AC_H2_CRIS"
<br>tr - the timerange
<br>useWebServiceHint - null means no preference, or "T", or "F" means use file template found in all.xml.
<br>mon - progress monitor for the download

### Returns:
array of strings, with filename|startTime|endTime

<a href="https://github.com/autoplot/dev/search?q=getFiles&unscoped_q=getFiles">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFilesAndRangesFromWebService"></a>
# getFilesAndRangesFromWebService
getFilesAndRangesFromWebService( String spid, DatumRange tr ) &rarr; String

get the list of files from the web service

### Parameters:
spid - the id like "AC_H2_CRIS"
<br>tr - the timerange constraint

### Returns:
filename|startTime|endTime

<a href="https://github.com/autoplot/dev/search?q=getFilesAndRangesFromWebService&unscoped_q=getFilesAndRangesFromWebService">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInstance"></a>
# getInstance
getInstance(  ) &rarr; CDAWebDB



### Returns:
org.autoplot.cdaweb.CDAWebDB


<a href="https://github.com/autoplot/dev/search?q=getInstance&unscoped_q=getInstance">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMasterFile"></a>
# getMasterFile
getMasterFile( String ds, ProgressMonitor p ) &rarr; String

return the name of a master file, which is used to override the metadata
 of the daily files.

### Parameters:
ds - the name, like A1_K0_MPA
<br>p - progress monitor

### Returns:
the name (http://...) of the master file to use, which may be one of the data files.

<a href="https://github.com/autoplot/dev/search?q=getMasterFile&unscoped_q=getMasterFile">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNaming"></a>
# getNaming
getNaming( String spid ) &rarr; String

returns the filename convention for spid, found in all.xml at /sites/datasite/dataset[@serviceprovider_ID='%s']/access
 For AC_H2_CRIS, this combines the subdividedby and filenaming properties to get %Y/ac_h2_cris_%Y%m%d_?%v.cdf

### Parameters:
spid - the id like "AC_H2_CRIS"

### Returns:
URI template like "%Y/ac_h2_cris_%Y%m%d_?%v.cdf"

<a href="https://github.com/autoplot/dev/search?q=getNaming&unscoped_q=getNaming">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getOriginalFilesAndRangesFromWebService"></a>
# getOriginalFilesAndRangesFromWebService
getOriginalFilesAndRangesFromWebService( String spid, DatumRange tr, ProgressMonitor mon ) &rarr; String

get the list of files from the web service

### Parameters:
spid - the service provider id, like "AC_H2_CRIS"
<br>tr - the timerange constraint
<br>mon - progress monitor

### Returns:
filename|startTime|endTime

<a href="https://github.com/autoplot/dev/search?q=getOriginalFilesAndRangesFromWebService&unscoped_q=getOriginalFilesAndRangesFromWebService">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSampleFile"></a>
# getSampleFile
getSampleFile( String spid ) &rarr; String

return a sample file from the dataset.

### Parameters:
spid - the id like "AC_H2_CRIS"

### Returns:
a downloadable file like http://cdaweb.gsfc.nasa.gov/pub/data/ace/cris/level_2_cdaweb/cris_h2/2015/ac_h2_cris_20151115_v06.cdf

<a href="https://github.com/autoplot/dev/search?q=getSampleFile&unscoped_q=getSampleFile">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSampleTime"></a>
# getSampleTime
getSampleTime( String spid ) &rarr; String

return a range of a file that could be plotted.  Right now, this
 just creates a FSM and gets a file.

### Parameters:
spid - the id like "AC_H2_CRIS"

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getSampleTime&unscoped_q=getSampleTime">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getServiceProviderIds"></a>
# getServiceProviderIds
getServiceProviderIds(  ) &rarr; Map



### Returns:
Map from serviceproviderId to description

<a href="https://github.com/autoplot/dev/search?q=getServiceProviderIds&unscoped_q=getServiceProviderIds">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTimeRange"></a>
# getTimeRange
getTimeRange( String spid ) &rarr; String

return the timerange spanning the availability of the dataset.

### Parameters:
spid - service provider id.

### Returns:
the time range (timerange_start, timerange_stop) for the dataset.

<a href="https://github.com/autoplot/dev/search?q=getTimeRange&unscoped_q=getTimeRange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isOnline"></a>
# isOnline
isOnline(  ) &rarr; boolean

returns true if the CDAWeb is on line.

### Returns:
true if the CDAWeb is on line.

<a href="https://github.com/autoplot/dev/search?q=isOnline&unscoped_q=isOnline">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void

4.2 seconds before getting description.  After too!

### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="maybeRefresh"></a>
# maybeRefresh
maybeRefresh( ProgressMonitor mon ) &rarr; void

refresh no more often than once per 10 minutes.  We don't need to refresh
 often.  Note it only takes a few seconds to refresh, plus download time,
 but we don't want to pound on the CDAWeb server needlessly.

### Parameters:
mon - a ProgressMonitor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=maybeRefresh&unscoped_q=maybeRefresh">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="refresh"></a>
# refresh
refresh( ProgressMonitor mon ) &rarr; void

Download and parse the all.xml to create a database of available products.

### Parameters:
mon - progress monitor for the task

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=refresh&unscoped_q=refresh">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

