# org.autoplot.html.HtmlTableDataSourceData source for extracting data from HTML tables.  This has been used
 for looking at real estate sales and weather history.
HtmlTableDataSource( java.net.URI uri )


***
<a name="PARAM_COLUMN"></a>
# PARAM_COLUMN

the parameter name (not label) to plot

***
<a name="PARAM_TABLE"></a>
# PARAM_TABLE



***
<a name="PARAM_UNITS"></a>
# PARAM_UNITS



***
<a name="getDataSet"></a>
# getDataSet
getDataSet( ProgressMonitor mon ) &rarr; QDataSet



### Parameters:
mon - a ProgressMonitor

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTable"></a>
# getTable
getTable( ProgressMonitor mon ) &rarr; QDataSet

read the table from the file.

### Parameters:
mon - a ProgressMonitor

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=getTable&unscoped_q=getTable">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTables"></a>
# getTables
getTables(  ) &rarr; List

return a list of the tables, with column and human readable description after.

### Returns:
a list of the tables, with column and human readable description after.

<a href="https://github.com/autoplot/dev/search?q=getTables&unscoped_q=getTables">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

