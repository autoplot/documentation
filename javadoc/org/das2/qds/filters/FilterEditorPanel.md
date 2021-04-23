# org.das2.qds.filters.FilterEditorPanelInterface for adding small GUIs to control each of the filters.  For example
 "|divide(5)" is controlled with a GUI that accepts the float parameter that 
 might check that the operand is not zero.  These should each implement get
 and setFilter, and fire off a property change event when the value is changed,
 so the GUI can be interactively.
***
<a name="PROP_FILTER"></a>
# PROP_FILTER



***
<a name="getFilter"></a>
# getFilter
getFilter(  ) &rarr; String

return the filter specified by the GUI.  The filter string will
 start with the pipe character.  This may be called from off of the event
 thread!

### Returns:
the filter string

<a href="https://github.com/autoplot/dev/search?q=getFilter&unscoped_q=getFilter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPanel"></a>
# getPanel
getPanel(  ) &rarr; JPanel

the panel for this editor.

### Returns:
the panel for this editor.

<a href="https://github.com/autoplot/dev/search?q=getPanel&unscoped_q=getPanel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setExpertMode"></a>
# setExpertMode
setExpertMode( boolean expert ) &rarr; void

If false, then remove options which might break products.

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

configure the GUI based on this input

### Parameters:
ds - the data that will be input to the filter

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setInput&unscoped_q=setInput">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="validateFilter"></a>
# validateFilter
validateFilter( String filter, QDataSet in ) &rarr; boolean

return true if the filter is valid

### Parameters:
filter - "slice1(-1)"
<br>in - the input, or null.

### Returns:
false if the input is clearly not valid.

<a href="https://github.com/autoplot/dev/search?q=validateFilter&unscoped_q=validateFilter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

