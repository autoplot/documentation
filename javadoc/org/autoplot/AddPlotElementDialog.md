# org.autoplot.AddPlotElementDialog

Allow additional plots to be added, and plot one URI against another.

# AddPlotElementDialog( java.awt.Frame parent, boolean modal )
Creates new form AddPlotElementDialog

***
<a name="PROP_MODIFIERS"></a>
# PROP_MODIFIERS



***
<a name="PROP_CANCELLED"></a>
# PROP_CANCELLED



***
<a name="getDepCount"></a>
# getDepCount
getDepCount(  ) &rarr; int

return the number of depend datasets added, 0, or -1 if no dataset
 should be plotted.

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=getDepCount&unscoped_q=getDepCount">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getModifiers"></a>
# getModifiers
getModifiers(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getModifiers&unscoped_q=getModifiers">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPrimaryDataSetSelector"></a>
# getPrimaryDataSetSelector
getPrimaryDataSetSelector(  ) &rarr; DataSetSelector



### Returns:
the primaryDataSetSelector

<a href="https://github.com/autoplot/dev/search?q=getPrimaryDataSetSelector&unscoped_q=getPrimaryDataSetSelector">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPrimaryFilters"></a>
# getPrimaryFilters
getPrimaryFilters(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getPrimaryFilters&unscoped_q=getPrimaryFilters">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSecondaryDataSetSelector"></a>
# getSecondaryDataSetSelector
getSecondaryDataSetSelector(  ) &rarr; DataSetSelector



### Returns:
the secondaryDataSetSelector

<a href="https://github.com/autoplot/dev/search?q=getSecondaryDataSetSelector&unscoped_q=getSecondaryDataSetSelector">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSecondaryFilters"></a>
# getSecondaryFilters
getSecondaryFilters(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getSecondaryFilters&unscoped_q=getSecondaryFilters">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTertiaryDataSetSelector"></a>
# getTertiaryDataSetSelector
getTertiaryDataSetSelector(  ) &rarr; DataSetSelector



### Returns:
the tertiaryDataSetSelector

<a href="https://github.com/autoplot/dev/search?q=getTertiaryDataSetSelector&unscoped_q=getTertiaryDataSetSelector">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTertiaryFilters"></a>
# getTertiaryFilters
getTertiaryFilters(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getTertiaryFilters&unscoped_q=getTertiaryFilters">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isCancelled"></a>
# isCancelled
isCancelled(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isCancelled&unscoped_q=isCancelled">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDepCount"></a>
# setDepCount
setDepCount( int i ) &rarr; void



### Parameters:
i - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDepCount&unscoped_q=setDepCount">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setMessagesLabelText"></a>
# setMessagesLabelText
setMessagesLabelText( String text ) &rarr; void

add additional text to the dialog.

### Parameters:
text - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMessagesLabelText&unscoped_q=setMessagesLabelText">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setModifiers"></a>
# setModifiers
setModifiers( int modifiers ) &rarr; void



### Parameters:
modifiers - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setModifiers&unscoped_q=setModifiers">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPrimaryFilter"></a>
# setPrimaryFilter
setPrimaryFilter( String f ) &rarr; void



### Parameters:
f - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPrimaryFilter&unscoped_q=setPrimaryFilter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSecondaryFilter"></a>
# setSecondaryFilter
setSecondaryFilter( String f ) &rarr; void



### Parameters:
f - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSecondaryFilter&unscoped_q=setSecondaryFilter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setShowAdditionalOperations"></a>
# setShowAdditionalOperations
setShowAdditionalOperations( boolean show ) &rarr; void

if true, then show the additional operations fields.

### Parameters:
show - if true, then show the additional operations fields.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setShowAdditionalOperations&unscoped_q=setShowAdditionalOperations">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setUsePrimaryFilters"></a>
# setUsePrimaryFilters
setUsePrimaryFilters( boolean show ) &rarr; void



### Parameters:
show - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUsePrimaryFilters&unscoped_q=setUsePrimaryFilters">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setUseSecondaryFilters"></a>
# setUseSecondaryFilters
setUseSecondaryFilters( boolean show ) &rarr; void



### Parameters:
show - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUseSecondaryFilters&unscoped_q=setUseSecondaryFilters">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

