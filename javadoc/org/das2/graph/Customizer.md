# org.das2.graph.Customizer

Interface to allow customizations to plots to be injected at the end of the DasPlot constructor.
 The caller needs to be very cautious using this, especially when calling any non-final methods.

***
<a name="customize"></a>
# customize
customize( org.das2.graph.DasPlot plot ) &rarr; void

Perform any action(s) to change the default behavior of a newly constructed plot.

### Parameters:
plot - the plot being customized

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=customize&unscoped_q=customize">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

