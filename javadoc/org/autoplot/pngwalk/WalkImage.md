# org.autoplot.pngwalk.WalkImageA class to manage an image for the PNGWalk tool. Handles downloading and
 thumbnail generation.
WalkImage( java.net.URI uri, boolean haveThumbs400 )


***
<a name="PROP_STATUS_CHANGE"></a>
# PROP_STATUS_CHANGE



***
<a name="PROP_BADGE_CHANGE"></a>
# PROP_BADGE_CHANGE



***
<a name="THUMB_SIZE"></a>
# THUMB_SIZE



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

***
<a name="getCaption"></a>
# getCaption
getCaption(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getCaption&unscoped_q=getCaption">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDatumRange"></a>
# getDatumRange
getDatumRange(  ) &rarr; DatumRange



### Returns:
org.das2.datum.DatumRange


<a href="https://github.com/autoplot/dev/search?q=getDatumRange&unscoped_q=getDatumRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getImage"></a>
# getImage
getImage(  ) &rarr; BufferedImage

return the image, or the missing image should the image be missing.

### Returns:
a java.awt.image.BufferedImage


<a href="https://github.com/autoplot/dev/search?q=getImage&unscoped_q=getImage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInitLoadBirthTime"></a>
# getInitLoadBirthTime
getInitLoadBirthTime(  ) &rarr; long

get the time that the image load was triggered.

### Returns:
the time in millis, to be compared to System.currentTimeMillis.

<a href="https://github.com/autoplot/dev/search?q=getInitLoadBirthTime&unscoped_q=getInitLoadBirthTime">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSquishedThumbnail"></a>
# getSquishedThumbnail
getSquishedThumbnail(  ) &rarr; BufferedImage



### Returns:
java.awt.image.BufferedImage


<a href="https://github.com/autoplot/dev/search?q=getSquishedThumbnail&unscoped_q=getSquishedThumbnail">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getSquishedThumbnail( boolean loadIfNeeded ) &rarr; BufferedImage<br>
***
<a name="getStatus"></a>
# getStatus
getStatus(  ) &rarr; Status



### Returns:
org.autoplot.pngwalk.WalkImage.Status


<a href="https://github.com/autoplot/dev/search?q=getStatus&unscoped_q=getStatus">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getThumbnail"></a>
# getThumbnail
getThumbnail(  ) &rarr; BufferedImage



### Returns:
java.awt.image.BufferedImage


<a href="https://github.com/autoplot/dev/search?q=getThumbnail&unscoped_q=getThumbnail">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getThumbnail( int w, int h, boolean waitOk ) &rarr; BufferedImage<br>
getThumbnail( boolean loadIfNeeded ) &rarr; BufferedImage<br>
***
<a name="getThumbnailDimension"></a>
# getThumbnailDimension
getThumbnailDimension( boolean loadIfNeeded ) &rarr; Dimension



### Parameters:
loadIfNeeded - a boolean

### Returns:
java.awt.Dimension


<a href="https://github.com/autoplot/dev/search?q=getThumbnailDimension&unscoped_q=getThumbnailDimension">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getThumbnailImmediately"></a>
# getThumbnailImmediately
getThumbnailImmediately(  ) &rarr; void

attempt to create the thumbnail on the current thread.  If there is no
 "thumbs400" directory and the image is not yet loaded, then no
 action takes place.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=getThumbnailImmediately&unscoped_q=getThumbnailImmediately">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getUri"></a>
# getUri
getUri(  ) &rarr; URI



### Returns:
java.net.URI


<a href="https://github.com/autoplot/dev/search?q=getUri&unscoped_q=getUri">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readImage"></a>
# readImage
readImage( java.io.File f ) &rarr; BufferedImage

return a file, that is never type=0.  This was a bug on Windows.

### Parameters:
f - a File

### Returns:
a java.awt.image.BufferedImage


<a href="https://github.com/autoplot/dev/search?q=readImage&unscoped_q=readImage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rotateImage"></a>
# rotateImage
rotateImage( java.awt.image.BufferedImage img, int angle ) &rarr; BufferedImage

rotate an image, unlike the rotate found in ImageDataSource, this will
 resize the image when the rotation is 90 degrees.

### Parameters:
img - the image
<br>angle - the angle to rotate clockwise, in degrees.

### Returns:
the rotated image.

<a href="https://github.com/autoplot/dev/search?q=rotateImage&unscoped_q=rotateImage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setCaption"></a>
# setCaption
setCaption( String caption ) &rarr; void



### Parameters:
caption - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCaption&unscoped_q=setCaption">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDatumRange"></a>
# setDatumRange
setDatumRange( DatumRange dr ) &rarr; void



### Parameters:
dr - a DatumRange

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDatumRange&unscoped_q=setDatumRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="waitForImage"></a>
# waitForImage
waitForImage(  ) &rarr; BufferedImage

contain logic which will wait for the image to load.

### Returns:
the image, or missingImage.

<a href="https://github.com/autoplot/dev/search?q=waitForImage&unscoped_q=waitForImage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

