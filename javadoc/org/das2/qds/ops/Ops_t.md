***
<a name="taggen"></a>
# taggen
taggen( double base, double dcadence, int len0, Units units ) &rarr; MutablePropertyDataSet

creates tags.  First tag will be start and they will increase by cadence.  Units specifies
 the units of each tag.

### Parameters:
base - a double
<br>dcadence - a double
<br>len0 - an int
<br>units - an Units

### Returns:
an org.das2.qds.MutablePropertyDataSet


<a href="https://github.com/autoplot/dev/search?q=taggen&unscoped_q=taggen">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="tan"></a>
# tan
tan( QDataSet ds ) &rarr; QDataSet

element-wise tan.

### Parameters:
ds - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=tan&unscoped_q=tan">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

tan( double ds ) &rarr; double<br>
tan( Object ds ) &rarr; QDataSet<br>
***
<a name="tanh"></a>
# tanh
tanh( QDataSet ds ) &rarr; QDataSet

element-wise tanh.

### Parameters:
ds - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=tanh&unscoped_q=tanh">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

tanh( double ds ) &rarr; double<br>
tanh( Object ds ) &rarr; QDataSet<br>
***
<a name="timegen"></a>
# timegen
timegen( String baseTime, String cadence, int len0 ) &rarr; QDataSet

returns rank 1 dataset with values that are times.

### Parameters:
baseTime - e.g. "2003-02-04T00:00"
<br>cadence - e.g. "4.3 sec" "1 day"
<br>len0 - the number of elements.

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=timegen&unscoped_q=timegen">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toDegrees"></a>
# toDegrees
toDegrees( QDataSet ds ) &rarr; QDataSet

convert the data to degrees by multiplying each element by 180/PI.
 This does not check the units of the data, but a future version might.

### Parameters:
ds - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=toDegrees&unscoped_q=toDegrees">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

toDegrees( Object ds ) &rarr; QDataSet<br>
***
<a name="toRadians"></a>
# toRadians
toRadians( QDataSet ds ) &rarr; QDataSet

convert the data to radians by multiplying each element by PI/180.
 This does not check the units of the data, but a future version might.

### Parameters:
ds - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=toRadians&unscoped_q=toRadians">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

toRadians( Object ds ) &rarr; QDataSet<br>
***
<a name="toTimeDataSet"></a>
# toTimeDataSet
toTimeDataSet( QDataSet years, QDataSet mons, QDataSet days, QDataSet hour, QDataSet minute, QDataSet second, QDataSet nano ) &rarr; QDataSet

return a rank 1 dataset of times.  All inputs should be rank 1 dataset (for now) or null.

### Parameters:
years - the years. (2010) Less than 100 is interpreted as 19xx.
<br>mons - the months (1..12), or null.  If null, then days are day of year.  These are interpreted as integers
<br>days - the day of month (1..28) or day of year.  This may be fractional.
<br>hour - null or the hours of the day.
<br>minute - null or the minutes of the day
<br>second - null or the seconds of the day
<br>nano - null or the nanoseconds (1e-9) of the day

### Returns:
rank 1 time data set.

<a href="https://github.com/autoplot/dev/search?q=toTimeDataSet&unscoped_q=toTimeDataSet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

toTimeDataSet( Object years, Object mons, Object days, Object hour, Object minute, Object second, Object nano ) &rarr; QDataSet<br>
***
<a name="total"></a>
# total
total( QDataSet ds ) &rarr; double

return the total of all the elements in the dataset.  If there are 
 invalid measurements, then fill is returned.
 Does not support BINS or BUNDLE dimensions.

### Parameters:
ds - a QDataSet

### Returns:
the unweighted total of the dataset, or -1e31 if fill was encountered.
### See Also:
<a href='Ops_t.md#total'>total(QDataSet, int)</a> total, which should be used instead.<br>

<a href="https://github.com/autoplot/dev/search?q=total&unscoped_q=total">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

total( QDataSet ds, ProgressMonitor mon ) &rarr; double<br>
total( Object ds1 ) &rarr; double<br>
total( QDataSet ds, int dim ) &rarr; QDataSet<br>
total( QDataSet ds, int dim, ProgressMonitor mon ) &rarr; QDataSet<br>
***
<a name="transpose"></a>
# transpose
transpose( QDataSet ds ) &rarr; QDataSet

transpose the rank 2 dataset.  result[i,j]= ds[j,i] for each i,j.

### Parameters:
ds - rank 2 dataset

### Returns:
rank 2 dataset

<a href="https://github.com/autoplot/dev/search?q=transpose&unscoped_q=transpose">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

transpose( Object ds ) &rarr; QDataSet<br>
***
<a name="trim"></a>
# trim
trim( QDataSet ds, int st, int en ) &rarr; QDataSet

trim the dataset to the indeces on the zeroth dimension.  Note
 the trim function can also be called directly.

### Parameters:
ds - the dataset to be trimmed.
<br>st - the start index
<br>en - the non-inclusive end index

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=trim&unscoped_q=trim">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

trim( QDataSet ds, DatumRange dr ) &rarr; QDataSet<br>
trim( QDataSet ds, Object odr ) &rarr; QDataSet<br>
trim( QDataSet ds, QDataSet st, QDataSet en ) &rarr; QDataSet<br>
trim( int dim, QDataSet ds, int st, int en ) &rarr; QDataSet<br>
trim( int dim, QDataSet ds, QDataSet st, QDataSet en ) &rarr; QDataSet<br>
***
<a name="trim1"></a>
# trim1
trim1( QDataSet ds, QDataSet st, QDataSet en ) &rarr; QDataSet

return the trim of the dataset ds where its DEPEND_1 (typically ytags) are
 within the range dr.  For example,
 if ds was frequencies from 10 Hz to 1e8 Hz, trim1( ds, 100Hz, 1000Hz ) would
 return just the data in this range.

### Parameters:
ds - the dataset to be trimmed, with a rank 1 monotonic DEPEND_1.
<br>st - rank 0 min value
<br>en - rank 0 max value

### Returns:
the subset of the data.
### See Also:
<a href='Ops_s.md#slice1'>slice1(QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=trim1&unscoped_q=trim1">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

trim1( QDataSet ds, int st, int en ) &rarr; QDataSet<br>
