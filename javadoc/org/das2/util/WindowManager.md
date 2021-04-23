# org.das2.util.WindowManagerKeep track of window positions.  Windows should be passed by this class
 before they are realized, and the name property of the dialog will be 
 used to look up the last size and position.  When the window has a parent,
 the position is stored relative to the parent.  Finally when a window
 is dismissed, this class should be called again so that the 
 position is kept.
WindowManager( )


***
<a name="getInstance"></a>
# getInstance
getInstance(  ) &rarr; WindowManager



### Returns:
org.das2.util.WindowManager


<a href="https://github.com/autoplot/dev/search?q=getInstance&unscoped_q=getInstance">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="recallWindowSizePosition"></a>
# recallWindowSizePosition
recallWindowSizePosition( java.awt.Window window ) &rarr; void

call this before the window.

### Parameters:
window - the window.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=recallWindowSizePosition&unscoped_q=recallWindowSizePosition">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="recordWindowSizePosition"></a>
# recordWindowSizePosition
recordWindowSizePosition( java.awt.Window window ) &rarr; void

record the final position of the dialog.  This will store the 
 position in the Java prefs manager for this class.

### Parameters:
window - the window

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=recordWindowSizePosition&unscoped_q=recordWindowSizePosition">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showConfirmDialog"></a>
# showConfirmDialog
showConfirmDialog( java.awt.Component parent, javax.swing.JPanel omessage, String title, int optionType, int messageType, javax.swing.Icon icon ) &rarr; int

TODO: this will show the icon.

### Parameters:
parent - a Component
<br>omessage - a JPanel
<br>title - a String
<br>optionType - an int
<br>messageType - an int
<br>icon - an Icon

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=showConfirmDialog&unscoped_q=showConfirmDialog">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

showConfirmDialog( java.awt.Component parent, Object omessage, String title, int optionType ) &rarr; int<br>
***
<a name="showModalDialog"></a>
# showModalDialog
showModalDialog( java.awt.Dialog dia ) &rarr; void

convenient method for showing dialog which is modal.

### Parameters:
dia - the dialog that is set to be modal.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showModalDialog&unscoped_q=showModalDialog">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

