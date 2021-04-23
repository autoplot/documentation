# org.autoplot.datasource.AutoplotSettingsAutoplot's settings, stored in Java preferences, include
 things like the last folder opened.  Also this code handles
 property resolution like ${HOME}/autoplot_data.
***
<a name="PREF_LAST_OPEN_FOLDER"></a>
# PREF_LAST_OPEN_FOLDER



***
<a name="PREF_RECENTLY_OPENED_FILES"></a>
# PREF_RECENTLY_OPENED_FILES



***
<a name="PREF_LAST_OPEN_VAP_FOLDER"></a>
# PREF_LAST_OPEN_VAP_FOLDER



***
<a name="PREF_LAST_OPEN_VAP_FILE"></a>
# PREF_LAST_OPEN_VAP_FILE



***
<a name="PROP_AUTOPLOTDATA"></a>
# PROP_AUTOPLOTDATA



***
<a name="PROP_FSCACHE"></a>
# PROP_FSCACHE



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

***
<a name="getAutoplotData"></a>
# getAutoplotData
getAutoplotData(  ) &rarr; String

return the location where Autoplot is storing its data.  This
 includes bookmarks, history, and the file cache, and 
 is typically "${HOME}/autoplot_data"

### Returns:
the user's Autoplot data folder.

<a href="https://github.com/autoplot/dev/search?q=getAutoplotData&unscoped_q=getAutoplotData">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFscache"></a>
# getFscache
getFscache(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getFscache&unscoped_q=getFscache">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPreferences"></a>
# getPreferences
getPreferences( java.lang.Class c ) &rarr; Preferences

wrapper that will handle legacy (v2016a) prefs, and will allow migration
 to ~/autoplot_data/config area.

### Parameters:
c - the class requesting preferences.

### Returns:
the preferences object this class should use.

<a href="https://github.com/autoplot/dev/search?q=getPreferences&unscoped_q=getPreferences">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="loadPreferences"></a>
# loadPreferences
loadPreferences(  ) &rarr; void

load the preferences,
 which include the location of the autoplot_data directory and fscache.
 The system property AUTOPLOT_DATA will override the user preference 
 autoplotData which is by default "${HOME}/autoplot_data", and
 can be set on the command line.  The environment variable AUTOPLOT_DATA
 will also override the default location.
 AUTOPLOT_FSCACHE is the location of the remote
 file mirror storing lots of data and can be moved separately.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=loadPreferences&unscoped_q=loadPreferences">[search for examples]</a>

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

***
<a name="resolveProperty"></a>
# resolveProperty
resolveProperty( String name ) &rarr; String

resolve the property, resolving references.  For example, ${HOME} 
 is replaced with System.getProperty("user.home").

### Parameters:
name - the name to resolve, such as PROP_AUTOPLOTDATA or PROP_FSCACHE

### Returns:
the value with references resolved.
 TODO: this should always make result end in slash...

<a href="https://github.com/autoplot/dev/search?q=resolveProperty&unscoped_q=resolveProperty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFscache"></a>
# setFscache
setFscache( String val ) &rarr; void



### Parameters:
val - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFscache&unscoped_q=setFscache">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="settings"></a>
# settings
settings(  ) &rarr; AutoplotSettings



### Returns:
org.autoplot.datasource.AutoplotSettings


<a href="https://github.com/autoplot/dev/search?q=settings&unscoped_q=settings">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

