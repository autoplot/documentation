# org.autoplot.bookmarks.Bookmark

Internal representation of a Bookmark, containing an Autoplot URI, title, and additional documentation 
 for the URI.  This can also be a folder that contains a list of Bookmarks, or a remote folder that is controlled be
 a remote bookmarks file./

***
<a name="TITLE_ERROR_OCCURRED"></a>
# TITLE_ERROR_OCCURRED



***
<a name="MSG_NO_REMOTE"></a>
# MSG_NO_REMOTE



***
<a name="TOOLTIP_NO_REMOTE"></a>
# TOOLTIP_NO_REMOTE



***
<a name="MSG_REMOTE"></a>
# MSG_REMOTE



***
<a name="TOOLTIP_REMOTE"></a>
# TOOLTIP_REMOTE



***
<a name="MSG_NOT_LOADED"></a>
# MSG_NOT_LOADED



***
<a name="TOOLTIP_NOT_LOADED"></a>
# TOOLTIP_NOT_LOADED



***
<a name="REMOTE_BOOKMARK_DEPTH_LIMIT"></a>
# REMOTE_BOOKMARK_DEPTH_LIMIT

limit on the number of remote containing remote containing remote...

***
<a name="PROP_ICON"></a>
# PROP_ICON



***
<a name="PROP_PARENT"></a>
# PROP_PARENT



***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void

Adds a PropertyChangeListener to the listener list.

### Parameters:
l - The listener to add.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="copy"></a>
# copy
copy(  ) &rarr; Bookmark



### Returns:
org.autoplot.bookmarks.Bookmark


<a href="https://github.com/autoplot/dev/search?q=copy&unscoped_q=copy">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="formatBookmark"></a>
# formatBookmark
formatBookmark( org.w3c.dom.Document doc, org.w3c.dom.Element parent, org.autoplot.bookmarks.Bookmark bookmark ) &rarr; void



### Parameters:
doc - a Document
<br>parent - an Element
<br>bookmark - a Bookmark

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=formatBookmark&unscoped_q=formatBookmark">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

formatBookmark( org.autoplot.bookmarks.Bookmark bookmark ) &rarr; String<br>
***
<a name="formatBooks"></a>
# formatBooks
formatBooks( java.util.List bookmarks ) &rarr; String

format the bookmarks into xml for persistent storage.

### Parameters:
bookmarks - List of Bookmark.List or Bookmark

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=formatBooks&unscoped_q=formatBooks">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

formatBooks( java.io.OutputStream out, java.util.List bookmarks ) &rarr; void<br>
***
<a name="formatBooksOld"></a>
# formatBooksOld
formatBooksOld( java.util.List bookmarks ) &rarr; String

format the bookmarks into xml for persistent storage.

### Parameters:
bookmarks - List of Bookmark.List or Bookmark

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=formatBooksOld&unscoped_q=formatBooksOld">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDescription"></a>
# getDescription
getDescription(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getDescription&unscoped_q=getDescription">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDescriptionUrl"></a>
# getDescriptionUrl
getDescriptionUrl(  ) &rarr; URL

returns the URL, or null if one is not available.

### Returns:
a java.net.URL


<a href="https://github.com/autoplot/dev/search?q=getDescriptionUrl&unscoped_q=getDescriptionUrl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getIcon"></a>
# getIcon
getIcon(  ) &rarr; ImageIcon



### Returns:
javax.swing.ImageIcon


<a href="https://github.com/autoplot/dev/search?q=getIcon&unscoped_q=getIcon">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getId"></a>
# getId
getId(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getId&unscoped_q=getId">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getParent"></a>
# getParent
getParent(  ) &rarr; Folder



### Returns:
org.autoplot.bookmarks.Bookmark.Folder


<a href="https://github.com/autoplot/dev/search?q=getParent&unscoped_q=getParent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTitle"></a>
# getTitle
getTitle(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getTitle&unscoped_q=getTitle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isHidden"></a>
# isHidden
isHidden(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isHidden&unscoped_q=isHidden">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parseBookmark"></a>
# parseBookmark
parseBookmark( String data ) &rarr; Bookmark



### Parameters:
data - a String

### Returns:
an org.autoplot.bookmarks.Bookmark


<a href="https://github.com/autoplot/dev/search?q=parseBookmark&unscoped_q=parseBookmark">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

parseBookmark( org.w3c.dom.Node element, String vers, int remoteLevel ) &rarr; Bookmark<br>
***
<a name="parseBookmarks"></a>
# parseBookmarks
parseBookmarks( String data ) &rarr; List



### Parameters:
data - a String

### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=parseBookmarks&unscoped_q=parseBookmarks">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

parseBookmarks( String data, int depth ) &rarr; List<br>
parseBookmarks( java.net.URL url ) &rarr; List<br>
parseBookmarks( org.w3c.dom.Element root ) &rarr; List<br>
parseBookmarks( org.w3c.dom.Element root, int remoteLevel ) &rarr; List<br>
parseBookmarks( org.w3c.dom.Element root, String vers, int remoteLevel ) &rarr; List<br>
***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void

Removes a PropertyChangeListener from the listener list.

### Parameters:
l - The listener to remove.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDescription"></a>
# setDescription
setDescription( String description ) &rarr; void



### Parameters:
description - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDescription&unscoped_q=setDescription">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDescriptionUrl"></a>
# setDescriptionUrl
setDescriptionUrl( java.net.URL descriptionUrl ) &rarr; void



### Parameters:
descriptionUrl - an URL

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDescriptionUrl&unscoped_q=setDescriptionUrl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setHidden"></a>
# setHidden
setHidden( boolean hidden ) &rarr; void



### Parameters:
hidden - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setHidden&unscoped_q=setHidden">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setIcon"></a>
# setIcon
setIcon( javax.swing.ImageIcon icon ) &rarr; void



### Parameters:
icon - an ImageIcon

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setIcon&unscoped_q=setIcon">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setId"></a>
# setId
setId( String id ) &rarr; void



### Parameters:
id - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setId&unscoped_q=setId">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setParent"></a>
# setParent
setParent( org.autoplot.bookmarks.Bookmark.Folder parent ) &rarr; void



### Parameters:
parent - a Bookmark.Folder

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setParent&unscoped_q=setParent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTitle"></a>
# setTitle
setTitle( String title ) &rarr; void



### Parameters:
title - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTitle&unscoped_q=setTitle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

