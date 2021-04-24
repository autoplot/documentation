# org.das2.qds.util.Griddata

Codes for interpolating from irregular grids to regular grids.
 
 For these codes we use "trigulations" which are datasets that contain connections
 of points in other datasets.  These are rank 2 datasets tri[n,3] where the 3 points are
 indeces of other datasets.
 
 Triangulations are generalized, where the typical case is a set of 3-node triangles.  However,
 2-point "triangles" can be used for linear interpolation, 4-point squares can be used for bilinear 
 interpolation, and 4-points for 3-D triangle interpolation. 
 
 DO NOT USE THIS CLASS, IT IS STILL UNDER DEVELOPMENT!  This is barely tested for the nfree=1-D case!

# Griddata( )


***
<a name="griddata"></a>
# griddata
griddata( QDataSet triangles, QDataSet itriangle, QDataSet weights, QDataSet zbuck ) &rarr; QDataSet

Perform the interpolation for arbitrary sets of nvert points.

### Parameters:
triangles - triangles mesh, presently tri[n,3] but may soon be tri[n,4] as well.
<br>itriangle - rank n mesh identifying the triangle to use
<br>weights - rank n+1 mesh (e.g. weights[m,3]) with a weight for each triangle node.
<br>zbuck - dependent Z values for each point.

### Returns:
dataset with the same geometry as itriangle.

<a href="https://github.com/autoplot/dev/search?q=griddata&unscoped_q=griddata">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

griddata( QDataSet xx, QDataSet yy, QDataSet buck ) &rarr; QDataSet<br>
***
<a name="triLocate"></a>
# triLocate
triLocate( QDataSet buck, QDataSet tri, QDataSet grid ) &rarr; QDataSet

for each element of grid, identify the matching triangle.

### Parameters:
buck - the data (e.g. buck[o,nfree])
<br>tri - the triangulation (e.g. tri[n,free+1])
<br>grid - the values to locate (e.g. grid[m,nfree])

### Returns:
the locations itri[o]

<a href="https://github.com/autoplot/dev/search?q=triLocate&unscoped_q=triLocate">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="triangulate"></a>
# triangulate
triangulate( QDataSet buck ) &rarr; QDataSet

return a rank 2 dataset [n,nvert] with the "triangles" connecting the buckshot data.

### Parameters:
buck - dataset[m,nvert-1].

### Returns:
tri[n,3]

<a href="https://github.com/autoplot/dev/search?q=triangulate&unscoped_q=triangulate">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="weights"></a>
# weights
weights( QDataSet buck, QDataSet tri, QDataSet grid, QDataSet itri ) &rarr; QDataSet

return the weights for each point of the grid.  Let nfree be the number of independent data dimensions.

### Parameters:
buck - the data (e.g. buck[o,nfree])
<br>tri - the triangulation (e.g. tri[n,nfree+1])
<br>grid - rank 2 dataset (e.g. grid[m,nfree])
<br>itri - the triangle to use for each point of grid. (e.g. itri[m])

### Returns:
rank 2 (e.g. weights[m,2])

<a href="https://github.com/autoplot/dev/search?q=weights&unscoped_q=weights">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

