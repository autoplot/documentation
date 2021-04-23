# org.autoplot.test.Test_031_MultiPanelPlotThis more advanced example shows how to create a 2x3 stack of 6 plots to look at the components of a fits file.

   1) Add 2x3 empty plots using layout tab, plots context menu, Canvas->AddPlots
   2) Edit DOM, plotElements[*].dataSourceFilterId='data_1' so they all plot the same data
   3) Edit DOM, plotElements[*].component slice0(i) to plot each element
   4) layout tab, plots context menu, Canvas->Add Hidden Plot to bind all the plot X and Y axes together
   5) demo XY binding, all Z axes should be automatically zoomed to just their slice.
Test_031_MultiPanelPlot( )


***
<a name="main"></a>
# main
main( java.lang.String[] argv ) &rarr; void



### Parameters:
argv - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="runIt"></a>
# runIt
runIt( Object o ) &rarr; int



### Parameters:
o - an Object

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=runIt&unscoped_q=runIt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

