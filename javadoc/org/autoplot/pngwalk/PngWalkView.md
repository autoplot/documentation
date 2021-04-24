# org.autoplot.pngwalk.PngWalkView

This is the abstract superclass for views in the PNGWalk tool.  Concrete
 subclasses will do the work of actually laying out a particular view and
 handling events on it.

***
<a name="PROP_THUMBNAILSIZE"></a>
# PROP_THUMBNAILSIZE



***
<a name="getMouseTarget"></a>
# getMouseTarget
getMouseTarget(  ) &rarr; JComponent

return the component that will generate mouse events.  Some
 components have a JScrollPane, so simply adding a listener to the 
 PngWalkView doesn't work.  The base class implementation of this 
 simply returns the PngWalkView, but such components should override
 this method.

### Returns:
a javax.swing.JComponent


<a href="https://github.com/autoplot/dev/search?q=getMouseTarget&unscoped_q=getMouseTarget">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMouseWheelListener"></a>
# getMouseWheelListener
getMouseWheelListener(  ) &rarr; MouseWheelListener

return the mouse wheel listener, which should be added to each panel so the sequence position is easily adjusted.

### Returns:
a java.awt.event.MouseWheelListener


<a href="https://github.com/autoplot/dev/search?q=getMouseWheelListener&unscoped_q=getMouseWheelListener">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPopup"></a>
# getPopup
getPopup(  ) &rarr; JPopupMenu



### Returns:
javax.swing.JPopupMenu


<a href="https://github.com/autoplot/dev/search?q=getPopup&unscoped_q=getPopup">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSequence"></a>
# getSequence
getSequence(  ) &rarr; WalkImageSequence



### Returns:
org.autoplot.pngwalk.WalkImageSequence


<a href="https://github.com/autoplot/dev/search?q=getSequence&unscoped_q=getSequence">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getThumbnailSize"></a>
# getThumbnailSize
getThumbnailSize(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getThumbnailSize&unscoped_q=getThumbnailSize">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isShowCaptions"></a>
# isShowCaptions
isShowCaptions(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isShowCaptions&unscoped_q=isShowCaptions">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="propertyChange"></a>
# propertyChange
propertyChange( java.beans.PropertyChangeEvent e ) &rarr; void

Respond to property changes on the {@list WalkImageSequence} this view
 represents.  The default implementation just calls <code>repaint()</code>,
 (or <code>sequencChanged()</code> if appropriate) but subclasses may override.

### Parameters:
e - a PropertyChangeEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=propertyChange&unscoped_q=propertyChange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSequence"></a>
# setSequence
setSequence( org.autoplot.pngwalk.WalkImageSequence sequence ) &rarr; void



### Parameters:
sequence - a WalkImageSequence

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSequence&unscoped_q=setSequence">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setShowCaptions"></a>
# setShowCaptions
setShowCaptions( boolean showCaptions ) &rarr; void



### Parameters:
showCaptions - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setShowCaptions&unscoped_q=setShowCaptions">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setThumbnailSize"></a>
# setThumbnailSize
setThumbnailSize( int thumbnailSize ) &rarr; void



### Parameters:
thumbnailSize - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setThumbnailSize&unscoped_q=setThumbnailSize">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

