# org.autoplot.hapiserver.Utilhelpful functions.
Util( )


***
<a name="HAPI_SERVER_HOME_PROPERTY"></a>
# HAPI_SERVER_HOME_PROPERTY

This should point to the name of the directory containing HAPI configuration.
 This directory should contain catalog.json, capabilities.json and a 
 subdirectory "info" which contains files with the name &lt;ID&gt;.json,
 each containing the info response.  Note these should also contain a
 tag "x_uri" which is the Autoplot URI that serves this data.

***
<a name="csvSplit"></a>
# csvSplit
csvSplit( String line, int nf ) &rarr; String

split, but not when comma is within quotes.

### Parameters:
line - for example 'a,b,"c,d"'
<br>nf - number of fields, or -1 for no constraint

### Returns:
['a','b','c,d']

<a href="https://github.com/autoplot/dev/search?q=csvSplit&unscoped_q=csvSplit">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDurationForHumans"></a>
# getDurationForHumans
getDurationForHumans( long dt ) &rarr; String

return the duration in a easily-human-consumable form.

### Parameters:
dt - the duration in milliseconds.

### Returns:
a duration like "2.6 hours"

<a href="https://github.com/autoplot/dev/search?q=getDurationForHumans&unscoped_q=getDurationForHumans">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getHapiHome"></a>
# getHapiHome
getHapiHome(  ) &rarr; File

return the root of the HAPI server.

### Returns:
the root of the HAPI server.

<a href="https://github.com/autoplot/dev/search?q=getHapiHome&unscoped_q=getHapiHome">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNumberOfElements"></a>
# getNumberOfElements
getNumberOfElements( JSONObject info ) &rarr; int

return the total number of elements of each parameter.

### Parameters:
info - the info

### Returns:
an int array with the number of elements in each parameter.

<a href="https://github.com/autoplot/dev/search?q=getNumberOfElements&unscoped_q=getNumberOfElements">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hapiVersion"></a>
# hapiVersion
hapiVersion(  ) &rarr; String

return the HAPI protocol version.

### Returns:
the HAPI protocol version.

<a href="https://github.com/autoplot/dev/search?q=hapiVersion&unscoped_q=hapiVersion">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="maybeInitialize"></a>
# maybeInitialize
maybeInitialize( ServletContext context ) &rarr; void

if HAPI_HOME has not been set, then set it.

### Parameters:
context - a ServletContext

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=maybeInitialize&unscoped_q=maybeInitialize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="raiseBadId"></a>
# raiseBadId
raiseBadId( String id, HttpServletResponse response, java.io.PrintWriter out ) &rarr; void

send a "bad id" response to the client.

### Parameters:
id - the id.
<br>response - the response object
<br>out - the print writer for the response object.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=raiseBadId&unscoped_q=raiseBadId">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="serverVersion"></a>
# serverVersion
serverVersion(  ) &rarr; String

return the server implementation version.

### Returns:
the server implementation version.

<a href="https://github.com/autoplot/dev/search?q=serverVersion&unscoped_q=serverVersion">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setHapiHome"></a>
# setHapiHome
setHapiHome( java.io.File f ) &rarr; void



### Parameters:
f - a File

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setHapiHome&unscoped_q=setHapiHome">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="subsetParams"></a>
# subsetParams
subsetParams( JSONObject info, String parameters ) &rarr; JSONObject

return a new JSONObject for the info request, with the subset of parameters.

### Parameters:
info - the root node of the info response.
<br>parameters - comma-delimited list of parameters.

### Returns:
the new JSONObject, with special tag __indexmap__ showing which columns are to be included in a data response.

<a href="https://github.com/autoplot/dev/search?q=subsetParams&unscoped_q=subsetParams">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="transfer"></a>
# transfer
transfer( java.io.InputStream src, java.io.OutputStream dest ) &rarr; void

transfers the data from one channel to another.  src and dest are
 closed after the operation is complete.

### Parameters:
src - an InputStream
<br>dest - an OutputStream

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=transfer&unscoped_q=transfer">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="validateJSON"></a>
# validateJSON
validateJSON( String json ) &rarr; boolean

return true if this is valid JSON, false otherwise, and log the exception at SEVERE.

### Parameters:
json - a String

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=validateJSON&unscoped_q=validateJSON">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

