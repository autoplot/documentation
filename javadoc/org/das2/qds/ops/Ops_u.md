***
<a name="unbundle"></a>
# unbundle
unbundle( QDataSet ds, String name ) &rarr; QDataSet

Extract the named bundled dataset.  For example, extract B_x from bundle of components.

### Parameters:
ds - the bundle of datasets, often rank 2 with BUNDLE_1 property
<br>name - the name of the bundled dataset, or "ch_&lt;i&gt;" where i is the dataset number

### Returns:
the named dataset
### See Also:
<a href='Ops_u.md#unbundle'>unbundle(QDataSet, int)</a> <br>
<a href='DataSetOps_b.md#bundleNames'>DataSetOps#bundleNames(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=unbundle&unscoped_q=unbundle">[search for examples]</a>

unbundle( QDataSet ds, int i ) &rarr; QDataSet<br>
***
<a name="unbundleBins"></a>
# unbundleBins
unbundleBins( QDataSet ds, int i ) &rarr; QDataSet

convenient method for getting the times from an events dataset, this
 unbundles the startTimes at i and the stopTimes at i+1 to a bins dataset.
 The second column can be durations as well.

### Parameters:
ds - the bundle.
<br>i - the index, 0 for a canonical events dataset.

### Returns:
rank 2 bins dataset.

<a href="https://github.com/autoplot/dev/search?q=unbundleBins&unscoped_q=unbundleBins">[search for examples]</a>

***
<a name="uniq"></a>
# uniq
uniq( QDataSet ds ) &rarr; QDataSet

Return the unique indeces from the rank 1 dataset.  If the 
 set is not monotonic, then return unique indeces from the monotonic
 portions.

### Parameters:
ds - rank 1 dataset, sorted, or mostly sorted.

### Returns:
the element indeces.
### See Also:
<a href='Ops_s.md#sort'>sort(java.lang.Object)</a> <br>
<a href='Ops_u.md#uniq'>uniq(QDataSet, QDataSet)</a> <br>
<a href='Ops_u.md#uniqValues'>uniqValues(QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=uniq&unscoped_q=uniq">[search for examples]</a>

uniq( QDataSet ds, QDataSet sort ) &rarr; QDataSet<br>
***
<a name="uniqValues"></a>
# uniqValues
uniqValues( QDataSet ds, QDataSet sort ) &rarr; QDataSet

return the unique elements from the dataset.  If sort is null, then
 the dataset is assumed to be monotonic, and only repeating values are
 coalesced.  If sort is non-null, then it is the result of the function
 "sort" and should be a rank 1 list of indeces that sort the data.

 renamed uniqValues from uniq to avoid confusion with the IDL command.

 This needs example code and should not be used for now.  See VirboAutoplot/src/scripts/test/testUniq.jy

### Parameters:
ds - rank 1 dataset, sorted, or mostly sorted.
<br>sort - null, or the rank 1 dataset of indeces

### Returns:
the subset of the data which is uniq.
### See Also:
<a href='Ops_u.md#uniq uniq, which returns the indeces.'>uniq uniq, which returns the indeces.</a> uniq, which returns the indeces.<br>
<a href='Ops_u.md#uniq'>uniq(QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=uniqValues&unscoped_q=uniqValues">[search for examples]</a>

***
<a name="unwrap"></a>
# unwrap
unwrap( QDataSet ds, double discont ) &rarr; QDataSet

SciPy's unwrap function, used in demo of hilbertSciPy, which unwraps
 a function that exists in a modulo space so that the differences are 
 minimal.

### Parameters:
ds - rank 1 dataset, containing values from 0 to discont
<br>discont - the discont, such as PI, TAU, 24, 60, 360, etc.

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=unwrap&unscoped_q=unwrap">[search for examples]</a>

