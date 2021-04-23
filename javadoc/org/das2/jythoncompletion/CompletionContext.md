# org.das2.jythoncompletion.CompletionContextCompletionContext describes a place in code where completion was triggered,
 containing the type of completion and the context around it.
CompletionContext( String contextType, String contextString, String completable )


***
<a name="METHOD_NAME"></a>
# METHOD_NAME



***
<a name="CLASS_METHOD_NAME"></a>
# CLASS_METHOD_NAME



***
<a name="ATTRIBUTE_NAME"></a>
# ATTRIBUTE_NAME



***
<a name="PACKAGE_NAME"></a>
# PACKAGE_NAME



***
<a name="MODULE_NAME"></a>
# MODULE_NAME



***
<a name="DEFAULT_NAME"></a>
# DEFAULT_NAME



***
<a name="STRING_LITERAL_ARGUMENT"></a>
# STRING_LITERAL_ARGUMENT

a string literal argument for a command like getDataSet.  
 We can delegate completion to an engine for this command.

***
<a name="COMMAND_ARGUMENT"></a>
# COMMAND_ARGUMENT

we are within the body of a command such as "plot" and we want to see
 what the arguments and named parameters are.

***
<a name="contextType"></a>
# contextType

the context type, such as COMMAND_ARGUMENT or STRING_LITERAL_ARGUMENT.
 In ds= getDataSet('/hom&lt;C&gt;'), this is STRING_LITERAL_ARGUMENT

***
<a name="contextString"></a>
# contextString

the context string, such as a command name.
 In ds= getDataSet('/hom&lt;C&gt;'), this is 'getDataSet'

***
<a name="completable"></a>
# completable

the item on which completion was triggered.
 In ds= getDataSet('/hom&lt;C&gt;'), this is '/hom'

***
<a name="getContextObjectClass"></a>
# getContextObjectClass
getContextObjectClass(  ) &rarr; Class

return null or the class for the context.

### Returns:
a java.lang.Class


<a href="https://github.com/autoplot/dev/search?q=getContextObjectClass&unscoped_q=getContextObjectClass">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setContextObjectClass"></a>
# setContextObjectClass
setContextObjectClass( java.lang.Class claz ) &rarr; void



### Parameters:
claz - a java.lang.Class

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setContextObjectClass&unscoped_q=setContextObjectClass">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

