# org.autoplot.das2Stream.Das2StreamDataSourceFormat

Format the data into das2 streams.

# Das2StreamDataSourceFormat( )


***
<a name="canFormat"></a>
# canFormat
canFormat( QDataSet ds ) &rarr; boolean



### Parameters:
ds - a QDataSet

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=canFormat&unscoped_q=canFormat">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="formatData"></a>
# formatData
formatData( String url, QDataSet data, ProgressMonitor mon ) &rarr; void



### Parameters:
url - a String
<br>data - a QDataSet
<br>mon - a ProgressMonitor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=formatData&unscoped_q=formatData">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBinary"></a>
# getBinary
getBinary( String uri ) &rarr; boolean



### Parameters:
uri - a String

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=getBinary&unscoped_q=getBinary">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDescription"></a>
# getDescription
getDescription(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getDescription&unscoped_q=getDescription">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFracSeconds"></a>
# getFracSeconds
getFracSeconds( String uri ) &rarr; int

Get the fractional seconds value for das2 text streams from an Autoplot URI

### Parameters:
uri - An Autoplot URI string

### Returns:
an integer from 0 to 12

<a href="https://github.com/autoplot/dev/search?q=getFracSeconds&unscoped_q=getFracSeconds">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSigDigits"></a>
# getSigDigits
getSigDigits( String uri ) &rarr; int

Get the number of general significant digits for das2 text streams from an 
 Autoplot URI

### Parameters:
uri - An Autoplot URI string

### Returns:
an integer from 2 to 14

<a href="https://github.com/autoplot/dev/search?q=getSigDigits&unscoped_q=getSigDigits">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getVersion"></a>
# getVersion
getVersion( String uri ) &rarr; String

Get the das2 stream version value from an Autoplot URI

### Parameters:
uri - an Autoplot URI string

### Returns:
a string representing the version value.  Only the strings
         QdsToD2sStream.FORMAT_2_2 or QdsToD2sStream.FORMAT_2_3_BASIC are returned

<a href="https://github.com/autoplot/dev/search?q=getVersion&unscoped_q=getVersion">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setOptions"></a>
# setOptions
setOptions( org.autoplot.datasource.URISplit lSplit, String version, boolean binary, int sigdigit, int fracsec ) &rarr; URISplit

Add Das2 export options into a split autoplot URI

### Parameters:
lSplit - an URISplit
<br>version - A version string, one of QdsToD2sStream.FORMAT_2_2, 
                QdsToD2sStream.FORMAT_2_3_BASIC, etc
<br>binary - True if a binary stream should be generated
<br>sigdigit - The number of significant digits to use for general text data output
<br>fracsec - The number of fractional seconds to use for general text time output

### Returns:
an org.autoplot.datasource.URISplit


<a href="https://github.com/autoplot/dev/search?q=setOptions&unscoped_q=setOptions">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

