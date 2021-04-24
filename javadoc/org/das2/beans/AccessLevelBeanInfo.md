# org.das2.beans.AccessLevelBeanInfo

This class is designed to implement access levels for bean properties.
 The system property "edu.uiowa.physics.das.beans.AccessLevelBeanInfo.AccessLevel" will
 determine the access level of the bean.  The access levels that are currently supported
 are "ALL" and "END_USER".  The access level must be set prior to this class being loaded.

***
<a name="getAccessLevel"></a>
# getAccessLevel
getAccessLevel(  ) &rarr; AccessLevel

Returns the access level for AccessLevelBeanInfo objects.

### Returns:
org.das2.beans.AccessLevelBeanInfo.AccessLevel


<a href="https://github.com/autoplot/dev/search?q=getAccessLevel&unscoped_q=getAccessLevel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBeanDescriptor"></a>
# getBeanDescriptor
getBeanDescriptor(  ) &rarr; BeanDescriptor

get the descriptor for the class.

### Returns:
a java.beans.BeanDescriptor


<a href="https://github.com/autoplot/dev/search?q=getBeanDescriptor&unscoped_q=getBeanDescriptor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLock"></a>
# getLock
getLock(  ) &rarr; Object



### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=getLock&unscoped_q=getLock">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getProperty"></a>
# getProperty
getProperty( java.beans.PropertyDescriptor pd ) &rarr; Property

get the Property for the PropertyDescriptor.

### Parameters:
pd - a PropertyDescriptor

### Returns:
an org.das2.beans.AccessLevelBeanInfo.Property


<a href="https://github.com/autoplot/dev/search?q=getProperty&unscoped_q=getProperty">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPropertyDescriptors"></a>
# getPropertyDescriptors
getPropertyDescriptors( org.das2.beans.AccessLevelBeanInfo.PersistenceLevel persistenceLevel ) &rarr; PropertyDescriptor

convenient method that only returns the descriptors for the specified persistence level.
 Also implements the property inheritance.

### Parameters:
persistenceLevel - an AccessLevelBeanInfo.PersistenceLevel

### Returns:
java.beans.PropertyDescriptor[]


<a href="https://github.com/autoplot/dev/search?q=getPropertyDescriptors&unscoped_q=getPropertyDescriptors">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getPropertyDescriptors(  ) &rarr; PropertyDescriptor<br>
***
<a name="setAccessLevel"></a>
# setAccessLevel
setAccessLevel( org.das2.beans.AccessLevelBeanInfo.AccessLevel level ) &rarr; void

Sets the access level for AccessLevelBeanInfo objects.

### Parameters:
level - an AccessLevelBeanInfo.AccessLevel

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAccessLevel&unscoped_q=setAccessLevel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

