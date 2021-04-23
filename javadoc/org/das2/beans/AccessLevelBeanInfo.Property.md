# org.das2.beans.AccessLevelBeanInfo.PropertyAccessLevelBeanInfo.Property is a helper class for subclasses of
 AccessLevelBeanInfo to specify a list of properties in a way that
 is independant of the underlying Bean/PropertyDescriptor implementation.
Property( String name, org.das2.beans.AccessLevelBeanInfo.AccessLevel level, org.das2.beans.AccessLevelBeanInfo.PersistenceLevel persistenceLevel, String getter, String setter, java.lang.Class editor )
Creates a new Property object.

Property( String name, org.das2.beans.AccessLevelBeanInfo.AccessLevel level, String getter, String setter, java.lang.Class editor )
Creates a new Property object.

Property( String name, org.das2.beans.AccessLevelBeanInfo.AccessLevel level, org.das2.beans.AccessLevelBeanInfo.PersistenceLevel persistenceLevel, String getter, String setter, String igetter, String isetter, java.lang.Class editor )
Creates a new Property object that is indexed.

Property( String name, org.das2.beans.AccessLevelBeanInfo.AccessLevel level, String getter, String setter, String igetter, String isetter, java.lang.Class editor )
Creates a new Property object that is indexed.

***
<a name="getLevel"></a>
# getLevel
getLevel(  ) &rarr; AccessLevel

Returns the access level for this property

### Returns:
org.das2.beans.AccessLevelBeanInfo.AccessLevel


<a href="https://github.com/autoplot/dev/search?q=getLevel&unscoped_q=getLevel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPersistenceLevel"></a>
# getPersistenceLevel
getPersistenceLevel(  ) &rarr; PersistenceLevel



### Returns:
org.das2.beans.AccessLevelBeanInfo.PersistenceLevel


<a href="https://github.com/autoplot/dev/search?q=getPersistenceLevel&unscoped_q=getPersistenceLevel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPropertyDescriptor"></a>
# getPropertyDescriptor
getPropertyDescriptor( java.lang.Class beanClass ) &rarr; PropertyDescriptor

Returns a PropertyDescriptor for this property that is associated
 with the specified bean class.

### Parameters:
beanClass - a java.lang.Class

### Returns:
java.beans.PropertyDescriptor


<a href="https://github.com/autoplot/dev/search?q=getPropertyDescriptor&unscoped_q=getPropertyDescriptor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

