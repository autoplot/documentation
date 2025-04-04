Purpose: define new features to complete DasAnnotation Audience: Das2
developers.

# Introduction

The DasAnnotation object allows annotations to be added to the
dasCanvas.

# Current State

It is positioned with a row and column, uses GrannyText, and allows
pointing at a coordinate.

It currently misses the bounds if you enlarge the font.

# Proposed Changes

  - This should have a position relative to the box control, similar to
    the legend.
  - The default is NW, but this could also be
    SW,NE,SE,OutsideSE,Above,Below.
  - It would be nice to have rotations and offsets. (NW;+3em+10pt,+2em)
  - It would be nice to be able to attach it to data as well, so instead
    of drawing an arrow, it would locate based on the data.

# Current State (2018-06-14)

This was all implemented, excluding rotations. See
[Annotations](Annotations.md) and
<http://autoplot.org//help.annotationCommand>

# New Proposed Changes

I'd like for annotations to be able to implement plot legends. This
would mean adding a new capability to the GrannyTextRenderer to insert
plot symbols and colors. See
<https://sourceforge.net/p/autoplot/feature-requests/634/>

