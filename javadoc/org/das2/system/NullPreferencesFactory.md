# org.das2.system.NullPreferencesFactory

Creates NullPreferences for use with applets.  The system property 
 java.util.prefs.PreferencesFactory should be set to
 org.das2.system.NullPreferencesFactory to use this class.
 
 System.setProperty( "java.util.prefs.PreferencesFactory", "org.das2.system.NullPreferencesFactory" ) doesn't
 work in applets--security exception.

 Also this works: java  -Djava.util.prefs.PreferencesFactory=org.das2.system.NullPreferencesFactory ...
 
 I'm not sure where I found this solution originally, but here is a nice writeup:
     http://www.allaboutbalance.com/articles/disableprefs/

# NullPreferencesFactory( )


***
<a name="systemRoot"></a>
# systemRoot
systemRoot(  ) &rarr; Preferences



### Returns:
java.util.prefs.Preferences


<a href="https://github.com/autoplot/dev/search?q=systemRoot&unscoped_q=systemRoot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="userRoot"></a>
# userRoot
userRoot(  ) &rarr; Preferences



### Returns:
java.util.prefs.Preferences


<a href="https://github.com/autoplot/dev/search?q=userRoot&unscoped_q=userRoot">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

