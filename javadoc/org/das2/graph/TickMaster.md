# org.das2.graph.TickMaster

Class for managing ticks.  When a set of plots shares a common column and
 axis setting, they should all use the same ticks.  The other problem this
 should fix is when a stack of plots all have heights within a couple of pixels
 of one another, we should try to use the same ticks for them.

 DasAxis clients should offer their ticks to this master, which will decide
 which set of ticks to use.

# TickMaster( )


***
<a name="getInstance"></a>
# getInstance
getInstance(  ) &rarr; TickMaster



### Returns:
org.das2.graph.TickMaster


<a href="https://github.com/autoplot/dev/search?q=getInstance&unscoped_q=getInstance">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="offerTickV"></a>
# offerTickV
offerTickV( org.das2.graph.DasAxis h, org.das2.graph.TickVDescriptor ticks ) &rarr; void

offer a set of ticks.  This can be called from off or on the event thread,
 but a new thread is started so the task is performed off the event thread.

### Parameters:
h - the axis
<br>ticks - null or the new ticks.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=offerTickV&unscoped_q=offerTickV">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="register"></a>
# register
register( org.das2.graph.DasAxis h ) &rarr; void



### Parameters:
h - a DasAxis

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=register&unscoped_q=register">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="requestTickV"></a>
# requestTickV
requestTickV( org.das2.graph.DasAxis h ) &rarr; TickVDescriptor

kludgy solution to problems where an axis didn't get the update from
 its parent.  This is only called as a last-ditch measure.

### Parameters:
h - a DasAxis

### Returns:
an org.das2.graph.TickVDescriptor


<a href="https://github.com/autoplot/dev/search?q=requestTickV&unscoped_q=requestTickV">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

