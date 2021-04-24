# org.autoplot.bookmarks.DelayMenu

JMenu that delays creating children until the folder is exposed.  Otherwise we would have thousands of
 JMenuItems created at once, which showed to be slow.

***
<a name="calculateMenu"></a>
# calculateMenu
calculateMenu( javax.swing.JMenu menu, java.util.List bookmarks, java.awt.event.ActionListener a ) &rarr; void

calculate a menu from the bookmarks, where when a bookmark is selected, an ActionEvent
 is fired with the actionCommand equal to the URI.  This was introduced to support
 invoking one of a set of scripts.

### Parameters:
menu - a JMenu
<br>bookmarks - a java.util.List
<br>a - an ActionListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=calculateMenu&unscoped_q=calculateMenu">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

