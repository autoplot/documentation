# org.das2.qstream.SerializeRegistry



# SerializeRegistry( )


***
<a name="getByName"></a>
# getByName
getByName( String name ) &rarr; SerializeDelegate

return the delegate without using a class instance.

### Parameters:
name - class name like "org.das2.

### Returns:
an org.das2.qstream.SerializeDelegate


<a href="https://github.com/autoplot/dev/search?q=getByName&unscoped_q=getByName">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDelegate"></a>
# getDelegate
getDelegate( java.lang.Class clas ) &rarr; SerializeDelegate

returns a delegate or null if the class is not supported.

### Parameters:
clas - the class

### Returns:
the delegate which can be used to format and parse the class

<a href="https://github.com/autoplot/dev/search?q=getDelegate&unscoped_q=getDelegate">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="register"></a>
# register
register( java.lang.Class clas, org.das2.qstream.SerializeDelegate sd ) &rarr; void

Clients like SerializeUtil are able to register methods for
 serializing additional classes.

### Parameters:
clas - the class
<br>sd - the delegate

### Returns:
void (returns nothing)

### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/autoplot/state/SerializeUtil in the Autoplot project/.md'>org.autoplot.state.SerializeUtil in the Autoplot project.</a> in the Autoplot project.<br>

<a href="https://github.com/autoplot/dev/search?q=register&unscoped_q=register">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

