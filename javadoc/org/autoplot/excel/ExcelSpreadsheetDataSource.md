# org.autoplot.excel.ExcelSpreadsheetDataSource

Creates QDataSets from an Excel spreadsheet using Apache POI library.<ul>
 <li>http://www.autoplot.org/data/swe-np.xls?column=data&depend0=dep0
 <li>http://sarahandjeremy.net/~jbf/autoplot/data/hudson_data/xls/2008-lion and tiger summary.xls?sheet=Samantha+tiger+lp+lofreq&firstRow=53&column=Complex_Modulus&depend0=Frequency
 <li>http://www.icip.iastate.edu/sites/default/files/uploads/tables/agriculture/ag-land-hist.xls?column=C14:BM14
 <li>file:///home/jbf/ct/hudson/data/xls/c2-70landvalues.xls?sheet=County&column=BM&depend0=A
 </ul>

# ExcelSpreadsheetDataSource( java.net.URI uri )
Creates a new instance of ExcelSpreadsheetDataSource.
 file://c:/myfile.xls?column=N&depend0=G
   parameters:
     column=id  the column ID for the data
     depend0=id the column ID for the x tags
 file://C:/iowaCitySales2004-2006.latlong.xls?column=M[2:]&depend0=B[2:]&plane0=C[2:]

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

