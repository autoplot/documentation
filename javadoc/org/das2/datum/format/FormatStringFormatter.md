# org.das2.datum.format.FormatStringFormatter

This is based on the C-style format strings introduced in Java 5 that
 we can now use.  When used with times, the format should be specified
 using URI_Templates like $Y$m$dT$H:$M:$S.  
 TODO: See Autoplot's DataSetUtil.toString, which shows use with Calendar objects.
 
 Here is a table showing some examples:
 <table summary="examples">
 <tr><td>%9.2f</td><td>decimal with two fractional places</td></tr>
 <tr><td>%9.2e</td><td>decimal in scientific notation</td></tr>
 <tr><td>%.2f</td><td>decimal with two fractional places, and some number of total spaces</td></tr>
 <tr><td>%5d</td><td>integer in five spaces.</td></tr>
 <tr><td>$Y$m$dZ</td><td>time specification.</td></tr>
 </table>

# FormatStringFormatter( String formatStr, boolean units )
create a new instance based on the Java format string.

***
<a name="format"></a>
# format
format( Datum datum ) &rarr; String



### Parameters:
datum - a Datum

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=format&unscoped_q=format">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

format( Datum datum, Units units ) &rarr; String<br>
***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

