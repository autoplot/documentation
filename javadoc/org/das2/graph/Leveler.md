# org.das2.graph.Leveler

Manages a set of rows or columns, making sure they fill a space without
 overlapping.  This is an ancient class that would manage a set of rows to support a 
 PaPCo- or Autoplot-like application.

# Leveler( org.das2.graph.DasCanvas parent )


# Leveler( org.das2.graph.DasCanvas parent, org.das2.graph.DasRow row )


***
<a name="addRow"></a>
# addRow
addRow( double nposition, double weight ) &rarr; DasRow



### Parameters:
nposition - a double
<br>weight - a double

### Returns:
org.das2.graph.DasRow


<a href="https://github.com/autoplot/dev/search?q=addRow&unscoped_q=addRow">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addRow( double nposition ) &rarr; DasRow<br>
addRow(  ) &rarr; DasRow<br>
***
<a name="deleteRow"></a>
# deleteRow
deleteRow( org.das2.graph.DasRow row ) &rarr; void



### Parameters:
row - a DasRow

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=deleteRow&unscoped_q=deleteRow">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPosition"></a>
# getPosition
getPosition( org.das2.graph.DasRow row ) &rarr; double



### Parameters:
row - a DasRow

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=getPosition&unscoped_q=getPosition">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRows"></a>
# getRows
getRows(  ) &rarr; List

returns a copy of the List of the Row objects.

### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=getRows&unscoped_q=getRows">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getWeight"></a>
# getWeight
getWeight( org.das2.graph.DasRow row ) &rarr; double



### Parameters:
row - a DasRow

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=getWeight&unscoped_q=getWeight">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rowCount"></a>
# rowCount
rowCount(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=rowCount&unscoped_q=rowCount">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setBottomMargin"></a>
# setBottomMargin
setBottomMargin( double nmargin ) &rarr; void



### Parameters:
nmargin - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setBottomMargin&unscoped_q=setBottomMargin">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setInsideMargin"></a>
# setInsideMargin
setInsideMargin( double n ) &rarr; void



### Parameters:
n - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setInsideMargin&unscoped_q=setInsideMargin">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTopMargin"></a>
# setTopMargin
setTopMargin( double nmargin ) &rarr; void



### Parameters:
nmargin - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTopMargin&unscoped_q=setTopMargin">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="whichRow"></a>
# whichRow
whichRow( int y ) &rarr; DasRow



### Parameters:
y - an int

### Returns:
org.das2.graph.DasRow


<a href="https://github.com/autoplot/dev/search?q=whichRow&unscoped_q=whichRow">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

