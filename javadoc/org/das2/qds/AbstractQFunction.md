# org.das2.qds.AbstractQFunctionAbstract class implements values and exampleOutput based on
 value and exampleInput.
AbstractQFunction( )


***
<a name="exampleInput"></a>
# exampleInput
exampleInput(  ) &rarr; QDataSet



### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=exampleInput&unscoped_q=exampleInput">[search for examples]</a>

***
<a name="exampleOutput"></a>
# exampleOutput
exampleOutput(  ) &rarr; QDataSet

this simply calls  value( exampleInput() ).

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=exampleOutput&unscoped_q=exampleOutput">[search for examples]</a>

***
<a name="value"></a>
# value
value( QDataSet parm ) &rarr; QDataSet



### Parameters:
parm - a QDataSet

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

***
<a name="values"></a>
# values
values( QDataSet vs ) &rarr; QDataSet

calculate the values by calling the  value function for
 each element of  vs.  A check is made for each call to the  value
 function that a dataset with the same rank and length is returned.

### Parameters:
vs - rank N+1 set of values, where {@code exampleInput} returns rank N.

### Returns:
rank M+1 set of values, where {@code value} returns rank M.

<a href="https://github.com/autoplot/dev/search?q=values&unscoped_q=values">[search for examples]</a>

