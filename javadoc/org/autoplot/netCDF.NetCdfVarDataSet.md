# org.autoplot.netCDF.NetCdfVarDataSetwraps a netCDF variable (or HDF5 variable) to present it as a QDataSet.
***
<a name="create"></a>
# create
create( Variable variable, String constraint, NetcdfDataset ncfile, ProgressMonitor mon ) &rarr; NetCdfVarDataSet



### Parameters:
variable - a Variable
<br>constraint - a String
<br>ncfile - a NetcdfDataset
<br>mon - a ProgressMonitor

### Returns:
org.autoplot.netCDF.NetCdfVarDataSet


<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="length"></a>
# length
length(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=length&unscoped_q=length">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

length( int dim ) &rarr; int<br>
length( int dim0, int dim1 ) &rarr; int<br>
length( int dim0, int dim1, int dim2 ) &rarr; int<br>
***
<a name="parseConstraint"></a>
# parseConstraint
parseConstraint( String constraint, long recCount ) &rarr; long

returns [ start, stop, stride ] or [ start, -1, -1 ] for slice.  This is
 provided to reduce code and for uniform behavior.
 
 See CdfJavaDataSource, which is where this was copied from.

### Parameters:
constraint - a String
<br>recCount - the number of records for when negative indeces are used.

### Returns:
[ start, stop, stride ] or [ start, -1, -1 ] for slice.

<a href="https://github.com/autoplot/dev/search?q=parseConstraint&unscoped_q=parseConstraint">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rank"></a>
# rank
rank(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=rank&unscoped_q=rank">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="slice"></a>
# slice
slice( int i ) &rarr; QDataSet



### Parameters:
i - an int

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=slice&unscoped_q=slice">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="trim"></a>
# trim
trim( int start, int end ) &rarr; QDataSet



### Parameters:
start - an int
<br>end - an int

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=trim&unscoped_q=trim">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="value"></a>
# value
value( int i ) &rarr; double



### Parameters:
i - an int

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

value( int i, int j ) &rarr; double<br>
value( int i, int j, int k ) &rarr; double<br>
value( int i, int j, int k, int l ) &rarr; double<br>
