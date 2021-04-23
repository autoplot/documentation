# org.autoplot.jythonsupport.JythonUtil.ParamTODO: this ought to remove the need for ParametersFormPanel.
Param( )


***
<a name="name"></a>
# name



***
<a name="label"></a>
# label



***
<a name="deft"></a>
# deft



***
<a name="value"></a>
# value



***
<a name="doc"></a>
# doc



***
<a name="enums"></a>
# enums



***
<a name="examples"></a>
# examples



***
<a name="constraints"></a>
# constraints

constraints for the value, such as:<ul>
 <li>'labels':['RBSP-A','RBSP-B'] labels for each enum.
 </ul>

***
<a name="type"></a>
# type

The parameter type:<ul>
 <li>T (TimeRange),
 <li>A (String, but note a string with the values enumerated either T
 or F is treated as a boolean.)
 <li>F (Double or Integer, but note the values [0,1] imply it's a
 boolean.),
 <li>D (Datum),
 <li>S (DatumRange),
 <li>U (Dataset URI),
 <li>L (URL), a file location, not a URI with parameters.
 <li>or R (the resource URI)
 </ul>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

