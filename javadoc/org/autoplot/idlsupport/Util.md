# org.autoplot.idlsupport.Util



# Util( )
normally a Util class is just a bunch of static methods, but its easier
 to get at the methods if we can create an instance.

***
<a name="enterEditor"></a>
# enterEditor
enterEditor( String uri ) &rarr; String

bring up the editor for this URI, or partial URI (vap+cdaweb:).  This
 was introduced to test Java GUIs in IDL.

### Parameters:
uri - a String

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=enterEditor&unscoped_q=enterEditor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDiscoverySources"></a>
# getDiscoverySources
getDiscoverySources(  ) &rarr; String

return an array of the sources that can be discovered.

### Returns:
an array of the sources that can be discovered.

<a href="https://github.com/autoplot/dev/search?q=getDiscoverySources&unscoped_q=getDiscoverySources">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlugins"></a>
# getPlugins
getPlugins(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getPlugins&unscoped_q=getPlugins">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getVersions"></a>
# getVersions
getVersions(  ) &rarr; String

In IDL, you would say:
 <code>Util= OBJ_NEW('IDLJavaObject$Static$Util', 'org.autoplot.idlsupport.Util')
 print, Util.getVersions()
 </code>

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getVersions&unscoped_q=getVersions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isMap"></a>
# isMap
isMap( Object o ) &rarr; boolean



### Parameters:
o - an Object

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isMap&unscoped_q=isMap">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isQDataSet"></a>
# isQDataSet
isQDataSet( Object o ) &rarr; boolean



### Parameters:
o - an Object

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isQDataSet&unscoped_q=isQDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="silenceLoggers"></a>
# silenceLoggers
silenceLoggers(  ) &rarr; void

Jared at Iowa was having the problem that loggers were on by default.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=silenceLoggers&unscoped_q=silenceLoggers">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="verboseLoggers"></a>
# verboseLoggers
verboseLoggers(  ) &rarr; void

Jared at Iowa was having the problem that loggers were on by default.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=verboseLoggers&unscoped_q=verboseLoggers">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

