# org.das2.util.filesystem.FileSystemSettings

controls for file systems.

***
<a name="PROP_LOCALCACHEDIR"></a>
# PROP_LOCALCACHEDIR

setting for the location of where the local cache is kept.

***
<a name="PROP_PERSISTENCE"></a>
# PROP_PERSISTENCE

setting for how long files should be kept and using in the cache.

***
<a name="PROP_ALLOWOFFLINE"></a>
# PROP_ALLOWOFFLINE

allow use of persistent, cached files when the file system is not accessible.
 FileSystem implementations will throw FileNotFound exception when remote
 resources are not available, and FileSystemOfflineExceptions are not
 thrown.

***
<a name="PROP_OFFLINE"></a>
# PROP_OFFLINE



***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addPropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="getConnectTimeoutMs"></a>
# getConnectTimeoutMs
getConnectTimeoutMs(  ) &rarr; int

return the connection timeout in milliseconds.

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=getConnectTimeoutMs&unscoped_q=getConnectTimeoutMs">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLocalCacheDir"></a>
# getLocalCacheDir
getLocalCacheDir(  ) &rarr; File

setting for the location of where the local cache is kept.

### Returns:
File that is the local cache directory.

<a href="https://github.com/autoplot/dev/search?q=getLocalCacheDir&unscoped_q=getLocalCacheDir">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPersistence"></a>
# getPersistence
getPersistence(  ) &rarr; Persistence

get the setting for how long files should be kept and using in the cache,
 e.g. Persistence.SESSION means during the session.

### Returns:
the setting

<a href="https://github.com/autoplot/dev/search?q=getPersistence&unscoped_q=getPersistence">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getReadTimeoutMs"></a>
# getReadTimeoutMs
getReadTimeoutMs(  ) &rarr; int

return the read timeout in milliseconds.

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=getReadTimeoutMs&unscoped_q=getReadTimeoutMs">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTemporaryFileTimeoutSeconds"></a>
# getTemporaryFileTimeoutSeconds
getTemporaryFileTimeoutSeconds(  ) &rarr; int

return the number of seconds that an unused temporary file will
 be left on the system before it may be deleted.  This presumes
 that the code can determine if a temporary file is in use, which is
 not really the case.

### Returns:
the number of seconds.

<a href="https://github.com/autoplot/dev/search?q=getTemporaryFileTimeoutSeconds&unscoped_q=getTemporaryFileTimeoutSeconds">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasAllPermission"></a>
# hasAllPermission
hasAllPermission(  ) &rarr; boolean

check the security manager to see if all permissions are allowed,
 True indicates is not an applet running in a sandbox.

 copy of DasAppliction.hasAllPermission

### Returns:
true if all permissions are allowed

<a href="https://github.com/autoplot/dev/search?q=hasAllPermission&unscoped_q=hasAllPermission">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isAllowOffline"></a>
# isAllowOffline
isAllowOffline(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isAllowOffline&unscoped_q=isAllowOffline">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isOffline"></a>
# isOffline
isOffline(  ) &rarr; boolean

true indicate file system is offline and cached files should be used.

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isOffline&unscoped_q=isOffline">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

removePropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="setAllowOffline"></a>
# setAllowOffline
setAllowOffline( boolean allowOffline ) &rarr; void



### Parameters:
allowOffline - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAllowOffline&unscoped_q=setAllowOffline">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLocalCacheDir"></a>
# setLocalCacheDir
setLocalCacheDir( java.io.File localCacheDir ) &rarr; void



### Parameters:
localCacheDir - a File

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLocalCacheDir&unscoped_q=setLocalCacheDir">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setOffline"></a>
# setOffline
setOffline( boolean offline ) &rarr; void

If true, then force the filesystems to be offline.  If false, then use each filesystem's status.
 FileSystem.reset() should be called after this.

### Parameters:
offline - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setOffline&unscoped_q=setOffline">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPersistence"></a>
# setPersistence
setPersistence( org.das2.util.filesystem.FileSystemSettings.Persistence persistence ) &rarr; void



### Parameters:
persistence - a FileSystemSettings.Persistence

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPersistence&unscoped_q=setPersistence">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRestrictPermission"></a>
# setRestrictPermission
setRestrictPermission( boolean v ) &rarr; void

true means don't attempt to gain access to applet-restricted functions.

### Parameters:
v - true means don't attempt to gain access to applet-restricted functions.

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/DasApplication.md#setRestrictPermission'>org.das2.DasApplication#setRestrictPermission</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setRestrictPermission&unscoped_q=setRestrictPermission">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

