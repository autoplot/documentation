# org.das2.qds.util.ReductionReduction is set of static methods for reducing data, or 
 averaging data to make smaller datasets.
Reduction( )


***
<a name="hexbin"></a>
# hexbin
hexbin( QDataSet ds, QDataSet z ) &rarr; QDataSet

reduce the buckshot scatter data by laying it out on a 2-D hexgrid and
 accumulating the hits to each cell.  This has not been thoroughly verified.

### Parameters:
ds - rank1 Y(X)
<br>z - null or data to average

### Returns:
rank 2 ds containing frequency of occurrence for each bin, with DEPEND_0=xxx and DEPEND_1=yyy.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/ops/Ops.md#histogram2d'>org.das2.qds.ops.Ops#histogram2d(QDataSet, QDataSet, int[], QDataSet, QDataSet)</a> <br>
<a href='https://cran.r-project.org/web/packages/hexbin/vignettes/hexagon_binning.pdf'>https://cran.r-project.org/web/packages/hexbin/vignettes/hexagon_binning.pdf</a> <br>

<a href="https://github.com/autoplot/dev/search?q=hexbin&unscoped_q=hexbin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="histogram2D"></a>
# histogram2D
histogram2D( QDataSet ds, QDataSet xxx, QDataSet yyy ) &rarr; QDataSet

reduce the buckshot scatter data by laying it out on a 2-D grid and
 accumulating the hits to each cell.  Written originally to support 
 SeriesRenderer, to replace the "200000 point limit" warning.

### Parameters:
ds - rank1 Y(X)
<br>xxx - rank1 dataset describes the bins, which must be uniformly linearly spaced, or log spaced.  Uses SCALE_TYPE property.
<br>yyy - rank1 dataset describes the bins, which must be uniformly linearly spaced, or log spaced.

### Returns:
rank 2 ds containing frequency of occurrence for each bin, with DEPEND_0=xxx and DEPEND_1=yyy.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/ops/Ops.md#histogram2d'>org.das2.qds.ops.Ops#histogram2d(QDataSet, QDataSet, int[], QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=histogram2D&unscoped_q=histogram2D">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="lastPointAt2D"></a>
# lastPointAt2D
lastPointAt2D( QDataSet ds, QDataSet xx, QDataSet yy, QDataSet xxx, QDataSet yyy ) &rarr; QDataSet

return the value of the last data point at each location.

### Parameters:
ds - rank1 data
<br>xx - rank 1 X values for each data point
<br>yy - rank 1 Y values for each data point
<br>xxx - rank 1 dataset describes the bins, which must be uniformly linearly spaced, or log spaced.  Uses SCALE_TYPE property.
<br>yyy - rank 1 dataset describes the bins, which must be uniformly linearly spaced, or log spaced.

### Returns:
rank 2 ds containing the last point at each bin, with DEPEND_0=xxx and DEPEND_1=yyy.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/ops/Ops.md#histogram2d'>org.das2.qds.ops.Ops#histogram2d(QDataSet, QDataSet, int[], QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=lastPointAt2D&unscoped_q=lastPointAt2D">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reduce2D"></a>
# reduce2D
reduce2D( QDataSet ds, QDataSet xLimit, QDataSet yLimit ) &rarr; QDataSet

produce a simpler version of the dataset by averaging adjacent data.
 code taken from org.das2.graph.GraphUtil.reducePath.  Adjacent points are
 averaged together until a point is found that is not in the bin, and then
 a new bin is started.  The bin's lower bounds are integer multiples
 of xLimit and yLimit.

 If yLimit is null, then averaging is done for all points in the x bin,
 regardless of how close they are in Y.  This is similarly true when
 xLimit is null.

 xLimit and yLimit are rank 0 datasets, so that they can indicate that binning
 should be done in log space rather than linear.  In this case, a SCALE_TYPE
 for the dataset should be "log" and its unit should be convertible to
 Units.logERatio (for example, Units.log10Ratio or Units.percentIncrease).
 Note when either is log, then averaging is done in the log space.

### Parameters:
ds - rank 1 dataset.  Must have DEPEND_0 (presently)
<br>xLimit - the size of the bins or null to indicate no limit.
<br>yLimit - the size of the bins or null to indicate no limit.

### Returns:
the reduced dataset, rank 1 with DEPEND_0.

<a href="https://github.com/autoplot/dev/search?q=reduce2D&unscoped_q=reduce2D">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reducex"></a>
# reducex
reducex( QDataSet ds, QDataSet xLimit ) &rarr; QDataSet

produce a simpler version of the dataset by averaging data adjacent in X.
 code taken from org.das2.graph.GraphUtil.reducePath.  Adjacent points are
 averaged together until a point is found that is not in the bin, and then
 a new bin is started.  The bin's lower bounds are integer multiples
 of xLimit.

 xLimit is a rank 0 dataset.

 2015-06-18: xcadence and bins are now regular.
 
 Because of high-resolution magnetometer data, this is extended to support this data type.
 
 This will set the DELTA_PLUS and DELTA_MINUS variables to the extremes of 
 each bin.  To remove these, use putProperty( QDataSet.DELTA_MINUS, None ) 
 (None in Jython, null for Java) and putProperty( QDataSet.DELTA_PLUS, None ).

### Parameters:
ds - rank 1 or rank 2 dataset.  Must have DEPEND_0 (presently) and be a qube.  If this is null, then the result is null.
<br>xLimit - the size of the bins or null to indicate no limit.

### Returns:
the reduced dataset, or null if the input dataset was null.

<a href="https://github.com/autoplot/dev/search?q=reducex&unscoped_q=reducex">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

reducex( QDataSet ds, QDataSet xLimit, boolean xregular ) &rarr; QDataSet<br>
