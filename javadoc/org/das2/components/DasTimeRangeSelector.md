# org.das2.components.DasTimeRangeSelector



# DasTimeRangeSelector( )
Creates a new instance of DasTimeRangeSelector

# DasTimeRangeSelector( Datum startTime, Datum endTime )


# DasTimeRangeSelector( DatumRange range )


***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void

Adds a PropertyChangeListener to the listener list.

### Parameters:
l - The listener to add.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addTimeRangeSelectionListener"></a>
# addTimeRangeSelectionListener
addTimeRangeSelectionListener( org.das2.event.TimeRangeSelectionListener listener ) &rarr; void

Registers TimeRangeSelectionListener to receive events.

### Parameters:
listener - The listener to register.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addTimeRangeSelectionListener&unscoped_q=addTimeRangeSelectionListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="enableFavorites"></a>
# enableFavorites
enableFavorites( String group ) &rarr; void

adds a droplist of recently entered times.  This should be a spacecraft string, or null.

### Parameters:
group - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=enableFavorites&unscoped_q=enableFavorites">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getEndTime"></a>
# getEndTime
getEndTime(  ) &rarr; Datum



### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getEndTime&unscoped_q=getEndTime">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMaximumSize"></a>
# getMaximumSize
getMaximumSize(  ) &rarr; Dimension



### Returns:
java.awt.Dimension


<a href="https://github.com/autoplot/dev/search?q=getMaximumSize&unscoped_q=getMaximumSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMinimumSize"></a>
# getMinimumSize
getMinimumSize(  ) &rarr; Dimension



### Returns:
java.awt.Dimension


<a href="https://github.com/autoplot/dev/search?q=getMinimumSize&unscoped_q=getMinimumSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRange"></a>
# getRange
getRange(  ) &rarr; DatumRange



### Returns:
org.das2.datum.DatumRange


<a href="https://github.com/autoplot/dev/search?q=getRange&unscoped_q=getRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getStartTime"></a>
# getStartTime
getStartTime(  ) &rarr; Datum



### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getStartTime&unscoped_q=getStartTime">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isWithin"></a>
# isWithin
isWithin( Datum s1, Datum s2 ) &rarr; boolean



### Parameters:
s1 - a Datum
<br>s2 - a Datum

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isWithin&unscoped_q=isWithin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener l ) &rarr; void

Removes a PropertyChangeListener from the listener list.

### Parameters:
l - The listener to remove.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeTimeRangeSelectionListener"></a>
# removeTimeRangeSelectionListener
removeTimeRangeSelectionListener( org.das2.event.TimeRangeSelectionListener listener ) &rarr; void

Removes TimeRangeSelectionListener from the list of listeners.

### Parameters:
listener - The listener to remove.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeTimeRangeSelectionListener&unscoped_q=removeTimeRangeSelectionListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setEndTime"></a>
# setEndTime
setEndTime( Datum s2 ) &rarr; void



### Parameters:
s2 - a Datum

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setEndTime&unscoped_q=setEndTime">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRange"></a>
# setRange
setRange( DatumRange range ) &rarr; void



### Parameters:
range - a DatumRange

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRange&unscoped_q=setRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setStartTime"></a>
# setStartTime
setStartTime( Datum s1 ) &rarr; void



### Parameters:
s1 - a Datum

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setStartTime&unscoped_q=setStartTime">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="timeRangeSelected"></a>
# timeRangeSelected
timeRangeSelected( org.das2.event.TimeRangeSelectionEvent e ) &rarr; void



### Parameters:
e - a TimeRangeSelectionEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=timeRangeSelected&unscoped_q=timeRangeSelected">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

