Purpose: Study how ephemeris could be discovered for many spacecraft.

Bob and I have been discussing with the CDAWeb guys how ephemeris could
be discovered for most any spacecraft. As a use case, we want to plot
density for many spacecraft at Earth as a function of ILT and L shell.

# Method 1

1.  start with dataset, say
    vap+cdaweb:ds=AC\_H2\_CRIS\&id=flux\_N\&timerange=2014-03-31
2.  identify SSC\_ID with Bernie's page at
    <http://cdaweb.gsfc.nasa.gov/registry/hdp/CdawebSscIds.xql> -\> ace
3.  call Bob's service to get data.
    <http://tsds.org/get/?catalog=SSCWeb&dataset=ace&parameters=X_GEO&start=-P3D&stop=2014-02-19&outformat=1>

This results in X\_GEO. How do I get multiple parameters? How do I get a
list of parameters?

