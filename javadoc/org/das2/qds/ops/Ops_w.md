***
<a name="where"></a>
# where
where( QDataSet ds ) &rarr; QDataSet

returns a dataset containing the indeces of where the dataset is non-zero.
 For a rank 1 dataset, returns a rank 1 dataset with indeces for the values.
 For a higher rank dataset, returns a rank 2 qube dataset with ds.rank()
 elements in the first dimension.  Note when the dataset is all zeros (false),
 the result is a zero-length array, as opposed to IDL which would return
 a -1 scalar.
 
 Note fill values are not included in the list, so it is not necessary that
 where(A).length + where(not A).length != where( A.or(not(A) ).length

 Note this is different from the SciPy "where" and similar to Matlab "find."

### Parameters:
ds - of any rank M, M&gt;0.

### Returns:
a rank 1 or rank 2 dataset with N by M elements, where N is the number
 of non-zero elements found.
### See Also:
<a href='Ops_p.md#putValues'>putValues(QDataSet, QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=where&unscoped_q=where">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

where( Object ds ) &rarr; QDataSet<br>
***
<a name="whereSequence"></a>
# whereSequence
whereSequence( QDataSet ds, QDataSet seq ) &rarr; QDataSet

return a list of indeces, similar to the where result.

### Parameters:
ds - rank 1 dataset of length N
<br>seq - rank 1 dataset, with length much less than N.

### Returns:
rank 1 list of indeces.
### See Also:
<a href='https://github.com/autoplot/dev/blob/master/demos/2021/20210115/whereSequence.jy'>https://github.com/autoplot/dev/blob/master/demos/2021/20210115/whereSequence.jy</a> <br>

<a href="https://github.com/autoplot/dev/search?q=whereSequence&unscoped_q=whereSequence">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="windowFunction"></a>
# windowFunction
windowFunction( org.das2.qds.ops.Ops.FFTFilterType filt, int len ) &rarr; QDataSet

return a dataset for the given filter type.  The result will be rank 1 and length len.

### Parameters:
filt - the type of the window.
<br>len - the length of the window.

### Returns:
rank 1 QDataSet with length len.

<a href="https://github.com/autoplot/dev/search?q=windowFunction&unscoped_q=windowFunction">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="within"></a>
# within
within( QDataSet ds, QDataSet bounds ) &rarr; QDataSet

return non-zero where the data in ds are within the bounds.  In Jython,
<blockquote><pre>
print within( [0,1,2,3,4], '2 to 4' ) --> [ 0,0,1,1,0 ]
print within( ttag, 'orbit:rbspa-pp:172' )
</pre></blockquote>
 
 Note, before March 2, 2015, this would incorrectly return the where of the result.

### Parameters:
ds - rank N dataset where N &gt; 0
<br>bounds - a rank 1 bounding box.

### Returns:
rank N dataset containing non-zero where the condition is true.
### See Also:
<a href='Ops_w.md#without'>without(QDataSet, QDataSet)</a> <br>
<a href='Ops_b.md#binsWithin'>binsWithin(QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=within&unscoped_q=within">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

within( Object ds, Object bounds ) &rarr; QDataSet<br>
***
<a name="without"></a>
# without
without( QDataSet ds, QDataSet bounds ) &rarr; QDataSet

return non-zero where the data in ds are outside of the bounds.  In Jython,
<blockquote><pre>
print without( [0,1,2,3,4], '2 to 4' ) --> [ 1,1,0,0,1 ]
print without( ttag, 'orbit:rbspa-pp:172' )
</pre></blockquote>
 Note if bounds contain fill, then everything is fill.

### Parameters:
ds - rank N dataset where N &gt; 0
<br>bounds - a rank 1 bounding box.

### Returns:
rank N dataset containing non-zero where the condition is true.
### See Also:
<a href='Ops_w.md#within'>within(QDataSet, QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=without&unscoped_q=without">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

without( Object ds, Object bounds ) &rarr; QDataSet<br>
