# org.autoplot.bookmarks.Bookmark.Folder



# Folder( String title )


# Folder( String title, String remoteUrl )


***
<a name="REMOTE_STATUS_NOT_LOADED"></a>
# REMOTE_STATUS_NOT_LOADED



***
<a name="REMOTE_STATUS_SUCCESSFUL"></a>
# REMOTE_STATUS_SUCCESSFUL



***
<a name="REMOTE_STATUS_UNSUCCESSFUL"></a>
# REMOTE_STATUS_UNSUCCESSFUL



***
<a name="copy"></a>
# copy
copy(  ) &rarr; Bookmark



### Returns:
org.autoplot.bookmarks.Bookmark


<a href="https://github.com/autoplot/dev/search?q=copy&unscoped_q=copy">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="equals"></a>
# equals
equals( Object obj ) &rarr; boolean



### Parameters:
obj - an Object

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=equals&unscoped_q=equals">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBookmarks"></a>
# getBookmarks
getBookmarks(  ) &rarr; List

return the bookmarks, the mutable internal store.  use copy() to
 get a deep copy.

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=getBookmarks&unscoped_q=getBookmarks">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRemoteStatus"></a>
# getRemoteStatus
getRemoteStatus(  ) &rarr; int

remote status indicator.
 -1 not loaded
 0 successful
 1 unsuccessful.

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getRemoteStatus&unscoped_q=getRemoteStatus">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRemoteStatusMsg"></a>
# getRemoteStatusMsg
getRemoteStatusMsg(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getRemoteStatusMsg&unscoped_q=getRemoteStatusMsg">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRemoteUrl"></a>
# getRemoteUrl
getRemoteUrl(  ) &rarr; String

a remote bookmark is one that is a copy of a folder at the remote
 location.  If it's a remote folder, then we use it to maintain the
 bookmarks.  We'll keep a local copy, but this may be updated.
 null indicates that this this a not a remote bookmark.

### Returns:
a URI or null.

<a href="https://github.com/autoplot/dev/search?q=getRemoteUrl&unscoped_q=getRemoteUrl">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hashCode"></a>
# hashCode
hashCode(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=hashCode&unscoped_q=hashCode">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRemoteStatus"></a>
# setRemoteStatus
setRemoteStatus( int status ) &rarr; void

set the remote status.

### Parameters:
status - the new status: -1 not loaded, 0 successful, 1 unsuccessful.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRemoteStatus&unscoped_q=setRemoteStatus">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRemoteStatusMsg"></a>
# setRemoteStatusMsg
setRemoteStatusMsg( String msg ) &rarr; void



### Parameters:
msg - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRemoteStatusMsg&unscoped_q=setRemoteStatusMsg">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRemoteUrl"></a>
# setRemoteUrl
setRemoteUrl( String url ) &rarr; void

set this to the location of the master copy of the bookmarks, or null.

### Parameters:
url - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRemoteUrl&unscoped_q=setRemoteUrl">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

