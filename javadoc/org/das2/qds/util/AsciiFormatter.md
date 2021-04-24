# org.das2.qds.util.AsciiFormatter

It would be useful to have a method for exporting data when working with
 QDataSet, so this is introduced.  This is very limited in its functionality,
 and should be extended as needed.

# AsciiFormatter( )


***
<a name="formatToFile"></a>
# formatToFile
formatToFile( java.io.File f, org.das2.qds.QDataSet[] dss ) &rarr; void

format to the given file

### Parameters:
f - the file
<br>dss - the datasets

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=formatToFile&unscoped_q=formatToFile">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

formatToFile( String f, org.das2.qds.QDataSet[] dss ) &rarr; void<br>
formatToFile( java.io.File f, QDataSet ds ) &rarr; void<br>
formatToFile( String f, QDataSet ds ) &rarr; void<br>
formatToFile( String f, double[][] dd ) &rarr; void<br>
