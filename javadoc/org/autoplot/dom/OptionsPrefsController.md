# org.autoplot.dom.OptionsPrefsController

listen to an Options class and manage storage and retrieval from persistent
 storage.

# OptionsPrefsController( org.autoplot.ApplicationModel model, org.autoplot.dom.Options options )
create a new controller with preferences for the options class.

***
<a name="PROP_LOADPERSISTENTPREFERENCES"></a>
# PROP_LOADPERSISTENTPREFERENCES



***
<a name="copyOptionsToPersistentPreferences"></a>
# copyOptionsToPersistentPreferences
copyOptionsToPersistentPreferences(  ) &rarr; void

write the current options out to persistent preferences, so that they will
 be used next session.  Note the persistent preferences is a Java Preference
 stored in ~/.java/... but it is being migrated to
 AUTOPLOT_DATA/config/options.preferences.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=copyOptionsToPersistentPreferences&unscoped_q=copyOptionsToPersistentPreferences">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isLoadPersistentPreferences"></a>
# isLoadPersistentPreferences
isLoadPersistentPreferences(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isLoadPersistentPreferences&unscoped_q=isLoadPersistentPreferences">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="loadPreferences"></a>
# loadPreferences
loadPreferences(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=loadPreferences&unscoped_q=loadPreferences">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="loadPreferencesWithEvents"></a>
# loadPreferencesWithEvents
loadPreferencesWithEvents(  ) &rarr; void

load the preferences which persist between sessions into dom.options, 
 firing events as they are set.  Note for headless mode and non-application
 modes, this has no effect.

### Returns:
void (returns nothing)

### See Also:
<a href='#loadPreferences'>loadPreferences()</a> loadPreferences which does not fire events.<br>

<a href="https://github.com/autoplot/dev/search?q=loadPreferencesWithEvents&unscoped_q=loadPreferencesWithEvents">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLoadPersistentPreferences"></a>
# setLoadPersistentPreferences
setLoadPersistentPreferences( boolean loadPersistentPreferences ) &rarr; void



### Parameters:
loadPersistentPreferences - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLoadPersistentPreferences&unscoped_q=setLoadPersistentPreferences">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

