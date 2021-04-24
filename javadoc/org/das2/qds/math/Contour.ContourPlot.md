# org.das2.qds.math.Contour.ContourPlot



# ContourPlot( QDataSet tds, QDataSet contourValues )


***
<a name="PERFORM_CONTOUR_RETURN_FORM4"></a>
# PERFORM_CONTOUR_RETURN_FORM4

return bundle of X,Y,Z[STEP] where STEP contains gaps indicating breaks.

***
<a name="PERFORM_CONTOUR_RETURN_FORM3"></a>
# PERFORM_CONTOUR_RETURN_FORM3

return bundle of X,Y,Z with DEPEND_0 equal to the step number, with a gap indicating a break.

***
<a name="performContour"></a>
# performContour
performContour(  ) &rarr; QDataSet

perform the contour using PERFORM_CONTOUR_RETURN_FORM3

### Returns:
rank 2 bundle of [n,3] with DEPEND_0 as the contour number
### See Also:
<a href='#performContour'>performContour(java.lang.Object)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=performContour&unscoped_q=performContour">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

performContour( Object form ) &rarr; QDataSet<br>
