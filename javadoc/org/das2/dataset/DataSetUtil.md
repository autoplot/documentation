# org.das2.dataset.DataSetUtil



# DataSetUtil( )


***
<a name="append"></a>
# append
append( org.das2.dataset.DataSet ds1, org.das2.dataset.DataSet ds2, org.das2.datum.CacheTag ct ) &rarr; DataSet

provides convenient method for appending datasets together.  The first
 dataset may be null, in which case the second is trivially returned.
 Presently a builder is used to create the new dataset, but in the future
 more efficient methods will be used.  If both ds1 and ds2 are null, then
 null is returned.

### Parameters:
ds1 - the first data set.  May be null.
<br>ds2 - the second data set.  This data set should be after ds1, and
    may be null.
<br>ct - the cache tag for the second dataset.  May be null, in which
    case guessCacheTag is used to identify the dataset cache tag.

### Returns:
org.das2.dataset.DataSet


<a href="https://github.com/autoplot/dev/search?q=append&unscoped_q=append">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

append( org.das2.dataset.DataSet ds1, org.das2.dataset.DataSet ds2 ) &rarr; DataSet<br>
***
<a name="closestColumn"></a>
# closestColumn
closestColumn( org.das2.dataset.DataSet table, Datum datum ) &rarr; int



### Parameters:
table - a DataSet
<br>datum - a Datum

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=closestColumn&unscoped_q=closestColumn">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

closestColumn( org.das2.dataset.DataSet table, double x, Units units ) &rarr; int<br>
closestColumn( org.das2.dataset.DataSet table, Datum xdatum, int guessIndex ) &rarr; int<br>
***
<a name="getAllPlaneIds"></a>
# getAllPlaneIds
getAllPlaneIds( org.das2.dataset.DataSet ds ) &rarr; String

returns all planes, including the default plane "".  This is to take care of
 inconsistent behavior of the ds.getPlaneIds() implementations.

### Parameters:
ds - a DataSet

### Returns:
java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=getAllPlaneIds&unscoped_q=getAllPlaneIds">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNextColumn"></a>
# getNextColumn
getNextColumn( org.das2.dataset.DataSet ds, Datum datum ) &rarr; int

returns the first column that is after the given datum.  Note the
 if the datum identifies (==) an xtag, then the previous column is
 returned.

### Parameters:
ds - a DataSet
<br>datum - a Datum

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getNextColumn&unscoped_q=getNextColumn">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPreviousColumn"></a>
# getPreviousColumn
getPreviousColumn( org.das2.dataset.DataSet ds, Datum datum ) &rarr; int

returns the first column that is before the given datum.  Note the
 if the datum identifies (==) an xtag, then the previous column is
 returned.

### Parameters:
ds - a DataSet
<br>datum - a Datum

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getPreviousColumn&unscoped_q=getPreviousColumn">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getWeightsDataSet"></a>
# getWeightsDataSet
getWeightsDataSet( org.das2.dataset.DataSet ds ) &rarr; DataSet



### Parameters:
ds - a DataSet

### Returns:
org.das2.dataset.DataSet


<a href="https://github.com/autoplot/dev/search?q=getWeightsDataSet&unscoped_q=getWeightsDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getXTagArrayDouble"></a>
# getXTagArrayDouble
getXTagArrayDouble( org.das2.dataset.DataSet vds, Units units ) &rarr; double



### Parameters:
vds - a DataSet
<br>units - an Units

### Returns:
double[]


<a href="https://github.com/autoplot/dev/search?q=getXTagArrayDouble&unscoped_q=getXTagArrayDouble">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getXTags"></a>
# getXTags
getXTags( org.das2.dataset.DataSet ds ) &rarr; DatumVector



### Parameters:
ds - a DataSet

### Returns:
org.das2.datum.DatumVector


<a href="https://github.com/autoplot/dev/search?q=getXTags&unscoped_q=getXTags">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="guessCacheTag"></a>
# guessCacheTag
guessCacheTag( org.das2.dataset.DataSet ds ) &rarr; CacheTag



### Parameters:
ds - a DataSet

### Returns:
org.das2.datum.CacheTag


<a href="https://github.com/autoplot/dev/search?q=guessCacheTag&unscoped_q=guessCacheTag">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="guessSizeBytes"></a>
# guessSizeBytes
guessSizeBytes( org.das2.dataset.DataSet ds ) &rarr; long

Give an estimate of the size of the data set, or PROPERTY_SIZE_BYTES if available.
 Generally this would be used as a penalty against the dataset, and it's probably
 better to overestimate the dataset size.

### Parameters:
ds - a DataSet

### Returns:
long


<a href="https://github.com/autoplot/dev/search?q=guessSizeBytes&unscoped_q=guessSizeBytes">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="guessXTagWidth"></a>
# guessXTagWidth
guessXTagWidth( org.das2.dataset.DataSet table ) &rarr; Datum

Provide a reasonable xTagWidth either by returning the specified xTagWidth property,
 or by statistically looking at the X tags.

### Parameters:
table - a DataSet

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=guessXTagWidth&unscoped_q=guessXTagWidth">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="log10"></a>
# log10
log10( org.das2.dataset.VectorDataSet ds ) &rarr; VectorDataSet



### Parameters:
ds - a VectorDataSet

### Returns:
org.das2.dataset.VectorDataSet


<a href="https://github.com/autoplot/dev/search?q=log10&unscoped_q=log10">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="xRange"></a>
# xRange
xRange( org.das2.dataset.DataSet ds ) &rarr; DatumRange

returns the xrange of the dataset.  This assumes that the xtags
 are monotonic.

### Parameters:
ds - a DataSet

### Returns:
a DatumRange


<a href="https://github.com/autoplot/dev/search?q=xRange&unscoped_q=xRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="xTagBinarySearch"></a>
# xTagBinarySearch
xTagBinarySearch( org.das2.dataset.DataSet ds, Datum datum, int low, int high ) &rarr; int

returns the index of a tag, or the  <tt>(-(<i>insertion point</i>) - 1)</tt>.  (See Arrays.binarySearch)

### Parameters:
ds - a DataSet
<br>datum - a Datum
<br>low - an int
<br>high - an int

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=xTagBinarySearch&unscoped_q=xTagBinarySearch">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="yRange"></a>
# yRange
yRange( org.das2.dataset.DataSet ds ) &rarr; DatumRange



### Parameters:
ds - a DataSet

### Returns:
org.das2.datum.DatumRange


<a href="https://github.com/autoplot/dev/search?q=yRange&unscoped_q=yRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="zRange"></a>
# zRange
zRange( org.das2.dataset.DataSet ds ) &rarr; DatumRange

guess a range that characterizes the data.  The DataSet property name
 DataSet.PROPERTY_Z_RANGE can be used by the dataset to explicitly 
 set this.

### Parameters:
ds - a DataSet

### Returns:
a DatumRange useful for setting axis range.

<a href="https://github.com/autoplot/dev/search?q=zRange&unscoped_q=zRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

