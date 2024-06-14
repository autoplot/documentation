# Purpose

Define metadata to go into PNG files.

# Introduction

At the September 2011 MMS meeting, we were talking about agreeing on a
standard for storing additional information within png files so that
plots can be recreated and nice thin clients written. This would include
for example, plot coordinates on the page. Javascript could then look at
this metadata and calculate new plot requests. Autoplot might also put
in metadata describing the location of the vap file that produced the
image.

# Proposed format

We would have separate "chunks" of data for each purpose. For example,
the plot coordinates and titles for each plotted image would be
contained in XML that is in one chunk, and Autoplot might store a
reference to a vap in another chunk, and someone else could throw the
data into another chunk.

## Possible chunk names

XML chunks have four-character codes that identify them. Within these
for bytes, the upper case bit has special meanings described in
<http://www.w3.org/TR/PNG-Structure.html#Chunk-naming-conventions>. So
maybe these chunks would be used:

```
xfrm  axis transformations in XML document.  This would have a set of pixels rectangles and data coordinates, one for each plot.  This should also contain the absolute size of the plot in case it is resized.
vapx  a reference to an autoplot .vap file that produced the image.  This may be a relative reference, relative to the png file.
```

## xfrm chunk

This would be an xml document, with nodes something like the following.
Note only one canvas/plot node would be required containing an xaxis and
yaxis with imin, imax, min and max.

```
canvas/title    
canvas/plot/title        optional title
canvas/plot/id           optional ID string
canvas/plot/xaxis/label  optional label
canvas/plot/xaxis/min    required data minimum
canvas/plot/xaxis/max    required data maximum
canvas/plot/xaxis/imin   required pixel minimum, top-left is [0,0]
canvas/plot/xaxis/imax   required pixel maximum
canvas/plot/xaxis/units  optional units string
canvas/plot/xaxis/log    optional log flag.  log="False" if not specified.
canvas/plot/xaxis/flipped  optional flag (True/False) indicating the axis is flipped.
canvas/plot/yaxis/label  optional label
canvas/plot/yaxis/min    required data minimum
canvas/plot/yaxis/max    required data maximum
canvas/plot/yaxis/imin   required pixel minimum, top-left is [0,0]
canvas/plot/yaxis/imax   required pixel maximum
canvas/plot/yaxis/units  optional units string
canvas/plot/yaxis/log    optional log flag.  log="False" if not specified.
canvas/plot/yaxis/flipped  optional flag (True/False) indicating the axis is flipped.
canvas/width             pixel width of the canvas.  Note if the image is resized, then this will be different than the image.  This is only available to scale the image.
canvas/height            pixel height of the canvas.  Note normalized coordinates might be a better way to support this.
canvas/text[*]           other text in the canvas, meant to allow for searching.
```

## First Implementation (Feb 2012)

A first implementation was in the code and pngs encoded with the das2
library would include the data. This JSON tree was significantly
different from the spec above. As far as I know, no one used this data.
It featured:

  - There's no special chunk type, and instead there is a tEXt block
    with "plotInfo" as the label.
  - a default plot that was the tallest of all the plots.
  - an array of all plots
  - UTC units for time. ISO8601 encoded times, of course.
  - all tags are required.

## Second Implementation (July 2013)

The second implementation changed things quite a bit, and I'm changing
things again before this gets into production. Note:

  - default plot is dropped. It's confusing, redundant, and it's not
    hard to simply say "plots\[0\]" and have a singleton list for other
    plotting systems.
  - top/bottom left/right are used to remove confusion and to
    acknowledge we first want to identify boundary.
  - support for flipped axes is dropped for now. This doesn't happen
    often and can be added later.
  - optional z-axis colorbars are supported by locating the colorbar
    which could be used to identify Z data value from color. This is
    also included because the Z-axis units are often important and
    should be searchable.
  - camelCase is used instead of underscores to improve readability in
    javascript.

## Final Implementation

  - tTXt node used to store the data.
  - keyword=plotInfo value=JSON
  - Example one-plot JSON looks like:

```
 { "size":[722,595],
   "numberOfPlots":1,
   "plots": [ {
     "title":"Ephem for Balloons, Radius is L, MLT=0 --->", 
     "xaxis": { "label":"", "min":-10.0, "max":10.0, "left":84, "right":638, "type":"lin", "units":"" },
     "yaxis": { "label":"", "min":-10.379172566142076, "max":9.620827433857922, "top":48, "bottom":535, "type":"lin", "units":"" }
   } ]
 }
```

  - And here's one with a time axis, which uses ISO8601 times:

```
 { "size":[722,642],
   "numberOfPlots":1,
   "plots": [
   {
     "title":"POLAR/HYD  Electron Differential Energy Flux", 
     "xaxis": { "label":"", "min":"2000-01-09T18:00:00.000Z", "max":"2000-01-10T00:00:00.000Z", "left":78, "right":644, "type":"lin", "units":"UTC" },
     "yaxis": { "label":"Electron Diff. Energy Flux (1/(cm^2-s-sr))", "min":18797.0, "max":1.8797E7, "top":52, "bottom":590, "type":"log", "units":"1/(cm^2-s-sr)" }
   }
 ]}
```

## Demonstration Applications

### Autoplot Thin Client Demo

This uses the rich ascii to interpret mouse gestures on the client side.
For example, shift-click on:

<https://jfaden.net/AutoplotServlet/thin/zoom/demo.jsp?uri=vap%2Bhapi%3Ahttps%3A%2F%2Fjfaden.net%2FHapiServerDemo%2Fhapi%3Fid%3DpoolTemperature%26timerange%3D2020-08-20%2FP2D>

and click on the image. The x and y position of the click is reported
below the "Reset" button. Now drag out a box, and the x-axis range will
be used to reset the x axis before another data load.

### Autoplot PNG Walk Tool

Users will be able to pick off points from plots generated by Autoplot
and any code that includes this metadata.

