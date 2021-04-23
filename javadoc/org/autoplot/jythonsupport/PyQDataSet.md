# org.autoplot.jythonsupport.PyQDataSetPyQDataSet wraps a QDataSet to provide Python operator overloading and
 indexing.  For example, the Python plus "+" operator is implemented in the
 method "__add__", and ds[0,:] is implemented in __getitem__ and __setitem__.
 The class PyQDataSetAdapter is responsible for creating the PyQDataSet when
 a QDataSet is brought into the Python interpreter.
PyQDataSet( )


PyQDataSet( QDataSet ds )
Note getDataSet will always provide a writable dataset.

***
<a name="__abs__"></a>
# __abs__
__abs__(  ) &rarr; PyObject



### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__abs__&unscoped_q=__abs__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__add__"></a>
# __add__
__add__( PyObject arg0 ) &rarr; PyQDataSet



### Parameters:
arg0 - a PyObject

### Returns:
org.autoplot.jythonsupport.PyQDataSet


<a href="https://github.com/autoplot/dev/search?q=__add__&unscoped_q=__add__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__and__"></a>
# __and__
__and__( PyObject o ) &rarr; PyObject



### Parameters:
o - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__and__&unscoped_q=__and__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__coerce_ex__"></a>
# __coerce_ex__
__coerce_ex__( PyObject arg0 ) &rarr; Object



### Parameters:
arg0 - a PyObject

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=__coerce_ex__&unscoped_q=__coerce_ex__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__delattr__"></a>
# __delattr__
__delattr__( String attr ) &rarr; void



### Parameters:
attr - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=__delattr__&unscoped_q=__delattr__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__div__"></a>
# __div__
__div__( PyObject arg0 ) &rarr; PyObject



### Parameters:
arg0 - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__div__&unscoped_q=__div__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__eq__"></a>
# __eq__
__eq__( PyObject o ) &rarr; PyObject



### Parameters:
o - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__eq__&unscoped_q=__eq__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__findattr__"></a>
# __findattr__
__findattr__( String name ) &rarr; PyObject



### Parameters:
name - a String

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__findattr__&unscoped_q=__findattr__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__float__"></a>
# __float__
__float__(  ) &rarr; PyFloat



### Returns:
PyFloat


<a href="https://github.com/autoplot/dev/search?q=__float__&unscoped_q=__float__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__floordiv__"></a>
# __floordiv__
__floordiv__( PyObject arg0 ) &rarr; PyObject



### Parameters:
arg0 - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__floordiv__&unscoped_q=__floordiv__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__ge__"></a>
# __ge__
__ge__( PyObject o ) &rarr; PyObject



### Parameters:
o - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__ge__&unscoped_q=__ge__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__getitem__"></a>
# __getitem__
__getitem__( PyObject arg0 ) &rarr; PyObject

This implements the Python indexing, such as data[4,:,3:5].  Note this
 includes many QDataSet operations: a single index represents a slice, a 
 range like 3:5 is a trim, an array is a sort, and a colon leaves a dimension
 alone.  See http://autoplot.org/developer.python.indexing

 TODO: preserve metadata
 TODO: verify all index types.

### Parameters:
arg0 - various python types http://autoplot.org/developer.python.indexing

### Returns:
element or subset of data.

<a href="https://github.com/autoplot/dev/search?q=__getitem__&unscoped_q=__getitem__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__gt__"></a>
# __gt__
__gt__( PyObject o ) &rarr; PyObject



### Parameters:
o - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__gt__&unscoped_q=__gt__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__int__"></a>
# __int__
__int__(  ) &rarr; PyObject



### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__int__&unscoped_q=__int__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__iter__"></a>
# __iter__
__iter__(  ) &rarr; PyObject



### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__iter__&unscoped_q=__iter__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__le__"></a>
# __le__
__le__( PyObject o ) &rarr; PyObject



### Parameters:
o - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__le__&unscoped_q=__le__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__len__"></a>
# __len__
__len__(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=__len__&unscoped_q=__len__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__long__"></a>
# __long__
__long__(  ) &rarr; PyLong



### Returns:
PyLong


<a href="https://github.com/autoplot/dev/search?q=__long__&unscoped_q=__long__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__lt__"></a>
# __lt__
__lt__( PyObject o ) &rarr; PyObject



### Parameters:
o - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__lt__&unscoped_q=__lt__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__mod__"></a>
# __mod__
__mod__( PyObject arg0 ) &rarr; PyObject



### Parameters:
arg0 - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__mod__&unscoped_q=__mod__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__mul__"></a>
# __mul__
__mul__( PyObject arg0 ) &rarr; PyObject



### Parameters:
arg0 - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__mul__&unscoped_q=__mul__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__ne__"></a>
# __ne__
__ne__( PyObject o ) &rarr; PyObject



### Parameters:
o - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__ne__&unscoped_q=__ne__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__neg__"></a>
# __neg__
__neg__(  ) &rarr; PyObject



### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__neg__&unscoped_q=__neg__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__nonzero__"></a>
# __nonzero__
__nonzero__(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=__nonzero__&unscoped_q=__nonzero__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__or__"></a>
# __or__
__or__( PyObject o ) &rarr; PyObject



### Parameters:
o - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__or__&unscoped_q=__or__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__pos__"></a>
# __pos__
__pos__(  ) &rarr; PyObject



### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__pos__&unscoped_q=__pos__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__pow__"></a>
# __pow__
__pow__( PyObject arg0 ) &rarr; PyObject



### Parameters:
arg0 - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__pow__&unscoped_q=__pow__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__radd__"></a>
# __radd__
__radd__( PyObject arg0 ) &rarr; PyObject



### Parameters:
arg0 - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__radd__&unscoped_q=__radd__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__rdiv__"></a>
# __rdiv__
__rdiv__( PyObject arg0 ) &rarr; PyObject



### Parameters:
arg0 - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__rdiv__&unscoped_q=__rdiv__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__rfloordiv__"></a>
# __rfloordiv__
__rfloordiv__( PyObject arg0 ) &rarr; PyObject



### Parameters:
arg0 - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__rfloordiv__&unscoped_q=__rfloordiv__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__rmod__"></a>
# __rmod__
__rmod__( PyObject arg0 ) &rarr; PyObject



### Parameters:
arg0 - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__rmod__&unscoped_q=__rmod__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__rmul__"></a>
# __rmul__
__rmul__( PyObject arg0 ) &rarr; PyObject



### Parameters:
arg0 - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__rmul__&unscoped_q=__rmul__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__rpow__"></a>
# __rpow__
__rpow__( PyObject arg0 ) &rarr; PyObject



### Parameters:
arg0 - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__rpow__&unscoped_q=__rpow__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__rsub__"></a>
# __rsub__
__rsub__( PyObject arg0 ) &rarr; PyObject



### Parameters:
arg0 - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__rsub__&unscoped_q=__rsub__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__setattr__"></a>
# __setattr__
__setattr__( String name, PyObject value ) &rarr; void



### Parameters:
name - a String
<br>value - a PyObject

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=__setattr__&unscoped_q=__setattr__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__setitem__"></a>
# __setitem__
__setitem__( PyObject arg0, PyObject arg1 ) &rarr; void

Assign the values to the indeces specified.  
 Note, if the value has units and the PyQDataSet does not yet have units, 
 then the units are assigned.
 See http://autoplot.org/developer.python.indexing

### Parameters:
arg0 - the indeces
<br>arg1 - the values to assign

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=__setitem__&unscoped_q=__setitem__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__sub__"></a>
# __sub__
__sub__( PyObject arg0 ) &rarr; PyObject



### Parameters:
arg0 - a PyObject

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=__sub__&unscoped_q=__sub__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="__tojava__"></a>
# __tojava__
__tojava__( java.lang.Class c ) &rarr; Object

This is what does the magical coersion, see https://sourceforge.net/p/autoplot/bugs/1861/

### Parameters:
c - the class needed.

### Returns:
instance of the class if available.

<a href="https://github.com/autoplot/dev/search?q=__tojava__&unscoped_q=__tojava__">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="append"></a>
# append
append( PyObject arg0 ) &rarr; PyQDataSet



### Parameters:
arg0 - a PyObject

### Returns:
org.autoplot.jythonsupport.PyQDataSet


<a href="https://github.com/autoplot/dev/search?q=append&unscoped_q=append">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getQDataSet"></a>
# getQDataSet
getQDataSet(  ) &rarr; QDataSet



### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=getQDataSet&unscoped_q=getQDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSerialNumber"></a>
# getSerialNumber
getSerialNumber(  ) &rarr; int

return the serial number.

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=getSerialNumber&unscoped_q=getSerialNumber">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="invoke"></a>
# invoke
invoke( String name ) &rarr; PyObject



### Parameters:
name - a String

### Returns:
PyObject


<a href="https://github.com/autoplot/dev/search?q=invoke&unscoped_q=invoke">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

invoke( String name, PyObject arg1 ) &rarr; PyObject<br>
invoke( String name, PyObject arg1, PyObject arg2 ) &rarr; PyObject<br>
invoke( String name, PyObject[] args, java.lang.String[] keywords ) &rarr; PyObject<br>
invoke( String name, PyObject[] args ) &rarr; PyObject<br>
***
<a name="isNumberType"></a>
# isNumberType
isNumberType(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isNumberType&unscoped_q=isNumberType">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putProperty"></a>
# putProperty
putProperty( PyString prop, Object value ) &rarr; void



### Parameters:
prop - a PyString
<br>value - an Object

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putProperty&unscoped_q=putProperty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

putProperty( PyString prop, int index, Object value ) &rarr; void<br>
***
<a name="putValue"></a>
# putValue
putValue( double value ) &rarr; void



### Parameters:
value - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putValue&unscoped_q=putValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

putValue( int i0, double value ) &rarr; void<br>
putValue( int i0, int i1, double value ) &rarr; void<br>
putValue( int i0, int i1, int i2, double value ) &rarr; void<br>
putValue( int i0, int i1, int i2, int i3, double value ) &rarr; void<br>
***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

