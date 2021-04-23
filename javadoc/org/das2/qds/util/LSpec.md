# org.das2.qds.util.LSpec

Form a rank 2 dataset with L and Time for tags by identifying monotonic sweeps
 in two rank 1 datasets, and interpolating along the sweep.

***
<a name="USER_PROP_SWEEPS"></a>
# USER_PROP_SWEEPS

identifies the sweep of each record

***
<a name="DIR_INWARD"></a>
# DIR_INWARD

just the inward sweeps

***
<a name="DIR_OUTWARD"></a>
# DIR_OUTWARD

just the outward sweeps

***
<a name="DIR_BOTH"></a>
# DIR_BOTH

include both sweeps

***
<a name="identifySweeps"></a>
# identifySweeps
identifySweeps( QDataSet lds, int dir ) &rarr; QDataSet

identify monotonically increasing or decreasing segments of the dataset.

### Parameters:
lds - the dataset which sweeps back and forth, such as LShell or MagLat (or a sine wave for testing).
<br>dir - 0=both 1=outward 2= inward

### Returns:
rank 2 data set of sweep indeces, dim0 is sweep number, dim1 is two-element [ start, end(inclusive) ].

<a href="https://github.com/autoplot/dev/search?q=identifySweeps&unscoped_q=identifySweeps">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rebin"></a>
# rebin
rebin( QDataSet lds, QDataSet zds, QDataSet lgrid ) &rarr; QDataSet

rebin the datasets to rank 2 dataset ( time, LShell ), by interpolating along sweeps.  This
 dataset has the property "sweeps", which is a dataset that indexes the input datasets.

### Parameters:
lds - rank 1 dataset of length N
<br>zds - rank 1 dataset of length N, indexed along with <tt>lds</tt>
<br>lgrid - rank 1 dataset indicating the dim 1 tags for the result dataset.

### Returns:
a rank 2 dataset, with one column per sweep, interpolated to <tt>lgrid</tt>

<a href="https://github.com/autoplot/dev/search?q=rebin&unscoped_q=rebin">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

rebin( QDataSet tlz, QDataSet lgrid, int dir ) &rarr; QDataSet<br>
rebin( QDataSet tt, QDataSet lds, QDataSet zds, QDataSet tspace, QDataSet lgrid, int dir ) &rarr; QDataSet<br>
rebin( QDataSet lds, QDataSet zds, QDataSet lgrid, int dir ) &rarr; QDataSet<br>
