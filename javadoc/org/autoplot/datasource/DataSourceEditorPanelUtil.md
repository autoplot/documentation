# org.autoplot.datasource.DataSourceEditorPanelUtil

Utilities for URLs.

# DataSourceEditorPanelUtil( )


***
<a name="getDataSourceEditorPanel"></a>
# getDataSourceEditorPanel
getDataSourceEditorPanel( javax.swing.JPanel parent, String uri ) &rarr; DataSourceEditorPanel

get an editor for the URI.  This must be inserted into the GUI, using getPanel.

### Parameters:
parent - a JPanel
<br>uri - a String

### Returns:
the editor panel.

<a href="https://github.com/autoplot/dev/search?q=getDataSourceEditorPanel&unscoped_q=getDataSourceEditorPanel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getDataSourceEditorPanel( java.net.URI uri ) &rarr; DataSourceEditorPanel<br>
getDataSourceEditorPanel( String suri ) &rarr; DataSourceEditorPanel<br>
***
<a name="getEditorByExt"></a>
# getEditorByExt
getEditorByExt( String extension ) &rarr; DataSourceEditorPanel

return the editor by the extension, like "cdf"

### Parameters:
extension - a String

### Returns:
an org.autoplot.datasource.DataSourceEditorPanel


<a href="https://github.com/autoplot/dev/search?q=getEditorByExt&unscoped_q=getEditorByExt">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

