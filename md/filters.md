Audience: Scientists

# Introduction

Autoplot allows data to be run through processes before plotting. For
example, data can be smoothed with a boxcar filter before plotting, or
waveform data can be processed with FFTs to make a spectrogram. These
are like unix pipes, where one dataset is input and one dataset is
output, rather than combining data from multiple sources.

These filter operations can be applied just before plotting, and are
added on the data tab under the "Data Post Processing" area. Filters are
added with the filters editor, and each filter added is given a small
GUI control to adjust any parameters.

# Selected Filters

`|histogram` perform an "auto" histogram of the data that automatically
sets bins.

`|log10` take the base-10 log of the data.

`|slice0(index)` slice the data on the zeroth dimension (often time) at
the given index.

`|slice1(index)` slice the data on the first dimension at the given
index.

`|collapse0` average over the zeroth dimension to reduce the
dimensionality.

`|transpose` transpose the rank 2 dataset.

`|fftPower(size)` plot power spectrum by breaking waveform data in
windows of length <em>size</em>.

`|smooth(size)` boxcar average over the rank 1 data.

`|diff` finite differences between adjacent elements in the rank 1 data.

`|accum` running sum of the rank 1 data. (opposite of diff).

`|grid` grid the rank2 buckshot but gridded data into a rank 2 table.

`|flatten` flatten a rank 2 dataset. The result is a n,3 dataset of
\[x,y,z\]. (opposite of grid)

`|negate` flip the sign on the data.

`|add(amount)` add a constant to the data. Note this can be datums like
"15sec".

`|multiply(amount)` multiply the data by add a constant.

`|cos` cos of the data in radians. (No units check)

`|sin` sin of the data in radians. (No units check)

`|toDegrees` convert the data to degrees. (No units check)

`|toRadians` convert the data to radians. (No units check)

# Edit Filters GUI

Normally filters would be added using the GUI. This screenshots sequence
shows how OMNI Beta data is loaded and boxcar smooth is applied:
<http://autoplot.org/data/tutorials/20170516_filters/20170516_1152.html>

The "add filter" dialog is the list of all available filters.

# Relationship to Scripting

Note that the filters are typically the same as the functions used in
Jython scripting. The filters are implemented in Autoplot by calling
these same routines. So for example, loading

```
vap+cdaweb:ds=OMNI_HRO_1MIN&id=Beta&timerange=Oct+2016
```

and applying the filter

```
|smooth(51)
```

is the same as the script:

```
ds= getDataSet( 'vap+cdaweb:ds=OMNI_HRO_1MIN&id=Beta&timerange=Oct+2016' )
ds= smooth( ds, 51 )
plot( ds )
```

Filters make the commonly-used functions of scripting available without
the overhead of scripting, and available within .vap files.

# Automatic Filters

Some filters are added automatically by Autoplot to provide a landing
page for the data. For example, suppose Flux data is loaded, which is a
function of Time, Pitch Angle, and Energy (represented as
Flux\[Time=1440,PitchAngle=19,Energy=30\]). Since a 2-D view of this
data is needed, Autoplot picks a dimension to run the "slice" filter on.
For example, "|slice1(10)" so that only the Flux at 90 degrees is shown.
The slice GUI will appear automatically on the data tab, and you can
select a different dimension or slice index.

## applyIndex

The apply index filter extracts a subset of a filter by using
Python-like syntax. For example, applyIndex1(105:255) keeps these
indices. The command can also remove elements, for any spec starting
with tilde (\~).

