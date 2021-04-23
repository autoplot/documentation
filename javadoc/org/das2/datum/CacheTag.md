# org.das2.datum.CacheTag

CacheTags are used to represent the coverage of datasets stored in a cache, and are
 the reference used to decide if a cache entry is capable of satisfying a data request.

# CacheTag( Datum start, Datum end, Datum resolution )
Constructs a new CacheTag.

# CacheTag( DatumRange range, Datum resolution )
Constructs a new CacheTag.

***
<a name="INTRINSIC"></a>
# INTRINSIC



***
<a name="append"></a>
# append
append( org.das2.datum.CacheTag tag1, org.das2.datum.CacheTag tag2 ) &rarr; CacheTag

Appends two CacheTags, when possible.  The new range covers the ranges, and the resolution is the lower of the two.

### Parameters:
tag1 - a CacheTag
<br>tag2 - a CacheTag that is adjacent to tag1

### Returns:
a CacheTag that covers both CacheTags precisely.

<a href="https://github.com/autoplot/dev/search?q=append&unscoped_q=append">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="contains"></a>
# contains
contains( org.das2.datum.CacheTag tag ) &rarr; boolean

Indicates if the cache tag the the capability of satifying the given cache tag.  If the tag has a lower (courser) resolution and its bounds are within
 this CacheTag.

### Parameters:
tag - a CacheTag to test.

### Returns:
true if the tag has a lower resolution and its bounds are within
 this CacheTag.

<a href="https://github.com/autoplot/dev/search?q=contains&unscoped_q=contains">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRange"></a>
# getRange
getRange(  ) &rarr; DatumRange

the range covered by the cache tag.

### Returns:
org.das2.datum.DatumRange


<a href="https://github.com/autoplot/dev/search?q=getRange&unscoped_q=getRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getResolution"></a>
# getResolution
getResolution(  ) &rarr; Datum

the resolution of the cache tag, which may be null.

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getResolution&unscoped_q=getResolution">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String

Returns a string representation of the object.

### Returns:
a human consumable representation of the cache tag.  This should fit on
 one line as it is used to list cache contents.

<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

