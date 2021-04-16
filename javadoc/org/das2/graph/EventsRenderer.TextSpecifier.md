# org.das2.graph.EventsRenderer.TextSpecifier
***
<a name="getText"></a>
# getText
getText( DatumRange range, Datum d ) &rarr; String

returns the text for the given datum.  null may be returned, indicating the
 default String.valueOf(d) should be used.

### Parameters:
range - the range of the event
<br>d - the Datum associated with the range

### Returns:
the string for the datum and range shown in a popup.

<a href="https://github.com/autoplot/dev/search?q=getText&unscoped_q=getText">[search for examples]</a>

