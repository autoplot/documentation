# org.autoplot.bookmarks.BookmarksManagerObject for managing the user's bookmarks.  This object sits quietly beside the Autoplot
 UI, becoming visible when the user asks to manage bookmarks.  This also populates the Bookmarks
 submenu.
BookmarksManager( java.awt.Frame parent, boolean modal )
creates new BookmarksManager.  Use

BookmarksManager( java.awt.Frame parent, boolean modal, String name )
Creates new BookmarksManager

***
<a name="addBookmark"></a>
# addBookmark
addBookmark( String surl ) &rarr; Bookmark



### Parameters:
surl - a String

### Returns:
org.autoplot.bookmarks.Bookmark


<a href="https://github.com/autoplot/dev/search?q=addBookmark&unscoped_q=addBookmark">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="findBookmarkByUri"></a>
# findBookmarkByUri
findBookmarkByUri( java.util.List list, String bookmarkURI, int remoteLimit ) &rarr; Bookmark

return the first bookmark with the URI that matches the bookmarkURI.  This is introduced
 to allow the tools bookmarks to be a set of trusted bookmarks.  
 
 See https://sourceforge.net/p/autoplot/bugs/1270/

### Parameters:
list - bookmarks list, such as manager.getList();
<br>bookmarkURI - the URI to find.
<br>remoteLimit - the number of times we can look at remote files.

### Returns:
null if the bookmark is not found.

<a href="https://github.com/autoplot/dev/search?q=findBookmarkByUri&unscoped_q=findBookmarkByUri">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getModel"></a>
# getModel
getModel(  ) &rarr; BookmarksManagerModel



### Returns:
org.autoplot.bookmarks.BookmarksManagerModel


<a href="https://github.com/autoplot/dev/search?q=getModel&unscoped_q=getModel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSelectedBookmark"></a>
# getSelectedBookmark
getSelectedBookmark(  ) &rarr; Bookmark

provide a means to get the selection.

### Returns:
the selected bookmark

<a href="https://github.com/autoplot/dev/search?q=getSelectedBookmark&unscoped_q=getSelectedBookmark">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasPrefNode"></a>
# hasPrefNode
hasPrefNode( String nodeName ) &rarr; boolean

returns true if the preference node exists.

### Parameters:
nodeName - a String

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=hasPrefNode&unscoped_q=hasPrefNode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="haveRemoteBookmark"></a>
# haveRemoteBookmark
haveRemoteBookmark( String bookmarksFile ) &rarr; boolean

return true if we are already using the remote bookmark, marked as a remote bookmark,
 at the root level.

### Parameters:
bookmarksFile - a String

### Returns:
true if we already have the bookmark.

<a href="https://github.com/autoplot/dev/search?q=haveRemoteBookmark&unscoped_q=haveRemoteBookmark">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isEdit"></a>
# isEdit
isEdit(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isEdit&unscoped_q=isEdit">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isPlay"></a>
# isPlay
isPlay(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isPlay&unscoped_q=isPlay">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="printBooks"></a>
# printBooks
printBooks( java.util.List book, String indent ) &rarr; void



### Parameters:
book - a java.util.List
<br>indent - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=printBooks&unscoped_q=printBooks">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

printBooks( org.autoplot.bookmarks.Bookmark book, String indent ) &rarr; void<br>
***
<a name="reload"></a>
# reload
reload(  ) &rarr; void

reload the bookmarks from disk.  Remote bookmarks will be reloaded slightly later.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reload&unscoped_q=reload">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resetPrefNode"></a>
# resetPrefNode
resetPrefNode( String nodeName ) &rarr; void

rename the pref node, to aid with version changes.  E.g. convert autoplot.xml to bookmarks.xml

### Parameters:
nodeName - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resetPrefNode&unscoped_q=resetPrefNode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resetToDefault"></a>
# resetToDefault
resetToDefault( String surl ) &rarr; void



### Parameters:
surl - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resetToDefault&unscoped_q=resetToDefault">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAddBookmark"></a>
# setAddBookmark
setAddBookmark( org.autoplot.bookmarks.Bookmark b ) &rarr; void



### Parameters:
b - a Bookmark

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAddBookmark&unscoped_q=setAddBookmark">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setHidePlotButtons"></a>
# setHidePlotButtons
setHidePlotButtons( boolean b ) &rarr; void



### Parameters:
b - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setHidePlotButtons&unscoped_q=setHidePlotButtons">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPlotActionsVisible"></a>
# setPlotActionsVisible
setPlotActionsVisible( boolean v ) &rarr; void

Hide the plot and edit buttons, because sometimes they are confusing.  For example
 we click "add bookmark" because we have a plot we want to keep.  It wouldn't 
 make sense for this editor to offer plot as an action because we have it
 plotted already.

### Parameters:
v - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPlotActionsVisible&unscoped_q=setPlotActionsVisible">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPrefNode"></a>
# setPrefNode
setPrefNode( String nodeName, String propName, String deft ) &rarr; void

setting this makes this manager the authority on bookmarks.  For example, 
<blockquote><pre><small>
 man.setPrefNode( "bookmarks", "autoplot.default.bookmarks",  "http://autoplot.org/data/bookmarks.xml" );
</small></pre></blockquote>

### Parameters:
nodeName - the name for the set of bookmarks.
<br>propName - property containing the URL for the default bookmarks
<br>deft - value to use if the propName has not been set.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPrefNode&unscoped_q=setPrefNode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

setPrefNode( String nodeName ) &rarr; void<br>
***
<a name="updateBookmarks"></a>
# updateBookmarks
updateBookmarks( javax.swing.JMenu bookmarksMenu, org.autoplot.datasource.DataSetSelector dataSetSelector ) &rarr; void

add the bookmarks to the JMenu.

### Parameters:
bookmarksMenu - a JMenu
<br>dataSetSelector - a DataSetSelector

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=updateBookmarks&unscoped_q=updateBookmarks">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

updateBookmarks( javax.swing.JMenu bookmarksMenu, org.autoplot.AutoplotUI app, org.autoplot.datasource.DataSetSelector dataSetSelector ) &rarr; void<br>
updateBookmarks( javax.swing.JMenu bookmarksMenu, String afterName, org.autoplot.AutoplotUI app, org.autoplot.datasource.DataSetSelector dataSetSelector ) &rarr; void<br>
