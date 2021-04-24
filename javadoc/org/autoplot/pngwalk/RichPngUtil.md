# org.autoplot.pngwalk.RichPngUtil

At the 2012 MMS meeting at UNH, a group of us proposed that we
 embed a little metadata within PNG images which provides lookup 
 information in JSON format.  

 Here is an example:
<blockquote><pre>
 { "size":[722,639],
 "numberOfPlots":1,
 "plots": [
    {
      "title":"AC/MFI  [PRELIMINARY VALUES - BROWSE USE ONLY] B-field magnitude", 
      "xaxis": { "label":"", "min":"2014-01-02T00:00:00.000Z", "max":"2014-01-03T00:00:00.000Z", "left":78, "right":644, "type":"lin", "units":"UTC" },
      "yaxis": { "label":"[PRELIM] <|B|> (nT)", "min":4.440892098500626E-16, "max":8.9, "top":52, "bottom":587, "type":"lin", "units":"nT" }
    }
 ] }
</pre></blockquote>

 See http://autoplot.org/richPng

# RichPngUtil( )


***
<a name="getRange"></a>
# getRange
getRange( JSONObject axis ) &rarr; DatumRange

return the range setting of the axis.  This looks at the "min" and
 "max" keys of the axis node.

### Parameters:
axis - a JSONObject

### Returns:
the axis range

<a href="https://github.com/autoplot/dev/search?q=getRange&unscoped_q=getRange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getXRange"></a>
# getXRange
getXRange( String json ) &rarr; DatumRange

attempt to get the time range of the plots, looking at each x axis
 for a timerange.

### Parameters:
json - rich png ascii string

### Returns:
null or the range found.

<a href="https://github.com/autoplot/dev/search?q=getXRange&unscoped_q=getXRange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

