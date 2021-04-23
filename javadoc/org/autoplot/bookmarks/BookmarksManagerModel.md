# org.autoplot.bookmarks.BookmarksManagerModel

Internal model for managing a set of bookmarks.

# BookmarksManagerModel( )


***
<a name="PROP_LIST"></a>
# PROP_LIST



***
<a name="PROP_BOOKMARK"></a>
# PROP_BOOKMARK

the contents of a bookmark changed, like the title or URL.

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
<a name="addRemoteBookmarks"></a>
# addRemoteBookmarks
addRemoteBookmarks( String surl ) &rarr; void

add the bookmarks in the remote URL to the list.

### Parameters:
surl - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addRemoteBookmarks&unscoped_q=addRemoteBookmarks">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addRemoteBookmarks( String surl, org.autoplot.bookmarks.Bookmark selectedBookmark ) &rarr; void<br>
***
<a name="getList"></a>
# getList
getList(  ) &rarr; List

get the bookmarks as a list.  This is a mutable copy of the internal list.

### Returns:
the list of bookmarks.

<a href="https://github.com/autoplot/dev/search?q=getList&unscoped_q=getList">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTreeModel"></a>
# getTreeModel
getTreeModel(  ) &rarr; TreeModel

get a TreeModel of the internal model, so GUIs can show the state.

### Returns:
a TreeModel.

<a href="https://github.com/autoplot/dev/search?q=getTreeModel&unscoped_q=getTreeModel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="importList"></a>
# importList
importList( java.util.List books ) &rarr; void

merge the given list into the list.

### Parameters:
books - a java.util.List

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=importList&unscoped_q=importList">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mergeList"></a>
# mergeList
mergeList( java.util.List src, java.util.List dest ) &rarr; void

merge in the bookmarks.  Items with the same title are repeated, and
 folders with the same name are merged.  When merging in a remote folder,
 the entire folder is replaced.

### Parameters:
src - the items to merge in
<br>dest - the list to update.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mergeList&unscoped_q=mergeList">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
propertyName - a String
<br>listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

removePropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="setList"></a>
# setList
setList( java.util.List list ) &rarr; void

set the bookmarks list.  This is used as the internal list, without making a copy.

### Parameters:
list - list of bookmarks.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setList&unscoped_q=setList">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

