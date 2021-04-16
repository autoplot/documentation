# org.das2.graph.DasDevicePositionDasRows and DasColumns are both DasDevidePositions that lay out the
 canvas.  Any object on the DasCanvas have a row and column object to indicate
 the position of the object.
DasDevicePosition( org.das2.graph.DasCanvas parent, double minimum, double maximum, boolean width )


***
<a name="PROP_DMAXIMUM"></a>
# PROP_DMAXIMUM



***
<a name="PROP_DMINIMUM"></a>
# PROP_DMINIMUM



***
<a name="PROP_EMMAXIMUM"></a>
# PROP_EMMAXIMUM



***
<a name="PROP_EMMINIMUM"></a>
# PROP_EMMINIMUM



***
<a name="PROP_MAXIMUM"></a>
# PROP_MAXIMUM



***
<a name="PROP_MINIMUM"></a>
# PROP_MINIMUM



***
<a name="PROP_PTMAXIMUM"></a>
# PROP_PTMAXIMUM



***
<a name="PROP_PTMINIMUM"></a>
# PROP_PTMINIMUM



***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

addPropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="addUpdateListener"></a>
# addUpdateListener
addUpdateListener( org.das2.graph.event.DasUpdateListener l ) &rarr; void

add an update listener

### Parameters:
l - update listener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addUpdateListener&unscoped_q=addUpdateListener">[search for examples]</a>

***
<a name="contains"></a>
# contains
contains( int x ) &rarr; boolean

returns true if ( getDMinimum() &lt;= x ) &amp;&amp; ( x &lt;= getDMaximum() );

### Parameters:
x - the pixel position

### Returns:
true if ( getDMinimum() &lt;= x ) &amp;&amp; ( x &lt;= getDMaximum() );

<a href="https://github.com/autoplot/dev/search?q=contains&unscoped_q=contains">[search for examples]</a>

***
<a name="formatFormatStr"></a>
# formatFormatStr
formatFormatStr( double[] arr ) &rarr; String

formats the three position specifiers efficiently.

### Parameters:
arr - three-element array [ npos, emoffset, pt_offset ].

### Returns:
String like "100%-5em+4pt"
### See Also:
<a href='#parseFormatStr'>parseFormatStr(java.lang.String)</a> <br>
<a href='#formatLayoutStr'>formatLayoutStr(org.das2.graph.DasDevicePosition, boolean)</a> which contains repeated code.<br>

<a href="https://github.com/autoplot/dev/search?q=formatFormatStr&unscoped_q=formatFormatStr">[search for examples]</a>

***
<a name="formatLayoutStr"></a>
# formatLayoutStr
formatLayoutStr( org.das2.graph.DasDevicePosition pos, boolean min ) &rarr; String

formats the row or column position into a string like

### Parameters:
pos - the row or column
<br>min - true if the minimum boundary is to be formatted, false if the maximum boundary is to be formatted.

### Returns:
String like "100%-5em+4pt"
### See Also:
<a href='#formatFormatStr'>formatFormatStr(double[])</a> which contains repeated code.<br>

<a href="https://github.com/autoplot/dev/search?q=formatLayoutStr&unscoped_q=formatLayoutStr">[search for examples]</a>

***
<a name="getDMaximum"></a>
# getDMaximum
getDMaximum(  ) &rarr; int

returns the pixel position of the maximum of the Row/Column.  This is
 the right side of a column and the bottom of a row.

### Returns:
the pixel position (pixel=point for now)

<a href="https://github.com/autoplot/dev/search?q=getDMaximum&unscoped_q=getDMaximum">[search for examples]</a>

***
<a name="getDMiddle"></a>
# getDMiddle
getDMiddle(  ) &rarr; int

returns pixel position (device position) of the the middle of the row or column

### Returns:
pixel position (device position) of the the middle of the row or column

<a href="https://github.com/autoplot/dev/search?q=getDMiddle&unscoped_q=getDMiddle">[search for examples]</a>

***
<a name="getDMinimum"></a>
# getDMinimum
getDMinimum(  ) &rarr; int

returns the pixel position of the minimum of the Row/Column.  This is
 the left side of a column and the top of a row.

### Returns:
the pixel position (pixel=point for now)

<a href="https://github.com/autoplot/dev/search?q=getDMinimum&unscoped_q=getDMinimum">[search for examples]</a>

***
<a name="getDasName"></a>
# getDasName
getDasName(  ) &rarr; String

get the name associated with this object.

### Returns:
the name associated with this object.

<a href="https://github.com/autoplot/dev/search?q=getDasName&unscoped_q=getDasName">[search for examples]</a>

***
<a name="getEmMaximum"></a>
# getEmMaximum
getEmMaximum(  ) &rarr; double

return the em offset that controls the position of the bottom/right boundary.

### Returns:
the em offset that controls the position of the bottom/right boundary.

<a href="https://github.com/autoplot/dev/search?q=getEmMaximum&unscoped_q=getEmMaximum">[search for examples]</a>

***
<a name="getEmMinimum"></a>
# getEmMinimum
getEmMinimum(  ) &rarr; double

return the em offset that controls the position of the top/left boundary.

### Returns:
the em offset that controls the position of the top/left boundary.

<a href="https://github.com/autoplot/dev/search?q=getEmMinimum&unscoped_q=getEmMinimum">[search for examples]</a>

***
<a name="getEmSize"></a>
# getEmSize
getEmSize(  ) &rarr; int

returns the em size for the canvas.  We define the em size as the 
 height of the font.

### Returns:
the em height in points.

<a href="https://github.com/autoplot/dev/search?q=getEmSize&unscoped_q=getEmSize">[search for examples]</a>

***
<a name="getMaximum"></a>
# getMaximum
getMaximum(  ) &rarr; double

return the normal position control of the bottom/right.

### Returns:
the normal position control of the bottom/right.

<a href="https://github.com/autoplot/dev/search?q=getMaximum&unscoped_q=getMaximum">[search for examples]</a>

***
<a name="getMinimum"></a>
# getMinimum
getMinimum(  ) &rarr; double

return the normal position control of the top/left.

### Returns:
the normal position control of the top/left.

<a href="https://github.com/autoplot/dev/search?q=getMinimum&unscoped_q=getMinimum">[search for examples]</a>

***
<a name="getParent"></a>
# getParent
getParent(  ) &rarr; DasCanvas

return the parent canvas.

### Returns:
the parent canvas.

<a href="https://github.com/autoplot/dev/search?q=getParent&unscoped_q=getParent">[search for examples]</a>

***
<a name="getParentDevicePosition"></a>
# getParentDevicePosition
getParentDevicePosition(  ) &rarr; DasDevicePosition

return the parent, or null.  If parent is non-null, then position is 
 relative to the parent.

### Returns:
the parent, or null.

<a href="https://github.com/autoplot/dev/search?q=getParentDevicePosition&unscoped_q=getParentDevicePosition">[search for examples]</a>

***
<a name="getPtMaximum"></a>
# getPtMaximum
getPtMaximum(  ) &rarr; int

return the points offset that controls the position of the bottom/right boundary.

### Returns:
the points offset that controls the position of the bottom/right boundary.

<a href="https://github.com/autoplot/dev/search?q=getPtMaximum&unscoped_q=getPtMaximum">[search for examples]</a>

***
<a name="getPtMinimum"></a>
# getPtMinimum
getPtMinimum(  ) &rarr; int

return the points offset that controls the position of the top/left boundary.

### Returns:
the points offset

<a href="https://github.com/autoplot/dev/search?q=getPtMinimum&unscoped_q=getPtMinimum">[search for examples]</a>

***
<a name="isValueIsAdjusting"></a>
# isValueIsAdjusting
isValueIsAdjusting(  ) &rarr; boolean

return true if the value is currently adjusting because a
 mutator lock is out.

### Returns:
true if the value is currently adjusting.

<a href="https://github.com/autoplot/dev/search?q=isValueIsAdjusting&unscoped_q=isValueIsAdjusting">[search for examples]</a>

***
<a name="parseFormatStr"></a>
# <del>parseFormatStr</del>
Deprecated: use parseLayoutStr.
***
<a name="parseLayoutStr"></a>
# parseLayoutStr
parseLayoutStr( String s, double em, int widthHeight, double fail ) &rarr; double

parse the format string into a pixel count.  Convenience method.
 parseFormatStr(s) will throw a parse exception and should be used to 
 verify strings.

### Parameters:
s - The string, like "5em+3pt"
<br>em - the em height of the font,
<br>widthHeight - the width or height of the dimension.
<br>fail - the value to return if the parsing fails.

### Returns:
the length in pixels (or points).

<a href="https://github.com/autoplot/dev/search?q=parseLayoutStr&unscoped_q=parseLayoutStr">[search for examples]</a>

parseLayoutStr( String s ) &rarr; double<br>
parseLayoutStr( org.das2.graph.DasDevicePosition pos, String spec ) &rarr; void<br>
***
<a name="removeListeners"></a>
# removeListeners
removeListeners(  ) &rarr; void

remove the listeners so that the DasRow or DasColumn can be garbage collected.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeListeners&unscoped_q=removeListeners">[search for examples]</a>

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

removePropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="removeUpdateListener"></a>
# removeUpdateListener
removeUpdateListener( org.das2.graph.event.DasUpdateListener l ) &rarr; void

remove an update listener

### Parameters:
l - update listener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeUpdateListener&unscoped_q=removeUpdateListener">[search for examples]</a>

***
<a name="setDMaximum"></a>
# setDMaximum
setDMaximum( int maximum ) &rarr; void

set the new pixel position of the bottom/right boundary.  
 em and pt offsets are not modified, and the normal position 
 is recalculated.

### Parameters:
maximum - new pixel maximum

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDMaximum&unscoped_q=setDMaximum">[search for examples]</a>

***
<a name="setDMinimum"></a>
# setDMinimum
setDMinimum( int minimum ) &rarr; void

set the new pixel position of the top/left boundary.  em and pt offsets
 are not modified, and the normal position is recalculated.

### Parameters:
minimum - new pixel minimum

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDMinimum&unscoped_q=setDMinimum">[search for examples]</a>

***
<a name="setDPosition"></a>
# setDPosition
setDPosition( int minimum, int maximum ) &rarr; void

set the new pixel location of both the min and max in one operation.

### Parameters:
minimum - the top or left
<br>maximum - the bottom or right

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDPosition&unscoped_q=setDPosition">[search for examples]</a>

***
<a name="setDasName"></a>
# setDasName
setDasName( String name ) &rarr; void

set the name associated with this object.

### Parameters:
name - the name associated with this object

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDasName&unscoped_q=setDasName">[search for examples]</a>

***
<a name="setEmMaximum"></a>
# setEmMaximum
setEmMaximum( double emMaximum ) &rarr; void

set the em offset that controls the position of the bottom/right boundary.

### Parameters:
emMaximum - the em offset.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setEmMaximum&unscoped_q=setEmMaximum">[search for examples]</a>

***
<a name="setEmMinimum"></a>
# setEmMinimum
setEmMinimum( double emMinimum ) &rarr; void

set the em offset that controls the position of the top/left boundary.

### Parameters:
emMinimum - the em offset.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setEmMinimum&unscoped_q=setEmMinimum">[search for examples]</a>

***
<a name="setMax"></a>
# setMax
setMax( double norm, double em, int pt ) &rarr; void

set all three as one atomic operation

### Parameters:
norm - normal position from 0 to 1.
<br>em - em offset from the normal position.
<br>pt - points offset from the normal position.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMax&unscoped_q=setMax">[search for examples]</a>

***
<a name="setMaximum"></a>
# setMaximum
setMaximum( double maximum ) &rarr; void

set the normal position of the minimum of the row or column.  
 For a row, this is the bottom.  For a column, this is the right side.

### Parameters:
maximum - normal (0-1) position

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMaximum&unscoped_q=setMaximum">[search for examples]</a>

***
<a name="setMin"></a>
# setMin
setMin( double norm, double em, int pt ) &rarr; void

set all three as one atomic operation

### Parameters:
norm - normal position from 0 to 1.
<br>em - em offset from the normal position.
<br>pt - points offset from the normal position.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMin&unscoped_q=setMin">[search for examples]</a>

***
<a name="setMinimum"></a>
# setMinimum
setMinimum( double minimum ) &rarr; void

set the normal position of the minimum of the row or column.  
 For a row, this is the top.  For a column, this is the left side.

### Parameters:
minimum - normal (0-1) position

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMinimum&unscoped_q=setMinimum">[search for examples]</a>

***
<a name="setParent"></a>
# setParent
setParent( org.das2.graph.DasCanvas parent ) &rarr; void

set the parent canvas.

### Parameters:
parent - canvas.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setParent&unscoped_q=setParent">[search for examples]</a>

***
<a name="setPtMaximum"></a>
# setPtMaximum
setPtMaximum( int ptMaximum ) &rarr; void

set the pt offset that controls the position of the bottom/right boundary.

### Parameters:
ptMaximum - the em offset.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPtMaximum&unscoped_q=setPtMaximum">[search for examples]</a>

***
<a name="setPtMinimum"></a>
# setPtMinimum
setPtMinimum( int ptMinimum ) &rarr; void

set the points offset that controls the position of the top/left boundary.

### Parameters:
ptMinimum - the points offset

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPtMinimum&unscoped_q=setPtMinimum">[search for examples]</a>

***
<a name="toRectangle"></a>
# toRectangle
toRectangle( org.das2.graph.DasRow row, org.das2.graph.DasColumn column ) &rarr; Rectangle

convenience method for creating a rectangle from a row and column.
 The rectangle will be in canvas pixel coordinates.

### Parameters:
row - row describing the top and bottom of the box.
<br>column - column describing the left and right sides of the box.

### Returns:
rectangle in canvas pixel coordinates.

<a href="https://github.com/autoplot/dev/search?q=toRectangle&unscoped_q=toRectangle">[search for examples]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String

return a human-readable string representing the object for debugging.

### Returns:
a human-readable string representing the object for debugging.

<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

