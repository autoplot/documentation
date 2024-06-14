# Introduction / Purpose

This is a series of human driven tests that test things that are not
easy to test in automatic testing. The order should be preserved in case
numbers are used to identify tests in bug reports. Also in bug reports,
the names of the tests, e.g. "run through bookmarks", should be used in
case order is changed.

Note that some of these have been converted into "Jemmy scripts," which
are nightly tests that simulate human interaction by manufacturing fake
GUI events. See <http://jfaden.net:8080/hudson/job/autoplot-test100/>
and in the source .../VATesting/src/org/autoplot/test/.

# Tests

## run through bookmarks

  - start autoplot with fresh session
  - select the first bookmark, Demos-\>Demo 1
  - select each bookmark after it, up to "browse a directory tree"
  - for "browse a directory tree," navigate through the tree to a
    dataset
  - for demo 12, fits file, verify that the data tab starts up and the
    slice index is adjustable.

## context overview

  - reset and plot bookmarks-\>demos-\>demo 5
  - zoom in on x and y with box zoom.
  - right-click on plot, "add plot"-\> "context overview"
  - a plot with its original ranges should be displayed below

# Proposed New Tests

New tests should be submitted here for review.

## Multi-panel plot

This more advanced example shows how to create a 2x3 stack of 6 plots to
look at the components of a fits file.

  - add 2x3 empty plots using layout tab, plots context menu,
    Canvas-\>AddPlots
  - Edit DOM, plotElements\[\*\].dataSourceFilterId='data\_1' so they
    all plot the same data
  - Edit DOM, plotElements\[\*\].component slice0(i) to plot each
    element
  - layout tab, plots context menu, Canvas-\>Add Hidden Plot to bind all
    the plot X and Y axes together
  - demo XY binding, all Z axes should be automatically zoomed to just
    their slice.

## Jython Data Source Filter

  - load
    vap+jyds:<http://autoplot.org/data/events/filterEventsFile.jyds>
  - enter the editor. Change the resourceURI file to
    downloads.20110101.log
  - plot this.
  - aggregate this, so the URI is
    vap+jyds:<http://autoplot.org/data/events/downloads.$Y$m$d.log?script=http://autoplot.org/data/events/filterEventsFile.jyds&timerange=2011-01-08>
  - enter the editor and change the range to "2011 Jan"

## Extremes

Ben found in his testing a bug where resetting the zoom after zooming
way in appeared to get in a deadlock.

  - load
    vap+cdf:<http://cdaweb.gsfc.nasa.gov/istp_public/data/polar/hyd_h0/2000/po_h0_hyd_20000109_v01.cdf?ELECTRON_DIFFERENTIAL_ENERGY_FLUX>
  - zoom out all the way with the mousewheel
  - zoom in all the way with the mousewheel
  - zoom out all the way
  - reset zoom
  - ctrl-Y and ctrl-Z to jump between zooms repeatedly.

I was not able to get it to hang on Linux.

## TimeSeriesBrowse

<https://sourceforge.net/tracker/?func=detail&aid=3484946&group_id=199733&atid=970682>

  - plot demo2
    vap+cdf:<http://cdaweb.gsfc.nasa.gov/istp_public/data/polar/hyd_h0/$Y/po_h0_hyd_$Y$m$d_v01.cdf?ELECTRON_DIFFERENTIAL_ENERGY_FLUX&timerange=20000109>
  - scan to next interval
  - inspect, select ions, note time range for aggregation is 20000110.
    plot below.
  - v2011\_6 updates the time and makes the binding. v2011\_7 leaves it
    alone and there is no binding made.

## Undo/Redo between timeseries and non-timeseries, components and no components

  - repeat 5 times:
      - demo 4
      - demo 5
  - I was getting a case where it wouldn't flip, as if some event is
    getting lost.
  - File-\>Edit-\>Undo... to go back 6 states.
  - Redo is insensitive (which it shouldn't be), and I get inconvertable
    xaxis units.

## PngWalk Stress Test 1

  - Start up the pngwalk tool pointed at
    <http://sarahandjeremy.net/~jbf/autoplot/cdf-pngs/>\*.png (or local
    copy of)
  - Options-\>Thumbnail Size-\>50 px
  - grid view
  - scroll down, scroll down, scroll down
  - maximize

I was able to get this to essentially hang, because all the threads
where locked.

## Mouse Zoom Pan

This was introduced before moving isotropic code down into dasCore.

  - Start up empty autoplot
  - zoom in with mouse wheel
  - pan with mouse wheel
  - turn on isotropic
  - wheel to zoom in on xaxis
  - wheel to zoom in on yaxis
  - wheel to zoom in on plot.

## Copy Plot Elements Down

This was introduced when the development branch showed a new bug.

  - vap+inline:ripplesVectorTimeSeries(200)\&RENDER\_TYPE=hugeScatter
  - set render type to hugeScatter (this is a bug, shouldn't have to do
    this)
  - copy plot elements down.
  - new plot should be hugeScatter. Bug was that it was scatter.

## Operations Cache is Properly Reset

To my horror I discovered the operations cache was not being properly
reset. This was in the development branch, and the v2012a\_12 actually
shows a different bug.

  - vap+inline:ripplesTimeSeries(2000)
  - set the operations to "|reducex('360 s')"
  - vap+inline:ripplesSpectrogramTimeSeries(2000)
  - set the operations to "|reducex('360 s')"

## Operations Cache does not properly update

Bill at the RPWS group pointed out a procedure where the operations
cache didn't update properly.

  - vap+das2Server:<http://jupiter.physics.uiowa.edu/das/server?end_time=2012-03-10T00:00:00.000Z&start_time=2012-03-09T00:00:00.000Z&dataset=Juno/WAV/Survey>
  - in the data tab, set operations to "|dbAboveBackgroundDim1(10)"
  - on the xaxis, hidden scan previous button
  - A blank plot appears, and the process dataset is
    dataset\[4,588\*,43\*\] while the loaded dataset is Spectral
    Densities\[4,570\*,43\*\] (note the name "Spectral Densities" is
    invalid as well.)

This was corrected in v2012b\_6 by temporarily disabling the cache. This
is bug
<https://sourceforge.net/tracker/?func=detail&aid=3573900&group_id=199733&atid=970682>

## JythonDataSource TSB is not properly set

Reiner was frustrated by this.
<http://sourceforge.net/tracker/?func=detail&aid=3576060&group_id=199733&atid=970682>

  - get a script with TSB like this:
  - <http://www-pw.physics.uiowa.edu/~jbf/autoplot/data/jyds/demoTsb.jyds?timerange=2012-04-18>
  - advance two days forward.
  - enter editor. Note the default is still used, and not the current x
    axis range.
  - Click plot on this and the original default timerange is reset.

## filters chain gui

  - plot
    vap+inline:ripples(100,110)+randn(100)/50+outerProduct(ones(100),randn(110)/50)
  - data tab, Data Post Processing panel, plus button (+), slice0
  - Slice Dimension on the filter gui should be set to dim0 or dim1.
    (It's not as of r15782)
  - mouse wheel on "Operations" text field, cursor on (0) should update
    slice dimension GUI.
  - resetting slice index to 10 should update "Operations" text field.

# Time Series Browse

## TimeSeriesBrowse without time axis

Tested on v2015a\_8

  - plot
    <http://autoplot.org/data/jyds/tsbNonTimeAxis.jyds?timerange=2000-01-03>
  - tear of the axis tab
  - on the axis tab, click on the scan next button (\>\>) to advance to
    the next interval.
  - in the time range editor, "2000-01-04T12:00/14:00" and see that the
    data is trimmed. Note this is because the jyds trims the data to
    timerange precisely.

## Two TimeSeriesBrowse without time axis, attached to plot.context

  - plot
    <http://autoplot.org/data/jyds/tsbNonTimeAxis.jyds?timerange=2000-01-03>
  - tear of the axis tab
  - enable the "legend label" and set the value to "%{PLOT\_CONTEXT}".
    Note there's a right-click context menu containing this insertion.
  - on the axis tab, click on the scan next button (\>\>) to advance to
    the next interval.
  - right-click on the plot, "add plot"-\>"copy plot elements down"
  - tear off the layout tab
  - in the bindings, delete the two bindings between the
    dom.plot\[:\].context property and the dom.timerange.
  - click on the lower plot to focus.
  - on the axis tab, click on the scan previous button (\<\<) to advance
    to the previous interval.
  - note the lower plot advances but the top one does not.

# Things that can't be tested with Jemmy tests

## Launch with URI

  - firefox
  - <http://autoplot.org/autoplot.jnlp?http://autoplot.org/data/autoplot.cdf?BGSM>
  - Autoplot should come up with BGSM loaded.

## Launch with URI into PNGWalk

  - firefox
  - <http://autoplot.org/autoplot.jnlp?version=devel&pngwalk:http://www-pw.physics.uiowa.edu/juno/mwg/pngwalks/threePanelSansFgm/product.pngwalk>
    (mwg password needed)
  - Autoplot pngwalk should come up.

# Jan 2015 tests

## FFTFilter

## Hanning

