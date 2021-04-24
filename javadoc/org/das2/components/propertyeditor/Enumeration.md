# org.das2.components.propertyeditor.Enumeration

Type-safe enumerations that are used as property types
 that are editable with a PropertyEditor should
 implement this interface.

***
<a name="getListIcon"></a>
# getListIcon
getListIcon(  ) &rarr; Icon

An icon can be provided that will be shown in a list
 along with the textual description of the element.
 This method should return <code>null</code> if there
 is no icon available.

### Returns:
the icon

<a href="https://github.com/autoplot/dev/search?q=getListIcon&unscoped_q=getListIcon">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String

Type-safe Enumerations implementing this interface
 should override the toString() method to return a
 <code>String</code> that will be helpful to the user
 when choosing this as an option from a list.

### Returns:
a concise string representation

<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

