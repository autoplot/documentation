# org.autoplot.jythonsupport.ui.Util

utility methods, for example getting parameters from a script.

# Util( )


***
<a name="getParams"></a>
# getParams
getParams( java.util.Map env, String src, java.util.Map params, ProgressMonitor mon ) &rarr; Map

get the parameters for the script.

### Parameters:
env - null, or a script context that can contain values such as dom and PWD.
<br>src - the script, all in one string.
<br>params - null or default values for the parameters.
<br>mon - a ProgressMonitor

### Returns:
list of parameters.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/autoplot/jythonsupport/ui/ParametersFormPanel.md#doVariables'>org.autoplot.jythonsupport.ui.ParametersFormPanel#doVariables(java.util.Map, java.lang.String, java.util.Map, javax.swing.JPanel)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getParams&unscoped_q=getParams">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

