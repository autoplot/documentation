# org.das2.qds.filters.AbstractFilterEditorPanelImplements the typical filter, where we don't care about the input data and
 the filter itself implements the GUI.  Note when the filter property would change, 
 the implementation must fire off a property change.
AbstractFilterEditorPanel( )


***
<a name="getFilter"></a>
# getFilter
getFilter(  ) &rarr; String

return the filter specified by the GUI.  The filter string will
 start with the pipe character.  When this would change, implementations should fire
 off a property change event like so:
<blockquote><pre>
firePropertyChange( PROP_FILTER, null, ff );
</pre></blockquote>
 where ff is the new value.

### Returns:
the filter string

<a href="https://github.com/autoplot/dev/search?q=getFilter&unscoped_q=getFilter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPanel"></a>
# getPanel
getPanel(  ) &rarr; JPanel



### Returns:
javax.swing.JPanel


<a href="https://github.com/autoplot/dev/search?q=getPanel&unscoped_q=getPanel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setExpertMode"></a>
# setExpertMode
setExpertMode( boolean expert ) &rarr; void



### Parameters:
expert - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setExpertMode&unscoped_q=setExpertMode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFilter"></a>
# setFilter
setFilter( String filter ) &rarr; void

configure the GUI based on this filter.  The filter string will
 start with the pipe character.

### Parameters:
filter - the filter string

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFilter&unscoped_q=setFilter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setInput"></a>
# setInput
setInput( QDataSet ds ) &rarr; void



### Parameters:
ds - a QDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setInput&unscoped_q=setInput">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="validateFilter"></a>
# validateFilter
validateFilter( String filter, QDataSet in ) &rarr; boolean



### Parameters:
filter - a String
<br>in - a QDataSet

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=validateFilter&unscoped_q=validateFilter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

