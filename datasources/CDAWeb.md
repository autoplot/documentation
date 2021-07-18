# CDAWeb
The CDAWeb at NASA/Goddard contains roughly 1400 data products from around 40 different missions. Each data product 
corresponds to CDF files spanning a mission, containing many plottable parameters. Instrument teams produce CDF 
files and provide them to the CDAWeb which makes the data available. An example URI is:

vap+cdaweb:ds=OMNI2_H0_MRG1HR&id=DST1800&timerange=Oct+2016

which means from the data identified as "OMNI2_H0_MRG1HR" plot the parameter "DST1800", loading data to cover the time range "Oct 2016."

File&rarr;Add Plot From&rarrCDAWeb will connect to the CDAWeb servers
and download a file indicating what products they offer.  

<img src='http://autoplot.org/wiki/images/CDAWebDB.png' width=160>

In this dialog you can find the mission or instrument, using filter to look at matching subsets, and once selected
an example CDF file for this data is downloaded.  The editor to pick the parameter is similar to that for a single
CDF file.  Note however that only data parameters can be loaded, so you cannot load just a set of timetags as you 
can with CDF files.  Also there is an "availability" checkbox, and when this is selected a bar showing where data 
is available is drawn but the data is not loaded.
