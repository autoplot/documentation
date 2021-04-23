# org.autoplot.dom.BindingSupportIt is apparent that the overhead of BeansBinding is so great that a lightweight
 binding engine would dramatically improve performance.  This encapsulates.
***
<a name="toStringConverter"></a>
# toStringConverter

converter for objects which have a toString/parse pair.  This works for:
 <ul>
 <li>DatumRange
 <li>Datum
 <li>Color
 </ul>
 The convertForward method captures the class of the object.

***
<a name="bind"></a>
# bind
bind( org.autoplot.dom.DomNode src, String srcProp, Object dst, String dstProp, Converter c ) &rarr; void

bind the two object properties together using a lightweight binding (introspection and
 property change listener, rather than beans binding.

### Parameters:
src - a DomNode
<br>srcProp - name of the property, which may not refer to a path (a.b.c)
<br>dst - an Object
<br>dstProp - name of the property, which may not refer to a path (a.b.c)
<br>c - bean converter for converting the property.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=bind&unscoped_q=bind">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="capitalize"></a>
# capitalize
capitalize( String name ) &rarr; String



### Parameters:
name - a String

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=capitalize&unscoped_q=capitalize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isBound"></a>
# isBound
isBound( Object node, String property ) &rarr; boolean

return true if the object is bound to something.  Note this is 
 beyond the vap bindings, and includes the bindings used to implement
 features like TimeSeriesBrowse.

### Parameters:
node - the dom node.
<br>property - the property name.

### Returns:
true if a binding is found.

<a href="https://github.com/autoplot/dev/search?q=isBound&unscoped_q=isBound">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="printStatus"></a>
# printStatus
printStatus(  ) &rarr; void

print the status of all the bindings.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=printStatus&unscoped_q=printStatus">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="totalBindings"></a>
# totalBindings
totalBindings(  ) &rarr; int

return the total number of bindings implemented in this facility.
 This was introduced to aid in debugging, when trying to identify memory 
 leaks.  https://sourceforge.net/p/autoplot/bugs/1362/

### Returns:
the total number of bindings implemented in this facility.

<a href="https://github.com/autoplot/dev/search?q=totalBindings&unscoped_q=totalBindings">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="unbind"></a>
# unbind
unbind( org.autoplot.dom.DomNode master ) &rarr; void



### Parameters:
master - a DomNode

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=unbind&unscoped_q=unbind">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

unbind( org.autoplot.dom.DomNode master, String property, Object dst, String dstProp ) &rarr; void<br>
