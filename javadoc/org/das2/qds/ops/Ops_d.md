***
<a name="dataIntersection"></a>
# dataIntersection
dataIntersection( int[] itE, int[] itB ) &rarr; int

return the values which occur in both rank 1 datasets.  Each dataset is sorted.

### Parameters:
itE - a bunch of values.
<br>itB - a bunch of values.

### Returns:
the set of values found in both.
### See Also:
<a href='Ops_e.md#eventsConjunction'>eventsConjunction(QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=dataIntersection&unscoped_q=dataIntersection">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

dataIntersection( QDataSet tE, QDataSet tB ) &rarr; QDataSet<br>
***
<a name="dataset"></a>
# dataset
dataset( Object arg0 ) &rarr; QDataSet

coerce Java objects like arrays Lists and scalars into a QDataSet.  
 This is introduced to mirror the useful Jython dataset command.  This is a nasty business that
 is surely going to cause all sorts of problems, so we should do it all in one place.
 See http://jfaden.net/jenkins/job/autoplot-test029/
 This supports:<ul>
   <li>int, float, double, etc to Rank 0 datasets
   <li>List&lt;Number&gt; to Rank 1 datasets.
   <li>Java arrays of Number to Rank 1-4 qubes datasets
   <li>Strings to rank 0 datasets with units ("5 s" or "2014-01-01T00:00")
   <li>Datums to rank 0 datasets
   <li>DatumRanges to rank 1 bins
 </ul>

### Parameters:
arg0 - null,QDataSet,Number,Datum,DatumRange,String,List,or array.

### Returns:
QDataSet

<a href="https://github.com/autoplot/dev/search?q=dataset&unscoped_q=dataset">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

dataset( Object arg0, Units u ) &rarr; QDataSet<br>
***
<a name="datum"></a>
# datum
datum( Object arg0 ) &rarr; Datum

coerce Java objects like numbers and strings into a Datum.
 This is introduced to mirror the useful Jython dataset command.  This is a nasty business that
 is surely going to cause all sorts of problems, so we should do it all in one place.
 See http://jfaden.net:8080/hudson/job/autoplot-test029/
 This supports:<ul>
   <li>int, float, double, etc to Rank 0 datasets
   <li>Strings to rank 0 datasets with units ("5 s" or "2014-01-01T00:00")
   <li>rank 0 datasets 
 </ul>

### Parameters:
arg0 - null,QDataSet,Number,Datum, or String.

### Returns:
Datum

<a href="https://github.com/autoplot/dev/search?q=datum&unscoped_q=datum">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="datumRange"></a>
# datumRange
datumRange( Object arg0 ) &rarr; DatumRange

coerce Java objects like arrays and strings into a DatumRange.
 This is introduced to mirror the useful Jython dataset command.  This is a nasty business that
 is surely going to cause all sorts of problems, so we should do it all in one place.
 See http://jfaden.net:8080/hudson/job/autoplot-test029/
 This supports:<ul>
   <li>2-element rank 1 QDataSet
   <li>Strings like ("5 to 15 s" or "2014-01-01")
   <li>2-element arrays and lists
 </ul>

### Parameters:
arg0 - null, QDataSet, String, array or List.

### Returns:
DatumRange

<a href="https://github.com/autoplot/dev/search?q=datumRange&unscoped_q=datumRange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="dblarr"></a>
# dblarr
dblarr( int len0 ) &rarr; QDataSet

create a rank 1 dataset filled with zeros, stored in 8-byte doubles.

### Parameters:
len0 - the length of the zeroth dimension.

### Returns:
rank 1 dataset filled with zeros.
### See Also:
<a href='Ops_z.md#zeros'>zeros(int)</a> <br>
<a href='Ops_f.md#fltarr'>fltarr(int)</a> <br>
<a href='Ops_b.md#bytarr'>bytarr(int)</a> <br>
<a href='Ops_s.md#shortarr'>shortarr(int)</a> <br>
<a href='Ops_i.md#intarr'>intarr(int)</a> <br>
<a href='Ops_l.md#lonarr'>lonarr(int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=dblarr&unscoped_q=dblarr">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

dblarr( int len0, int len1 ) &rarr; QDataSet<br>
dblarr( int len0, int len1, int len2 ) &rarr; QDataSet<br>
***
<a name="decimate"></a>
# decimate
decimate( QDataSet ds ) &rarr; QDataSet

reduce the size of the data by keeping every 10th measurement.

### Parameters:
ds - a qube dataset.

### Returns:
a decimated qube dataset.
### See Also:
<a href='Ops_d.md#decimate'>decimate(QDataSet, int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=decimate&unscoped_q=decimate">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

decimate( QDataSet ds, int m ) &rarr; QDataSet<br>
decimate( QDataSet ds, int m, int n ) &rarr; QDataSet<br>
***
<a name="dependsOn"></a>
# dependsOn
dependsOn( QDataSet ds, int dim, QDataSet dep ) &rarr; MutablePropertyDataSet

declare that the dataset is a dependent parameter of an independent parameter.
 This isolates the QDataSet semantics, and verifies correctness.  See also link(x,y).

### Parameters:
ds - the dataset
<br>dim - dimension to declare dependence: 0,1,2.
<br>dep - the independent dataset.

### Returns:
the dataset, which may be a copy if the data was not mutable.

<a href="https://github.com/autoplot/dev/search?q=dependsOn&unscoped_q=dependsOn">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="detrend"></a>
# detrend
detrend( QDataSet yy, int size ) &rarr; QDataSet

remove D/C and low-frequency components from the data by subtracting
 out the smoothed data with a boxcar of the given size.  Points on the 
 end are zero.

### Parameters:
yy - rank 1 dataset
<br>size - size of the boxcar

### Returns:
dataset

<a href="https://github.com/autoplot/dev/search?q=detrend&unscoped_q=detrend">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

detrend( Object yy, int size ) &rarr; QDataSet<br>
***
<a name="diff"></a>
# diff
diff( QDataSet ds ) &rarr; QDataSet

return array that is the differences between each successive pair in the dataset.
 Result[i]= ds[i+1]-ds[i], so that for an array with N elements, an array with
 N-1 elements is returned.  When the data has a DEPEND_0, the result
 will have a DEPEND_0 which contains the average of the corresponding points.

### Parameters:
ds - a rank 1 dataset with N elements.

### Returns:
a rank 1 dataset with N-1 elements.
### See Also:
<a href='Ops_a.md#accum'>accum(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=diff&unscoped_q=diff">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

diff( Object ds ) &rarr; QDataSet<br>
***
<a name="dimensionCount"></a>
# dimensionCount
dimensionCount( QDataSet dss ) &rarr; int

returns the number of physical dimensions of a dataset.
 <ul>
 <li>JOIN, BINS   do not increase dataset dimensionality.
 <li>DEPEND       increases dimensionality by dimensionality of DEPEND ds.
 <li>BUNDLE       increases dimensionality by N, where N is the number of bundled datasets.
 </ul>
 Note this includes implicit dimensions taken by the primary dataset:
 <ul>
   <li>Z(time,freq)&rarr;3
   <li>rand(20,20)&rarr;3
   <li>B_gsm(20,[X,Y,Z])&rarr;4
 </ul>

### Parameters:
dss - the dataset

### Returns:
the number of dimensions occupied by the data.

<a href="https://github.com/autoplot/dev/search?q=dimensionCount&unscoped_q=dimensionCount">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

dimensionCount( Object dss ) &rarr; int<br>
***
<a name="dindgen"></a>
# dindgen
dindgen( int len0 ) &rarr; QDataSet

returns rank 1 dataset with values [0.,1.,2.,...]

### Parameters:
len0 - an int

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=dindgen&unscoped_q=dindgen">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

dindgen( int len0, int len1 ) &rarr; QDataSet<br>
dindgen( int len0, int len1, int len2 ) &rarr; QDataSet<br>
dindgen( int len0, int len1, int len2, int len3 ) &rarr; QDataSet<br>
***
<a name="distance"></a>
# distance
distance( int len0, double c0, double r0 ) &rarr; QDataSet

return a table of distances d[len0] to the indeces c0; in units of r0.
 This is motivated by a need for more interesting datasets for testing.

### Parameters:
len0 - the length of the dataset
<br>c0 - the center point 0
<br>r0 - the units to normalize in the 0 direction

### Returns:
rank 2 table

<a href="https://github.com/autoplot/dev/search?q=distance&unscoped_q=distance">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

distance( int len0, int len1, double c0, double c1, double r0, double r1 ) &rarr; QDataSet<br>
***
<a name="div"></a>
# div
div( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

element-wise div of two datasets with compatible geometry.

### Parameters:
ds1 - a QDataSet
<br>ds2 - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=div&unscoped_q=div">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

div( Object ds1, Object ds2 ) &rarr; QDataSet<br>
***
<a name="divide"></a>
# divide
divide( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

element-wise divide of two datasets with compatible geometry.  Either
 ds1 or ds2 should be dimensionless, or the units be convertible.
 TODO: units improvements.

### Parameters:
ds1 - the numerator
<br>ds2 - the divisor

### Returns:
the ds1/ds2

<a href="https://github.com/autoplot/dev/search?q=divide&unscoped_q=divide">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

divide( Object ds1, Object ds2 ) &rarr; QDataSet<br>
***
<a name="divp"></a>
# divp
divp( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

This div goes with modp, where -18 divp 10 = -2 and -18 modp 10 = 8.
 the div operator always goes towards zero, but divp always goes to
 the more negative number so the remainder is positive.

### Parameters:
ds1 - a QDataSet
<br>ds2 - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=divp&unscoped_q=divp">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

divp( Object ds1, Object ds2 ) &rarr; QDataSet<br>
