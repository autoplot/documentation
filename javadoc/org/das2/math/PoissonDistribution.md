# org.das2.math.PoissonDistributionClass for generating numbers from a Poisson distribution.
PoissonDistribution( )


***
<a name="poisson"></a>
# poisson
poisson( double L, java.util.Random random ) &rarr; int

This function generates a random variate with the poisson distribution.

 Uses inversion by chop-down method for L &lt; 17, and ratio-of-uniforms
 method for L &ge; 17.

 For L &lt; 1.E-6 numerical inaccuracy is avoided by direct calculation.
 For L &gt; 2E9 too big--throws IllegalArgumentException

### Parameters:
L - a double
<br>random - a Random

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=poisson&unscoped_q=poisson">[search for examples]</a>

