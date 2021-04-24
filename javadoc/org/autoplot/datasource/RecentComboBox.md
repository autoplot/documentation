# org.autoplot.datasource.RecentComboBox

decorate a comboBox so that it remembers recent entries.  This listens for ActionEvents from a JComboBox
 and adds valid items to its droplist.  The recent entries are stored in the bookmarks folder in the file
 "recent.PREF.txt" where PREF is a string assigned to this object identifying the theme, such as "timerange".
 Specifically, the event is validated and recorded into the file, then the file is loaded, sorted and saved
 again.

# RecentComboBox( )


***
<a name="PREF_NODE_TIMERANGE"></a>
# PREF_NODE_TIMERANGE



***
<a name="actionPerformed"></a>
# actionPerformed
actionPerformed( java.awt.event.ActionEvent e ) &rarr; void



### Parameters:
e - an ActionEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=actionPerformed&unscoped_q=actionPerformed">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addToRecent"></a>
# addToRecent
addToRecent( String s ) &rarr; void

add the item to the list of recent entries.  This will reload the
 recent file, probably firing events.

### Parameters:
s - the item

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addToRecent&unscoped_q=addToRecent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addToRecent( String s, boolean reload ) &rarr; void<br>
***
<a name="getText"></a>
# getText
getText(  ) &rarr; String

get the string value, which is also the getSelectedItem.

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getText&unscoped_q=getText">[search for examples]</a>
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
<a name="setPreferenceNode"></a>
# setPreferenceNode
setPreferenceNode( String pref ) &rarr; void

associate the history with a file.  This should be called immediately after creating the object.

### Parameters:
pref - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPreferenceNode&unscoped_q=setPreferenceNode">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setText"></a>
# setText
setText( String text ) &rarr; void

to make it easier to convert GUIs with JTextFields to RecentComboBoxes, setText is available.

### Parameters:
text - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setText&unscoped_q=setText">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setVerifier"></a>
# setVerifier
setVerifier( org.autoplot.datasource.InputVerifier v ) &rarr; void

allow filtering of invalid entries so they aren't recorded in history.

### Parameters:
v - an InputVerifier

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setVerifier&unscoped_q=setVerifier">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

