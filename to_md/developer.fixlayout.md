Purpose: Consider the logic of the "fix layout" operation

Audience: Programmers and interested scientists

# Introduction

The fix layout is intended to correct layout mistakes and provide an
easy way to accomplish attractive looking layouts. For example, one can
grab on to an axis edge (with shift-click) and drag it down so that it
overlaps part of another plot to make it bigger, then run the "fix
layout" command to fix the overlap. Also, if ephemeris is added to the
top plot of a two-plot layout, then the loaded ticks will overwrite the
bottom plot. Fix layout will also fix this.

Another important aspect of fix layout is that it is idempotent, meaning
once applied if applied again it should have no effect. We've added a
number of options to fix layout now, and there's a remaining bug where a
plot with a title grows, breaking the idempotent rule.

So this page is to consider what does the operator mean to do? What
spacing should be preserved? A 1-em tall events bar should remain 1-em
high, for example. It's y-axis is not used, so maybe it should be turned
off.

# Define the operation

These are the aspects:

  - unused whitespace is recovered.
  - the em-height of a plot is preserved.
  - the relative sizes of the plots is preserved.
  - the margins are used to make the row layout easier to interpret.
  - hidden plots which bind together other plots are preserved. A block
    of X,Y,and Z plots might be linked by a hidden plot.

Define **relativeSize** which is the size relative to other plots. The
relative size is based on the percentage part of the layout, so a plot
which is 50%,100% is twice the relativeSize of a plot which is 75%,100%;
but this is also true for 50%,100%-1em 75%,100%-1em. This is to preserve
the 0%,0%+1em of an events bar.

Define **additionalEmSize** which is the additional ems added and
subtracted to make room for labels. This will be preserved through the
operation.

# Current Algorithm

  - identify Rows which are actually used.
  - implement hideTitles, moveLegendsOutsideNE, hideTimeAxes.
  - define **totalHeightPixels** as the sum of each row (except the
    margin).
  - define **relativePlotHeight** as the per-row height normalized by
    totalHeightPixels.
  - define **MaxUp** as the per-row maximum additional pixels needed for
    the titles attached to the row.
  - define **MaxDn** as the per-row maximum additional pixels needed for
    the x-axes attached to the row.
  - calculate the space available to the plots.
  - define **newPlotHeight** as the new height of each row in pixels.
