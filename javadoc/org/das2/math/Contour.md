# org.das2.math.ContourContouring based on code published in Javatech, Volume 13 Issue 9, "Contour Plotting In Java"
 by David Rand.  This code is based on Fortran code implementing 1978 article by W. V. Snyder.
 W. V. Snyder, "Algorithm 531, Contour plotting [J6]," ACM Trans. Math. Softw. 4, 3 (Sept. 1978), 290-294.
Contour( )


***
<a name="PLANE_X"></a>
# PLANE_X



***
<a name="PLANE_Y"></a>
# PLANE_Y



***
<a name="contour"></a>
# contour
contour( org.das2.dataset.TableDataSet tds, org.das2.datum.DatumVector levels ) &rarr; VectorDataSet

returns a rank 1 dataset, a vector dataset, listing the points
 of the contour paths.  The data set will have three planes:
 X, Y and the default plane is the Z.

### Parameters:
tds - a TableDataSet
<br>levels - a DatumVector

### Returns:
org.das2.dataset.VectorDataSet


<a href="https://github.com/autoplot/dev/search?q=contour&unscoped_q=contour">[search for examples]</a>

contour( org.das2.dataset.TableDataSet tds, Datum level ) &rarr; VectorDataSet<br>
