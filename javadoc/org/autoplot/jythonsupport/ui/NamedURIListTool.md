# org.autoplot.jythonsupport.ui.NamedURIListToolGUI for creating a list of URIs and variables associated with them.
NamedURIListTool( )


***
<a name="PROP_TIMERANGE"></a>
# PROP_TIMERANGE



***
<a name="PROP_SHOWIDS"></a>
# PROP_SHOWIDS



***
<a name="getIds"></a>
# getIds
getIds(  ) &rarr; String

return the id for each URI.

### Returns:
the ids

<a href="https://github.com/autoplot/dev/search?q=getIds&unscoped_q=getIds">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTimeRange"></a>
# getTimeRange
getTimeRange(  ) &rarr; DatumRange



### Returns:
org.das2.datum.DatumRange


<a href="https://github.com/autoplot/dev/search?q=getTimeRange&unscoped_q=getTimeRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getUriForId"></a>
# getUriForId
getUriForId( String name ) &rarr; String

return the URI for the name, something that when resolved will result in
 the dataset.

### Parameters:
name - a String

### Returns:
the URI or null if the name is not found.

<a href="https://github.com/autoplot/dev/search?q=getUriForId&unscoped_q=getUriForId">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getUris"></a>
# getUris
getUris(  ) &rarr; String

return the uris.

### Returns:
the uris.

<a href="https://github.com/autoplot/dev/search?q=getUris&unscoped_q=getUris">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isShowIds"></a>
# isShowIds
isShowIds(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isShowIds&unscoped_q=isShowIds">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="makeupName"></a>
# makeupName
makeupName( java.util.List names ) &rarr; String

make up a name that does not exist in the list of names.

### Parameters:
names - names that must be unique with the new name

### Returns:
the new name

<a href="https://github.com/autoplot/dev/search?q=makeupName&unscoped_q=makeupName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="refresh"></a>
# refresh
refresh(  ) &rarr; void

rebuild the GUI based on the uris.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=refresh&unscoped_q=refresh">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="selectDataId"></a>
# selectDataId
selectDataId( String id ) &rarr; String

return null if nothing is selected, the URI otherwise.

### Parameters:
id - the current selection, which can be an identifier, QDataSet.UNITS, or 10.0.

### Returns:
null if nothing is selected, the URI otherwise.

<a href="https://github.com/autoplot/dev/search?q=selectDataId&unscoped_q=selectDataId">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataMashUp"></a>
# setDataMashUp
setDataMashUp( org.autoplot.jythonsupport.ui.DataMashUp dmu ) &rarr; void

set the DataMashUp tool so we can handle variable rename.

### Parameters:
dmu - a DataMashUp

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataMashUp&unscoped_q=setDataMashUp">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setIds"></a>
# setIds
setIds( java.util.List ids ) &rarr; void

set the ids, where these should be one ID for each URI.  When there
 are the same number of URIs and IDs, refresh is called.

### Parameters:
ids - a java.util.List

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setIds&unscoped_q=setIds">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setIsAuto"></a>
# setIsAuto
setIsAuto( java.util.List isAuto ) &rarr; void

set the automatic renaming flag for each ID.   When there
 are the same number as URIs and IDs, refresh is called.

### Parameters:
isAuto - a java.util.List

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setIsAuto&unscoped_q=setIsAuto">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setShowIds"></a>
# setShowIds
setShowIds( boolean showIds ) &rarr; void



### Parameters:
showIds - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setShowIds&unscoped_q=setShowIds">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTimeRange"></a>
# setTimeRange
setTimeRange( DatumRange timeRange ) &rarr; void



### Parameters:
timeRange - a DatumRange

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTimeRange&unscoped_q=setTimeRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setUris"></a>
# setUris
setUris( java.util.List uris ) &rarr; void

set the URIs, where there should be one for each ID.  When there
 are the same number of URIs and IDs, refresh is called.

### Parameters:
uris - a java.util.List

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUris&unscoped_q=setUris">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

