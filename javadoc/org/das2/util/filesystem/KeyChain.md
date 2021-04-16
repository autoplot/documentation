# org.das2.util.filesystem.KeyChainclass that contains the credentials for websites.  This is first
 introduced so that ftp://papco:@mrfrench.lanl.gov/ and subdirectories
 would just ask for credentials once.  Also, this allows all the sensitive
 information to be stored in one class.
KeyChain( )


***
<a name="addCookie"></a>
# addCookie
addCookie( String url, String cookie ) &rarr; void

Add a cookie for the URL.  This was added as a work-around to provide
 access to the MMS data server at LASP.

### Parameters:
url - a String
<br>cookie - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addCookie&unscoped_q=addCookie">[search for examples]</a>

***
<a name="checkUserInfo"></a>
# checkUserInfo
checkUserInfo( java.net.URL url ) &rarr; String

return null or the stored user info.  This allows clients to attempt to
 use stored user info without bothering the scientist if the info isn't 
 needed.

### Parameters:
url - the URL

### Returns:
the user info (user:password) associated, or null if the user info isn't found.

<a href="https://github.com/autoplot/dev/search?q=checkUserInfo&unscoped_q=checkUserInfo">[search for examples]</a>

***
<a name="clearAll"></a>
# clearAll
clearAll(  ) &rarr; void

clear all passwords.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=clearAll&unscoped_q=clearAll">[search for examples]</a>

***
<a name="clearUserPassword"></a>
# clearUserPassword
clearUserPassword( java.net.URI uri ) &rarr; void



### Parameters:
uri - an URI

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=clearUserPassword&unscoped_q=clearUserPassword">[search for examples]</a>

clearUserPassword( java.net.URL url ) &rarr; void<br>
***
<a name="getDefault"></a>
# getDefault
getDefault(  ) &rarr; KeyChain

get the single instance of the class.

### Returns:
the single instance of the class.

<a href="https://github.com/autoplot/dev/search?q=getDefault&unscoped_q=getDefault">[search for examples]</a>

***
<a name="getInstance"></a>
# getInstance
getInstance( String name ) &rarr; KeyChain

get the instance for this name.  This is added to support future applications, such as servlets, where
 multiple users are using the same process.

### Parameters:
name - a String

### Returns:
an org.das2.util.filesystem.KeyChain


<a href="https://github.com/autoplot/dev/search?q=getInstance&unscoped_q=getInstance">[search for examples]</a>

***
<a name="getUserInfo"></a>
# getUserInfo
getUserInfo( java.net.URI uri ) &rarr; String

get the user credentials, maybe throwing CancelledOperationException if the
 user hits cancel.

### Parameters:
uri - an URI

### Returns:
a String

### See Also:
<a href='#getUserInfo'>getUserInfo(java.net.URL)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getUserInfo&unscoped_q=getUserInfo">[search for examples]</a>

getUserInfo( java.net.URL url ) &rarr; String<br>
getUserInfo( java.net.URL url, String userInfo ) &rarr; String<br>
***
<a name="getUserInfoBase64Encoded"></a>
# getUserInfoBase64Encoded
getUserInfoBase64Encoded( java.net.URL url ) &rarr; String

return the user info but base-64 encoded.  This is put in so that
 a future version of the software can cache these as well.  This is
 intended to be inserted like so:
 <code>
 connection= theUrl.getConnection();
 String encode= KeyChain.getDefault().getUserInfoBase64Encoded( theUrl );
 if ( encode!=null ) connection.setRequestProperty("Authorization", "Basic " + encode);
 </code>

### Parameters:
url - the URL which may contain user info.

### Returns:
the base-64 encoded credentials.

<a href="https://github.com/autoplot/dev/search?q=getUserInfoBase64Encoded&unscoped_q=getUserInfoBase64Encoded">[search for examples]</a>

***
<a name="getWWWAuthenticate"></a>
# getWWWAuthenticate
getWWWAuthenticate( java.net.URL url ) &rarr; String

return null or the WWW-Authenticate string.

### Parameters:
url - an URL

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getWWWAuthenticate&unscoped_q=getWWWAuthenticate">[search for examples]</a>

***
<a name="hideUserInfo"></a>
# hideUserInfo
hideUserInfo( java.net.URI root ) &rarr; String



### Parameters:
root - an URI

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=hideUserInfo&unscoped_q=hideUserInfo">[search for examples]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

***
<a name="resolveUserInfo"></a>
# resolveUserInfo
resolveUserInfo( java.net.URI root ) &rarr; URI

plug the username and password into the URI.

### Parameters:
root - the URI, possibly needing a username and password.

### Returns:
the URI with the username and password.

<a href="https://github.com/autoplot/dev/search?q=resolveUserInfo&unscoped_q=resolveUserInfo">[search for examples]</a>

***
<a name="setParentGUI"></a>
# setParentGUI
setParentGUI( java.awt.Component c ) &rarr; void



### Parameters:
c - a Component

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setParentGUI&unscoped_q=setParentGUI">[search for examples]</a>

***
<a name="setUserInfo"></a>
# setUserInfo
setUserInfo( java.net.URL url, String userInfo ) &rarr; void

insert the userInfo into the table of stored passwords.
 TODO: note the path is not used in the hash, and it should be.

### Parameters:
url - an URL
<br>userInfo - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUserInfo&unscoped_q=setUserInfo">[search for examples]</a>

***
<a name="writeKeysFile"></a>
# writeKeysFile
writeKeysFile(  ) &rarr; void

dump the loaded keys into the file new File( FileSystem.settings().getLocalCacheDir(), "keychain.txt" )

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeKeysFile&unscoped_q=writeKeysFile">[search for examples]</a>

writeKeysFile( boolean toFile ) &rarr; void<br>
