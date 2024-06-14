Purpose: describe definitively how aggregation should be done.

Audience: developers and interested scientists.

# Introduction

Aggregation has been one of Autoplot's main features, making a pile of
files into a useful service comparable to the Time Series Browse
capabilities of the Das2Server and CDAWeb plugins. When the data
returned by the aggregation are not a function of time, useful
functionality is supported. For example, suppose you have a Jython
datasource:

```
tr= getParam( 'timerange', '2014-01-09', 'timerange to load' )
ds1= getDataSet( '`<http://cdaweb.gsfc.nasa.gov/istp_public/data/ace/sis/level_2_cdaweb/sis_k0/$Y/ac_k0_sis_$Y$m$d_v$v.cdf?H_lo>`', tr )
ds2= getDataSet( '`<http://cdaweb.gsfc.nasa.gov/istp_public/data/ace/sis/level_2_cdaweb/sis_k0/$Y/ac_k0_sis_$Y$m$d_v$v.cdf?H_hi>`', tr )
result= link( ds1,ds2 )
```

this too is a TSB, and likewise

<http://cdaweb.gsfc.nasa.gov/istp_public/data/ace/sis/level_2_cdaweb/sis_k0/$Y/ac_k0_sis_$Y$m$d_v$v.cdf?H_hi&DEPEND_0=H_lo>

does reasonable things.

This is to enumerate the uses and expected behavior.

# First Obvious case, when each granule is a time series

Each call returns dependent data that is a function of independent
parameter time:

`vap+dat:`<http://cdaweb.gsfc.nasa.gov/istp_public/data/voyager/voyager1/plasma/sedr/v1_sedr_1977.asc?time=field0&column=field7&timeFormat=$Y+$j+$H+$M+$S>  
`vap+dat:http://cdaweb.gsfc.nasa.gov/istp_public/data/voyager/voyager1/plasma/sedr/v1_sedr_1978.asc?time=field0&column=field7&timeFormat=$Y+$j+$H+$M+$S`

Clearly, the two datasets are appended.

# Data returns a non-time-series

`vap+dat:http://cdaweb.gsfc.nasa.gov/istp_public/data/voyager/voyager1/plasma/sedr/v1_sedr_$Y.asc?column=field9&depend0=field8`

X data is combined, Y data is combined.

# Data returns an image

What got me thinking about this was I was surprised when aggregating
image files, that the result was not a failure, but instead it started
stacking the images side-by-side. That must be a side-effect of other
code, and it's not an entirely undesirable result. However what I was
hoping to add was logic that would add a dimension in this case, so if
each granule returned

```
image[x;y;r,g,b]
```

then the aggregation would be

```
image[i;x;y;r,g,b]
```

and then I could slice on dim0 to quickly scan through the images and
get slices of a pixel value over time.

See
<http://jfaden.net/~jbf/camE/2016/08/26/$Y$m$dT$H$M$x.jpg?channel=greyscale&timerange=2016-08-26>

Another case is where each file contains one measurement.

# Slicing and Aggregating should be inverse operations

Slicing adds the property CONTEXT\_0, so aggregation should be able to
form a DEPEND\_0 by forming a dataset from the CONTEXT\_0 properties.

