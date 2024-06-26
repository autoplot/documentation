# Introduction

Auto Range Hints are additional controls for the axes so that when
Autoplot autoranges, constaints can be applied. For example, sometimes
you want the data to appear with an optimal range, but a particular
scale is desired so comparisons can be made between plots.

# Setting the hints

This control doesn't have a convenient place in the GUI, and this may
change, but for now the following procedure may be used:

1.  plot your data, or for example,
    <http://cdaweb.gsfc.nasa.gov/istp_public/data/polar/hydra/hyd_h0/$Y/po_h0_hyd_$Y$m$d_v01.cdf?ELECTRON_DIFFERENTIAL_ENERGY_FLUX&timerange=2000-01-09&slice1=1>
2.  right-click on the yaxis, "Axis Properties."
3.  set autoRangeHints to "log=T\&width=4"
4.  this will pick the best range where 4 log cycles are visible.

# Available Hints

    includeZero   T or F     make sure that zero is within the result.
    width         30nT       use this width.  This is a formatted datum which 
                             is parsed with the units of the axis, or the number of cycles with log.
    log           T or F     force log or linear axis
    widths        30nT,300nT,3000nT   use one of these widths
    center        0          constrain the center to be this location
