# org.das2.datum.DomainDivider

Divides a given range of input values into useful intervals.  This can be
 used, for example, to determine the locations of tick marks on an axis.
 Implementations will vary their behavior based on a number of factors including
 the type of data in question.
 <p>
 Note that the intervals need not be uniformly sized.  For example, this would
 be the case when dividing a time interval into months, or into log spaced
 intervals.
 <p>
 Implementations should have protected constructors so factory methods in
 <code>DomainDividerUtil</code> can access them.

***
<a name="MAX_BOUNDARIES"></a>
# MAX_BOUNDARIES



***
<a name="boundaries"></a>
# boundaries
boundaries( Datum min, Datum max ) &rarr; DatumVector

Returns the boundaries between intervals on the given data range. When
 min or max lay on a boundary, it should be returned.  Note this is
 inconsistent with DatumRange logic, where the max is exclusive.
 If min>=max, then an empty list should be returned.

### Parameters:
min - a Datum
<br>max - a Datum

### Returns:
a <code>DatumVector</code> containing the boundary values

<a href="https://github.com/autoplot/dev/search?q=boundaries&unscoped_q=boundaries">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="boundaryCount"></a>
# boundaryCount
boundaryCount( Datum min, Datum max ) &rarr; long

Compute the number of intervals produced by this <code>DomainDivider</code>
 on the given range.  This allows the DomainDivider to indicate the number
 of intervals (e.g. a zillion) without having to enumerate them.  When
 min or max lay on a boundary, it should be counted.  If min>=max, then 
 zero should be returned.

### Parameters:
min - a Datum
<br>max - a Datum

### Returns:
a long


<a href="https://github.com/autoplot/dev/search?q=boundaryCount&unscoped_q=boundaryCount">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="coarserDivider"></a>
# coarserDivider
coarserDivider( boolean superset ) &rarr; DomainDivider

Return a new divider with larger intervals.  If the <code>superset</code>
 parameter is true, the interval boundaries of the new divider are
 guaranteed to align with (some) interval boundaries of the existing one.
 In other words, the existing divider will subdivide the new one.

### Parameters:
superset - true to force boundary alignment with the calling <code>DomainDivider</code>.
   For a given range, the boundaries will be aligned.

### Returns:
the new DomainDivider object

<a href="https://github.com/autoplot/dev/search?q=coarserDivider&unscoped_q=coarserDivider">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="finerDivider"></a>
# finerDivider
finerDivider( boolean superset ) &rarr; DomainDivider

Return a new divider with smaller intervals. If the <code>superset</code>
 parameter is true, the interval boundaries of the existing divider are
 guaranteed to align with (some) intervals of the new one.  In other
 words, the new divider will subdivide the existing one.

### Parameters:
superset - true to force boundary alignment with the calling <code>DomainDivider</code>
     For a given range, the boundaries will be aligned.

### Returns:
the new DomainDivider object

<a href="https://github.com/autoplot/dev/search?q=finerDivider&unscoped_q=finerDivider">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rangeContaining"></a>
# rangeContaining
rangeContaining( Datum v ) &rarr; DatumRange

Return a <code>DatumRange</code> representing the interval containing
 the given value.

### Parameters:
v - a Datum

### Returns:
a DatumRange


<a href="https://github.com/autoplot/dev/search?q=rangeContaining&unscoped_q=rangeContaining">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

