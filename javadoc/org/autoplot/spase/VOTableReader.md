# org.autoplot.spase.VOTableReader

Convert VOTable into QDataSet.  This will return a bundle of parameters.

# VOTableReader( )


***
<a name="getDataSet"></a>
# getDataSet
getDataSet(  ) &rarr; QDataSet

Get the dataset.  If no records were read, then a zero-length dataset is
 returned.

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readHeader"></a>
# readHeader
readHeader( String s, ProgressMonitor monitor ) &rarr; QDataSet

return just the header for the data.  This is just the BUNDLE_1 property of the dataset 
 that would have been read for the readTable command.

### Parameters:
s - String reference to a local file.
<br>monitor - progress monitor for the read.

### Returns:
the header.  For example h.property( QDataSet.LABEL, 1 )

<a href="https://github.com/autoplot/dev/search?q=readHeader&unscoped_q=readHeader">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="readTable"></a>
# readTable
readTable( String s, ProgressMonitor monitor ) &rarr; QDataSet

read the table from the stream s.

### Parameters:
s - String reference to a local file.
<br>monitor - progress monitor will provide line number updates.

### Returns:
the bundle dataset loaded.

<a href="https://github.com/autoplot/dev/search?q=readTable&unscoped_q=readTable">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

readTable( String s ) &rarr; QDataSet<br>
