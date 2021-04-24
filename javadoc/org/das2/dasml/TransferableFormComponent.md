# org.das2.dasml.TransferableFormComponent



# TransferableFormComponent( org.das2.dasml.FormPanel panel )


# TransferableFormComponent( org.das2.dasml.FormText text )


# TransferableFormComponent( org.das2.dasml.FormTextField textField )


# TransferableFormComponent( org.das2.dasml.FormButton button )


# TransferableFormComponent( org.das2.dasml.FormCheckBox checkBox )


# TransferableFormComponent( org.das2.dasml.FormRadioButtonGroup buttonGroup )


# TransferableFormComponent( org.das2.dasml.FormRadioButton radioButton )


# TransferableFormComponent( org.das2.dasml.FormTab form )


# TransferableFormComponent( org.das2.dasml.FormChoice choice )


# TransferableFormComponent( org.das2.dasml.FormList list )


# TransferableFormComponent( org.das2.dasml.FormWindow window )


***
<a name="COMPONENT_FLAVOR"></a>
# COMPONENT_FLAVOR



***
<a name="PANEL_FLAVOR"></a>
# PANEL_FLAVOR



***
<a name="TEXT_FLAVOR"></a>
# TEXT_FLAVOR



***
<a name="TEXTFIELD_FLAVOR"></a>
# TEXTFIELD_FLAVOR



***
<a name="BUTTON_FLAVOR"></a>
# BUTTON_FLAVOR



***
<a name="CHECKBOX_FLAVOR"></a>
# CHECKBOX_FLAVOR



***
<a name="BUTTONGROUP_FLAVOR"></a>
# BUTTONGROUP_FLAVOR



***
<a name="RADIOBUTTON_FLAVOR"></a>
# RADIOBUTTON_FLAVOR



***
<a name="TAB_FLAVOR"></a>
# TAB_FLAVOR



***
<a name="CHOICE_FLAVOR"></a>
# CHOICE_FLAVOR



***
<a name="LIST_FLAVOR"></a>
# LIST_FLAVOR



***
<a name="WINDOW_FLAVOR"></a>
# WINDOW_FLAVOR



***
<a name="DASML_FRAGMENT_FLAVOR"></a>
# DASML_FRAGMENT_FLAVOR



***
<a name="getTransferData"></a>
# getTransferData
getTransferData( java.awt.datatransfer.DataFlavor flavor ) &rarr; Object

Returns an object which represents the data to be transferred.  The class
 of the object returned is defined by the representation class of the flavor.

### Parameters:
flavor - the requested flavor for the data

### Returns:
java.lang.Object

### See Also:
<a href='DataFlavor.md#getRepresentationClass'>DataFlavor#getRepresentationClass</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getTransferData&unscoped_q=getTransferData">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTransferDataFlavors"></a>
# getTransferDataFlavors
getTransferDataFlavors(  ) &rarr; DataFlavor

Returns an array of DataFlavor objects indicating the flavors the data
 can be provided in.  The array should be ordered according to preference
 for providing the data (from most richly descriptive to least descriptive).

### Returns:
an array of data flavors in which this data can be transferred

<a href="https://github.com/autoplot/dev/search?q=getTransferDataFlavors&unscoped_q=getTransferDataFlavors">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDataFlavorSupported"></a>
# isDataFlavorSupported
isDataFlavorSupported( java.awt.datatransfer.DataFlavor flavor ) &rarr; boolean

Returns whether or not the specified data flavor is supported for
 this object.

### Parameters:
flavor - the requested flavor for the data

### Returns:
boolean indicating whether or not the data flavor is supported

<a href="https://github.com/autoplot/dev/search?q=isDataFlavorSupported&unscoped_q=isDataFlavorSupported">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

