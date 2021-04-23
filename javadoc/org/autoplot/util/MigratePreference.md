# org.autoplot.util.MigratePreferenceThis allows a legacy preference to be used alongside a new preference,
 keeping the users preferences.
MigratePreference( java.util.prefs.Preferences p1, java.util.prefs.Preferences p2 )
create a new where preferences are first read from p1 and if not found 
 there the data is read from from p2 (and if not found there then the
 default is used.  When writing a preference, a copy is made to both
 p1 and p2.

***
<a name="absolutePath"></a>
# absolutePath
absolutePath(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=absolutePath&unscoped_q=absolutePath">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addNodeChangeListener"></a>
# addNodeChangeListener
addNodeChangeListener( java.util.prefs.NodeChangeListener ncl ) &rarr; void



### Parameters:
ncl - a NodeChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addNodeChangeListener&unscoped_q=addNodeChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addPreferenceChangeListener"></a>
# addPreferenceChangeListener
addPreferenceChangeListener( java.util.prefs.PreferenceChangeListener pcl ) &rarr; void



### Parameters:
pcl - a PreferenceChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPreferenceChangeListener&unscoped_q=addPreferenceChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="childrenNames"></a>
# childrenNames
childrenNames(  ) &rarr; String



### Returns:
java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=childrenNames&unscoped_q=childrenNames">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="clear"></a>
# clear
clear(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=clear&unscoped_q=clear">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="exportNode"></a>
# exportNode
exportNode( java.io.OutputStream os ) &rarr; void



### Parameters:
os - an OutputStream

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=exportNode&unscoped_q=exportNode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="exportSubtree"></a>
# exportSubtree
exportSubtree( java.io.OutputStream os ) &rarr; void



### Parameters:
os - an OutputStream

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=exportSubtree&unscoped_q=exportSubtree">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="flush"></a>
# flush
flush(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=flush&unscoped_q=flush">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="get"></a>
# get
get( String key, String def ) &rarr; String



### Parameters:
key - a String
<br>def - a String

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=get&unscoped_q=get">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBoolean"></a>
# getBoolean
getBoolean( String key, boolean def ) &rarr; boolean



### Parameters:
key - a String
<br>def - a boolean

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=getBoolean&unscoped_q=getBoolean">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getByteArray"></a>
# getByteArray
getByteArray( String key, byte[] def ) &rarr; byte



### Parameters:
key - a String
<br>def - a byte[]

### Returns:
byte[]


<a href="https://github.com/autoplot/dev/search?q=getByteArray&unscoped_q=getByteArray">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDouble"></a>
# getDouble
getDouble( String key, double def ) &rarr; double



### Parameters:
key - a String
<br>def - a double

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=getDouble&unscoped_q=getDouble">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFloat"></a>
# getFloat
getFloat( String key, float def ) &rarr; float



### Parameters:
key - a String
<br>def - a float

### Returns:
float


<a href="https://github.com/autoplot/dev/search?q=getFloat&unscoped_q=getFloat">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInt"></a>
# getInt
getInt( String key, int def ) &rarr; int



### Parameters:
key - a String
<br>def - an int

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getInt&unscoped_q=getInt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLong"></a>
# getLong
getLong( String key, long def ) &rarr; long



### Parameters:
key - a String
<br>def - a long

### Returns:
long


<a href="https://github.com/autoplot/dev/search?q=getLong&unscoped_q=getLong">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isUserNode"></a>
# isUserNode
isUserNode(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isUserNode&unscoped_q=isUserNode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="keys"></a>
# keys
keys(  ) &rarr; String



### Returns:
java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=keys&unscoped_q=keys">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="name"></a>
# name
name(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=name&unscoped_q=name">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="node"></a>
# node
node( String pathName ) &rarr; Preferences



### Parameters:
pathName - a String

### Returns:
java.util.prefs.Preferences


<a href="https://github.com/autoplot/dev/search?q=node&unscoped_q=node">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="nodeExists"></a>
# nodeExists
nodeExists( String pathName ) &rarr; boolean



### Parameters:
pathName - a String

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=nodeExists&unscoped_q=nodeExists">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parent"></a>
# parent
parent(  ) &rarr; Preferences



### Returns:
java.util.prefs.Preferences


<a href="https://github.com/autoplot/dev/search?q=parent&unscoped_q=parent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="put"></a>
# put
put( String key, String value ) &rarr; void



### Parameters:
key - a String
<br>value - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=put&unscoped_q=put">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putBoolean"></a>
# putBoolean
putBoolean( String key, boolean value ) &rarr; void



### Parameters:
key - a String
<br>value - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putBoolean&unscoped_q=putBoolean">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putByteArray"></a>
# putByteArray
putByteArray( String key, byte[] value ) &rarr; void



### Parameters:
key - a String
<br>value - a byte[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putByteArray&unscoped_q=putByteArray">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putDouble"></a>
# putDouble
putDouble( String key, double value ) &rarr; void



### Parameters:
key - a String
<br>value - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putDouble&unscoped_q=putDouble">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putFloat"></a>
# putFloat
putFloat( String key, float value ) &rarr; void



### Parameters:
key - a String
<br>value - a float

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putFloat&unscoped_q=putFloat">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putInt"></a>
# putInt
putInt( String key, int value ) &rarr; void



### Parameters:
key - a String
<br>value - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putInt&unscoped_q=putInt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putLong"></a>
# putLong
putLong( String key, long value ) &rarr; void



### Parameters:
key - a String
<br>value - a long

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putLong&unscoped_q=putLong">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="remove"></a>
# remove
remove( String key ) &rarr; void



### Parameters:
key - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=remove&unscoped_q=remove">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeNode"></a>
# removeNode
removeNode(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeNode&unscoped_q=removeNode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeNodeChangeListener"></a>
# removeNodeChangeListener
removeNodeChangeListener( java.util.prefs.NodeChangeListener ncl ) &rarr; void



### Parameters:
ncl - a NodeChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeNodeChangeListener&unscoped_q=removeNodeChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePreferenceChangeListener"></a>
# removePreferenceChangeListener
removePreferenceChangeListener( java.util.prefs.PreferenceChangeListener pcl ) &rarr; void



### Parameters:
pcl - a PreferenceChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePreferenceChangeListener&unscoped_q=removePreferenceChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="sync"></a>
# sync
sync(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=sync&unscoped_q=sync">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

