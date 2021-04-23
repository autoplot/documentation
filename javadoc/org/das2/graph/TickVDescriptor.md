# org.das2.graph.TickVDescriptor

A TickVDescriptor describes the position that ticks
 should be drawn, so that a fairly generic tick drawing routine
 can be used for multiple types of axes.

# TickVDescriptor( double[] minorTicks, double[] ticks, Units units )


# TickVDescriptor( QDataSet ticks )
create the tickVDescriptor for a bunch of given ticks.  The first two ticks are used
 to derive minor ticks, using the DomainDivider code.

***
<a name="bestTickVLinear"></a>
# bestTickVLinear
bestTickVLinear( Datum min, Datum max, int nTicksMin, int nTicksMax, boolean fin ) &rarr; TickVDescriptor

return a set of linear ticks, within the given constraints.

### Parameters:
min - the minimum
<br>max - the maximum
<br>nTicksMin - the minimum number of ticks.
<br>nTicksMax - the maximum number of ticks.
<br>fin - final, useful when debugging.

### Returns:
an org.das2.graph.TickVDescriptor


<a href="https://github.com/autoplot/dev/search?q=bestTickVLinear&unscoped_q=bestTickVLinear">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bestTickVLogNew"></a>
# bestTickVLogNew
bestTickVLogNew( Datum minD, Datum maxD, int nTicksMin, int nTicksMax, boolean fin ) &rarr; TickVDescriptor

return a set of log ticks, within the given constraints.

### Parameters:
minD - the minimum
<br>maxD - the maximum
<br>nTicksMin - the minimum number of ticks.
<br>nTicksMax - the maximum number of ticks.
<br>fin - final, useful when debugging.

### Returns:
an org.das2.graph.TickVDescriptor


<a href="https://github.com/autoplot/dev/search?q=bestTickVLogNew&unscoped_q=bestTickVLogNew">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bestTickVTime"></a>
# bestTickVTime
bestTickVTime( Datum minD, Datum maxD, int nTicksMin, int nTicksMax, boolean fin ) &rarr; TickVDescriptor



### Parameters:
minD - a Datum
<br>maxD - a Datum
<br>nTicksMin - an int
<br>nTicksMax - an int
<br>fin - a boolean

### Returns:
org.das2.graph.TickVDescriptor


<a href="https://github.com/autoplot/dev/search?q=bestTickVTime&unscoped_q=bestTickVTime">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="bestTickVTimeOrdinal"></a>
# bestTickVTimeOrdinal
bestTickVTimeOrdinal( Datum minD, Datum maxD, int nTicksMin, int nTicksMax, boolean fin ) &rarr; TickVDescriptor

return a set of ticks counting off ordinal time ranges, such as months, years, days, etc.

### Parameters:
minD - the minimum
<br>maxD - the maximum
<br>nTicksMin - the minimum number of ticks.
<br>nTicksMax - the maximum number of ticks.
<br>fin - final, useful when debugging.

### Returns:
an org.das2.graph.TickVDescriptor


<a href="https://github.com/autoplot/dev/search?q=bestTickVTimeOrdinal&unscoped_q=bestTickVTimeOrdinal">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="enclosingRange"></a>
# enclosingRange
enclosingRange( DatumRange dr, boolean minor ) &rarr; DatumRange

Defining method for getting the range close to the given range,
 but containing at least one minor(or major) tick interval.

### Parameters:
dr - a DatumRange
<br>minor - find the range from the minor ticks.

### Returns:
a DatumRange

### See Also:
<a href='DomainDivider.md'>DomainDivider</a> <br>

<a href="https://github.com/autoplot/dev/search?q=enclosingRange&unscoped_q=enclosingRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="findTick"></a>
# findTick
findTick( Datum xDatum, double direction, boolean minor ) &rarr; Datum

Locates the next or previous tick starting at xDatum.

### Parameters:
xDatum - find the tick closest to this.
<br>direction - -1 previous, 1 next, 0 closest
<br>minor - find closest minor tick, major if false.

### Returns:
the closest tick.  If there is no tick in the given direction, then
   the behavior is undefined.

<a href="https://github.com/autoplot/dev/search?q=findTick&unscoped_q=findTick">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFormatter"></a>
# getFormatter
getFormatter(  ) &rarr; DatumFormatter



### Returns:
org.das2.datum.format.DatumFormatter


<a href="https://github.com/autoplot/dev/search?q=getFormatter&unscoped_q=getFormatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMajorTicks"></a>
# getMajorTicks
getMajorTicks(  ) &rarr; DatumVector



### Returns:
org.das2.datum.DatumVector


<a href="https://github.com/autoplot/dev/search?q=getMajorTicks&unscoped_q=getMajorTicks">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMinorTicks"></a>
# getMinorTicks
getMinorTicks(  ) &rarr; DatumVector



### Returns:
org.das2.datum.DatumVector


<a href="https://github.com/autoplot/dev/search?q=getMinorTicks&unscoped_q=getMinorTicks">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDayOfYear"></a>
# isDayOfYear
isDayOfYear(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isDayOfYear&unscoped_q=isDayOfYear">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="newTickVDescriptor"></a>
# newTickVDescriptor
newTickVDescriptor( org.das2.datum.DatumVector majorTicks, org.das2.datum.DatumVector minorTicks ) &rarr; TickVDescriptor



### Parameters:
majorTicks - a DatumVector
<br>minorTicks - a DatumVector

### Returns:
org.das2.graph.TickVDescriptor


<a href="https://github.com/autoplot/dev/search?q=newTickVDescriptor&unscoped_q=newTickVDescriptor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

newTickVDescriptor( java.util.List majorTicks, java.util.List minorTicks ) &rarr; TickVDescriptor<br>
***
<a name="setDayOfYear"></a>
# setDayOfYear
setDayOfYear( boolean dayOfYear ) &rarr; void



### Parameters:
dayOfYear - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDayOfYear&unscoped_q=setDayOfYear">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFormatter"></a>
# setFormatter
setFormatter( org.das2.datum.format.DatumFormatter datumFormatter ) &rarr; void



### Parameters:
datumFormatter - a DatumFormatter

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFormatter&unscoped_q=setFormatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String

Returns a String representation of the TickVDescriptor.

### Returns:
a String representation of the TickVDescriptor.

<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

