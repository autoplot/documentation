# org.das2.DasApplication

DasApplication object manages per-application resources, like object name space, 
 dataset caching, progress monitoring, exception handling and a network speed limiter.

***
<a name="createMainFrame"></a>
# <del>createMainFrame</del>
Deprecated: use createMainFrame( String title, Container container );
createMainFrame( String title, java.awt.Container container ) &rarr; JFrame<br>
createMainFrame(  ) &rarr; JFrame<br>
createMainFrame( String title ) &rarr; JFrame<br>
***
<a name="getDas2UserDirectory"></a>
# getDas2UserDirectory
getDas2UserDirectory(  ) &rarr; File

returns the location of the local directory sandbox.  For example,
 The web filesystem object downloads temporary files to here, logging
 properties file, etc.

 Assume that this File is local, so I/O is quick, and that the process
 has write access to this area.
 For definition, assume that at least 1Gb of storage is available as
 well.

### Returns:
java.io.File


<a href="https://github.com/autoplot/dev/search?q=getDas2UserDirectory&unscoped_q=getDas2UserDirectory">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDas2Version"></a>
# getDas2Version
getDas2Version(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getDas2Version&unscoped_q=getDas2Version">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSetCache"></a>
# getDataSetCache
getDataSetCache(  ) &rarr; DataSetCache



### Returns:
org.das2.dataset.DataSetCache


<a href="https://github.com/autoplot/dev/search?q=getDataSetCache&unscoped_q=getDataSetCache">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDefaultApplication"></a>
# getDefaultApplication
getDefaultApplication(  ) &rarr; DasApplication



### Returns:
org.das2.DasApplication


<a href="https://github.com/autoplot/dev/search?q=getDefaultApplication&unscoped_q=getDefaultApplication">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getExceptionHandler"></a>
# getExceptionHandler
getExceptionHandler(  ) &rarr; ExceptionHandler

warning: this code is repeated in FileSystem to avoid dependence.

### Returns:
an org.das2.util.ExceptionHandler


<a href="https://github.com/autoplot/dev/search?q=getExceptionHandler&unscoped_q=getExceptionHandler">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInputStreamMeter"></a>
# getInputStreamMeter
getInputStreamMeter(  ) &rarr; InputStreamMeter



### Returns:
org.das2.client.InputStreamMeter


<a href="https://github.com/autoplot/dev/search?q=getInputStreamMeter&unscoped_q=getInputStreamMeter">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLogger"></a>
# getLogger
getLogger(  ) &rarr; Logger



### Returns:
java.util.logging.Logger


<a href="https://github.com/autoplot/dev/search?q=getLogger&unscoped_q=getLogger">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getLogger( org.das2.system.LoggerId id ) &rarr; Logger<br>
***
<a name="getMainFrame"></a>
# getMainFrame
getMainFrame(  ) &rarr; JFrame



### Returns:
javax.swing.JFrame


<a href="https://github.com/autoplot/dev/search?q=getMainFrame&unscoped_q=getMainFrame">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMonitorFactory"></a>
# getMonitorFactory
getMonitorFactory(  ) &rarr; MonitorFactory



### Returns:
org.das2.system.MonitorFactory


<a href="https://github.com/autoplot/dev/search?q=getMonitorFactory&unscoped_q=getMonitorFactory">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNameContext"></a>
# getNameContext
getNameContext(  ) &rarr; NameContext



### Returns:
org.das2.NameContext


<a href="https://github.com/autoplot/dev/search?q=getNameContext&unscoped_q=getNameContext">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getProperty"></a>
# getProperty
getProperty( String name, String deft ) &rarr; String

support restricted security environment by checking permissions before 
 checking property.

### Parameters:
name - a String
<br>deft - a String

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getProperty&unscoped_q=getProperty">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasAllPermission"></a>
# hasAllPermission
hasAllPermission(  ) &rarr; boolean

check the security manager to see if all permissions are allowed,
 True indicates is not an applet running in a sandbox.
 See FileSystemSettings, which has a copy of this code

### Returns:
true if all permissions are allowed

<a href="https://github.com/autoplot/dev/search?q=hasAllPermission&unscoped_q=hasAllPermission">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isApplet"></a>
# isApplet
isApplet(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isApplet&unscoped_q=isApplet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isHeadless"></a>
# isHeadless
isHeadless(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isHeadless&unscoped_q=isHeadless">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isInteractive"></a>
# isInteractive
isInteractive(  ) &rarr; boolean

Getter for property interactive.

### Returns:
Value of property interactive.

<a href="https://github.com/autoplot/dev/search?q=isInteractive&unscoped_q=isInteractive">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isJavaWebStart"></a>
# isJavaWebStart
isJavaWebStart(  ) &rarr; boolean

return true if the application appears to have been launched with Java WebStart.

### Returns:
true if it appears that Java Webstart was used to launch the application.

<a href="https://github.com/autoplot/dev/search?q=isJavaWebStart&unscoped_q=isJavaWebStart">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isReloadLoggingProperties"></a>
# isReloadLoggingProperties
isReloadLoggingProperties(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isReloadLoggingProperties&unscoped_q=isReloadLoggingProperties">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="quit"></a>
# quit
quit(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=quit&unscoped_q=quit">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resetDefaultApplication"></a>
# resetDefaultApplication
resetDefaultApplication(  ) &rarr; void

nasty, evil method for releasing resources on a server.  DO NOT USE THIS!!!!

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resetDefaultApplication&unscoped_q=resetDefaultApplication">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setApplet"></a>
# setApplet
setApplet( boolean applet ) &rarr; void



### Parameters:
applet - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setApplet&unscoped_q=setApplet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setExceptionHandler"></a>
# setExceptionHandler
setExceptionHandler( org.das2.util.ExceptionHandler h ) &rarr; void

explicitly set the ExceptionHandler that will handle runtime exceptions

### Parameters:
h - an ExceptionHandler

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setExceptionHandler&unscoped_q=setExceptionHandler">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setHeadless"></a>
# setHeadless
setHeadless( boolean headless ) &rarr; void



### Parameters:
headless - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setHeadless&unscoped_q=setHeadless">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setInteractive"></a>
# setInteractive
setInteractive( boolean interactive ) &rarr; void

Setter for property interactive.

### Parameters:
interactive - New value of property interactive.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setInteractive&unscoped_q=setInteractive">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setMainFrame"></a>
# setMainFrame
setMainFrame( javax.swing.JFrame frame ) &rarr; void



### Parameters:
frame - a JFrame

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMainFrame&unscoped_q=setMainFrame">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setReloadLoggingProperties"></a>
# setReloadLoggingProperties
setReloadLoggingProperties( boolean v ) &rarr; void



### Parameters:
v - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setReloadLoggingProperties&unscoped_q=setReloadLoggingProperties">[search for examples]</a>
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
<a href='FileSystemSettings.md#setRestrictPermission'>FileSystemSettings#setRestrictPermission(boolean)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=setRestrictPermission&unscoped_q=setRestrictPermission">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="suggestNameFor"></a>
# suggestNameFor
suggestNameFor( Object c ) &rarr; String



### Parameters:
c - an Object

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=suggestNameFor&unscoped_q=suggestNameFor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

