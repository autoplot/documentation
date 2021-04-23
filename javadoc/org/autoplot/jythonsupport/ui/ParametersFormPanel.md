# org.autoplot.jythonsupport.ui.ParametersFormPanel

GUI component for controlling script parameters.

# ParametersFormPanel( )


***
<a name="doVariables"></a>
# doVariables
doVariables( java.util.Map env, java.io.File f, java.util.Map params, javax.swing.JPanel paramsPanel ) &rarr; FormData

Populates the JPanel with options.  See org.autoplot.jythonsupport.ui.Util.createForm.

### Parameters:
env - environment variables such as PWD and dom.
<br>f - the file containing the script.
<br>params - map containing any settings for the variables.
<br>paramsPanel - a JPanel

### Returns:
the FormData from the initial view, since some clients will not show a GUI when there are no parameters.

<a href="https://github.com/autoplot/dev/search?q=doVariables&unscoped_q=doVariables">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

doVariables( String src, java.util.Map params, javax.swing.JPanel zparamsPanel ) &rarr; FormData<br>
doVariables( java.util.Map env, String src, java.util.Map params, javax.swing.JPanel zparamsPanel ) &rarr; FormData<br>
***
<a name="getFormData"></a>
# getFormData
getFormData(  ) &rarr; FormData

return the current state of the form data.

### Returns:
an org.autoplot.jythonsupport.ui.ParametersFormPanel.FormData


<a href="https://github.com/autoplot/dev/search?q=getFormData&unscoped_q=getFormData">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="redoVariables"></a>
# redoVariables
redoVariables( java.util.Map env, String src, java.util.Map params, javax.swing.JPanel paramsPanel ) &rarr; void

Repopulates the JPanel with options, to be used when the parameters can change the params that are read in.

### Parameters:
env - environment variables such as PWD and dom.
<br>src - the script loaded into a string.
<br>params - map containing any settings for the variables.
<br>paramsPanel - the GUI which needs to be revalidated.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=redoVariables&unscoped_q=redoVariables">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resetVariables"></a>
# resetVariables
resetVariables( org.autoplot.jythonsupport.ui.ParametersFormPanel.FormData fd, java.util.Map params ) &rarr; void

extract the data from the form into params. Note, strings and URIs are 
 quoted, not sure why.

### Parameters:
fd - form data containing GUI references
<br>params - map to contain the settings for each parameter, reading from the GUI.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resetVariables&unscoped_q=resetVariables">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

