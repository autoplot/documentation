# CDF Files

Reads in a variable from a [Common Data
Format](https://cdf.gsfc.nasa.gov/) file.

  - mime type: application/x-cdf-file (Note some servers advertise a
    content type of application/x-netcdf.)
  - extension: .cdf
  - Example URL:
    [4] vap+cdf:https://cdaweb.gsfc.nasa.gov/sp_phys/data/ace/swepam/level_2_cdaweb/swe_k0/2012/ac_k0_swe_20121229_v01.cdf?He_ratio
  - Supports formatting: Yes, rank 1 and 2, though not yet ISTP
    compliant.
  - Parameters
      - The parameter is the name of the cdf variable.
      - If not specified, a list of possible variables is given.
  - Wildcards and aggregation

In the following, we tell autoplot that the file name has a four-digit
year, a two-digit month, and a two-digit day. Then we ask it to plot
data on the day 20000109 using the time wildcards described in
[5](https://autoplot.org/autoplot/index.php/Main_Page#Wildcards_and_Aggregation).

The first part of the url is

<https://cdaweb.gsfc.nasa.gov/istp_public/data/polar/hyd_h0/>

the file part of the url is

```
2000/po_h0_hyd_$Y$m$d_v01.cdf?ELECTRON_DIFFERENTIAL_ENERGY_FLUX&timerange=20000101
```
to specify more than one day, use

```
2000/po_h0_hyd_$Y$m$d_v01.cdf?ELECTRON_DIFFERENTIAL_ENERGY_FLUX&timerange=20000101 - 20000103 (end is not inclusive)
```
to allow access to data that crosses a year boundary, use

```
$Y/po_h0_hyd_$Y$m$d_v01.cdf?ELECTRON_DIFFERENTIAL_ENERGY_FLUX&timerange=20001231 through 20010101
