# org.autoplot.datasource.DataSourceEditorPanelInterface for discovering a GUI editor for an URL.
 Note the correct order to use a GUI is:
 <tt>
    reject( String uri ) is the URI close enough that we can create an editor for it?  Editors that never reject, "allow discovery"
      setExpertMode( boolean ) if available, then expert mode is supported and the options should be restricted to reliable options.
    prepare( String uri, Window parent, ProgressMonitor mon )  prepare the GUI, maybe by downloading resources, etc
    setURI( String uri ) set the URI for editing.  This is the oldest method and is a bit redundant.
    getPanel()           enter the GUI.
    getURI()             may be called at any time.  Note this should return a valid URI.  The intent here is that this could be called multiple times.
 </tt>
 Data Sources that support discovery will create a DataSourceEditorPanel with
 no parameters, e.g. "vap+cdaweb:"
***
<a name="getPanel"></a>
# getPanel
getPanel(  ) &rarr; JPanel

return the GUI to edit the URI.

### Returns:
a javax.swing.JPanel


<a href="https://github.com/autoplot/dev/search?q=getPanel&unscoped_q=getPanel">[search for examples]</a>

***
<a name="getURI"></a>
# getURI
getURI(  ) &rarr; String

return the URI configured by the editor.  This should be the fully-qualified
 URI, with the "vap+&lt;ext&gt;:" scheme.

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getURI&unscoped_q=getURI">[search for examples]</a>

***
<a name="markProblems"></a>
# markProblems
markProblems( java.util.List problems ) &rarr; void

mark the problems identified by the data source.  Note the reject method here doesn't provide the list,
 but instead the DataSourceFactory.reject method.  This is because often data providers intentionally provide a
 partial URI for the user to complete via the editor.

### Parameters:
problems - a java.util.List

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=markProblems&unscoped_q=markProblems">[search for examples]</a>

***
<a name="prepare"></a>
# prepare
prepare( String uri, java.awt.Window parent, ProgressMonitor mon ) &rarr; boolean

load any needed resources.  Return false if cancel, true to proceed into the gui.
 Throw a FileNotFoundException if needed resources is not found.

### Parameters:
uri - partially-completed URI
<br>parent - the parent GUI.
<br>mon - monitor to indicate slow process.

### Returns:
true to proceed, false if to cancel.

<a href="https://github.com/autoplot/dev/search?q=prepare&unscoped_q=prepare">[search for examples]</a>

***
<a name="reject"></a>
# reject
reject( String uri ) &rarr; boolean

reject the URI, perhaps because we aren't close enough to identify a resource.
 For example, a CDF URI contains the name of the file but not the variable to plot,
 so we need to enter the editor panel to complete the URI.
 Leaving the editor should never result in a URI that would reject.

### Parameters:
uri - a String

### Returns:
true if the URI is not usable.

<a href="https://github.com/autoplot/dev/search?q=reject&unscoped_q=reject">[search for examples]</a>

***
<a name="setURI"></a>
# setURI
setURI( String uri ) &rarr; void

initialize the editor to edit this URI.  This may be incomplete, and the editor
 should make it valid so getUri is valid.  Note also that the URI will be
 be the same as in prepare.  If exceptions occur here, they must be re-thrown as
 runtime exceptions, and they should be checked for in prepare().

### Parameters:
uri - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setURI&unscoped_q=setURI">[search for examples]</a>

