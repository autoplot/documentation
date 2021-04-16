# org.autoplot.AutoplotDataServerData server for U. Iowa P.W. Group converts URIs into streams of data.  These would typically
 be qstream or older das2stream format, but the code (apparently) supports .xls, .dat, and .bin as well.

 See also AutoplotServer, which serves images.
AutoplotDataServer( )


***
<a name="doService"></a>
# doService
doService( String timeRange, String suri, String step, boolean stream, String format, java.io.PrintStream out, boolean ascii, java.util.Set outEmpty, ProgressMonitor mon ) &rarr; void

Perform the data service.

### Parameters:
timeRange - the time range to send out, such as "May 2003", or "" for none, or null for none.
<br>suri - the data source to read in.  If this has TimeSeriesBrowse, then we can stream the data.
<br>step - step size, such as "24 hr" or "3600s".  If the URI contains $H, "3600s" is used.
<br>stream - if true, send data out as it is read.
<br>format - FORM_QDS, FORM_D2S, FORM_HAPI
<br>out - stream which receives the data.
<br>ascii - if true, use ascii types for qstreams and das2streams.
<br>outEmpty - for the streaming library, so we don't put progress out until we've output the initial header.
<br>mon - progress monitor to monitor the stream.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=doService&unscoped_q=doService">[search for examples]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

