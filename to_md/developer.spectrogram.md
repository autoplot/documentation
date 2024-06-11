# Purpose

Reiner and I were talking about the spectrogram algorithm and its
shortcomings, and this page is the beginning of identifying and
addressing these issues. Also Jon and Larry at APL have a long-standing
request to have more control of the algorithm.

# The current algorithm

The current algorithm was developed for viewing data produced by
instruments from the Radio and Plasma Wave Group at Iowa. This data
looks best when interpolating between measurements in both time and
frequency. Typically there are no data dropouts, and the data is fairly
smooth, so picking nearest neighbors would introduce cusps in the data.
It's useful to think about the frequency content of the image, like a
2-D FFT. Nearest neighbor sampling introduces high-frequency cusps in
the visualization of the data. Also they tend to have as many channels
in Y as there are pixels, so NN sampling would introduce strange Nyquist
features.

1.  Identify pixels location for all data points.
2.  Average all the data at the same pixel location. This is done in the
    linear space.
3.  (If you set the rebin mode to "noInterpolateNoEnlarge" it will stop
    here)
4.  For each pixel row:
    1.  identify the adjacent values bracketing the pixel.
    2.  "Interpolate" the value if possible. This is either picking a
        close neighbor, or interpolating between two values depending on
        rebin setting
5.  We now have a pixel grid with horizontal lines.
6.  For each pixel column:
    1.  identify the adjacent values, which may have been interpolated,
        bracketing the pixel.
    2.  "Interpolate" the value if possible. This is either picking a
        close neighbor, or interpolating between two values depending on
        rebin

# Shortcomings of the algorithm

1.  limited control: interpolate or NN. Requests for NN in X,
    interpolate in Y.
2.  Interpolation is done in the data space, should be done in pixel
    color space
3.  Algorithm still introduces Nyquist effects, because of pixel shift
    into bins.
4.  Data gaps are sometimes incorrectly drawn because shifting pixels
    means we must adjust interpolation limits.
5.  Nearest Neighbor interpolation is sub-optimal implementation
    (Reiner's original complaint.) (This is a bug that can be
    addressed).
6.  Nearest Neighbor interpolation may fail because we loose the
    identity of the dataset table when we put it into bins.
7.  Nearest Neighbor interpolation may fail to show single-point drop
    out.

# Communication of Average Type

Another problem the Das2server has, as well as the spectrogram renderer,
is that averages are always done as linear averages. Larry and I were
just chatting about this and enumerated a bunch of average types. Note
the CDAWeb has a similar property, and I believe this would satisfy a
number of needs.

**linear** return the linear average of two points, using weights.

**geometric** return the geometric average of two points, using weights.

**nearestNeighbor** return the point with the bigger weight.

**max** return the larger point.

**mod360** return the linear average, where 259 and 1 are 2 units apart.

**mod24** return the linear average, where 23 and 1 are 2 units apart.

**modPI** return the linear average, where PI and 2\*PI are the same

**modTAU** return the linear average, where PI and 3\*PI are the same

**mod\_m90\_p90** where 89 and 91 are the same, as are -89 and -91.

**mode** return the point with the biggest weight.

**median** return the median-filter point. This is more complex than
others, requiring a number of points.

Larry suggests that we might be able to express each algorithmically. So
for example instead of "linear" we would say "(MA\*WA+MB\*WB)/(WA+WB)"
or instead of "nearestNeighbor" we would say "WA\>WB?MA:MB". (Larry will
correct these provide expressions for others.)

See <https://spdf.gsfc.nasa.gov/istp_guide/vattributes.html#AVG_TYPE>

# See Also

1.  <http://das2.org/wiki/index.php/SpectrogramRenderer>
2.  <https://sourceforge.net/tracker/index.php?func=detail&aid=3237397&group_id=199733&atid=970682>
    "gaps in das2 spectrograms back"
3.  <https://sourceforge.net/tracker/index.php?func=detail&aid=3117538&group_id=199733&atid=970682>
    "Cluster/PEACE interpolation issue with das2 nn spectrograms"
4.  <http://autoplot.org/developer.spectrogram.rebin>
