# org.das2.components.TearoffTabbedPaneLike the Swing TabbedPane, but this allows the tabs to be 
 removed to other windows or other TearoffTabbedPanes.
TearoffTabbedPane( )
create a new TearoffTabbedPane

***
<a name="addTab"></a>
# addTab
addTab( String title, javax.swing.Icon icon, java.awt.Component component ) &rarr; void



### Parameters:
title - a String
<br>icon - an Icon
<br>component - a Component

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addTab&unscoped_q=addTab">[search for examples]</a>

addTab( String title, java.awt.Component component ) &rarr; void<br>
addTab( String title, javax.swing.Icon icon, java.awt.Component component, String tip ) &rarr; void<br>
***
<a name="dock"></a>
# dock
dock( java.awt.Component c ) &rarr; void

return the component into this TearoffTabbedPane.

### Parameters:
c - the component.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dock&unscoped_q=dock">[search for examples]</a>

***
<a name="getFrameComponentListener"></a>
# getFrameComponentListener
getFrameComponentListener( java.awt.Component panel1, java.awt.Component frame1, java.awt.Component panel2, java.awt.Component frame2, Object direction ) &rarr; ComponentListener

get the listener that will keep the two JFrames close together

### Parameters:
panel1 - component within the master frame.
<br>frame1 - master frame that controls.
<br>panel2 - component within the compliant frame
<br>frame2 - compliant frame that follows.
<br>direction - the direction, which is STICK_RIGHT (private) or null

### Returns:
a listener

<a href="https://github.com/autoplot/dev/search?q=getFrameComponentListener&unscoped_q=getFrameComponentListener">[search for examples]</a>

***
<a name="getTabByTitle"></a>
# getTabByTitle
getTabByTitle( String title ) &rarr; Component

return the tab contents, the first tab with this name.

### Parameters:
title - a String

### Returns:
the component in this tab.

<a href="https://github.com/autoplot/dev/search?q=getTabByTitle&unscoped_q=getTabByTitle">[search for examples]</a>

***
<a name="hideMouseAdapter"></a>
# hideMouseAdapter
hideMouseAdapter(  ) &rarr; void

I needed a way to hide the mouseAdapter, since we can't do this automatically.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=hideMouseAdapter&unscoped_q=hideMouseAdapter">[search for examples]</a>

***
<a name="insertTab"></a>
# insertTab
insertTab( String title, javax.swing.Icon icon, java.awt.Component component, String tip, int index ) &rarr; void



### Parameters:
title - a String
<br>icon - an Icon
<br>component - a Component
<br>tip - a String
<br>index - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=insertTab&unscoped_q=insertTab">[search for examples]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

***
<a name="peek"></a>
# peek
peek(  ) &rarr; void

show all the tabs descriptions

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=peek&unscoped_q=peek">[search for examples]</a>

***
<a name="remove"></a>
# remove
remove( java.awt.Component c ) &rarr; void



### Parameters:
c - a Component

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=remove&unscoped_q=remove">[search for examples]</a>

***
<a name="removeTabAt"></a>
# removeTabAt
removeTabAt( int index ) &rarr; void



### Parameters:
index - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeTabAt&unscoped_q=removeTabAt">[search for examples]</a>

***
<a name="setSelectedIndex"></a>
# setSelectedIndex
setSelectedIndex( int index ) &rarr; void



### Parameters:
index - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSelectedIndex&unscoped_q=setSelectedIndex">[search for examples]</a>

***
<a name="setSelectedTab"></a>
# setSelectedTab
setSelectedTab( String title ) &rarr; void

this will set the selected tab, or raise the babysitter

### Parameters:
title - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSelectedTab&unscoped_q=setSelectedTab">[search for examples]</a>

***
<a name="slideRight"></a>
# slideRight
slideRight( int tabIndex ) &rarr; void

instead of undocking, "slide" the component into a second JFrame that follows the first.
 This may create the JFrame that accepts tabs.

### Parameters:
tabIndex - the tab to slide (0 is the left or first tab)

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=slideRight&unscoped_q=slideRight">[search for examples]</a>

***
<a name="tearOff"></a>
# tearOff
tearOff( int tabIndex, java.awt.Container newContainer ) &rarr; void



### Parameters:
tabIndex - an int
<br>newContainer - a Container

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=tearOff&unscoped_q=tearOff">[search for examples]</a>

