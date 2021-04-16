# org.autoplot.EventsListToolUtil
EventsListToolUtil( )


***
<a name="deflts"></a>
# deflts
deflts( org.autoplot.datasource.DataSetSelector sel ) &rarr; void



### Parameters:
sel - a DataSetSelector

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=deflts&unscoped_q=deflts">[search for examples]</a>

***
<a name="getEventsList"></a>
# getEventsList
getEventsList( org.autoplot.AutoplotUI t ) &rarr; TimeRangeToolEventsList

find the GUI for this application, creating one if necessary.

### Parameters:
t - the app.

### Returns:
the single TimeRangeToolEventsList for the app.

<a href="https://github.com/autoplot/dev/search?q=getEventsList&unscoped_q=getEventsList">[search for examples]</a>

***
<a name="setEventsListURI"></a>
# setEventsListURI
setEventsListURI( org.autoplot.AutoplotUI t, String uri ) &rarr; void

set the location of the events list we should use.  <code>show(t)</code> 
 should be called to show the GUI.

### Parameters:
t - the app
<br>uri - the location of the events list.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setEventsListURI&unscoped_q=setEventsListURI">[search for examples]</a>

***
<a name="show"></a>
# show
show( org.autoplot.AutoplotUI t ) &rarr; void

this must be called on the event thread.

### Parameters:
t - an AutoplotUI

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=show&unscoped_q=show">[search for examples]</a>

