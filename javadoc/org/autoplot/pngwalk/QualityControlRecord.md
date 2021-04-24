# org.autoplot.pngwalk.QualityControlRecord



***
<a name="PROP_STATUS"></a>
# PROP_STATUS



***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void



### Parameters:
l - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCommentsHTML"></a>
# getCommentsHTML
getCommentsHTML(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getCommentsHTML&unscoped_q=getCommentsHTML">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getImageURI"></a>
# getImageURI
getImageURI(  ) &rarr; URI



### Returns:
java.net.URI


<a href="https://github.com/autoplot/dev/search?q=getImageURI&unscoped_q=getImageURI">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLastComment"></a>
# getLastComment
getLastComment(  ) &rarr; String

return the last comment.

### Returns:
the last comment, or "" if no comments have been added.

<a href="https://github.com/autoplot/dev/search?q=getLastComment&unscoped_q=getLastComment">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNewCommentText"></a>
# getNewCommentText
getNewCommentText(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getNewCommentText&unscoped_q=getNewCommentText">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRecord"></a>
# getRecord
getRecord( java.net.URI imageURI ) &rarr; QualityControlRecord

Retrieve the quality control record for the named pngwalk image.  It is assumed that
 the previously saved record, if there is one, exists in the same folder as the image.  If
 a saved record is not found, a new one will be created.

### Parameters:
imageURI - an URI

### Returns:
an org.autoplot.pngwalk.QualityControlRecord


<a href="https://github.com/autoplot/dev/search?q=getRecord&unscoped_q=getRecord">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getRecord( java.net.URI imageURI, java.net.URI qcFolder ) &rarr; QualityControlRecord<br>
***
<a name="getStatus"></a>
# getStatus
getStatus(  ) &rarr; Status



### Returns:
org.autoplot.pngwalk.QualityControlRecord.Status


<a href="https://github.com/autoplot/dev/search?q=getStatus&unscoped_q=getStatus">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void



### Parameters:
l - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="save"></a>
# save
save(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=save&unscoped_q=save">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setNewCommentText"></a>
# setNewCommentText
setNewCommentText( String reviewer, String commentText ) &rarr; void

Set the "new" commentText on this record.  This commentText will be appended to the existing
 list of comments when the record is written.

### Parameters:
reviewer - a String
<br>commentText - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setNewCommentText&unscoped_q=setNewCommentText">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setStatus"></a>
# setStatus
setStatus( org.autoplot.pngwalk.QualityControlRecord.Status newStatus ) &rarr; void



### Parameters:
newStatus - a QualityControlRecord.Status

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setStatus&unscoped_q=setStatus">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

