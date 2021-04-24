# org.das2.qds.MutablePropertyDataSet

Some QDataSets allow their properties to be changed.  Note scripts should
 never assume a dataset is mutable, and should call the putProperty method 
 instead, which will make a copy if necessary.  Note the terms mutable, 
 writable, and modifiable are all used in this documentation and interchangeable.

***
<a name="isImmutable"></a>
# isImmutable
isImmutable(  ) &rarr; boolean

return true if the dataset has been made immutable.

### Returns:
true if the dataset has been made immutable.

<a href="https://github.com/autoplot/dev/search?q=isImmutable&unscoped_q=isImmutable">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="makeImmutable"></a>
# makeImmutable
makeImmutable(  ) &rarr; void

mark the dataset as being immutable.  Once this is called, calls to
 mutating properties will print warning messages for now, but will soon
 be an error.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=makeImmutable&unscoped_q=makeImmutable">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putProperty"></a>
# putProperty
putProperty( String name, Object value ) &rarr; void

assign the name value to the property.  Note that name__i can be
 used as a alias for an indexed property, but when possible 
 putProperty(name,i,value) should be used.

### Parameters:
name - property name like "UNITS" (Use QDataSet.UNITS)
<br>value - the property value.

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/ops/Ops.md#putProperty'>org.das2.qds.ops.Ops#putProperty(QDataSet, java.lang.String, java.lang.Object)</a> putProperty which properly checks mutability of the dataset<br>
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/QDataSet.md#UNITS'>QDataSet#UNITS</a> <br>

<a href="https://github.com/autoplot/dev/search?q=putProperty&unscoped_q=putProperty">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

putProperty( String name, int index, Object value ) &rarr; void<br>
