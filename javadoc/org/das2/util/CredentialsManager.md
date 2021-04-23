# org.das2.util.CredentialsManager

Provides per-resource login credentials 
 
 This class maintains a map of login credentials by resource ID.  The resource ID's 
 themselves are just strings.  The only expectation on resource ID strings is that they
 should be suitable for use as the Keys to a hash map.  Otherwise no formation rules are
 assumed nor expected.  User names and passwords for multiple web-sites, ftp sites, etc.
 are maintained by a single instance of this class.  Call:
 
    CredentialsManager.getManager()
 
 to get a reference to that single instance.
 
 In a graphical environment this class handles presenting dialogs to the user to gather
 logon credentials.  In a shell environment it will interact with the TTY to get user
 information.  
 
 An example of using this class to handle Das 2.1 server authentication which html
 location information formatting follows:
 <code>
 
 CredentialsManage cm = CrentialsManager.getMannager();
 String sLocId = "planet.physics.uiowa.edu/das/das2Server|voyager1/pwi/SpecAnalyzer-4s-Efield";
 
 if(!cm.hasCredentials(sLocId)){
    DasServer svr = DasServer.create(sDsdf);
    String sDesc = String.Format("<html><h1>%s</h1><h3>Server:  %s</h3><h3>DataSource: %s</h3>",
                                 DasServer.getName(), "planet.physics.uiowa.edu",
                                 "voyager1 > pwi > SpecAnalyzer-4s-Efield");
    cm.setDescription(sLocId, sDesc, DasServer.getLogo());
 }
 
 String sHash = getHttpBasicHash(sLocId)
 
 </code>
 
 Two previous classes, org.das2.util.filesystem.KeyChain (autoplot) and
 org.das2.client.Authenticator have approached this problem as well.  However both of
 those classes make assumptions that are not valid in general.  The first assumes that
 the caller somehow knows the username.  The second assumes that you are talking to
 a first generation Das 2.1 server.  Details of server communication are beyond the 
 scope of this class.

***
<a name="getHttpBasicHash"></a>
# getHttpBasicHash
getHttpBasicHash( String sLocationId ) &rarr; String

Get credentials in the form of a hashed HTTP Basic authentication string
 
 If there are no credentials stored for the given location id, this function may
 trigger interaction with the user, such as presenting modal dialogs, or changing the
 TTY to non-echo.

### Parameters:
sLocationId - A unique string identifying a location.  There are no formation
 rules on the string, but convenience functions are provided if a uniform naming 
 convention is desired.

### Returns:
The string USERNAME + ":" + PASSWORD that is then run through a base64 
 encoding.  If no credentials are available for the given location ID and none can be 
 gathered from the user (possibly due to the java.awt.headless being set or the
 user pressing cancel), null is returned.
### See Also:
<a href='#getHttpBasicHashRaw'>getHttpBasicHashRaw(java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getHttpBasicHash&unscoped_q=getHttpBasicHash">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getHttpBasicHashRaw"></a>
# getHttpBasicHashRaw
getHttpBasicHashRaw( String sLocationId ) &rarr; String

Get credentials in the form of a hashed HTTP Basic authentication string.

 If there are no credentials stored for the given location id, this function
 may trigger interaction with the user, such as presenting modal dialogs, or
 changing the TTY to non-echo.

### Parameters:
sLocationId - A unique string identifying a location. There are no formation
 rules on the string, but convenience functions are provided if a uniform naming
 convention is desired.

### Returns:
The string USERNAME + ":" + PASSWORD. If no credentials are available for
 the given location ID and none can be gathered from the user (possibly due to the
 java.awt.headless being set or the user pressing cancel), null is returned.
### See Also:
<a href='#getHttpBasicHash'>getHttpBasicHash(java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getHttpBasicHashRaw&unscoped_q=getHttpBasicHashRaw">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMannager"></a>
# getMannager
getMannager(  ) &rarr; CredentialsManager

Get a reference to the authentication manager.  
 
 Typically this is the function you want to use to get started.

### Returns:
org.das2.util.CredentialsManager


<a href="https://github.com/autoplot/dev/search?q=getMannager&unscoped_q=getMannager">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getMannager( String sWhich ) &rarr; CredentialsManager<br>
***
<a name="hasCredentials"></a>
# hasCredentials
hasCredentials( String sLocationId ) &rarr; boolean

Determine if there are any stored credentials for this location 
 
 If either a username or a password have been provided for the location
 then it is considered to have credentials

### Parameters:
sLocationId - The location to describe, can not be null.

### Returns:
true if there are stored credentials, false otherwise

<a href="https://github.com/autoplot/dev/search?q=hasCredentials&unscoped_q=hasCredentials">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasDescription"></a>
# hasDescription
hasDescription( String sLocationId ) &rarr; boolean

Determine if a given location has been described
 
 Gathering descriptive information about a remote location may trigger communication
 with a remote site.  Use this function to see if such communication is needed.

### Parameters:
sLocationId - The location in question

### Returns:
true if the location has been described, false otherwise

<a href="https://github.com/autoplot/dev/search?q=hasDescription&unscoped_q=hasDescription">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasIcon"></a>
# hasIcon
hasIcon( String sLocationId ) &rarr; boolean

Determine is a site image has been set for a location ID.  
 
 This function is provided because retrieving the logo for a site may trigger remote
 host communication.  Use this function to see if such communication is needed.

### Parameters:
sLocationId - the location in question

### Returns:
true if the location has as attached icon logo

<a href="https://github.com/autoplot/dev/search?q=hasIcon&unscoped_q=hasIcon">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="invalidate"></a>
# invalidate
invalidate( String sLocationId ) &rarr; void

Let the credentials manager know that stored credentials for a location are invalid

### Parameters:
sLocationId - a String

### Returns:
a void


<a href="https://github.com/autoplot/dev/search?q=invalidate&unscoped_q=invalidate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDescription"></a>
# setDescription
setDescription( String sLocationId, String sDescription ) &rarr; void

Provide a description of a location for use in authentication dialogs.
 
 Use this function to tie a string description to a location id.  This description
 will be used when interacting with the user.  If no description is present, then just
 the location ID itself will be used to identify the site to the end user.
 Usually location strings aren't that easy to read so use of this function or the
 version with an icon argument is recommended, though not required.

### Parameters:
sLocationId - The location to describe, can not be null.
<br>sDescription - A string to present to a user when prompting for a credentials
 for this location, may be a basic HTML string.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDescription&unscoped_q=setDescription">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

setDescription( String sLocationId, String sDescription, javax.swing.ImageIcon icon ) &rarr; void<br>
***
<a name="setHttpBasicHashRaw"></a>
# setHttpBasicHashRaw
setHttpBasicHashRaw( String sLocationId, String userInfo ) &rarr; void



### Parameters:
sLocationId - a String
<br>userInfo - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setHttpBasicHashRaw&unscoped_q=setHttpBasicHashRaw">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

