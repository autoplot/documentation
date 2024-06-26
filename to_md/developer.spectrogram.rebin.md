Purpose: Work up a plan for introducing new rebin types and making a
transition

Audience: developers and interested scientists

# The problem

Das2's spectrogram rebinning methods were developed for RPWS data
produced by the group, and they do not serve the Autoplot community
perfectly well. Nearest Neighbor rebinning was introduced at some point
to try and improve the situation, but it has not been optimal. Also,
many of the names are confusing. For example, "binAverage" is poor
because it's the interpolation that make this routine uniq, and actually
different styles of interpolation satisfy most of the needs of
scientists.

What also makes this difficult is the names for the algorithms are used
in the vap files.

# glossary

  - rebinning--the task of going from the data space to the pixel space.

# new names for interpolation

  - binAverage -\> bilinearInterp or interpXinterpY
  - nearestNeighbor -\> binXbinY
  - noInterpolate
  - noInterpolateNoEnlarge

# new names for color bars

  - color\_wedge -\> rainbow
  - wrapped\_color\_wedge -\> wrappedRainbow

# See also

  - <http://autoplot.org//developer.spectrogram>
