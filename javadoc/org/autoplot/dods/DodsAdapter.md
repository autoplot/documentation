# org.autoplot.dods.DodsAdapter
DodsAdapter( java.net.URL source, String variable )
Creates a new instance of DodsAdapter

***
<a name="getAddOffset"></a>
# getAddOffset
getAddOffset(  ) &rarr; double

Getter for property addOffset.

### Returns:
Value of property addOffset.

<a href="https://github.com/autoplot/dev/search?q=getAddOffset&unscoped_q=getAddOffset">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getConstraint"></a>
# getConstraint
getConstraint(  ) &rarr; String

get the constraint, such as "?sst[0:100:1811][0:10:35][0:10:71]"

### Returns:
the constraint

<a href="https://github.com/autoplot/dev/search?q=getConstraint&unscoped_q=getConstraint">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSet"></a>
# getDataSet
getDataSet( java.util.Map attributes ) &rarr; QDataSet

This is the code that converts the OpenDAP structures and data types into QDataSet

### Parameters:
attributes - a java.util.Map

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDepend0Name"></a>
# getDepend0Name
getDepend0Name(  ) &rarr; String

Getter for property depend0Name.

### Returns:
Value of property depend0Name.

<a href="https://github.com/autoplot/dev/search?q=getDepend0Name&unscoped_q=getDepend0Name">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDepend1Name"></a>
# getDepend1Name
getDepend1Name(  ) &rarr; String

Getter for property depend1Name.

### Returns:
Value of property depend1Name.

<a href="https://github.com/autoplot/dev/search?q=getDepend1Name&unscoped_q=getDepend1Name">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDependName"></a>
# getDependName
getDependName( int index ) &rarr; String

Indexed getter for property dependName.

### Parameters:
index - Index of the property.

### Returns:
Value of the property at <CODE>index</CODE>.

<a href="https://github.com/autoplot/dev/search?q=getDependName&unscoped_q=getDependName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDimProperties"></a>
# getDimProperties
getDimProperties( int i ) &rarr; HashMap



### Parameters:
i - an int

### Returns:
java.util.HashMap


<a href="https://github.com/autoplot/dev/search?q=getDimProperties&unscoped_q=getDimProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDimUnits"></a>
# getDimUnits
getDimUnits( int index ) &rarr; Units

Indexed getter for property dimUnits, which specifies the units of a dimension tag.

### Parameters:
index - Index of the property.

### Returns:
Value of the property at <CODE>index</CODE>.

<a href="https://github.com/autoplot/dev/search?q=getDimUnits&unscoped_q=getDimUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getScaleFactor"></a>
# getScaleFactor
getScaleFactor(  ) &rarr; double

Getter for property scaleFactor.

### Returns:
Value of property scaleFactor.

<a href="https://github.com/autoplot/dev/search?q=getScaleFactor&unscoped_q=getScaleFactor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSource"></a>
# getSource
getSource(  ) &rarr; URL



### Returns:
java.net.URL


<a href="https://github.com/autoplot/dev/search?q=getSource&unscoped_q=getSource">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getUnits"></a>
# getUnits
getUnits(  ) &rarr; Units

Getter for property units.

### Returns:
Value of property units.

<a href="https://github.com/autoplot/dev/search?q=getUnits&unscoped_q=getUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getVariable"></a>
# getVariable
getVariable(  ) &rarr; String

get the variable, such as "sst"

### Returns:
the variable

<a href="https://github.com/autoplot/dev/search?q=getVariable&unscoped_q=getVariable">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="loadDataset"></a>
# loadDataset
loadDataset( ProgressMonitor mon, java.util.Map attr ) &rarr; void

Load the dataset.

### Parameters:
mon - progress monitor
<br>attr - look for hints in attr about the length of the load.  Virbo/TSDS put a recCount for sequences.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=loadDataset&unscoped_q=loadDataset">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putAllProperties"></a>
# putAllProperties
putAllProperties( java.util.Map p ) &rarr; void



### Parameters:
p - a java.util.Map

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putAllProperties&unscoped_q=putAllProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAddOffset"></a>
# setAddOffset
setAddOffset( double addOffset ) &rarr; void

Setter for property addOffset.

### Parameters:
addOffset - New value of property addOffset.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAddOffset&unscoped_q=setAddOffset">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setConstraint"></a>
# setConstraint
setConstraint( String c ) &rarr; void



### Parameters:
c - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setConstraint&unscoped_q=setConstraint">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDepend0Name"></a>
# setDepend0Name
setDepend0Name( String depend0Name ) &rarr; void

Setter for property depend0Name.

### Parameters:
depend0Name - New value of property depend0Name.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDepend0Name&unscoped_q=setDepend0Name">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDepend1Name"></a>
# setDepend1Name
setDepend1Name( String depend1Name ) &rarr; void

Setter for property depend1Name.

### Parameters:
depend1Name - New value of property depend1Name.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDepend1Name&unscoped_q=setDepend1Name">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDependName"></a>
# setDependName
setDependName( int index, String dependName ) &rarr; void

Indexed setter for property dependName.

### Parameters:
index - Index of the property.
<br>dependName - New value of the property at <CODE>index</CODE>.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDependName&unscoped_q=setDependName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDimProperties"></a>
# setDimProperties
setDimProperties( int dim, java.util.Map p ) &rarr; void



### Parameters:
dim - an int
<br>p - a java.util.Map

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDimProperties&unscoped_q=setDimProperties">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDimUnits"></a>
# setDimUnits
setDimUnits( int index, Units dimUnits ) &rarr; void

Specifies the units of a dimension tag.

### Parameters:
index - Index of the property.
<br>dimUnits - New value of the property at <CODE>index</CODE>.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDimUnits&unscoped_q=setDimUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setScaleFactor"></a>
# setScaleFactor
setScaleFactor( double scaleFactor ) &rarr; void

Setter for property scaleFactor.

### Parameters:
scaleFactor - New value of property scaleFactor.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setScaleFactor&unscoped_q=setScaleFactor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setUnits"></a>
# setUnits
setUnits( Units units ) &rarr; void

Setter for property units.

### Parameters:
units - New value of property units.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUnits&unscoped_q=setUnits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setValidRange"></a>
# setValidRange
setValidRange( double min, double max ) &rarr; void



### Parameters:
min - a double
<br>max - a double

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setValidRange&unscoped_q=setValidRange">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

