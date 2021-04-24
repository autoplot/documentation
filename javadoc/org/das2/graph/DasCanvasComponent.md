# org.das2.graph.DasCanvasComponent

Super class providing base functionality for all canvas components such as 
 DasAxis, DasPlot, and DasLabel.

# DasCanvasComponent( )
constructs a DasCanvasComponent, creating the
 DasMouseInputAdapter for it and assigning a
 default name to it.

***
<a name="PROPERTIES_ACTION"></a>
# PROPERTIES_ACTION

action for entering the properties editor.

***
<a name="PROP_OPAQUEBACKGROUND"></a>
# PROP_OPAQUEBACKGROUND



***
<a name="acceptContext"></a>
# acceptContext
acceptContext( int x, int y ) &rarr; boolean

returns true if the component is suitable context for the point.  For example,
 the operator right-clicks at the point, is this point a transparent region of
 the component, and accepting context would be confusing to the operator?  This
 was first introduced to support the annotation component, which draws a compact
 background bubble around a message, which is typically smaller than its bounds,
 plus an arrow.

### Parameters:
x - the x location on the canvas, with (0,0) being the upper-left corner.
<br>y - the y location on the canvas, with (0,0) being the upper-left corner.

### Returns:
true if the component accepts the context at this point.

<a href="https://github.com/autoplot/dev/search?q=acceptContext&unscoped_q=acceptContext">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addMouseModule"></a>
# addMouseModule
addMouseModule( org.das2.event.MouseModule module ) &rarr; void

Add the MouseModule to the list of MouseModules
 attached to the component via the DasMouseInputAdapter.
 MouseModules will appear the in the order that they
 are added.

### Parameters:
module - the mouse module to add

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/event/MouseModule.md'>org.das2.event.MouseModule</a> <br>

<a href="https://github.com/autoplot/dev/search?q=addMouseModule&unscoped_q=addMouseModule">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getActions"></a>
# getActions
getActions(  ) &rarr; Action

return a list of actions.  This is used by the DasMouseInputAdapter.

### Returns:
the actions this provides.

<a href="https://github.com/autoplot/dev/search?q=getActions&unscoped_q=getActions">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getActiveRegion"></a>
# getActiveRegion
getActiveRegion(  ) &rarr; Shape

returns the active region of the canvas component, which is not necessarily the bounds.

### Returns:
the active region of the canvas component

<a href="https://github.com/autoplot/dev/search?q=getActiveRegion&unscoped_q=getActiveRegion">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCanvas"></a>
# getCanvas
getCanvas(  ) &rarr; DasCanvas

get the DasCanvas which contains this DasCanvasComponent.

### Returns:
the DasCanvas which contains this DasCanvasComponent.

<a href="https://github.com/autoplot/dev/search?q=getCanvas&unscoped_q=getCanvas">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getColumn"></a>
# getColumn
getColumn(  ) &rarr; DasColumn

accessor for the DasColumn used for positioning the component.

### Returns:
DasColumn used for positioning the component.

<a href="https://github.com/autoplot/dev/search?q=getColumn&unscoped_q=getColumn">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDasMouseInputAdapter"></a>
# getDasMouseInputAdapter
getDasMouseInputAdapter(  ) &rarr; DasMouseInputAdapter

Get the DasMouseInputAdapter, which handles mouse input for the component.

### Returns:
the dasMouseInputAdapter.

<a href="https://github.com/autoplot/dev/search?q=getDasMouseInputAdapter&unscoped_q=getDasMouseInputAdapter">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDasName"></a>
# getDasName
getDasName(  ) &rarr; String

Get the String identifier for the component which identifies
 the component within the application.  This name should be
 consistent between sessions of an application, where
 applicable, for persistent state support.

### Returns:
the name of the component.

<a href="https://github.com/autoplot/dev/search?q=getDasName&unscoped_q=getDasName">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getEmSize"></a>
# getEmSize
getEmSize(  ) &rarr; double

convenient method intended to encourage use of em's.  returns the em size for the canvas.  
 We define the em size as the height of the component's font.

### Returns:
the height of the component's font.

<a href="https://github.com/autoplot/dev/search?q=getEmSize&unscoped_q=getEmSize">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFont"></a>
# getFont
getFont(  ) &rarr; Font

return the font used to paint the component.

### Returns:
the font.

<a href="https://github.com/autoplot/dev/search?q=getFont&unscoped_q=getFont">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLineThicknessDouble"></a>
# getLineThicknessDouble
getLineThicknessDouble( String lineThickness ) &rarr; double

return the thickness of the lines (in points or pixels), as specified
 in the lineThickness parameter.  Example inputs include "", "1px", and
 ".1em".

### Parameters:
lineThickness - a String

### Returns:
a double


<a href="https://github.com/autoplot/dev/search?q=getLineThicknessDouble&unscoped_q=getLineThicknessDouble">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRow"></a>
# getRow
getRow(  ) &rarr; DasRow

accessor for the DasRow used for positioning the component.

### Returns:
DasRow used for positioning the component.

<a href="https://github.com/autoplot/dev/search?q=getRow&unscoped_q=getRow">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isOpaqueBackground"></a>
# isOpaqueBackground
isOpaqueBackground(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isOpaqueBackground&unscoped_q=isOpaqueBackground">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeMouseModule"></a>
# removeMouseModule
removeMouseModule( org.das2.event.MouseModule module ) &rarr; void

Remove the MouseModule from the list of MouseModules
 attached to the component via the DasMouseInputAdapter.

### Parameters:
module - the mouse module to remove

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/event/MouseModule.md'>org.das2.event.MouseModule</a> <br>

<a href="https://github.com/autoplot/dev/search?q=removeMouseModule&unscoped_q=removeMouseModule">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resize"></a>
# resize
resize(  ) &rarr; void

Called by the DasCanvas layout manager to request this component
 to set its bounds.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resize&unscoped_q=resize">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setColumn"></a>
# setColumn
setColumn( org.das2.graph.DasColumn c ) &rarr; void

set the DasColumn for positioning the component horizontally.
 The current column is disconnected, and a propertyChange is
 fired.

### Parameters:
c - the DasColumn

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setColumn&unscoped_q=setColumn">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDasName"></a>
# setDasName
setDasName( String name ) &rarr; void

Set the String identifier for the component which identifies
 the component within the application.  This name should be
 consistent between sessions of an application, where
 applicable, for persistent state support.  For example,
 "timeAxis1" or "theTimeAxis"

### Parameters:
name - unique String identifying the component within
 the application.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDasName&unscoped_q=setDasName">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setOpaqueBackground"></a>
# setOpaqueBackground
setOpaqueBackground( boolean opaqueBackground ) &rarr; void



### Parameters:
opaqueBackground - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setOpaqueBackground&unscoped_q=setOpaqueBackground">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRow"></a>
# setRow
setRow( org.das2.graph.DasRow r ) &rarr; void

set the DasRow for positioning the component vertically.
 The current row is disconnected, and a propertyChange is
 fired.

### Parameters:
r - the DasRow

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRow&unscoped_q=setRow">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showProperties"></a>
# showProperties
showProperties(  ) &rarr; void

popup the PropertyEditor for editing the state
 of this component.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showProperties&unscoped_q=showProperties">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
a concise String representation of the object.

<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="update"></a>
# update
update(  ) &rarr; void

posts an update event on the SystemEventQueue, indicating that work needs to be
 done to get the get the component back into a valid state.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=update&unscoped_q=update">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

