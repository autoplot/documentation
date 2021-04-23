# org.autoplot.servlet.ServletUtil

Utilities for the servlets

# ServletUtil( )


***
<a name="checkSecurity"></a>
# checkSecurity
checkSecurity( HttpServletResponse response, String id, String suri, String vap ) &rarr; SecurityResponse

This checks the whitelist for the URI, and also inserts headers into the response.

### Parameters:
response - a HttpServletResponse
<br>id - null or the id, which is mapped to a URI.
<br>suri - null or the uri.
<br>vap - null or the vap

### Returns:
true if the URI is whitelisted

<a href="https://github.com/autoplot/dev/search?q=checkSecurity&unscoped_q=checkSecurity">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="dumpWhitelistToLogger"></a>
# dumpWhitelistToLogger
dumpWhitelistToLogger( java.util.logging.Level level ) &rarr; void

dump the whitelist to the logger at the given level.

### Parameters:
level - the level to log at.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dumpWhitelistToLogger&unscoped_q=dumpWhitelistToLogger">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getIdMap"></a>
# getIdMap
getIdMap(  ) &rarr; Map

return the id map, checking no more than once per 5 seconds, and
 creating an empty file if one is not found.  
 See HOME/autoplot_data/server/

### Returns:
map from one string to another.

<a href="https://github.com/autoplot/dev/search?q=getIdMap&unscoped_q=getIdMap">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getIntParameter"></a>
# getIntParameter
getIntParameter( HttpServletRequest request, String name, int dval ) &rarr; int



### Parameters:
request - a HttpServletRequest
<br>name - a String
<br>dval - an int

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getIntParameter&unscoped_q=getIntParameter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getServletContact"></a>
# getServletContact
getServletContact(  ) &rarr; String

return the contact info for the server

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getServletContact&unscoped_q=getServletContact">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getServletHome"></a>
# getServletHome
getServletHome(  ) &rarr; File



### Returns:
java.io.File


<a href="https://github.com/autoplot/dev/search?q=getServletHome&unscoped_q=getServletHome">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getStringParameter"></a>
# getStringParameter
getStringParameter( HttpServletRequest request, String name, String dval ) &rarr; String



### Parameters:
request - a HttpServletRequest
<br>name - a String
<br>dval - a String

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getStringParameter&unscoped_q=getStringParameter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getWhiteList"></a>
# getWhiteList
getWhiteList(  ) &rarr; List

return the whitelist, checking no more than once per 5 seconds, and
 creating the default file if one is not found.  
 See HOME/autoplot_data/server/whitelist.txt

### Returns:
list of regular expressions to allow.

<a href="https://github.com/autoplot/dev/search?q=getWhiteList&unscoped_q=getWhiteList">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isWhitelisted"></a>
# isWhitelisted
isWhitelisted( String suri ) &rarr; boolean

return true if the suri is whitelisted, meaning we trust that 
 content from this address will not harm the server.

### Parameters:
suri - the uri.

### Returns:
true if the suri is whitelisted.

<a href="https://github.com/autoplot/dev/search?q=isWhitelisted&unscoped_q=isWhitelisted">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="securityCheckPart2"></a>
# securityCheckPart2
securityCheckPart2( org.autoplot.servlet.ServletUtil.SecurityResponse sr ) &rarr; void

this is the part that throws the exception if security violation occurs.

### Parameters:
sr - a ServletUtil.SecurityResponse

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=securityCheckPart2&unscoped_q=securityCheckPart2">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

