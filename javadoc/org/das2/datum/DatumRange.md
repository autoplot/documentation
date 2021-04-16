# org.das2.datum.DatumRangeA DatumRange is provided as a means to carry an ordered pair of Datums
 representing an interval.  This sort of data structure comes up often in
 processing, and it's useful to define once and get the operators
 implemented correctly.  Consider using this object whenever you see
 pairs of Datums in interfaces and codes (e.g. tbegin,tend), they are probably
 a DatumRange!
DatumRange( Datum s1, Datum s2 )
Creates valid DatumRange from two Datums.

DatumRange( double s1, double s2, Units units )
create a datum range from two doubles in the context of units.

***
<a name="compareTo"></a>
# compareTo
compareTo( Object o ) &rarr; int

Compare this to another DatumRange, ordered by the lesser datum, 
 then the greater datum.  This is mostly provided for .equals, but also 
 so there is a consistent ordering convention though out the system.

### Parameters:
o - the DatumRange to compare this DatumRange to.

### Returns:
an int &lt; 0 if this comes before DatumRange a in this DatumRange's units space, 0 if they are equal, and &gt; 0 otherwise.

<a href="https://github.com/autoplot/dev/search?q=compareTo&unscoped_q=compareTo">[search for examples]</a>

***
<a name="contains"></a>
# contains
contains( DatumRange dr ) &rarr; boolean

returns true of param dr is contained by this, so that this.union(dr).equals(this).

### Parameters:
dr - the datum range to test.

### Returns:
true iff this.union(dr).equals(this);

<a href="https://github.com/autoplot/dev/search?q=contains&unscoped_q=contains">[search for examples]</a>

contains( Datum d ) &rarr; boolean<br>
***
<a name="convertTo"></a>
# convertTo
convertTo( Units u ) &rarr; DatumRange

return this DatumRange in new units.  Note this may cause some functions
 of a DatumRange to change, such as the next() for a MonthDatumRange, but
 implementations should attempt to preserve type.

### Parameters:
u - the new units.

### Returns:
the DatumRange in the new units.

<a href="https://github.com/autoplot/dev/search?q=convertTo&unscoped_q=convertTo">[search for examples]</a>

***
<a name="equals"></a>
# equals
equals( Object o ) &rarr; boolean

returns true if the two endpoints are equal.

### Parameters:
o - an Object

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=equals&unscoped_q=equals">[search for examples]</a>

***
<a name="getUnits"></a>
# getUnits
getUnits(  ) &rarr; Units

return the units of the DatumRange.

### Returns:
the units of the DatumRange.

<a href="https://github.com/autoplot/dev/search?q=getUnits&unscoped_q=getUnits">[search for examples]</a>

***
<a name="hashCode"></a>
# hashCode
hashCode(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=hashCode&unscoped_q=hashCode">[search for examples]</a>

***
<a name="include"></a>
# include
include( Datum d ) &rarr; DatumRange

return a new DatumRange that includes the given Datum, extending the
 range if necessary.  For example, 
 <pre> [0,1).include(2)&rarr; [0,2)  (note this is exclusive of 2 since it's the end).
 [0,1).include(-1)&rarr; [-1,1).
 [0,1).include(0.5) &rarr; [0,1]  (and returns the same DatumRange object)
 </pre>
 Also, including a fill Datum returns the same DatumRange as well.

### Parameters:
d - the Datum to include

### Returns:
the new range.

<a href="https://github.com/autoplot/dev/search?q=include&unscoped_q=include">[search for examples]</a>

***
<a name="intersection"></a>
# intersection
intersection( DatumRange dr ) &rarr; DatumRange

returns the intersection of the two intersecting ranges.  This is a range that contains(d) if 
 and only if this.contains(d) and dr.contains(d).

### Parameters:
dr - a valid datum range.

### Returns:
the intersection of the two intersecting ranges.
### See Also:
<a href='DatumRangeUtil.md#sloppyIntersection'>DatumRangeUtil#sloppyIntersection(org.das2.datum.DatumRange, org.das2.datum.DatumRange)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=intersection&unscoped_q=intersection">[search for examples]</a>

***
<a name="intersects"></a>
# intersects
intersects( DatumRange dr ) &rarr; boolean

returns true of the DatumRange overlaps this.  Note that the endpoints are not
 included in the comparison, so that Tuesday.intersects(Wednesday)==false.

### Parameters:
dr - a valid datum range

### Returns:
true of the DatumRange overlaps this

<a href="https://github.com/autoplot/dev/search?q=intersects&unscoped_q=intersects">[search for examples]</a>

***
<a name="max"></a>
# max
max(  ) &rarr; Datum

returns the bigger value or stop of the range.

### Returns:
the bigger value or stop of the range.

<a href="https://github.com/autoplot/dev/search?q=max&unscoped_q=max">[search for examples]</a>

***
<a name="middle"></a>
# middle
middle(  ) &rarr; Datum

returns the middle value of the range, often useful when 
 the most descriptive value is needed.

### Returns:
the middle value of the range.

<a href="https://github.com/autoplot/dev/search?q=middle&unscoped_q=middle">[search for examples]</a>

***
<a name="min"></a>
# min
min(  ) &rarr; Datum

returns the smaller value or start of the range.

### Returns:
the smaller value or start of the range.

<a href="https://github.com/autoplot/dev/search?q=min&unscoped_q=min">[search for examples]</a>

***
<a name="newDatumRange"></a>
# newDatumRange
newDatumRange( double min, double max, Units units ) &rarr; DatumRange

creates a new DatumRange object with the range specified in the space
 identified by units.  Note that min must be &lt;= max.

### Parameters:
min - the minimum value
<br>max - the maximum value which is greater than or equal to the min.
<br>units - the units of the two doubles.

### Returns:
the DatumRange

<a href="https://github.com/autoplot/dev/search?q=newDatumRange&unscoped_q=newDatumRange">[search for examples]</a>

***
<a name="next"></a>
# next
next(  ) &rarr; DatumRange

returns the next DatumRange covering the space defined by Units.  Typically,
 this will be a range with a min equal to this datum's max, and the same width.
 Some implementations of DatumRange may return a range with a different width
 than this DatumRange's width, for example, when advancing month-by-month
 with a MonthDatumRange.

### Returns:
the next DatumRange covering the space defined by Units.

<a href="https://github.com/autoplot/dev/search?q=next&unscoped_q=next">[search for examples]</a>

***
<a name="normalize"></a>
# <del>normalize</del>
Deprecated: Use DatumRangeUtil.normalize
***
<a name="previous"></a>
# previous
previous(  ) &rarr; DatumRange

returns the previous DatumRange covering the space defined by Units.  See
 next().

### Returns:
the previous DatumRange covering the space defined by Units

<a href="https://github.com/autoplot/dev/search?q=previous&unscoped_q=previous">[search for examples]</a>

***
<a name="rescale"></a>
# <del>rescale</del>
Deprecated: Use DatumRangeUtil.rescale
***
<a name="toString"></a>
# toString
toString(  ) &rarr; String

returns a human consumable representation of the string.  This should also be parsable with 
 DatumRangeUtil.parseDatumRange, but this has not been verified to complete certainty.

### Returns:
the DatumRange as a String.

<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

***
<a name="union"></a>
# union
union( DatumRange dr ) &rarr; DatumRange

returns the union of the two intersecting or adjacent ranges.

### Parameters:
dr - the other range of consistent units.

### Returns:
DatumRange union of the two DatumRanges

<a href="https://github.com/autoplot/dev/search?q=union&unscoped_q=union">[search for examples]</a>

***
<a name="width"></a>
# width
width(  ) &rarr; Datum

returns the width of the range, which is simply the greater minus the lessor.
 Note that the units of the result will not necessarily be the same as the
 endpoints, for example with LocationDatums.

### Returns:
Datum that is the width of the range (max.subtract(min)).

<a href="https://github.com/autoplot/dev/search?q=width&unscoped_q=width">[search for examples]</a>

***
<a name="zoomOut"></a>
# zoomOut
zoomOut( double factor ) &rarr; DatumRange

returns a scaled DatumRange, with a new width that is the this
 datumRange's width multiplied by factor, and the same center.
 1.0 is the same range, 2.0 has twice the width, etc.

### Parameters:
factor - double representing the new range's width divided by this range's width.

### Returns:
a scaled DatumRange, with a new width that is the this
 datumRange's width multiplied by factor, and the same center.

<a href="https://github.com/autoplot/dev/search?q=zoomOut&unscoped_q=zoomOut">[search for examples]</a>

