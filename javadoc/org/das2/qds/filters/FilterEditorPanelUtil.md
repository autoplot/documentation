# org.das2.qds.filters.FilterEditorPanelUtil

Utility classes

# FilterEditorPanelUtil( )


***
<a name="decimalRegex"></a>
# decimalRegex
decimalRegex(  ) &rarr; String

return regular expression for decimal regex, without leading 
 or trailing whitespace.
 From http://www.regular-expressions.info/floatingpoint.html
 modified to allow "1.e4"

### Returns:
regular expression for a decimal, without whitespace.  Note it contains (groups)!

<a href="https://github.com/autoplot/dev/search?q=decimalRegex&unscoped_q=decimalRegex">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="decimalRegexSloppy"></a>
# decimalRegexSloppy
decimalRegexSloppy(  ) &rarr; String

sloppy regex to be used when the number doesn't need to be parsed.

### Returns:
regular expression that would match a decimal, without whitespace.

<a href="https://github.com/autoplot/dev/search?q=decimalRegexSloppy&unscoped_q=decimalRegexSloppy">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

