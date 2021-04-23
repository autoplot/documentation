# org.autoplot.datasource.TimeRangeEditor

Standard control for controlling a DatumRange containing times, with
 next and previous buttons, and a launcher into the TimeRangeTool.

# TimeRangeEditor( )


***
<a name="PROP_USE_DOY"></a>
# PROP_USE_DOY



***
<a name="PROP_RESCALE"></a>
# PROP_RESCALE



***
<a name="PROP_RANGE"></a>
# PROP_RANGE



***
<a name="PROP_CONTROL_RANGE"></a>
# PROP_CONTROL_RANGE



***
<a name="PROP_CARDSELECTED"></a>
# PROP_CARDSELECTED



***
<a name="getNoOneListeningRange"></a>
# getNoOneListeningRange
getNoOneListeningRange(  ) &rarr; DatumRange

special marker object indicates that the "no one listening" message should be shown.

### Returns:
special marker object

<a href="https://github.com/autoplot/dev/search?q=getNoOneListeningRange&unscoped_q=getNoOneListeningRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRange"></a>
# getRange
getRange(  ) &rarr; DatumRange

get the timerange.

### Returns:
the timerange.

<a href="https://github.com/autoplot/dev/search?q=getRange&unscoped_q=getRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRescale"></a>
# getRescale
getRescale(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getRescale&unscoped_q=getRescale">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getUriFocusListener"></a>
# getUriFocusListener
getUriFocusListener(  ) &rarr; PropertyChangeListener



### Returns:
java.beans.PropertyChangeListener


<a href="https://github.com/autoplot/dev/search?q=getUriFocusListener&unscoped_q=getUriFocusListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isCardSelected"></a>
# isCardSelected
isCardSelected(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isCardSelected&unscoped_q=isCardSelected">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isUseDoy"></a>
# isUseDoy
isUseDoy(  ) &rarr; boolean

true if day of year should be used instead of year, month, day.

### Returns:
true if day of year should be used

<a href="https://github.com/autoplot/dev/search?q=isUseDoy&unscoped_q=isUseDoy">[search for examples]</a>

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
<a name="makeThinner"></a>
# makeThinner
makeThinner(  ) &rarr; void

re-layout the GUI to make it thinner.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=makeThinner&unscoped_q=makeThinner">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="revalidate"></a>
# revalidate
revalidate(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=revalidate&unscoped_q=revalidate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAlternatePeer"></a>
# setAlternatePeer
setAlternatePeer( String label, String card ) &rarr; void



### Parameters:
label - a String
<br>card - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAlternatePeer&unscoped_q=setAlternatePeer">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setCardSelected"></a>
# setCardSelected
setCardSelected( boolean cardSelected ) &rarr; void



### Parameters:
cardSelected - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCardSelected&unscoped_q=setCardSelected">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setCardSelectedNoEventKludge"></a>
# setCardSelectedNoEventKludge
setCardSelectedNoEventKludge( boolean cardSelected ) &rarr; void



### Parameters:
cardSelected - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCardSelectedNoEventKludge&unscoped_q=setCardSelectedNoEventKludge">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setControlRange"></a>
# setControlRange
setControlRange( DatumRange value ) &rarr; void

set the range displayed, regardless of the rescaling.

### Parameters:
value - a DatumRange

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setControlRange&unscoped_q=setControlRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataSetSelectorPeer"></a>
# setDataSetSelectorPeer
setDataSetSelectorPeer( org.autoplot.datasource.DataSetSelector peer ) &rarr; void

provide a shortcut to a DataSetSelector editor.

### Parameters:
peer - a DataSetSelector

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSetSelectorPeer&unscoped_q=setDataSetSelectorPeer">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setEnabled"></a>
# setEnabled
setEnabled( boolean enabled ) &rarr; void



### Parameters:
enabled - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setEnabled&unscoped_q=setEnabled">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setNoOneListeningRange"></a>
# setNoOneListeningRange
setNoOneListeningRange( DatumRange dr ) &rarr; void

special marker object indicates that the "no one listening" message should be shown.

### Parameters:
dr - a DatumRange

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setNoOneListeningRange&unscoped_q=setNoOneListeningRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRange"></a>
# setRange
setRange( DatumRange value ) &rarr; void

set the range for the controller.  Note that if the rescale range
 is not "" or "0%,100%" then the controlRange will be different.

### Parameters:
value - a DatumRange

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRange&unscoped_q=setRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRescale"></a>
# setRescale
setRescale( String rescale ) &rarr; void

Add extra time to the range, and account for this extra time
 with the next and previous buttons.  Example values are:
 <li>"" the default behavior
 <li>0%,100% also the default behavior
 <li>-10%,110% add ten percent before and after the interval
 <li>0%-1hr,100%+1hr add an hour before and after the interval
 Note the GUI will always report the 0%,100% time, without the context.

### Parameters:
rescale - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRescale&unscoped_q=setRescale">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setUseDoy"></a>
# setUseDoy
setUseDoy( boolean useDoy ) &rarr; void

prefer use of day of year rather than year, month, day.

### Parameters:
useDoy - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUseDoy&unscoped_q=setUseDoy">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

