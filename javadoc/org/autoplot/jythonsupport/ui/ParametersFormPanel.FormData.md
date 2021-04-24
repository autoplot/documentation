# org.autoplot.jythonsupport.ui.ParametersFormPanel.FormData

represent the data on the form.

# FormData( )


***
<a name="count"></a>
# count



***
<a name="implement"></a>
# implement
implement( PythonInterpreter interp, String param, String value ) &rarr; void

Convert the parameter to Jython types.
<blockquote><pre>
 T (TimeRange)
 A (String)
 F (Double or Integer)
 R (URI)
 L (URL) a resource URL (local file or web file).
 D Datum
 S DatumRange
 </pre></blockquote>

### Parameters:
interp - the interpreter
<br>param - the param name
<br>value - the param value

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=implement&unscoped_q=implement">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

