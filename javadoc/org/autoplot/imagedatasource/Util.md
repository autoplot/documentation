# org.autoplot.imagedatasource.Util



# Util( )


***
<a name="parseGPSString"></a>
# parseGPSString
parseGPSString( String s ) &rarr; double

returns 45.50833333333333 from 45deg30'30", where the text "deg" is
    a placeholder for the unicode degree symbol (its not replicated
    here since non-ASCII characters choke some development tools)

### Parameters:
s - a GPS coordinate with degrees minutes and seconds

### Returns:
decimal version of string

<a href="https://github.com/autoplot/dev/search?q=parseGPSString&unscoped_q=parseGPSString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

