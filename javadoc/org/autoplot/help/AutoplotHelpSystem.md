# org.autoplot.help.AutoplotHelpSystemEncapsulates JavaHelp functionality for convenient access by components.
***
<a name="displayDefaultHelp"></a>
# displayDefaultHelp
displayDefaultHelp(  ) &rarr; void

Display the help window with default page displayed

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=displayDefaultHelp&unscoped_q=displayDefaultHelp">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="displayHelpFromEvent"></a>
# displayHelpFromEvent
displayHelpFromEvent( java.awt.event.ActionEvent e ) &rarr; void



### Parameters:
e - an ActionEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=displayHelpFromEvent&unscoped_q=displayHelpFromEvent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

displayHelpFromEvent( java.awt.event.ActionEvent e, Object focus ) &rarr; void<br>
***
<a name="getHelpSystem"></a>
# getHelpSystem
getHelpSystem(  ) &rarr; AutoplotHelpSystem

Returns a reference to the help system, or <code>null</code> if it hasn't been
 initialized.

### Returns:
the single instance

<a href="https://github.com/autoplot/dev/search?q=getHelpSystem&unscoped_q=getHelpSystem">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="initialize"></a>
# initialize
initialize( java.awt.Component uiBase ) &rarr; void



### Parameters:
uiBase - a Component

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=initialize&unscoped_q=initialize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="registerHelpID"></a>
# registerHelpID
registerHelpID( java.awt.Component c, String helpID ) &rarr; void

Components can call this method to register a help ID string.  The JavaHelp
 system will use this ID string as a hash key to find the correct HTML file
 to display for context-sensitive help.

 TitledBorder panels and children that are TitledBorders will have their
 title behave like a link into the documentation.

### Parameters:
c - a Component
<br>helpID - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=registerHelpID&unscoped_q=registerHelpID">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="unregisterHelpID"></a>
# unregisterHelpID
unregisterHelpID( java.awt.Component c, String helpID ) &rarr; void

remove the component.

### Parameters:
c - a Component
<br>helpID - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=unregisterHelpID&unscoped_q=unregisterHelpID">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

