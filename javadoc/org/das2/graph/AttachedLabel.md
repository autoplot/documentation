# org.das2.graph.AttachedLabelA canvas component for labeling things that is positioned just outside of a row,column box.
AttachedLabel( String label, int orientation, double emOffset )
constructs an AttachedLabel.

***
<a name="TOP"></a>
# TOP

This value indicates that the axis should be located at the top of its cell

***
<a name="BOTTOM"></a>
# BOTTOM

This value indicates that the axis should be located at the bottom of its cell

***
<a name="LEFT"></a>
# LEFT

This value indicates that the axis should be located to the left of its cell

***
<a name="RIGHT"></a>
# RIGHT

This value indicateds that the axis should be located to the right of its cell

***
<a name="HORIZONTAL"></a>
# HORIZONTAL

This value indicates that the axis should be oriented horizontally

***
<a name="VERTICAL"></a>
# VERTICAL

This value indicates that the axis should be oriented vertically

***
<a name="clone"></a>
# clone
clone(  ) &rarr; Object

clones the component

### Returns:
clone of this.

<a href="https://github.com/autoplot/dev/search?q=clone&unscoped_q=clone">[search for examples]</a>

***
<a name="getActiveRegion"></a>
# getActiveRegion
getActiveRegion(  ) &rarr; Shape



### Returns:
the bounds of the label

<a href="https://github.com/autoplot/dev/search?q=getActiveRegion&unscoped_q=getActiveRegion">[search for examples]</a>

***
<a name="getDLength"></a>
# getDLength
getDLength(  ) &rarr; int



### Returns:
returns the length in pixels of the axis.

<a href="https://github.com/autoplot/dev/search?q=getDLength&unscoped_q=getDLength">[search for examples]</a>

***
<a name="getDevicePosition"></a>
# <del>getDevicePosition</del>
Deprecated: It's not clear how this should be used, and it does not appear to be used within dasCore and dasApps.
***
<a name="getEmOffset"></a>
# getEmOffset
getEmOffset(  ) &rarr; double

Getter for property emOffset.

### Returns:
Value of property emOffset.

<a href="https://github.com/autoplot/dev/search?q=getEmOffset&unscoped_q=getEmOffset">[search for examples]</a>

***
<a name="getLabel"></a>
# getLabel
getLabel(  ) &rarr; String

Accessor method for the title property of this axis.

### Returns:
A String instance that contains the title displayed
    for this axis, or <code>null</code> if the axis has no title.

<a href="https://github.com/autoplot/dev/search?q=getLabel&unscoped_q=getLabel">[search for examples]</a>

***
<a name="getLabelFont"></a>
# getLabelFont
getLabelFont(  ) &rarr; Font

get the current font of the compoennt.

### Returns:
Font of the component.

<a href="https://github.com/autoplot/dev/search?q=getLabelFont&unscoped_q=getLabelFont">[search for examples]</a>

***
<a name="getOrientation"></a>
# getOrientation
getOrientation(  ) &rarr; int

return orientation int

### Returns:
AttachedLabel.TOP, etc.

<a href="https://github.com/autoplot/dev/search?q=getOrientation&unscoped_q=getOrientation">[search for examples]</a>

***
<a name="isHorizontal"></a>
# isHorizontal
isHorizontal(  ) &rarr; boolean

true if the label is horizontal

### Returns:
true if the  label is horizontal

<a href="https://github.com/autoplot/dev/search?q=isHorizontal&unscoped_q=isHorizontal">[search for examples]</a>

***
<a name="resize"></a>
# resize
resize(  ) &rarr; void

revalidate component after resize.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resize&unscoped_q=resize">[search for examples]</a>

***
<a name="setEmOffset"></a>
# setEmOffset
setEmOffset( double emOffset ) &rarr; void

Setter for property emOffset.

### Parameters:
emOffset - New value of property emOffset.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setEmOffset&unscoped_q=setEmOffset">[search for examples]</a>

***
<a name="setLabel"></a>
# setLabel
setLabel( String t ) &rarr; void

Mutator method for the title property of this axis.

 The title for this axis is displayed below the ticks for horizontal axes
 or to left of the ticks for vertical axes.

### Parameters:
t - The new title for this axis

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLabel&unscoped_q=setLabel">[search for examples]</a>

***
<a name="setLabelFont"></a>
# setLabelFont
setLabelFont( java.awt.Font labelFont ) &rarr; void

set the font of the label.

### Parameters:
labelFont - Font for the component.  Currently this is ignored.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLabelFont&unscoped_q=setLabelFont">[search for examples]</a>

***
<a name="setOrientation"></a>
# setOrientation
setOrientation( int orientation ) &rarr; void

Sets the side of the row,column box to locate the label.

### Parameters:
orientation - should be one of AttachedLabel.TOP, AttachedLabel.BOTTOM, AttachedLabel.LEFT, AttachedLabel.RIGHT

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setOrientation&unscoped_q=setOrientation">[search for examples]</a>

