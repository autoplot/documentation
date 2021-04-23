# org.autoplot.dom.TimeSeriesBrowseController

When the data source supports loading additional data when the time axis (or plot context) changes, then
 this is responsible for loading additional data.

***
<a name="PROP_TIMERANGE"></a>
# PROP_TIMERANGE



***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
propertyName - a String
<br>listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addPropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="getPlotId"></a>
# getPlotId
getPlotId(  ) &rarr; String

return the id of the plot to which we are listening.

### Returns:
the id of the plot

<a href="https://github.com/autoplot/dev/search?q=getPlotId&unscoped_q=getPlotId">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isListeningToAxis"></a>
# isListeningToAxis
isListeningToAxis(  ) &rarr; boolean

returns true if the TSB is listening to an axis and not the application timeRange property.
 This is the typical mode.

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isListeningToAxis&unscoped_q=isListeningToAxis">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isPendingChanges"></a>
# isPendingChanges
isPendingChanges(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isPendingChanges&unscoped_q=isPendingChanges">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="pendingChanges"></a>
# pendingChanges
pendingChanges( java.util.Map c ) &rarr; void



### Parameters:
c - a java.util.Map

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=pendingChanges&unscoped_q=pendingChanges">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
propertyName - a String
<br>listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

removePropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="updateTsb"></a>
# updateTsb
updateTsb( boolean autorange ) &rarr; void

load the new dataset, etc.

### Parameters:
autorange - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=updateTsb&unscoped_q=updateTsb">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

