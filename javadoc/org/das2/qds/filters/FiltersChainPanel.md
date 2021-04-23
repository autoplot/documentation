# org.das2.qds.filters.FiltersChainPanel

Chain together a number of FilterEditorPanels to one long filter chain.  For example,
 |slice1(0)|smooth(5) would add two of the FilterEditorPanel to control each
 filter.  Additionally, this adds and removes filters from the chain.

# FiltersChainPanel( )
Creates new form FiltersChainPanel

***
<a name="PROP_ADDSUBTRACTBUTTONS"></a>
# PROP_ADDSUBTRACTBUTTONS



***
<a name="getFilter"></a>
# getFilter
getFilter(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getFilter&unscoped_q=getFilter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInput"></a>
# getInput
getInput(  ) &rarr; QDataSet

get the current dataset used to show and configure each step.

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=getInput&unscoped_q=getInput">[search for examples]</a>

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
<a name="isAddSubtractButtons"></a>
# isAddSubtractButtons
isAddSubtractButtons(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isAddSubtractButtons&unscoped_q=isAddSubtractButtons">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resetInput"></a>
# resetInput
resetInput( QDataSet ds ) &rarr; void

reset the input, even if this dataset is already in use.

### Parameters:
ds - the dataset, or null.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=resetInput&unscoped_q=resetInput">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAddSubtractButtons"></a>
# setAddSubtractButtons
setAddSubtractButtons( boolean addSubtractButtons ) &rarr; void



### Parameters:
addSubtractButtons - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAddSubtractButtons&unscoped_q=setAddSubtractButtons">[search for examples]</a>

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

set the filter, and rebuild the GUI.  Note this should be called from the 
 event thread.  TODO: This means that filters are happening on the event thread,
 which is going to lead to problems.

### Parameters:
filter - the filter for the block, such as "|slice1(2)"

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFilter&unscoped_q=setFilter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setInput"></a>
# setInput
setInput( QDataSet ds ) &rarr; void

the filter must be set before this is called.  This will set 
 droplist labels, etc.

### Parameters:
ds - the dataset, or null.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setInput&unscoped_q=setInput">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="validateFilter"></a>
# validateFilter
validateFilter( String filter ) &rarr; boolean

return true if the filter appears that it will be valid, and 
 false when it clearly won't be.

### Parameters:
filter - a String

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=validateFilter&unscoped_q=validateFilter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

validateFilter( String filter, QDataSet in ) &rarr; boolean<br>
