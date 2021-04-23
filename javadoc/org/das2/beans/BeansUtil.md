# org.das2.beans.BeansUtil

Utilities for JavaBeans conventions, allowing custom editors to be 
 used to edit JavaBeans with set/get properties.

# BeansUtil( )


***
<a name="asAccessLevelBeanInfo"></a>
# asAccessLevelBeanInfo
asAccessLevelBeanInfo( java.beans.BeanInfo beanInfo, java.lang.Class beanClass ) &rarr; AccessLevelBeanInfo

Returns an AccessLevelBeanInfo for the BeanInfo class, implementing the logic
 of how to handle implicit properties.

### Parameters:
beanInfo - a BeanInfo
<br>beanClass - a java.lang.Class

### Returns:
org.das2.beans.AccessLevelBeanInfo


<a href="https://github.com/autoplot/dev/search?q=asAccessLevelBeanInfo&unscoped_q=asAccessLevelBeanInfo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="findEditor"></a>
# findEditor
findEditor( java.lang.Class propertyClass ) &rarr; PropertyEditor



### Parameters:
propertyClass - a java.lang.Class

### Returns:
java.beans.PropertyEditor


<a href="https://github.com/autoplot/dev/search?q=findEditor&unscoped_q=findEditor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBeanInfo"></a>
# getBeanInfo
getBeanInfo( java.lang.Class c ) &rarr; BeanInfo



### Parameters:
c - a java.lang.Class

### Returns:
java.beans.BeanInfo


<a href="https://github.com/autoplot/dev/search?q=getBeanInfo&unscoped_q=getBeanInfo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getEditor"></a>
# getEditor
getEditor( java.beans.PropertyDescriptor pd ) &rarr; PropertyEditor

One-stop place to get the editor for the given propertyDescriptor.

### Parameters:
pd - the property descriptor

### Returns:
the editor

<a href="https://github.com/autoplot/dev/search?q=getEditor&unscoped_q=getEditor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPropertyDescriptors"></a>
# getPropertyDescriptors
getPropertyDescriptors( java.lang.Class c ) &rarr; PropertyDescriptor

Use reflection to get a list of all the property names for the class.
 The properties are returned in the order specified, and put inherited properties
 at the end of the list.  Implement the include/exclude logic.  
 
 This will not return write-only descriptors!!!

### Parameters:
c - a java.lang.Class

### Returns:
java.beans.PropertyDescriptor[]


<a href="https://github.com/autoplot/dev/search?q=getPropertyDescriptors&unscoped_q=getPropertyDescriptors">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPropertyNames"></a>
# getPropertyNames
getPropertyNames( java.beans.PropertyDescriptor[] propertyList ) &rarr; String



### Parameters:
propertyList - a java.beans.PropertyDescriptor[]

### Returns:
java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=getPropertyNames&unscoped_q=getPropertyNames">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getPropertyNames( java.lang.Class c ) &rarr; String<br>
***
<a name="registerEditor"></a>
# registerEditor
registerEditor( java.lang.Class beanClass, java.lang.Class editorClass ) &rarr; void

see BeanBindingDemo2.java

### Parameters:
beanClass - the bean class, e.g. Datum.class
<br>editorClass - the editor class, e.g. DatumEditor.class

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=registerEditor&unscoped_q=registerEditor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

