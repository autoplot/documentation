# org.autoplot.datasource.DataSourceFormatEditorPanel

similar to DataSourceEditorPanel, this one is arguments for output.

***
<a name="getPanel"></a>
# getPanel
getPanel(  ) &rarr; JPanel

return the editor

### Returns:
a javax.swing.JPanel


<a href="https://github.com/autoplot/dev/search?q=getPanel&unscoped_q=getPanel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getURI"></a>
# getURI
getURI(  ) &rarr; String

return the URI configured by the editor.  This should be the fully-qualified
 URI, with the "vap+<ext>:" scheme.

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getURI&unscoped_q=getURI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setURI"></a>
# setURI
setURI( String uri ) &rarr; void

initialize the editor to edit this URI.  This may be incomplete, and the editor
 should make it valid so getUri is valid.

### Parameters:
uri - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setURI&unscoped_q=setURI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

