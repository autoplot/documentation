# org.das2.datum.BasisModel a basis vector that defines a dimension.  For example, Units.us2000 has the
 getOffsetUnits() &rarr; Units.microseconds  and getBasis()&rarr; "since 2000-01-01T00:00".
Basis( String id, String description, org.das2.datum.Basis parent, double d, String offsetUnitsString )


***
<a name="physicalZero"></a>
# physicalZero

special basis representing physical zero for all combinations of physical units.

***
<a name="fahrenheit"></a>
# fahrenheit



***
<a name="kelvin"></a>
# kelvin



***
<a name="centigrade"></a>
# centigrade



***
<a name="since2000"></a>
# since2000



***
<a name="since2010"></a>
# since2010



***
<a name="since1980"></a>
# since1980



***
<a name="since1970"></a>
# since1970



***
<a name="since1958"></a>
# since1958



***
<a name="modifiedJulian"></a>
# modifiedJulian



***
<a name="julian"></a>
# julian



***
<a name="since0000"></a>
# since0000



***
<a name="getDescription"></a>
# getDescription
getDescription(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getDescription&unscoped_q=getDescription">[search for examples]</a>

***
<a name="getId"></a>
# getId
getId(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getId&unscoped_q=getId">[search for examples]</a>

***
<a name="getOffset"></a>
# getOffset
getOffset( org.das2.datum.Basis basis, Units u ) &rarr; double

return the location of this basis in given basis, in the given units.

### Parameters:
basis - a Basis
<br>u - an Units

### Returns:
a double


<a href="https://github.com/autoplot/dev/search?q=getOffset&unscoped_q=getOffset">[search for examples]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

***
<a name="registerConverter"></a>
# registerConverter
registerConverter( org.das2.datum.Basis toBasis, double d, Units u ) &rarr; void

specify offset to another basis.  Register to

### Parameters:
toBasis - a Basis
<br>d - a double
<br>u - an Units

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=registerConverter&unscoped_q=registerConverter">[search for examples]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

