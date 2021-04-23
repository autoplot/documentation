# org.das2.event.DasMouseInputAdapter

DasMouseInputAdapter delegates mouse and key events to mouse modules, which
 do something with the events.  Also, mouse events are promoted to MouseDragEvents
 which conveniently store information about the entire drag gesture.

 The base class of MouseModule has do-nothing stubs for KeyListener, MouseListener,
 MouseMotionListener, and MouseWheelListener, which can be implemented if the
 module wants to do something with these events.  Also MouseDragEvents will be
 sent to the module as its DragRenderer has requested: after the mouse release,
 during the drag, or when keys are pressed.

 The module will first receive the low-level events before receiving the MouseDragEvents.

# DasMouseInputAdapter( org.das2.graph.DasCanvasComponent parent )
Create a DasMouseInputAdapter to handle mouse events for the component.

***
<a name="NULL_FEEDBACK"></a>
# NULL_FEEDBACK



***
<a name="addMenu"></a>
# addMenu
addMenu( String label ) &rarr; JMenu

return a menu with font to match LAF.

### Parameters:
label - a String

### Returns:
a javax.swing.JMenu


<a href="https://github.com/autoplot/dev/search?q=addMenu&unscoped_q=addMenu">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addMenuItem"></a>
# addMenuItem
addMenuItem( java.awt.Component b ) &rarr; void



### Parameters:
b - a Component

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addMenuItem&unscoped_q=addMenuItem">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addMouseModule"></a>
# addMouseModule
addMouseModule( org.das2.event.MouseModule module ) &rarr; void

add a mouse module to the list of available modules.  If a module with the same
 label exists already, it will be replaced.

### Parameters:
module - the module

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addMouseModule&unscoped_q=addMouseModule">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="cancel"></a>
# cancel
cancel(  ) &rarr; void

allow clients to cancel, to take the same action as if cancel 
 were pressed.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=cancel&unscoped_q=cancel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getActive"></a>
# getActive
getActive(  ) &rarr; MouseModule

return the active mouse module, for scripting.  Active means the 
 button has been pressed, etc.

### Returns:
null or the active module.

<a href="https://github.com/autoplot/dev/search?q=getActive&unscoped_q=getActive">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFeedback"></a>
# getFeedback
getFeedback(  ) &rarr; Feedback

get the feedback object, so its message can be set.

### Returns:
the feedback object.

<a href="https://github.com/autoplot/dev/search?q=getFeedback&unscoped_q=getFeedback">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getKeyAdapter"></a>
# getKeyAdapter
getKeyAdapter(  ) &rarr; KeyAdapter



### Returns:
java.awt.event.KeyAdapter


<a href="https://github.com/autoplot/dev/search?q=getKeyAdapter&unscoped_q=getKeyAdapter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getModuleByLabel"></a>
# getModuleByLabel
getModuleByLabel( String label ) &rarr; MouseModule

remove the mouse module with the label.

### Parameters:
label - the label (case-sensitive)

### Returns:
null if not found, or the module.

<a href="https://github.com/autoplot/dev/search?q=getModuleByLabel&unscoped_q=getModuleByLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMouseModule"></a>
# getMouseModule
getMouseModule( int i ) &rarr; MouseModule



### Parameters:
i - an int

### Returns:
org.das2.event.MouseModule


<a href="https://github.com/autoplot/dev/search?q=getMouseModule&unscoped_q=getMouseModule">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMouseModules"></a>
# getMouseModules
getMouseModules(  ) &rarr; MouseModule



### Returns:
org.das2.event.MouseModule[]


<a href="https://github.com/autoplot/dev/search?q=getMouseModules&unscoped_q=getMouseModules">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMousePressPosition"></a>
# getMousePressPosition
getMousePressPosition(  ) &rarr; Point

returns the position of the last mouse press.  This is a hack so that
 the mouse position can be obtained to get the context of the press.
 The result point is in the parent's coordinate system.

### Returns:
the position of the mouse press, or null if a press has not been received.
### See Also:
<a href='#getMousePressPositionOnCanvas'>getMousePressPositionOnCanvas()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getMousePressPosition&unscoped_q=getMousePressPosition">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMousePressPositionOnCanvas"></a>
# getMousePressPositionOnCanvas
getMousePressPositionOnCanvas(  ) &rarr; Point

return the position of the last mouse press, in the canvas coordinate frame.

### Returns:
the position of the mouse press in the canvas coordinate frame, or null if a press has not been received.
### See Also:
<a href='#getMousePressPosition'>getMousePressPosition()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getMousePressPositionOnCanvas&unscoped_q=getMousePressPositionOnCanvas">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNumInserted"></a>
# getNumInserted
getNumInserted(  ) &rarr; int

return number of elements for diagnostic purposes.

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=getNumInserted&unscoped_q=getNumInserted">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPinned"></a>
# getPinned
getPinned(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=getPinned&unscoped_q=getPinned">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPrimaryModule"></a>
# getPrimaryModule
getPrimaryModule(  ) &rarr; MouseModule



### Returns:
org.das2.event.MouseModule


<a href="https://github.com/autoplot/dev/search?q=getPrimaryModule&unscoped_q=getPrimaryModule">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPrimaryModuleByLabel"></a>
# getPrimaryModuleByLabel
getPrimaryModuleByLabel(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getPrimaryModuleByLabel&unscoped_q=getPrimaryModuleByLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPrimaryPopupMenu"></a>
# getPrimaryPopupMenu
getPrimaryPopupMenu(  ) &rarr; JPopupMenu

added so ColumnColumnConnector could delegate to DasPlot's adapter.

### Returns:
a javax.swing.JPopupMenu


<a href="https://github.com/autoplot/dev/search?q=getPrimaryPopupMenu&unscoped_q=getPrimaryPopupMenu">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSecondaryModule"></a>
# getSecondaryModule
getSecondaryModule(  ) &rarr; MouseModule



### Returns:
org.das2.event.MouseModule


<a href="https://github.com/autoplot/dev/search?q=getSecondaryModule&unscoped_q=getSecondaryModule">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSecondaryModuleByLabel"></a>
# getSecondaryModuleByLabel
getSecondaryModuleByLabel(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getSecondaryModuleByLabel&unscoped_q=getSecondaryModuleByLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSecondaryPopupMenu"></a>
# getSecondaryPopupMenu
getSecondaryPopupMenu(  ) &rarr; JPopupMenu

access popup menu so that synchronized blocks are minimized.

### Returns:
a javax.swing.JPopupMenu


<a href="https://github.com/autoplot/dev/search?q=getSecondaryPopupMenu&unscoped_q=getSecondaryPopupMenu">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isHoverHighlite"></a>
# isHoverHighlite
isHoverHighlite(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isHoverHighlite&unscoped_q=isHoverHighlite">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mouseDragged"></a>
# mouseDragged
mouseDragged( java.awt.event.MouseEvent e ) &rarr; void



### Parameters:
e - a MouseEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mouseDragged&unscoped_q=mouseDragged">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mouseEntered"></a>
# mouseEntered
mouseEntered( java.awt.event.MouseEvent e ) &rarr; void



### Parameters:
e - a MouseEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mouseEntered&unscoped_q=mouseEntered">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mouseExited"></a>
# mouseExited
mouseExited( java.awt.event.MouseEvent e ) &rarr; void



### Parameters:
e - a MouseEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mouseExited&unscoped_q=mouseExited">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mouseMoved"></a>
# mouseMoved
mouseMoved( java.awt.event.MouseEvent e ) &rarr; void



### Parameters:
e - a MouseEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mouseMoved&unscoped_q=mouseMoved">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mousePressed"></a>
# mousePressed
mousePressed( java.awt.event.MouseEvent e ) &rarr; void



### Parameters:
e - a MouseEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mousePressed&unscoped_q=mousePressed">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mouseReleased"></a>
# mouseReleased
mouseReleased( java.awt.event.MouseEvent e ) &rarr; void



### Parameters:
e - a MouseEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mouseReleased&unscoped_q=mouseReleased">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mouseWheelMoved"></a>
# mouseWheelMoved
mouseWheelMoved( java.awt.event.MouseWheelEvent e ) &rarr; void

the mouse wheel was turned so many units.  
 Delegate this to the primary module, so that if it is set to "ZoomX"
 then the mousewheel will be in just the X direction.

### Parameters:
e - the mouse wheel event

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=mouseWheelMoved&unscoped_q=mouseWheelMoved">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="paint"></a>
# paint
paint( java.awt.Graphics g1 ) &rarr; void



### Parameters:
g1 - a Graphics

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=paint&unscoped_q=paint">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="releaseAll"></a>
# releaseAll
releaseAll(  ) &rarr; void

remove all references to mouse modules

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=releaseAll&unscoped_q=releaseAll">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeMenuItem"></a>
# removeMenuItem
removeMenuItem( String label ) &rarr; void

hack to provide way to get rid of "Dump Data".

### Parameters:
label - string to search for.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeMenuItem&unscoped_q=removeMenuItem">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeMouseModule"></a>
# removeMouseModule
removeMouseModule( org.das2.event.MouseModule module ) &rarr; void



### Parameters:
module - a MouseModule

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeMouseModule&unscoped_q=removeMouseModule">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="replaceMenuItem"></a>
# replaceMenuItem
replaceMenuItem( String label, java.awt.Component b ) &rarr; void

provide a way for an alternate implementation to be added at the position
 occupied by "label".

### Parameters:
label - the parameter to find, e.h.
<br>b - a Component

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=replaceMenuItem&unscoped_q=replaceMenuItem">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="replaceMouseModule"></a>
# replaceMouseModule
replaceMouseModule( org.das2.event.MouseModule oldModule, org.das2.event.MouseModule newModule ) &rarr; void



### Parameters:
oldModule - a MouseModule
<br>newModule - a MouseModule

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=replaceMouseModule&unscoped_q=replaceMouseModule">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resetName"></a>
# resetName
resetName( String name ) &rarr; void

set the name of the menus to help with debugging

### Parameters:
name - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resetName&unscoped_q=resetName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFeedback"></a>
# setFeedback
setFeedback( org.das2.event.DasMouseInputAdapter.Feedback f ) &rarr; void



### Parameters:
f - a DasMouseInputAdapter.Feedback

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFeedback&unscoped_q=setFeedback">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setHoverHighlite"></a>
# setHoverHighlite
setHoverHighlite( boolean value ) &rarr; void

glow the outline of the mouse area, for development.

### Parameters:
value - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setHoverHighlite&unscoped_q=setHoverHighlite">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setMenuLabel"></a>
# setMenuLabel
setMenuLabel( String id ) &rarr; void



### Parameters:
id - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMenuLabel&unscoped_q=setMenuLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setMouseModule"></a>
# setMouseModule
setMouseModule( int i, org.das2.event.MouseModule mouseModule ) &rarr; void

//TODO: check this
 Setter for property mouseModules.

### Parameters:
i - the index
<br>mouseModule - the new mouseModule to use.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMouseModule&unscoped_q=setMouseModule">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setMousePressPositionOnCanvas"></a>
# setMousePressPositionOnCanvas
setMousePressPositionOnCanvas( java.awt.Point p ) &rarr; void

set the mouse press position, so that it is a bean property and one
 DasMouseInputAdapter can delegate to another.

### Parameters:
p - a Point

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMousePressPositionOnCanvas&unscoped_q=setMousePressPositionOnCanvas">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPinned"></a>
# setPinned
setPinned( boolean b ) &rarr; void



### Parameters:
b - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPinned&unscoped_q=setPinned">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPrimaryModule"></a>
# setPrimaryModule
setPrimaryModule( org.das2.event.MouseModule module ) &rarr; void

set the primary module, the module receiving left-button events, to the
 module provided.  If the module is not already loaded, implicitly addMouseModule
 is called.

### Parameters:
module - the module

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPrimaryModule&unscoped_q=setPrimaryModule">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPrimaryModuleByLabel"></a>
# setPrimaryModuleByLabel
setPrimaryModuleByLabel( String label ) &rarr; void



### Parameters:
label - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPrimaryModuleByLabel&unscoped_q=setPrimaryModuleByLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSecondaryModule"></a>
# setSecondaryModule
setSecondaryModule( org.das2.event.MouseModule module ) &rarr; void

set the secondary module, the module receiving middle-button events, to the
 module provided.  If the module is not already loaded, implicitly addMouseModule
 is called.

### Parameters:
module - a MouseModule

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSecondaryModule&unscoped_q=setSecondaryModule">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSecondaryModuleByLabel"></a>
# setSecondaryModuleByLabel
setSecondaryModuleByLabel( String label ) &rarr; void



### Parameters:
label - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSecondaryModuleByLabel&unscoped_q=setSecondaryModuleByLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

