# org.autoplot.excel.ExcelUtilUtilties.
ExcelUtil( )


***
<a name="getColumnNumber"></a>
# getColumnNumber
getColumnNumber( HSSFSheet sheet, String id, int firstRow ) &rarr; short



### Parameters:
sheet - a HSSFSheet
<br>id - a String
<br>firstRow - an int

### Returns:
short


<a href="https://github.com/autoplot/dev/search?q=getColumnNumber&unscoped_q=getColumnNumber">[search for examples]</a>

***
<a name="getColumns"></a>
# getColumns
getColumns( HSSFWorkbook wb, String ssheet, String firstRowString, ProgressMonitor mon ) &rarr; Map

inspect the first row for columns.  Strings may be picked up as labels if the
 next row contains values.

### Parameters:
wb - a HSSFWorkbook
<br>ssheet - the sheet name
<br>firstRowString - the firstRow or null.
<br>mon - a ProgressMonitor

### Returns:
a java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getColumns&unscoped_q=getColumns">[search for examples]</a>

***
<a name="getSheets"></a>
# getSheets
getSheets( HSSFWorkbook wb, org.autoplot.datasource.CompletionContext cc, ProgressMonitor mon ) &rarr; List



### Parameters:
wb - a HSSFWorkbook
<br>cc - a CompletionContext
<br>mon - a ProgressMonitor

### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=getSheets&unscoped_q=getSheets">[search for examples]</a>

