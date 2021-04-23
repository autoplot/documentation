# org.autoplot.datasource.RecentComboBoxModelProvide a comboBoxModel so that the ComboBox remembers recent entries.  This listens for ActionEvents from a
 JComboBox and adds valid items to its droplist.  The recent entries are stored in the bookmarks folder in the
 file "recent.PREF.txt" where PREF is a string assigned to this object identifying the theme, such as
 "timerange".  Specifically, the event is validated and recorded into the file, then the file is loaded,
 sorted and saved again.
RecentComboBoxModel( String pref )


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
<a name="setVerifier"></a>
# setVerifier
setVerifier( org.autoplot.datasource.RecentComboBoxModel.InputVerifier v ) &rarr; void

allow filtering of invalid entries so they aren't recorded in history.

### Parameters:
v - a RecentComboBoxModel.InputVerifier

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setVerifier&unscoped_q=setVerifier">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

