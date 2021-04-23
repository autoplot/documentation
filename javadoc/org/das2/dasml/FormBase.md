# org.das2.dasml.FormBaseThis class displays a Java form that is generated from an XML Document that is provided as input.
FormBase( java.net.URL url, org.xml.sax.ErrorHandler eh, boolean editable )
Creates a FormBase object

FormBase( java.io.InputStream in, org.xml.sax.ErrorHandler eh, boolean editable )


FormBase( java.io.Reader reader, org.xml.sax.ErrorHandler eh, boolean editable )


FormBase( boolean editable )


***
<a name="addForm"></a>
# addForm
addForm( org.das2.dasml.FormTab form ) &rarr; void



### Parameters:
form - a FormTab

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addForm&unscoped_q=addForm">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addWindow"></a>
# addWindow
addWindow( org.das2.dasml.FormWindow window ) &rarr; void



### Parameters:
window - a FormWindow

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addWindow&unscoped_q=addWindow">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="checkValue"></a>
# checkValue
checkValue( String name, java.lang.Class type, String tag ) &rarr; Object



### Parameters:
name - a String
<br>type - a java.lang.Class
<br>tag - a String

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=checkValue&unscoped_q=checkValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="deregisterComponent"></a>
# deregisterComponent
deregisterComponent(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=deregisterComponent&unscoped_q=deregisterComponent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDOMElement"></a>
# getDOMElement
getDOMElement( org.w3c.dom.Document document ) &rarr; Element



### Parameters:
document - a Document

### Returns:
org.w3c.dom.Element


<a href="https://github.com/autoplot/dev/search?q=getDOMElement&unscoped_q=getDOMElement">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDasApplication"></a>
# getDasApplication
getDasApplication(  ) &rarr; DasApplication



### Returns:
org.das2.DasApplication


<a href="https://github.com/autoplot/dev/search?q=getDasApplication&unscoped_q=getDasApplication">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDasName"></a>
# getDasName
getDasName(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getDasName&unscoped_q=getDasName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDnDSupport"></a>
# getDnDSupport
getDnDSupport(  ) &rarr; DnDSupport



### Returns:
org.das2.util.DnDSupport


<a href="https://github.com/autoplot/dev/search?q=getDnDSupport&unscoped_q=getDnDSupport">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getEditingMode"></a>
# getEditingMode
getEditingMode(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=getEditingMode&unscoped_q=getEditingMode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getForm"></a>
# getForm
getForm(  ) &rarr; FormBase



### Returns:
org.das2.dasml.FormBase


<a href="https://github.com/autoplot/dev/search?q=getForm&unscoped_q=getForm">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getWindowList"></a>
# getWindowList
getWindowList(  ) &rarr; List



### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=getWindowList&unscoped_q=getWindowList">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="invoke"></a>
# invoke
invoke( String name, java.lang.String[] args ) &rarr; Object



### Parameters:
name - a String
<br>args - a java.lang.String[]

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=invoke&unscoped_q=invoke">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="registerComponent"></a>
# registerComponent
registerComponent(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=registerComponent&unscoped_q=registerComponent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeWindow"></a>
# removeWindow
removeWindow( org.das2.dasml.FormWindow window ) &rarr; void



### Parameters:
window - a FormWindow

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeWindow&unscoped_q=removeWindow">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="serialize"></a>
# serialize
serialize( java.io.OutputStream out ) &rarr; void

Writes the XML representation of this form to the specified
 byte stream

### Parameters:
out - the specified byte stream

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=serialize&unscoped_q=serialize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDasName"></a>
# setDasName
setDasName( String name ) &rarr; void



### Parameters:
name - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDasName&unscoped_q=setDasName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setEditingMode"></a>
# setEditingMode
setEditingMode( boolean b ) &rarr; void



### Parameters:
b - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setEditingMode&unscoped_q=setEditingMode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="startDrag"></a>
# startDrag
startDrag( int x, int y, int action, java.awt.event.MouseEvent evt ) &rarr; boolean



### Parameters:
x - an int
<br>y - an int
<br>action - an int
<br>evt - a MouseEvent

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=startDrag&unscoped_q=startDrag">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

