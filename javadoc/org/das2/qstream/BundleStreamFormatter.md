# org.das2.qstream.BundleStreamFormatterLike SimpleStreamFormatter, but this correctly handles bundles.
 This also shows a brute-force method for formatting streams.
BundleStreamFormatter( )


***
<a name="FORMAT_PATTERN"></a>
# FORMAT_PATTERN



***
<a name="HEX_FORMAT_PATTERN"></a>
# HEX_FORMAT_PATTERN



***
<a name="format"></a>
# format
format( QDataSet ds, java.io.OutputStream osout, boolean asciiTypes ) &rarr; void

format the rank 2 bundle.

### Parameters:
ds - rank 2 bundle dataset.
<br>osout - an OutputStream
<br>asciiTypes - true if ascii types should be used.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=format&unscoped_q=format">[search for examples]</a>

***
<a name="guessAsciiTransferType"></a>
# guessAsciiTransferType
guessAsciiTransferType( QDataSet ds ) &rarr; TransferType

guess an ASCII transfer type which can accurately and efficiently 
 represent the data in the dataset.  If the format property
 is found, then a TransferType based on the format is used.

### Parameters:
ds - the dataset

### Returns:
the transfer type.

<a href="https://github.com/autoplot/dev/search?q=guessAsciiTransferType&unscoped_q=guessAsciiTransferType">[search for examples]</a>

