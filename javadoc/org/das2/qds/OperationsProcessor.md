# org.das2.qds.OperationsProcessor

Extract the sprocess from DataSetOps.

# OperationsProcessor( )


***
<a name="getArgumentIndex"></a>
# getArgumentIndex
getArgumentIndex( String arg, int deft ) &rarr; Object

container for the logic for slicing at an index vs slicing at a datum.  If the string is
 an integer, then we return the index.  If the index is a string, then we need to 
 find the corresponding index to the rank 0 dataset elsewhere.
 If the string argument is not parseable, then deft is returned.

### Parameters:
arg - String that encodes a datum position or index.
<br>deft - default value.

### Returns:
an integer index or a dataset indicating the index.

<a href="https://github.com/autoplot/dev/search?q=getArgumentIndex&unscoped_q=getArgumentIndex">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="sprocess"></a>
# sprocess
sprocess( String c, QDataSet fillDs, ProgressMonitor mon ) &rarr; QDataSet

sprocess implements the poorly-named filters string / process string of Autoplot, allowing
 clients to "pipe" data through a chain of operations.  For example, the filters string 
 "|slice0(9)|histogram()" will slice on the ninth index and then take a histogram of that
 result.  See http://www.papco.org/wiki/index.php/DataReductionSpecs (TODO: wiki page was lost,
 which could probably be recovered.)  There's a big problem here:
 if the command is not recognized, then it is ignored.  We should probably change this,
 but the change should be at a major version change in case it breaks things.

### Parameters:
c - process string like "slice0(9)|histogram()"
<br>fillDs - The dataset loaded from the data source controller, with initial filters (like fill) applied.
<br>mon - monitor for the processing.

### Returns:
the dataset after the process string is applied.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/<a href="http://autoplot/org/developer/dataset/filters">http://autoplot/org/developer/dataset/filters</a>.md'><a href="http://autoplot.org/developer.dataset.filters">http://autoplot.org/developer.dataset.filters</a></a> <br>
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/<a href="http://autoplot/org/developer/panel_rank_reduction">http://autoplot/org/developer/panel_rank_reduction</a>.md'><a href="http://autoplot.org/developer.panel_rank_reduction">http://autoplot.org/developer.panel_rank_reduction</a></a> <br>
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/org/das2/qds/filters/FilterEditorPanel.md'>org.das2.qds.filters.FilterEditorPanel</a> <br>

<a href="https://github.com/autoplot/dev/search?q=sprocess&unscoped_q=sprocess">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

