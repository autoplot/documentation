# org.das2.util.NumberFormatUtilprovide convenient and consistent access to DecimalFormat objects.
NumberFormatUtil( )


***
<a name="getDecimalFormat"></a>
# getDecimalFormat
getDecimalFormat(  ) &rarr; DecimalFormat

handles the localization problem (bug 0000294) by always returning a DecimalFormat
 for Locale.US. (Sorry, rest of world.)

### Returns:
DecimalFormat

<a href="https://github.com/autoplot/dev/search?q=getDecimalFormat&unscoped_q=getDecimalFormat">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getDecimalFormat( String spec ) &rarr; DecimalFormat<br>
