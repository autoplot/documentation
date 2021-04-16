# org.das2.qds.demos.PlasmaModelModel of plasma distribution function for given density, temperature, speed.
 A java.util.Random object is passed in so that the data may be reproducible
 (by using a given starting seed).
PlasmaModel( )


***
<a name="counts"></a>
# counts
counts( Datum energy, java.util.Random random ) &rarr; int

return the counts at this energy, assuming an isotropic distribution, and
 Poisson noise is added to the result.

### Parameters:
energy - in eV
<br>random - source of random numbers.

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=counts&unscoped_q=counts">[search for examples]</a>

counts( Datum energy, Datum pitch, java.util.Random random ) &rarr; int<br>
***
<a name="f"></a>
# f
f( Datum energy ) &rarr; double

return f at the given energy

### Parameters:
energy - a Datum

### Returns:
a double


<a href="https://github.com/autoplot/dev/search?q=f&unscoped_q=f">[search for examples]</a>

f( Datum energy, Datum pitchAngle ) &rarr; double<br>
***
<a name="fcounts"></a>
# fcounts
fcounts( Datum energy ) &rarr; double

return the counts at this energy, assuming an isotropic distribution.  No
 Poisson noise is added to the output.

### Parameters:
energy - a Datum

### Returns:
a double


<a href="https://github.com/autoplot/dev/search?q=fcounts&unscoped_q=fcounts">[search for examples]</a>

fcounts( Datum energy, Datum pitch ) &rarr; double<br>
***
<a name="getDensity"></a>
# getDensity
getDensity(  ) &rarr; Datum

get the model density

### Returns:
a Datum


<a href="https://github.com/autoplot/dev/search?q=getDensity&unscoped_q=getDensity">[search for examples]</a>

***
<a name="getGeomFactor"></a>
# getGeomFactor
getGeomFactor(  ) &rarr; Datum

get the detector geometry factor

### Returns:
the detector geometry factor

<a href="https://github.com/autoplot/dev/search?q=getGeomFactor&unscoped_q=getGeomFactor">[search for examples]</a>

***
<a name="getRank2"></a>
# getRank2
getRank2(  ) &rarr; QDataSet

return a rank 2 dataset with time as DEPEND_0 and energy as DEPEND_1.

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=getRank2&unscoped_q=getRank2">[search for examples]</a>

***
<a name="getRank3"></a>
# getRank3
getRank3(  ) &rarr; QDataSet

return a rank 2 dataset with time as DEPEND_0 and energy as DEPEND_1.

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=getRank3&unscoped_q=getRank3">[search for examples]</a>

***
<a name="getWcParl"></a>
# getWcParl
getWcParl(  ) &rarr; Datum

get the parallel speed.

### Returns:
a Datum


<a href="https://github.com/autoplot/dev/search?q=getWcParl&unscoped_q=getWcParl">[search for examples]</a>

***
<a name="getWcPerp"></a>
# getWcPerp
getWcPerp(  ) &rarr; Datum

get the perpendicular speed

### Returns:
the perpendicular speed

<a href="https://github.com/autoplot/dev/search?q=getWcPerp&unscoped_q=getWcPerp">[search for examples]</a>

***
<a name="setDensity"></a>
# setDensity
setDensity( Datum density ) &rarr; void

set the model density

### Parameters:
density - a Datum

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDensity&unscoped_q=setDensity">[search for examples]</a>

***
<a name="setGeomFactor"></a>
# setGeomFactor
setGeomFactor( Datum geom ) &rarr; void

set the detector geometry factor

### Parameters:
geom - the detector geometry factor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setGeomFactor&unscoped_q=setGeomFactor">[search for examples]</a>

***
<a name="setWcPerp"></a>
# setWcPerp
setWcPerp( Datum wcperp ) &rarr; void

set the perpendicular speed

### Parameters:
wcperp - perpendicular speed

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setWcPerp&unscoped_q=setWcPerp">[search for examples]</a>

***
<a name="setWcparl"></a>
# setWcparl
setWcparl( Datum wcparl ) &rarr; void

set the parallel speed

### Parameters:
wcparl - a Datum

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setWcparl&unscoped_q=setWcparl">[search for examples]</a>

