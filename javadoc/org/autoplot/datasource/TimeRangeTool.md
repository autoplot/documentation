# org.autoplot.datasource.TimeRangeTool

GUI for creating valid time ranges by calendar times, orbit, or NRT

# TimeRangeTool( )
Creates new form TimeRangeTool

***
<a name="getSelectedRange"></a>
# getSelectedRange
getSelectedRange(  ) &rarr; String

return the range selected, the type of which will depend on which tab is visible.

### Returns:
the range selected

<a href="https://github.com/autoplot/dev/search?q=getSelectedRange&unscoped_q=getSelectedRange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAdditionalSpacecraftForOrbit"></a>
# setAdditionalSpacecraftForOrbit
setAdditionalSpacecraftForOrbit( java.lang.String[] scs ) &rarr; void

Add additional spacecraft and orbit files to the 
 this must be called before the GUI is created.
 
 These will be the names of local orbit/event files or missions not
 hard-coded into Autoplot.

### Parameters:
scs - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAdditionalSpacecraftForOrbit&unscoped_q=setAdditionalSpacecraftForOrbit">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSelectedRange"></a>
# setSelectedRange
setSelectedRange( String s ) &rarr; void

set the selected range.  When the range is an orbit range (for example orbit:rbspa-pp:300),
 the orbit list will be set.

### Parameters:
s - a timerange parseable with <code>DatumRangeUtil.parseTimeRange(s);</code>

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSelectedRange&unscoped_q=setSelectedRange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

