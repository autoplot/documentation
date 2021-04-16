# org.das2.qds.math.PoissonDistributionPoissonDistribution generates numbers from the Poisson distribution.
 Adapted from stocc.cpp. 
 2018-08-28.  Made thread safe, use in Jython scripts will be broken.
PoissonDistribution( )


***
<a name="poisson"></a>
# poisson
poisson( double L, java.util.Random random ) &rarr; int

This function generates a random variate with the Poisson distribution.

 Uses inversion by chop-down method for L &lt; 17, and ratio-of-uniforms
 method for L &gt;= 17.

 For L &lt; 1.E-6 numerical inaccuracy is avoided by direct calculation.
 For L &gt; 2E9 too big--throws IllegalArgumentException
 
 Note this was a static method before 2018-08-28 (v2018a_8), so Jython calls
 should be PoissonDistribution().poisson().

### Parameters:
L - the real value
<br>random - a random number source

### Returns:
the integer value.

<a href="https://github.com/autoplot/dev/search?q=poisson&unscoped_q=poisson">[search for examples]</a>

