# org.das2.qds.math.Contour

Contouring based on code published in Javatech, Volume 13 Issue 9, "Contour Plotting In Java"
 by David Rand.  This code is based on Fortran code implementing 1978 article by W. V. Snyder.
 W. V. Snyder, "Algorithm 531, Contour plotting [J6]," ACM Trans. Math. Softw. 4, 3 (Sept. 1978), 290-294.

# Contour( )


***
<a name="contour"></a>
# contour
contour( QDataSet tds, QDataSet levels ) &rarr; QDataSet

returns a rank 2 dataset, a bundle dataset, listing the points
 of the contour paths.  The dataset will be ds[n,3] where
 the bundled datasets are: [x,y,z] and where DEPEND_0 indicates the step number.
 Jumps in the step number indicate a break in the contour.

### Parameters:
tds - the rank 2 table dataset
<br>levels - the rank 1 levels

### Returns:
rank 2 bundle of x,y,z where DEPEND_0 indicates the step number.

<a href="https://github.com/autoplot/dev/search?q=contour&unscoped_q=contour">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

contour( QDataSet tds, Datum level ) &rarr; QDataSet<br>
