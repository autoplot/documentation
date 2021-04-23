# org.das2.components.propertyeditor.PropertyEditorThis class implements a Hierarchical property editor
PropertyEditor( Object bean )
create a PropertyEditor for the bean.

***
<a name="MULTIPLE"></a>
# MULTIPLE



***
<a name="addSaveAction"></a>
# addSaveAction
addSaveAction( javax.swing.AbstractAction abstractAction ) &rarr; void

add a save button, and perform the given action.

### Parameters:
abstractAction - the action to perform.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addSaveAction&unscoped_q=addSaveAction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createPeersEditor"></a>
# createPeersEditor
createPeersEditor( Object leader, java.lang.Object[] peers ) &rarr; PropertyEditor

create a PropertyEditor when we are editing several beans at once.

### Parameters:
leader - the leader bean, which is used to get settings for all components.
<br>peers - the peers, which must all be instances of the leader's class.

### Returns:
a PropertyEditor for editing several beans at once.

<a href="https://github.com/autoplot/dev/search?q=createPeersEditor&unscoped_q=createPeersEditor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="doLayout"></a>
# doLayout
doLayout(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=doLayout&unscoped_q=doLayout">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDialog"></a>
# getDialog
getDialog( java.awt.Component c ) &rarr; JDialog

allow clients to get at the dialog so it can be positioned.

### Parameters:
c - parent, if initializing.

### Returns:
the dialog.

<a href="https://github.com/autoplot/dev/search?q=getDialog&unscoped_q=getDialog">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getListenForExternalChanges"></a>
# getListenForExternalChanges
getListenForExternalChanges(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=getListenForExternalChanges&unscoped_q=getListenForExternalChanges">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isBean"></a>
# isBean
isBean( Object lbean ) &rarr; boolean

return true if the object is a Java Bean that fires property change events.
 This checks to see if listeners can be registered.

### Parameters:
lbean - an object which may be a bean

### Returns:
true if the object has an addPropertyChangeListener method.

<a href="https://github.com/autoplot/dev/search?q=isBean&unscoped_q=isBean">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="refresh"></a>
# refresh
refresh(  ) &rarr; void

request a refresh, the same as if the "refresh" button was pressed.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=refresh&unscoped_q=refresh">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setListenForExternalChanges"></a>
# setListenForExternalChanges
setListenForExternalChanges( boolean v ) &rarr; void



### Parameters:
v - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setListenForExternalChanges&unscoped_q=setListenForExternalChanges">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showDialog"></a>
# showDialog
showDialog( java.awt.Component c ) &rarr; void



### Parameters:
c - a Component

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showDialog&unscoped_q=showDialog">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

showDialog( java.awt.Component c, String title, java.awt.Image icon ) &rarr; void<br>
***
<a name="showModalDialog"></a>
# showModalDialog
showModalDialog( java.awt.Component c ) &rarr; void



### Parameters:
c - a Component

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=showModalDialog&unscoped_q=showModalDialog">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

