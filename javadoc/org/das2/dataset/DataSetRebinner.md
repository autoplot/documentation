# org.das2.dataset.DataSetRebinner



***
<a name="rebin"></a>
# rebin
rebin( QDataSet ds, org.das2.dataset.RebinDescriptor x, org.das2.dataset.RebinDescriptor y, org.das2.dataset.RebinDescriptor z ) &rarr; QDataSet

create a new QDataSet in a rank 2 table with x and y tags described by x and y.

### Parameters:
ds - The input dataset, either a rank 2 or rank 3 dataset.  Note this may include rank 1 dataset and rank 2 bundles at some point.
<br>x - describes the column labels.  (Note this may become a QDataSet at some point).
<br>y - describes the row labels.
<br>z - describes the Z space for the rebinning, in particular log.

### Returns:
a rank 2 QDataSet with the given rows and columns.

<a href="https://github.com/autoplot/dev/search?q=rebin&unscoped_q=rebin">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

