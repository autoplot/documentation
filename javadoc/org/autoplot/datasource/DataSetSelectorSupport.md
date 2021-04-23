# org.autoplot.datasource.DataSetSelectorSupport

Additional actions for the DataSetSelector.

***
<a name="browseLocal"></a>
# browseLocal
browseLocal( java.awt.Component parent ) &rarr; String

Show a file chooser component, and return the name of a data or .vap file.

### Parameters:
parent - parent component for focus.

### Returns:
the URI for the vap file.

<a href="https://github.com/autoplot/dev/search?q=browseLocal&unscoped_q=browseLocal">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="browseLocalVap"></a>
# browseLocalVap
browseLocalVap( java.awt.Component parent, String initialSelection ) &rarr; String

Show a file chooser component, and return the name of a .vap file.

### Parameters:
parent - parent component for focus.  If a dataSetSelector is
 used then its timerange is used for the initial timerange.
 This will now allow a non-local vap to be browsed as well.
<br>initialSelection - if non-null, then the initial selection.

### Returns:
the URI for the vap file, or null if cancel was pressed.

<a href="https://github.com/autoplot/dev/search?q=browseLocalVap&unscoped_q=browseLocalVap">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPluginsText"></a>
# getPluginsText
getPluginsText(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getPluginsText&unscoped_q=getPluginsText">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="openLocalAction"></a>
# openLocalAction
openLocalAction(  ) &rarr; Action

get "Add Plot from Local File..." action

### Returns:
the action

<a href="https://github.com/autoplot/dev/search?q=openLocalAction&unscoped_q=openLocalAction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="openLocalVapAction"></a>
# openLocalVapAction
openLocalVapAction(  ) &rarr; Action

get the "Open .vap File..." action

### Returns:
the action

<a href="https://github.com/autoplot/dev/search?q=openLocalVapAction&unscoped_q=openLocalVapAction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

