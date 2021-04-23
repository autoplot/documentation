# org.das2.components.propertyeditor.DisplayableType-safe enumerations that are used as property types
 that are editable with a PropertyEditor should
 implement this interface.
***
<a name="drawListIcon"></a>
# drawListIcon
drawListIcon( java.awt.Graphics2D g, int x, int y ) &rarr; void

implement this to provide nice drawing of icon on printing graphics context.

### Parameters:
g - the graphics context.
<br>x - the x position, typically 0.
<br>y - the y position, typically 0.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=drawListIcon&unscoped_q=drawListIcon">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getListIcon"></a>
# getListIcon
getListIcon(  ) &rarr; Icon

An icon can be provided that will be shown in a list
 along with the textual description of the element.
 This method should return <code>null</code> if there
 is no icon available, or a roughly 16x16 pixel icon.

### Returns:
the icon.

<a href="https://github.com/autoplot/dev/search?q=getListIcon&unscoped_q=getListIcon">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getListLabel"></a>
# getListLabel
getListLabel(  ) &rarr; String

return a <code>String</code> that will help the user
 identify this item when choosing from a list.

### Returns:
the list label.

<a href="https://github.com/autoplot/dev/search?q=getListLabel&unscoped_q=getListLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

