# Purpose

Describe logic for how timerange binding and control should be done. The
goal is to get a set of transparent and describable rules that the users
can understand and discuss, and make sure the code is doing this.

# Introduction

This page is introduced around the release of the 2011 version, and
Reiner indicated that he still couldn't follow the logic--he'd like to
adjust the time by editing the timerange= property of a URI, but instead
it is bound to the timerange already set.

# Desired Logic

## Use Case 1, Single Plot

This is the trivial case. When the data comes back with time location
units, the x axis is bound to the timerange property.

## Use Case 2, Stack of plots at the same time

Three URIs from the same time are added as a stack of plots. As each is
loaded, it is found to have a timerange consistent with the timerange
property, and is bound.

## Use Case 3, Add plot after zooming in

Data from 2011-01-10 is loaded and the timerange property is bound. We
zoom into a feature, and want to add a second dataset. We enter the GUI
with the current timerange setting, select the parameter, and exit the
GUI with the timerange unchanged. This new dataset is bound to the
existing plot axis.

## Use Case 4, Add new plot with shifted timerange

Data from 2011-01-10 is loaded and the timerange property is bound. We
expect to an upstream satellite will see the feature on the previous
day. We bring up a GUI for it, the user sets the timerange to the
previous day, and exit the GUI. Since the timerange of the data returned
is a day earlier, we do not bind to the timerange.

## Use Case 5, Using timerange property in URI to control timerange

A stack of plots, each is already bound. Changing the URI of the top
plot from ...\&timerange=2011-01-10 to ...\&timerange=2011-01-09 resets
the plot, but the binding is preserved, so all the plots are reset with
new times. The user must manually unbind the axis to explore a shifted
time.

## Use Case 6, Using timerange in data source editor GUI to control time

A stack of plots, each is already bound. Entering the GUI for the top
plot has a similar effect, changing the timerange in the GUI changes the
URI timerange, and the binding is preserved. Autoplot should decorate
the GUI to indicate to the user that the timerange is bound.

## Use Case 7, plot context controlled by timerange, and the context controls the TimeSeriesBrowse

A stack of two plots with TSB controlled by the dom.timeRange. The top
plot has the filter |"histogram()" applied to it, so the
dom.plot\[0\].context is bound to dom.timerange, and the TSB now listens
to the dom.plot\[0\].context.

## Use Case 8, plot context controlled by timerange, and the context controls the TimeSeriesBrowse, no time axes

One plot is of a histogram of a TSB dataset. As the dom.timeRange is
adjusted, the histogram updates.

# Notes

  - Note the use case 6 logic has the feature of providing a GUI when
    there are stacks from two spacecraft shifted in time.

# Notes on the current logic

  - Use cases 5 and 6 are currently unimplemented. Changing the URI
    resets everything about the plot element, including any bindings.

# Testing Sequences

## test001

  - plot vap+cdaweb:ds=AC\_K0\_SWE\&id=Vp\&timerange=2012-04-26
  - scan previous
  - use the editor to select Np
  - plot below. Note the editor didn't have the timeaxis range in there,
    and it properly loads the explicit time "2012-04-26" instead of the
    timeaxis range.
  - the two plots should have the same time, but don't.

Note, a lot of people have commented on and are surprised when the
original URI doesn't update the timerange. This is intentional behavior,
but it should probably be reviewed.

This actually was a bug in the CDAWeb module. It would ignore the time
if it was outside of the dataset's valid range. This was not properly
set for ACE. I've loosened up this rule by enlarging the mission
timerange.

## Test002

  - plot vap+cdaweb:ds=AC\_K0\_SWE\&id=Vp\&timerange=2012-04-26
  - plot vap+cdaweb:ds=AC\_K0\_SWE\&id=Np\&timerange=2012-04-20.
  - reset
  - from history, plot
    vap+cdaweb:ds=AC\_K0\_SWE\&id=Vp\&timerange=2012-04-26
  - from history, plot
    vap+cdaweb:ds=AC\_K0\_SWE\&id=Np\&timerange=2012-04-20 below.
  - someone will complain that these aren't bound.

## Test003

The verifies use case 6.

  - plot
    vap+das2server:<http://emfisis.physics.uiowa.edu/das/das2Server?dataset=rbsp/emfisis/em2/Emag.dsdf&start_time=2012-05-10T19:00:00.000Z&end_time=2012-05-10T21:00:00.000Z>
  - plot below
    vap+das2server:<http://emfisis.physics.uiowa.edu/das/das2Server?dataset=rbsp/emfisis/em2/Emag.dsdf&start_time=2012-05-10T19:00:00.000Z&end_time=2012-05-10T21:00:00.000Z>
  - edit the top panel, to make the timerange "2012-05-10 20:00 to
    22:00"
  - the dom timerange should update to this time.

## Test004

This verifies use case 7.

```
reset()
plot( 0,'vap+cdaweb:ds=GE_K0_EFD&id=Ss&filter=geo&timerange=1993-01-01' )
plot( 1,'vap+cdaweb:ds=GE_K0_EFD&id=Ss&filter=geo&timerange=1993-01-01' )
dom.plotElements[0].component= '|histogram(0,200,1)'
waitUntilIdle()
dom.timeRange = dom.timeRange.next()
```
## Test005

This verifies use case 8.

