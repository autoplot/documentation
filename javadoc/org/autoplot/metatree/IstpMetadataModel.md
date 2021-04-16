# org.autoplot.metatree.IstpMetadataModelMetadata model for ISTP conventions.  For example, FIELDNAM is mapped to QDataSet.NAME, SCALEMIN is 
 mapped to TYPICAL_MIN, etc.  When LaTeX fragments are found in axis titles 
 {@code (s.contains("^{") || s.contains("_{"))}, then this is converted 
 into Granny control strings.
IstpMetadataModel( )


***
<a name="USER_PROP_VIRTUAL_FUNCTION"></a>
# USER_PROP_VIRTUAL_FUNCTION

Non-null, non-empty String if it is virtual.  The string will be like "compute_magnitude(B_xyz_gse)"

***
<a name="USER_PROP_VIRTUAL_COMPONENT_"></a>
# USER_PROP_VIRTUAL_COMPONENT_



***
<a name="VALUE_MIN"></a>
# VALUE_MIN



***
<a name="VALUE_MAX"></a>
# VALUE_MAX



***
<a name="doubleValue"></a>
# doubleValue
doubleValue( Object o, Units units, double deflt, Object minmax ) &rarr; double

returns the Entry that is convertible to double as a double.
 When there is an array, throw IllegalArgumentException.
 Note this is used in CdfDataSource and other projects.

### Parameters:
o - the datum in double, int, String, array, etc.
<br>units - the units of the datum, result is returned in these units.
<br>deflt - the default value
<br>minmax - VALUE_MIN or VALUE_MAX or null.

### Returns:
the double or

<a href="https://github.com/autoplot/dev/search?q=doubleValue&unscoped_q=doubleValue">[search for examples]</a>

***
<a name="getLabel"></a>
# getLabel
getLabel(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getLabel&unscoped_q=getLabel">[search for examples]</a>

***
<a name="getValidRange"></a>
# getValidRange
getValidRange( java.util.Map attrs, Units units ) &rarr; DatumRange

Return the range from VALIDMIN to VALIDMAX.  If the unit is an ordinal unit (see LABL_PTR_1), then return null.
 Note QDataSet only allows times from 1000AD to 9000AD when Units are TimeLocationUnits.
 Note this is used in CdfDataSource and other projects.

### Parameters:
attrs - the ISTP attributes
<br>units - the units for this variable, used to interpret doubles.

### Returns:
the range.

<a href="https://github.com/autoplot/dev/search?q=getValidRange&unscoped_q=getValidRange">[search for examples]</a>

***
<a name="maybeReduceRank2"></a>
# maybeReduceRank2
maybeReduceRank2( org.das2.qds.MutablePropertyDataSet depDs ) &rarr; MutablePropertyDataSet

RBSP/ECT/MAGEIS has files where typically the energy labels are
 constant, but they must be rank 2 because they can vary.  Seth 
 wishes the Energy labels be shown when they are constant, and this 
 is a quick check to detect the case.  The data can also contain
 fill records and channels that contain all fill.

### Parameters:
depDs - a MutablePropertyDataSet

### Returns:
the rank 1 dataset or null.

<a href="https://github.com/autoplot/dev/search?q=maybeReduceRank2&unscoped_q=maybeReduceRank2">[search for examples]</a>

***
<a name="properties"></a>
# properties
properties( java.util.Map meta ) &rarr; Map

Interpret the ISTP metadata into QDataSet properties.

### Parameters:
meta - a java.util.Map

### Returns:
a java.util.Map


<a href="https://github.com/autoplot/dev/search?q=properties&unscoped_q=properties">[search for examples]</a>

