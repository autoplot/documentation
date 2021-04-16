# org.das2.components.DatumEditor
DatumEditor( )
Creates a new instance of DatumEditor

***
<a name="addActionListener"></a>
# addActionListener
addActionListener( java.awt.event.ActionListener al ) &rarr; void



### Parameters:
al - an ActionListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addActionListener&unscoped_q=addActionListener">[search for examples]</a>

***
<a name="addCellEditorListener"></a>
# addCellEditorListener
addCellEditorListener( javax.swing.event.CellEditorListener l ) &rarr; void



### Parameters:
l - a CellEditorListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addCellEditorListener&unscoped_q=addCellEditorListener">[search for examples]</a>

***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
propertyName - a String
<br>listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

addPropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="cancelCellEditing"></a>
# cancelCellEditing
cancelCellEditing(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=cancelCellEditing&unscoped_q=cancelCellEditing">[search for examples]</a>

***
<a name="getAsText"></a>
# getAsText
getAsText(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getAsText&unscoped_q=getAsText">[search for examples]</a>

***
<a name="getCellEditorValue"></a>
# getCellEditorValue
getCellEditorValue(  ) &rarr; Object

Returns the value stored in this editor.

### Returns:
the current value being edited

<a href="https://github.com/autoplot/dev/search?q=getCellEditorValue&unscoped_q=getCellEditorValue">[search for examples]</a>

***
<a name="getCustomEditor"></a>
# getCustomEditor
getCustomEditor(  ) &rarr; Component



### Returns:
<code>this</code>
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/java/beans/PropertyEditor.md#getCustomEditor'>java.beans.PropertyEditor#getCustomEditor()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getCustomEditor&unscoped_q=getCustomEditor">[search for examples]</a>

***
<a name="getDatum"></a>
# getDatum
getDatum(  ) &rarr; Datum



### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getDatum&unscoped_q=getDatum">[search for examples]</a>

***
<a name="getJavaInitializationString"></a>
# getJavaInitializationString
getJavaInitializationString(  ) &rarr; String

This PropertyEditor implementation does not support generating java
 code.

### Returns:
The string "???"

<a href="https://github.com/autoplot/dev/search?q=getJavaInitializationString&unscoped_q=getJavaInitializationString">[search for examples]</a>

***
<a name="getTableCellEditorComponent"></a>
# getTableCellEditorComponent
getTableCellEditorComponent( javax.swing.JTable table, Object value, boolean isSelected, int row, int column ) &rarr; Component



### Parameters:
table - a JTable
<br>value - an Object
<br>isSelected - a boolean
<br>row - an int
<br>column - an int

### Returns:
java.awt.Component


<a href="https://github.com/autoplot/dev/search?q=getTableCellEditorComponent&unscoped_q=getTableCellEditorComponent">[search for examples]</a>

***
<a name="getTags"></a>
# getTags
getTags(  ) &rarr; String

This PropertyEditor implementation does not support enumerated
 values.

### Returns:
null

<a href="https://github.com/autoplot/dev/search?q=getTags&unscoped_q=getTags">[search for examples]</a>

***
<a name="getToolTipText"></a>
# getToolTipText
getToolTipText( java.awt.event.MouseEvent event ) &rarr; String



### Parameters:
event - a MouseEvent

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getToolTipText&unscoped_q=getToolTipText">[search for examples]</a>

***
<a name="getUnits"></a>
# getUnits
getUnits(  ) &rarr; Units



### Returns:
org.das2.datum.Units


<a href="https://github.com/autoplot/dev/search?q=getUnits&unscoped_q=getUnits">[search for examples]</a>

***
<a name="getValue"></a>
# getValue
getValue(  ) &rarr; Object



### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=getValue&unscoped_q=getValue">[search for examples]</a>

***
<a name="isCellEditable"></a>
# isCellEditable
isCellEditable( java.util.EventObject anEvent ) &rarr; boolean



### Parameters:
anEvent - an EventObject

### Returns:
<code>true</code>
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/javax/swing/CellEditor.md#isCellEditable'>javax.swing.CellEditor#isCellEditable(java.util.EventObject)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isCellEditable&unscoped_q=isCellEditable">[search for examples]</a>

***
<a name="isPaintable"></a>
# isPaintable
isPaintable(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isPaintable&unscoped_q=isPaintable">[search for examples]</a>

***
<a name="paintValue"></a>
# paintValue
paintValue( java.awt.Graphics g, java.awt.Rectangle r ) &rarr; void



### Parameters:
g - a Graphics
<br>r - a Rectangle

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=paintValue&unscoped_q=paintValue">[search for examples]</a>

***
<a name="removeActionListener"></a>
# removeActionListener
removeActionListener( java.awt.event.ActionListener al ) &rarr; void



### Parameters:
al - an ActionListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeActionListener&unscoped_q=removeActionListener">[search for examples]</a>

***
<a name="removeCellEditorListener"></a>
# removeCellEditorListener
removeCellEditorListener( javax.swing.event.CellEditorListener l ) &rarr; void



### Parameters:
l - a CellEditorListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeCellEditorListener&unscoped_q=removeCellEditorListener">[search for examples]</a>

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
<a name="setAsText"></a>
# setAsText
setAsText( String text ) &rarr; void



### Parameters:
text - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAsText&unscoped_q=setAsText">[search for examples]</a>

***
<a name="setColumns"></a>
# setColumns
setColumns( int columns ) &rarr; void



### Parameters:
columns - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setColumns&unscoped_q=setColumns">[search for examples]</a>

***
<a name="setUnits"></a>
# setUnits
setUnits( Units units ) &rarr; void



### Parameters:
units - an Units

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUnits&unscoped_q=setUnits">[search for examples]</a>

***
<a name="setValue"></a>
# setValue
setValue( Object value ) &rarr; void



### Parameters:
value - the Datum object to be editted.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setValue&unscoped_q=setValue">[search for examples]</a>

***
<a name="shouldSelectCell"></a>
# shouldSelectCell
shouldSelectCell( java.util.EventObject anEvent ) &rarr; boolean



### Parameters:
anEvent - an EventObject

### Returns:
<code>true</code>
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/javax/swing/CellEditor.md#shouldSelectCell'>javax.swing.CellEditor#shouldSelectCell(java.util.EventObject)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=shouldSelectCell&unscoped_q=shouldSelectCell">[search for examples]</a>

***
<a name="stopCellEditing"></a>
# stopCellEditing
stopCellEditing(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=stopCellEditing&unscoped_q=stopCellEditing">[search for examples]</a>

***
<a name="supportsCustomEditor"></a>
# supportsCustomEditor
supportsCustomEditor(  ) &rarr; boolean



### Returns:
true
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/java/beans/PropertyEditor.md#supportsCustomEditor'>java.beans.PropertyEditor#supportsCustomEditor()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=supportsCustomEditor&unscoped_q=supportsCustomEditor">[search for examples]</a>
