# org.autoplot.pngwalk.WalkImageSequence<p>This class maintains a list of <code>WalkImage</code>s and provides functionality
 for navigating through it.  Whenever the current index is changed, whether explicitly
 set or via one of the navigation functions, a <code>PropertyChangeEvent</code> is fired.
 This allows UI code to control the index and view code to respond.</p>

 <p>Access is also provided to the {@link WalkImage} objects so that view
 code can retrieve images, thumbnails, etc.</p>
WalkImageSequence( String template )
Create an image sequence based on a URI template.

***
<a name="PROP_INDEX"></a>
# PROP_INDEX



***
<a name="PROP_SELECTED_INDECES"></a>
# PROP_SELECTED_INDECES



***
<a name="PROP_IMAGE_LOADED"></a>
# PROP_IMAGE_LOADED



***
<a name="PROP_THUMB_LOADED"></a>
# PROP_THUMB_LOADED



***
<a name="PROP_USESUBRANGE"></a>
# PROP_USESUBRANGE



***
<a name="PROP_SEQUENCE_CHANGED"></a>
# PROP_SEQUENCE_CHANGED



***
<a name="PROP_BADGE_CHANGE"></a>
# PROP_BADGE_CHANGE



***
<a name="PROP_TIMERANGE"></a>
# PROP_TIMERANGE



***
<a name="PROP_STATUS"></a>
# PROP_STATUS



***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void

things we fire events for:
   PROP_BADGE_CHANGE
   and others

### Parameters:
l - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

addPropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="currentImage"></a>
# currentImage
currentImage(  ) &rarr; WalkImage



### Returns:
org.autoplot.pngwalk.WalkImage


<a href="https://github.com/autoplot/dev/search?q=currentImage&unscoped_q=currentImage">[search for examples]</a>

***
<a name="findIndex"></a>
# findIndex
findIndex( String name ) &rarr; int

returns the index of the name, or -1 if the name is not found.  This is not the full 
 filename, but instead just the part of the name within the walk.  For example,
 For example if getTemplate is file:/tmp/$Y$m$d.gif, then the setSelectedName might be 20141111.gif.

### Parameters:
name - the file name.

### Returns:
the index, or -1 if the name is not found.

<a href="https://github.com/autoplot/dev/search?q=findIndex&unscoped_q=findIndex">[search for examples]</a>

***
<a name="first"></a>
# first
first(  ) &rarr; void

Move the index to the first image in the list.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=first&unscoped_q=first">[search for examples]</a>

***
<a name="getActiveSubrange"></a>
# getActiveSubrange
getActiveSubrange(  ) &rarr; List

return the active subrange of the sequence.  This is the portion of the pngwalk being used.

### Returns:
the subrange of the sequence.
### See Also:
<a href='https://sourceforge.net/p/autoplot/feature-requests/493/'>https://sourceforge.net/p/autoplot/feature-requests/493/</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getActiveSubrange&unscoped_q=getActiveSubrange">[search for examples]</a>

***
<a name="getAllTimes"></a>
# getAllTimes
getAllTimes(  ) &rarr; List

Return a <code>java.awt.List</code> of the times associated with this sequence.
 This list will include times associated with missing images, and is not restricted
 to any currently active subrange.

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=getAllTimes&unscoped_q=getAllTimes">[search for examples]</a>

***
<a name="getImage"></a>
# getImage
getImage( java.net.URI image ) &rarr; WalkImage

return the WalkImage object for the given URI.

### Parameters:
image - the location

### Returns:
the object modeling this image.

<a href="https://github.com/autoplot/dev/search?q=getImage&unscoped_q=getImage">[search for examples]</a>

***
<a name="getIndex"></a>
# getIndex
getIndex(  ) &rarr; int

Return the current value of the index, where index is that of the displayImages.

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=getIndex&unscoped_q=getIndex">[search for examples]</a>

***
<a name="getQCFilter"></a>
# getQCFilter
getQCFilter(  ) &rarr; String

returns the current QC filter, where "" means no filter, otherwise 
 the characters indicate:
 <ul>
 <li>o okay are shown
 <li>p problem are shown
 <li>i ignore are shown
 </ul>

### Returns:
the filter, for example "" or "op" for okay and problem.

<a href="https://github.com/autoplot/dev/search?q=getQCFilter&unscoped_q=getQCFilter">[search for examples]</a>

***
<a name="getQCFolder"></a>
# getQCFolder
getQCFolder(  ) &rarr; URI



### Returns:
java.net.URI


<a href="https://github.com/autoplot/dev/search?q=getQCFolder&unscoped_q=getQCFolder">[search for examples]</a>

***
<a name="getQualityControlSequence"></a>
# getQualityControlSequence
getQualityControlSequence(  ) &rarr; QualityControlSequence

this may be null if even though we are using QualityControl, if the user
 hasn't logged in yet.

### Returns:
an org.autoplot.pngwalk.QualityControlSequence


<a href="https://github.com/autoplot/dev/search?q=getQualityControlSequence&unscoped_q=getQualityControlSequence">[search for examples]</a>

***
<a name="getSelectedIndeces"></a>
# getSelectedIndeces
getSelectedIndeces(  ) &rarr; List



### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=getSelectedIndeces&unscoped_q=getSelectedIndeces">[search for examples]</a>

***
<a name="getSelectedName"></a>
# getSelectedName
getSelectedName(  ) &rarr; String

return the name of the selected image.  This is not the full 
 filename, but instead just the part of the name within the walk.  For example,
 For example if getTemplate is file:/tmp/$Y$m$d.gif, then the setSelectedName might be 20141111.gif.

### Returns:
the name of the selected image.

<a href="https://github.com/autoplot/dev/search?q=getSelectedName&unscoped_q=getSelectedName">[search for examples]</a>

***
<a name="getStatus"></a>
# getStatus
getStatus(  ) &rarr; String

get the current status

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getStatus&unscoped_q=getStatus">[search for examples]</a>

***
<a name="getTemplate"></a>
# getTemplate
getTemplate(  ) &rarr; String

return the template representing the sequence.

### Returns:
the template

<a href="https://github.com/autoplot/dev/search?q=getTemplate&unscoped_q=getTemplate">[search for examples]</a>

***
<a name="getTimeSpan"></a>
# getTimeSpan
getTimeSpan(  ) &rarr; DatumRange

Return the time range covered by this sequence.  This is the total range
 of available images, not any currently displayed subrange.  Will be null
 if no date template was used to create the sequence.

### Returns:
the time range covered by this sequence.

<a href="https://github.com/autoplot/dev/search?q=getTimeSpan&unscoped_q=getTimeSpan">[search for examples]</a>

***
<a name="getTimerange"></a>
# getTimerange
getTimerange(  ) &rarr; DatumRange

constraint for the limit of the time ranges listed.  Note timespan
 is what was found.  This does not appear to be the current image
 timerange.

### Returns:
a DatumRange


<a href="https://github.com/autoplot/dev/search?q=getTimerange&unscoped_q=getTimerange">[search for examples]</a>

***
<a name="imageAt"></a>
# imageAt
imageAt( int n ) &rarr; WalkImage

return the image of the subrange.

### Parameters:
n - an int

### Returns:
an org.autoplot.pngwalk.WalkImage


<a href="https://github.com/autoplot/dev/search?q=imageAt&unscoped_q=imageAt">[search for examples]</a>

***
<a name="imageAtNoSubRange"></a>
# imageAtNoSubRange
imageAtNoSubRange( int n ) &rarr; WalkImage

get the image in the sequence, regardless of the subrange.

### Parameters:
n - an int

### Returns:
an org.autoplot.pngwalk.WalkImage


<a href="https://github.com/autoplot/dev/search?q=imageAtNoSubRange&unscoped_q=imageAtNoSubRange">[search for examples]</a>

***
<a name="initialLoad"></a>
# initialLoad
initialLoad(  ) &rarr; void

do the initial listing of the remote filesystem.  This should not
 be done on the event thread, and should be done before the
 sequence is used.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=initialLoad&unscoped_q=initialLoad">[search for examples]</a>

***
<a name="isShowMissing"></a>
# isShowMissing
isShowMissing(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isShowMissing&unscoped_q=isShowMissing">[search for examples]</a>

***
<a name="isUseSubRange"></a>
# isUseSubRange
isUseSubRange(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isUseSubRange&unscoped_q=isUseSubRange">[search for examples]</a>

***
<a name="last"></a>
# last
last(  ) &rarr; void

Move the image to the last image in the list.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=last&unscoped_q=last">[search for examples]</a>

***
<a name="next"></a>
# next
next(  ) &rarr; void

Advance the index to the next image in the list.  If the index is already
 at the last image, do nothing.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=next&unscoped_q=next">[search for examples]</a>

***
<a name="prev"></a>
# prev
prev(  ) &rarr; void

Step the index to the previous image in the list.  If the index is already
 at the first image, do nothing.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=prev&unscoped_q=prev">[search for examples]</a>

***
<a name="propertyChange"></a>
# propertyChange
propertyChange( java.beans.PropertyChangeEvent e ) &rarr; void



### Parameters:
e - a PropertyChangeEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=propertyChange&unscoped_q=propertyChange">[search for examples]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void



### Parameters:
l - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

removePropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="setActiveSubrange"></a>
# setActiveSubrange
setActiveSubrange( int first, int last ) &rarr; void

Set the sequence's active subrange to a range from first to last, inclusive.
 First and last are indices into the list obtained from <code>getAllTimes()</code>.

### Parameters:
first - an int
<br>last - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setActiveSubrange&unscoped_q=setActiveSubrange">[search for examples]</a>

setActiveSubrange( DatumRange range ) &rarr; void<br>
***
<a name="setIndex"></a>
# setIndex
setIndex( int index ) &rarr; void

Set the index explicitly.

### Parameters:
index - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setIndex&unscoped_q=setIndex">[search for examples]</a>

***
<a name="setQCFilter"></a>
# setQCFilter
setQCFilter( String s ) &rarr; void

string containing combination of "opi" meaning that each should be shown.
 "" will show everything.  The list can include:<ul>
 <li>o okay are shown
 <li>p problem are shown
 <li>i ignore are shown
 </ul>

### Parameters:
s - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setQCFilter&unscoped_q=setQCFilter">[search for examples]</a>

***
<a name="setQCFolder"></a>
# setQCFolder
setQCFolder( java.net.URI folder ) &rarr; void



### Parameters:
folder - an URI

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setQCFolder&unscoped_q=setQCFolder">[search for examples]</a>

***
<a name="setSelectedIndeces"></a>
# setSelectedIndeces
setSelectedIndeces( java.util.List sel ) &rarr; void



### Parameters:
sel - a java.util.List

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSelectedIndeces&unscoped_q=setSelectedIndeces">[search for examples]</a>

***
<a name="setShowMissing"></a>
# setShowMissing
setShowMissing( boolean showMissing ) &rarr; void



### Parameters:
showMissing - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setShowMissing&unscoped_q=setShowMissing">[search for examples]</a>

***
<a name="setTimerange"></a>
# setTimerange
setTimerange( DatumRange timerange ) &rarr; void

constraint for the limit of the time ranges listed.  Note timespan
 is what was found.

### Parameters:
timerange - a DatumRange

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTimerange&unscoped_q=setTimerange">[search for examples]</a>

***
<a name="setUseSubRange"></a>
# setUseSubRange
setUseSubRange( boolean useSubRange ) &rarr; void



### Parameters:
useSubRange - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUseSubRange&unscoped_q=setUseSubRange">[search for examples]</a>

***
<a name="size"></a>
# size
size(  ) &rarr; int

return the number of images in the sequence.

### Returns:
the number of images in the sequence.

<a href="https://github.com/autoplot/dev/search?q=size&unscoped_q=size">[search for examples]</a>

***
<a name="skipBy"></a>
# skipBy
skipBy( int n ) &rarr; void

Skip forward or backward by the specified number of images.  Positive
 numbers skip forward; negative skip backward.  If skipping the requested
 number of frames would put the index out of range, the skip moves to the
 last or first image, as appropriate.

### Parameters:
n - The number of images to skip.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=skipBy&unscoped_q=skipBy">[search for examples]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

