# org.autoplot.util.TransparentLogger
***
<a name="addHandler"></a>
# addHandler
addHandler( java.util.logging.Handler handler ) &rarr; void



### Parameters:
handler - a Handler

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addHandler&unscoped_q=addHandler">[search for examples]</a>

***
<a name="config"></a>
# config
config( String msg ) &rarr; void



### Parameters:
msg - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=config&unscoped_q=config">[search for examples]</a>

***
<a name="entering"></a>
# entering
entering( String sourceClass, String sourceMethod, java.lang.Object[] params ) &rarr; void



### Parameters:
sourceClass - a String
<br>sourceMethod - a String
<br>params - a java.lang.Object[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=entering&unscoped_q=entering">[search for examples]</a>

entering( String sourceClass, String sourceMethod, Object param1 ) &rarr; void<br>
entering( String sourceClass, String sourceMethod ) &rarr; void<br>
***
<a name="exiting"></a>
# exiting
exiting( String sourceClass, String sourceMethod, Object result ) &rarr; void



### Parameters:
sourceClass - a String
<br>sourceMethod - a String
<br>result - an Object

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=exiting&unscoped_q=exiting">[search for examples]</a>

exiting( String sourceClass, String sourceMethod ) &rarr; void<br>
***
<a name="fine"></a>
# fine
fine( String msg ) &rarr; void



### Parameters:
msg - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=fine&unscoped_q=fine">[search for examples]</a>

***
<a name="finer"></a>
# finer
finer( String msg ) &rarr; void



### Parameters:
msg - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=finer&unscoped_q=finer">[search for examples]</a>

***
<a name="finest"></a>
# finest
finest( String msg ) &rarr; void



### Parameters:
msg - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=finest&unscoped_q=finest">[search for examples]</a>

***
<a name="getFilter"></a>
# getFilter
getFilter(  ) &rarr; Filter



### Returns:
java.util.logging.Filter


<a href="https://github.com/autoplot/dev/search?q=getFilter&unscoped_q=getFilter">[search for examples]</a>

***
<a name="getHandlers"></a>
# getHandlers
getHandlers(  ) &rarr; Handler



### Returns:
java.util.logging.Handler[]


<a href="https://github.com/autoplot/dev/search?q=getHandlers&unscoped_q=getHandlers">[search for examples]</a>

***
<a name="getLevel"></a>
# getLevel
getLevel(  ) &rarr; Level



### Returns:
java.util.logging.Level


<a href="https://github.com/autoplot/dev/search?q=getLevel&unscoped_q=getLevel">[search for examples]</a>

***
<a name="getLogger"></a>
# getLogger
getLogger( String name ) &rarr; Logger



### Parameters:
name - a String

### Returns:
java.util.logging.Logger


<a href="https://github.com/autoplot/dev/search?q=getLogger&unscoped_q=getLogger">[search for examples]</a>

***
<a name="getName"></a>
# getName
getName(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getName&unscoped_q=getName">[search for examples]</a>

***
<a name="getParent"></a>
# getParent
getParent(  ) &rarr; Logger



### Returns:
java.util.logging.Logger


<a href="https://github.com/autoplot/dev/search?q=getParent&unscoped_q=getParent">[search for examples]</a>

***
<a name="getResourceBundle"></a>
# getResourceBundle
getResourceBundle(  ) &rarr; ResourceBundle



### Returns:
java.util.ResourceBundle


<a href="https://github.com/autoplot/dev/search?q=getResourceBundle&unscoped_q=getResourceBundle">[search for examples]</a>

***
<a name="getResourceBundleName"></a>
# getResourceBundleName
getResourceBundleName(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getResourceBundleName&unscoped_q=getResourceBundleName">[search for examples]</a>

***
<a name="getUseParentHandlers"></a>
# getUseParentHandlers
getUseParentHandlers(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=getUseParentHandlers&unscoped_q=getUseParentHandlers">[search for examples]</a>

***
<a name="info"></a>
# info
info( String msg ) &rarr; void



### Parameters:
msg - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=info&unscoped_q=info">[search for examples]</a>

***
<a name="isLoggable"></a>
# isLoggable
isLoggable( java.util.logging.Level level ) &rarr; boolean



### Parameters:
level - a Level

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isLoggable&unscoped_q=isLoggable">[search for examples]</a>

***
<a name="log"></a>
# log
log( java.util.logging.Level level, String msg, java.lang.Throwable thrown ) &rarr; void



### Parameters:
level - a Level
<br>msg - a String
<br>thrown - a Throwable

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=log&unscoped_q=log">[search for examples]</a>

log( java.util.logging.Level level, String msg, java.lang.Object[] params ) &rarr; void<br>
log( java.util.logging.Level level, String msg, Object param1 ) &rarr; void<br>
log( java.util.logging.Level level, String msg ) &rarr; void<br>
log( java.util.logging.LogRecord record ) &rarr; void<br>
***
<a name="logp"></a>
# logp
logp( java.util.logging.Level level, String sourceClass, String sourceMethod, String msg, java.lang.Throwable thrown ) &rarr; void



### Parameters:
level - a Level
<br>sourceClass - a String
<br>sourceMethod - a String
<br>msg - a String
<br>thrown - a Throwable

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=logp&unscoped_q=logp">[search for examples]</a>

logp( java.util.logging.Level level, String sourceClass, String sourceMethod, String msg, java.lang.Object[] params ) &rarr; void<br>
logp( java.util.logging.Level level, String sourceClass, String sourceMethod, String msg, Object param1 ) &rarr; void<br>
logp( java.util.logging.Level level, String sourceClass, String sourceMethod, String msg ) &rarr; void<br>
***
<a name="logrb"></a>
# logrb
logrb( java.util.logging.Level level, String sourceClass, String sourceMethod, String bundleName, String msg, java.lang.Throwable thrown ) &rarr; void



### Parameters:
level - a Level
<br>sourceClass - a String
<br>sourceMethod - a String
<br>bundleName - a String
<br>msg - a String
<br>thrown - a Throwable

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=logrb&unscoped_q=logrb">[search for examples]</a>

logrb( java.util.logging.Level level, String sourceClass, String sourceMethod, String bundleName, String msg, java.lang.Object[] params ) &rarr; void<br>
logrb( java.util.logging.Level level, String sourceClass, String sourceMethod, String bundleName, String msg, Object param1 ) &rarr; void<br>
logrb( java.util.logging.Level level, String sourceClass, String sourceMethod, String bundleName, String msg ) &rarr; void<br>
***
<a name="removeHandler"></a>
# removeHandler
removeHandler( java.util.logging.Handler handler ) &rarr; void



### Parameters:
handler - a Handler

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeHandler&unscoped_q=removeHandler">[search for examples]</a>

***
<a name="setFilter"></a>
# setFilter
setFilter( java.util.logging.Filter newFilter ) &rarr; void



### Parameters:
newFilter - a Filter

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFilter&unscoped_q=setFilter">[search for examples]</a>

***
<a name="setLevel"></a>
# setLevel
setLevel( java.util.logging.Level newLevel ) &rarr; void



### Parameters:
newLevel - a Level

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLevel&unscoped_q=setLevel">[search for examples]</a>

***
<a name="setParent"></a>
# setParent
setParent( java.util.logging.Logger parent ) &rarr; void



### Parameters:
parent - a Logger

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setParent&unscoped_q=setParent">[search for examples]</a>

***
<a name="setUseParentHandlers"></a>
# setUseParentHandlers
setUseParentHandlers( boolean useParentHandlers ) &rarr; void



### Parameters:
useParentHandlers - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUseParentHandlers&unscoped_q=setUseParentHandlers">[search for examples]</a>

***
<a name="severe"></a>
# severe
severe( String msg ) &rarr; void



### Parameters:
msg - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=severe&unscoped_q=severe">[search for examples]</a>

***
<a name="throwing"></a>
# throwing
throwing( String sourceClass, String sourceMethod, java.lang.Throwable thrown ) &rarr; void



### Parameters:
sourceClass - a String
<br>sourceMethod - a String
<br>thrown - a Throwable

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=throwing&unscoped_q=throwing">[search for examples]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

***
<a name="warning"></a>
# warning
warning( String msg ) &rarr; void



### Parameters:
msg - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=warning&unscoped_q=warning">[search for examples]</a>

