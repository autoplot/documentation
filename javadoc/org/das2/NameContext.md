# org.das2.NameContext

An instance of <code>NameContext</code> defines the name space for a
 dasml/das2 application.  Methods for querying values of properties are
 also provided.

***
<a name="SIMPLE_NAME"></a>
# SIMPLE_NAME



***
<a name="INDEXED_NAME"></a>
# INDEXED_NAME



***
<a name="QUALIFIED_NAME"></a>
# QUALIFIED_NAME



***
<a name="get"></a>
# get
get( String name ) &rarr; Object



### Parameters:
name - a String

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=get&unscoped_q=get">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getIndexedPropertyValue"></a>
# getIndexedPropertyValue
getIndexedPropertyValue( Object obj, String property, int index ) &rarr; Object



### Parameters:
obj - an Object
<br>property - a String
<br>index - an int

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=getIndexedPropertyValue&unscoped_q=getIndexedPropertyValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPropertyValue"></a>
# getPropertyValue
getPropertyValue( Object obj, String property ) &rarr; Object



### Parameters:
obj - an Object
<br>property - a String

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=getPropertyValue&unscoped_q=getPropertyValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="put"></a>
# put
put( String name, Object value ) &rarr; void

Associates a value with a name in this context.  The <code>name</code>
 parameter must being with a letter and can only consist of alphanumeric
 characters and '_'.

### Parameters:
name - the name for the value to be associated with
<br>value - the value being named

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=put&unscoped_q=put">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="remove"></a>
# remove
remove( String name ) &rarr; void



### Parameters:
name - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=remove&unscoped_q=remove">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="set"></a>
# set
set( String name, Object value ) &rarr; void



### Parameters:
name - a String
<br>value - an Object

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=set&unscoped_q=set">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setIndexedPropertyValue"></a>
# setIndexedPropertyValue
setIndexedPropertyValue( Object obj, String property, int index, Object value ) &rarr; void



### Parameters:
obj - an Object
<br>property - a String
<br>index - an int
<br>value - an Object

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setIndexedPropertyValue&unscoped_q=setIndexedPropertyValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPropertyValue"></a>
# setPropertyValue
setPropertyValue( Object obj, String property, Object value ) &rarr; void



### Parameters:
obj - an Object
<br>property - a String
<br>value - an Object

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPropertyValue&unscoped_q=setPropertyValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

