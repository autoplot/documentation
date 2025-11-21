Audience: Scientists using Jython scripting

Purpose: Describe usage of the Jython plot command.

# Introduction

The plot command is the script analog to the green play button, putting
data on to the plot. Its controls are similar to that of IDL, but
because plots and plotElements are two separate things, differences
show.

# Basic Usage

```
plot( URI, title='My Plot' )  
```
replaces the first data source with the data from the URI, possibly
setting up Time Series Browse so other time ranges will be loaded. Or

```
plot( pos, URI, title='Second Plot' )
```
where pos is the *data* position, which with typical use is also the
plot position, with 0 being the top-most plot.

## namedParams

All of these are optional, and may have no effect for a particular
render type:

* **color** named color, RBG value, or Color enumeration.  Examples include 'DarkRed', '0x00FF00', and Color.GREEN.
* **symbolSize** the size of the symbols, in pixels roughly, of the symbols.
* **lineThick** the thickness of the connecting lines, in pixels.
* **lineStyle** enumeration of values, one of: solid,none,dotfine,dashfine
* **symbol** the plot symbol, one of: dots triangles cross
* **symbolFill** the method for filling or not filling the symbol center, one of 'none', 'solid', or 'outline'. (Note this is not saved in .vap files.)
* **legendLabel** label for the legend box.
* **title** title for the plot
* **[xyz]title**  axis labels.
* **[xyz]range**  axis ranges, e.g. '0 to 50' or '2016-01-01'
* **[xyz]tickValues**  values to use for tick positions.  Use array of strings for times.
* **[xyz]autoRangeHints** 
* **[xy]scale**  data-to-pixel ratio.
* **renderType** explicitly sets the renderType, to one of the values: scatter, colorScatter, series, nnSpectrogram, spectrogram, contour, fillToZero, stairSteps, hugeScatter, polar, bounds, digital, stackedHistogram
* **xpos** override horizontal position of plot, eg. '50%+1em,100%-2em'
* **ypos** override vertical position of plot, eg. '0%+1em,25%-2em', 0 is top
* **row** the row or rowId of the row to use.
* **column** the column or columnId of the column to use.
* **[xy]drawTickLabels** False turns off the x or y tick labels for the plot

NOTE: arguments should be flexible, so findgen(5) can be used as well as
\[0,1,2,3,4\], and timegen('2018-001T00:00Z','24hr',3) instead of
\['2018-001T00:00Z','2018-002T00:00Z','2018-003T00:00Z'\], and Color.RED
as well as 'Red' and 0xFF0000.

### color

Color can be a Java color object (Color.GREEN), or a string which can be
converted into a color. Examples include:

**DarkRed** X11 color names are resolved. See https://en.wikipedia.org/wiki/X11_color_names and note spaces should be removed from names.
**0x00FF00** RGB colors specified in hex.
**0xA000FF00** ARGB where A is the 'alpha'or transparency channel where 0&nbsp;is&nbsp;completely&nbsp;invisible&nbsp;and&nbsp;255&nbsp;(FF)&nbsp;is&nbsp;completely&nbsp;opaque.`  
**`Color.RED`**`&nbsp;Java&nbsp;color&nbsp;object.`

### renderType

The string name for the render type to be used for this data. Examples
include:

  - scatter
  - colorScatter
  - series
  - nnSpectrogram
  - spectrogram
  - contour
  - fillToZero
  - stairSteps
  - hugeScatter
  - polar
  - bounds
  - digital
  - stackedHistogram

See <http://autoplot.org/developer.renderTypes>

### xpos,column

xpos and column are two names for the same thing, the column that
specifies the location of the plot. When this is a position string like
"10%,90%" a column is found with this position, and if not found one is
added. Note a plot can be used here as well.

### ypos,row

ypos and row are like the xpos and column named parameters, but for
vertical positioning.

### rightAxisOf

This is another plot for which this should be the right axis (opposite
the default left), where a second plot is added so that the right and
left plots can be controlled independently.

# Advanced Usage

(plot,plotElement) = plot( 1, 'vap+inline:ripples(400)' )

plot is the plot containing the plot element. The "1" first argument
refers to dom.dataSourceFilters\[1\] .

