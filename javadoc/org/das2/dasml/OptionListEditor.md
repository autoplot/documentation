# org.das2.dasml.OptionListEditor
OptionListEditor( )
Creates a new instance of FormChoiceEditor

***
<a name="addCellEditorListener"></a>
# addCellEditorListener
addCellEditorListener( javax.swing.event.CellEditorListener l ) &rarr; void

Adds a listener to the list that's notified when the editor
 stops, or cancels editing.

### Parameters:
l - the CellEditorListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addCellEditorListener&unscoped_q=addCellEditorListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="cancelCellEditing"></a>
# cancelCellEditing
cancelCellEditing(  ) &rarr; void

Tells the editor to cancel editing and not accept any partially
 edited value.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=cancelCellEditing&unscoped_q=cancelCellEditing">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getAsText"></a>
# getAsText
getAsText(  ) &rarr; String

Gets the property value as text.

### Returns:
The property value as a human editable string.
 <p>   Returns null if the value can't be expressed as an editable string.
 <p>   If a non-null value is returned, then the PropertyEditor should
 	     be prepared to parse that string back in setAsText().

<a href="https://github.com/autoplot/dev/search?q=getAsText&unscoped_q=getAsText">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCellEditorValue"></a>
# getCellEditorValue
getCellEditorValue(  ) &rarr; Object

Returns the value contained in the editor.

### Returns:
the value contained in the editor

<a href="https://github.com/autoplot/dev/search?q=getCellEditorValue&unscoped_q=getCellEditorValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCustomEditor"></a>
# getCustomEditor
getCustomEditor(  ) &rarr; Component

A PropertyEditor may choose to make available a full custom Component
 that edits its property value.  It is the responsibility of the
 PropertyEditor to hook itself up to its editor Component itself and
 to report property value changes by firing a PropertyChange event.
 <P>
 The higher-level code that calls getCustomEditor may either embed
 the Component in some larger property sheet, or it may put it in
 its own individual dialog, or ...

### Returns:
A java.awt.Component that will allow a human to directly
      edit the current property value.  May be null if this is
 	    not supported.

<a href="https://github.com/autoplot/dev/search?q=getCustomEditor&unscoped_q=getCustomEditor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getJavaInitializationString"></a>
# getJavaInitializationString
getJavaInitializationString(  ) &rarr; String

This method is intended for use when generating Java code to set
 the value of the property.  It should return a fragment of Java code
 that can be used to initialize a variable with the current property
 value.
 <p>
 Example results are "2", "new Color(127,127,34)", "Color.orange", etc.

### Returns:
A fragment of Java code representing an initializer for the
   	current value.

<a href="https://github.com/autoplot/dev/search?q=getJavaInitializationString&unscoped_q=getJavaInitializationString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getOptions"></a>
# getOptions
getOptions(  ) &rarr; ListOption



### Returns:
org.das2.dasml.ListOption[]


<a href="https://github.com/autoplot/dev/search?q=getOptions&unscoped_q=getOptions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTableCellEditorComponent"></a>
# getTableCellEditorComponent
getTableCellEditorComponent( javax.swing.JTable table, Object value, boolean isSelected, int row, int column ) &rarr; Component

Sets an initial <code>value</code> for the editor.  This will cause
  the editor to <code>stopEditing</code> and lose any partially
  edited value if the editor is editing when this method is called. <p>

  Returns the component that should be added to the client's
  <code>Component</code> hierarchy.  Once installed in the client's
  hierarchy this component will then be able to draw and receive
  user input.

### Parameters:
table - the <code>JTable</code> that is asking the
 				editor to edit; can be <code>null</code>
<br>value - the value of the cell to be edited; it is
 				up to the specific editor to interpret
 				and draw the value.  For example, if value is
 				the string "true", it could be rendered as a
 				string or it could be rendered as a check
 				box that is checked.  <code>null</code>
 				is a valid value
<br>isSelected - true if the cell is to be rendered with
 				highlighting
<br>row - the row of the cell being edited
<br>column - the column of the cell being edited

### Returns:
the component for editing

<a href="https://github.com/autoplot/dev/search?q=getTableCellEditorComponent&unscoped_q=getTableCellEditorComponent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTags"></a>
# getTags
getTags(  ) &rarr; String

If the property value must be one of a set of known tagged values,
 then this method should return an array of the tags.  This can
 be used to represent (for example) enum values.  If a PropertyEditor
 supports tags, then it should support the use of setAsText with
 a tag value as a way of setting the value and the use of getAsText
 to identify the current value.

### Returns:
The tag values for this property.  May be null if this
   property cannot be represented as a tagged value.

<a href="https://github.com/autoplot/dev/search?q=getTags&unscoped_q=getTags">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getValue"></a>
# getValue
getValue(  ) &rarr; Object

Gets the property value.

### Returns:
The value of the property.  Primitive types such as "int" will
 be wrapped as the corresponding object type such as "java.lang.Integer".

<a href="https://github.com/autoplot/dev/search?q=getValue&unscoped_q=getValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isCellEditable"></a>
# isCellEditable
isCellEditable( java.util.EventObject anEvent ) &rarr; boolean

Asks the editor if it can start editing using <code>anEvent</code>.
 <code>anEvent</code> is in the invoking component coordinate system.
 The editor can not assume the Component returned by
 <code>getCellEditorComponent</code> is installed.  This method
 is intended for the use of client to avoid the cost of setting up
 and installing the editor component if editing is not possible.
 If editing can be started this method returns true.

### Parameters:
anEvent - the event the editor should use to consider
 				whether to begin editing or not

### Returns:
true if editing can be started
### See Also:
<a href='#shouldSelectCell'>shouldSelectCell</a> <br>

<a href="https://github.com/autoplot/dev/search?q=isCellEditable&unscoped_q=isCellEditable">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isPaintable"></a>
# isPaintable
isPaintable(  ) &rarr; boolean

Determines whether this property editor is paintable.

### Returns:
True if the class will honor the paintValue method.

<a href="https://github.com/autoplot/dev/search?q=isPaintable&unscoped_q=isPaintable">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="paintValue"></a>
# paintValue
paintValue( java.awt.Graphics gfx, java.awt.Rectangle box ) &rarr; void

Paint a representation of the value into a given area of screen
 real estate.  Note that the propertyEditor is responsible for doing
 its own clipping so that it fits into the given rectangle.
 <p>
 If the PropertyEditor doesn't honor paint requests (see isPaintable)
 this method should be a silent noop.
 <p>
 The given Graphics object will have the default font, color, etc of
 the parent container.  The PropertyEditor may change graphics attributes
 such as font and color and doesn't need to restore the old values.

### Parameters:
gfx - Graphics object to paint into.
<br>box - Rectangle within graphics object into which we should paint.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=paintValue&unscoped_q=paintValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeCellEditorListener"></a>
# removeCellEditorListener
removeCellEditorListener( javax.swing.event.CellEditorListener l ) &rarr; void

Removes a listener from the list that's notified

### Parameters:
l - the CellEditorListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeCellEditorListener&unscoped_q=removeCellEditorListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAsText"></a>
# setAsText
setAsText( String text ) &rarr; void

Set the property value by parsing a given String.  May raise
 java.lang.IllegalArgumentException if either the String is
 badly formatted or if this kind of property can't be expressed
 as text.

### Parameters:
text - The string to be parsed.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAsText&unscoped_q=setAsText">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setOptions"></a>
# setOptions
setOptions( org.das2.dasml.ListOption[] options ) &rarr; void



### Parameters:
options - an org.das2.dasml.ListOption[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setOptions&unscoped_q=setOptions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setValue"></a>
# setValue
setValue( Object value ) &rarr; void

Set (or change) the object that is to be edited.  Primitive types such
 as "int" must be wrapped as the corresponding object type such as
 "java.lang.Integer".

### Parameters:
value - The new target object to be edited.  Note that this
     object should not be modified by the PropertyEditor, rather
     the PropertyEditor should create a new object to hold any
     modified value.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setValue&unscoped_q=setValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="shouldSelectCell"></a>
# shouldSelectCell
shouldSelectCell( java.util.EventObject anEvent ) &rarr; boolean

Returns true if the editing cell should be selected, false otherwise.
 Typically, the return value is true, because is most cases the editing
 cell should be selected.  However, it is useful to return false to
 keep the selection from changing for some types of edits.
 eg. A table that contains a column of check boxes, the user might
 want to be able to change those checkboxes without altering the
 selection.  (See Netscape Communicator for just such an example)
 Of course, it is up to the client of the editor to use the return
 value, but it doesn't need to if it doesn't want to.

### Parameters:
anEvent - the event the editor should use to start
 				editing

### Returns:
true if the editor would like the editing cell to be selected;
    otherwise returns false
### See Also:
<a href='#isCellEditable'>isCellEditable</a> <br>

<a href="https://github.com/autoplot/dev/search?q=shouldSelectCell&unscoped_q=shouldSelectCell">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showDialog"></a>
# showDialog
showDialog(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showDialog&unscoped_q=showDialog">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="stopCellEditing"></a>
# stopCellEditing
stopCellEditing(  ) &rarr; boolean

Tells the editor to stop editing and accept any partially edited
 value as the value of the editor.  The editor returns false if
 editing was not stopped; this is useful for editors that validate
 and can not accept invalid entries.

### Returns:
true if editing was stopped; false otherwise

<a href="https://github.com/autoplot/dev/search?q=stopCellEditing&unscoped_q=stopCellEditing">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="supportsCustomEditor"></a>
# supportsCustomEditor
supportsCustomEditor(  ) &rarr; boolean

Determines whether this property editor supports a custom editor.

### Returns:
True if the propertyEditor can provide a custom editor.

<a href="https://github.com/autoplot/dev/search?q=supportsCustomEditor&unscoped_q=supportsCustomEditor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

