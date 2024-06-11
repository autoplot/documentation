This is an old set of URIs for testing, back when this was done by hand
when making a release. Autoplot is tested now automatically and
continuously, see <http://jfaden.net/hudson/>. See also
<http://autoplot.org//developer.listOfUris> . This is tested with
<http://jfaden.net:8080/hudson/job/autoplot-test140/>

TODO: this page should be updated to make a correct set of links, and
Autoplot's test140 which tests all the URIs on a page should be used to
test. That way, any one could add URIs here and they would be tested.

TODO: This uses an old vap server, jnlp.cgi, which does not appear to be
working. This page should be updated to use
<http://autoplot.org/autoplot.jnlp>?...

# TSDS

This loads:

<http://timeseries.org/get.cgi?StartDate=19950101&EndDate=19950109&ppd=144&out=tsml&param1=OMNI_OMNIHR-22-v0>  
<http://timeseries.org/get.cgi?StartDate=19950101&EndDate=19950104&ext=bin&out=tsml&ppd=144&param1=OMNI_OMNIHR-22-v0>  
<http://timeseries.org/OMNI_OMNIHR-22-v0-to_19950101-tf_19950104-ppd_144-filter_0-ext_bin.bin>

# Das2Server

Autoplot gets confused about the escaping. "vap+das2server" turns into
"vap das2server" and the das2Server file part is removed. This probably
has something to do with its TimeSeriesBrowse capability.

{{ Launch2 |
uri=vap+das2server:<http://www-wbd.physics.uiowa.edu/das/das2Server?dataset=das2_1/cluster/wbd/r_wbd&start_time=2007-04-17T08:40Z&end_time=2007-04-17T08:50Z&spacecraft=c1&mode=DSN&antenna=Any&frequencyOffset=Any&fftSize=1024>
}}

Fails to use log for z-axis: {{ Launch2 |
uri=vap+das2server:<http://www-wbd.physics.uiowa.edu/das/das2Server?dataset=das2_1/cluster/wbd/r_wbd&start_time=2007-04-17T08:40Z&end_time=2007-04-17T08:50Z&spacecraft=c1&mode=DSN&antenna=Ey&frequencyOffset=Any&fftSize=1024>
}}

# CDF

{{ Launch2 |
uri=<http://cdaweb.gsfc.nasa.gov/istp_public/data/canopus/mari_mag/1994/cn_k0_mari_19940122_v01.cdf?Epoch>}}

{{ Launch2 |
uri=<http://cdaweb.gsfc.nasa.gov/istp_public/data/canopus/bars/%Y/cn_k0_bars_%Y%m%d_v>...cdf?E\_vel\&timerange=1993-01-02+through+1993-01-14}}

{{ Launch2 |
uri=<ftp://cdaweb.gsfc.nasa.gov/pub/istp/imp8/mag_15sec/1973/i8_15sec_mag_19731030_v02.cdf>}}

No data is drawn: {{ Launch2 |
uri=vap:<ftp://cdaweb.gsfc.nasa.gov/pub/istp/themis/tha/l2/fgm/2007/tha_l2_fgm_20070224_v01.cdf?tha_fgh_gse>}}

IndexOutOfBoundsException: {{ Launch2 |
uri=<http://cdaweb.gsfc.nasa.gov/istp_public/data/cluster/c2/pp/cis/2003/c2_pp_cis_20030104_v02.cdf?N_p__C2_PP_CIS>}}

Suspect problem identifying valid data: {{ Launch2 |
uri=<http://cdaweb.gsfc.nasa.gov/istp_public/data/cluster/c2/pp/fgm/2003/c2_pp_fgm_20030114_v01.cdf?Epoch__C2_PP_FGM>}}

Fails to guess cadence: {{ Launch2 |
uri=<ftp://cdaweb.gsfc.nasa.gov/pub/istp/imp8/mag_15sec/2000/i8_15sec_mag_20000101_v02.cdf?F1_Average_B_15s>}}

Strange message:

`java.lang.RuntimeException: java.lang.IllegalArgumentException: not supported: Lo E PD`  
`at org.virbo.autoplot.ApplicationModel.resetDataSetSourceURL(ApplicationModel.java:249)`

{{ Launch2 |
uri=<ftp://cdaweb.gsfc.nasa.gov/pub/istp/lanl/97_spa/2005/l7_k0_spa_20050405_v01.cdf?spa_p_dens>}}
This is described in bug
<https://sourceforge.net/tracker2/index.php?func=detail&aid=2620088&group_id=199733&atid=970682>.

No data is displayed: {{ Launch2 |
uri=vap:<ftp://cdaweb.gsfc.nasa.gov/pub/istp/themis/tha/l2/fgm/2007/tha_l2_fgm_20070224_v01.cdf?tha_fgh_gse>}}
This is corrected and will be released soon. The problem was the
"COMPONENT\_0" conventions used for Themis lead to the timetags being
interpretted as invalid.

Vectors plotted as spectrogram: {{ Launch2 |
uri=<ftp://cdaweb.gsfc.nasa.gov/pub/istp/geotail/def_or/1995/ge_or_def_19950101_v02.cdf?GSE_POS>}}

Works fine, but nicely demonstrates AutoHistogram's robust statistics
and the potential to indentify fill values automatically: {{ Launch2 |
uri=<ftp://cdaweb.gsfc.nasa.gov/pub/istp/geotail/mgf/1998/ge_k0_mgf_19980102_v01.cdf?IB>}}

# OpenDAP

Rank 2 spectrogram over OpenDAP: {{ Launch2 |
uri=<http://cdaweb.gsfc.nasa.gov/cgi-bin/opendap/nph-dods/istp_public/data/polar/hyd_h0/2002/po_h0_hyd_20020110_v01.cdf.html?ELECTRON_DIFFERENTIAL_ENERGY_FLUX>}}

# FITS

This fails because negative CADENCE and MONOTONIC=true. {{ Launch2 |
uri=vap:<http://www.astro.princeton.edu/~frei/Gcat_htm/Catalog/Fits/n4013_lR.fits>}}

# ASCII

Autoplot doesn't download this URL: {{ Launch2 |
uri=vap+bin:<ftp://ftp.nmh.ac.uk/wdc/obsdata/hourval/single_year/1909/clh1909.wdc>}}

java.lang.IllegalArgumentException: unable to identify time format for
1990-11-05T16:31:00.000Z {{ Launch2 |
uri=vap+dat:<http://www.igpp.ucla.edu/cache2/GOMA_3001/DATA/SUMMARY/E1_SUMM_GSE_GSM.TAB?timeFormat=ISO8601&column=field1>}}

This demonstrates fractional day of year: {{ Launch2 |
uri=vap+dat:<http://wind.nasa.gov/swe_apbimax/wi_swe_fc_apbimax.1995005.txt?comment=;&column=21&timeFormat=$Y+$j&time=field0>}}

Fill string is recognized, -1e31 is inserted, but this is not marked as
fill: {{ Launch2 |
uri=vap+dat:<http://goes.ngdc.noaa.gov/data/avg/$Y/A105$y$m.TXT?skip=23&timeFormat=$y$m$d+$H$M&column=E1&time=YYMMDD&fill=32700&timerange=Dec+2004>}}

I'd expect this to read in the column as a rank 1 dataset: {{ Launch2 |
uri=<http://www-pw.physics.uiowa.edu/~jbf/L1times.2.dat?fixedColumns=29-35>}}

And this gets a null pointer exception in AsciiParser.getFieldIndex line
1024: {{ Launch2 |
uri=<http://www-pw.physics.uiowa.edu/~jbf/L1times.2.dat?fixedColumns=0-24,29-35&column=field1>}}

Very large with $b and ${skip}: {{ Launch2 |
uri=<http://vho.nasa.gov/mission/soho/celias_pm_30sec/2003.txt>}}

High resolution OMNI data: {{ Launch2 |
uri=vap+dat:<ftp://nssdcftp.gsfc.nasa.gov/spacecraft_data/omni/high_res_omni/monthly_1min/omni_min200101.asc?time=field0&column=field14&timeFormat=$Y+$j+$H+$M&validMax=9999>}}

Comment parameter used: {{ Launch2 |
uri=<http://wind.nasa.gov/swe_apbimax/wi_swe_fc_apbimax.2001017.txt?column=field2&comment=;&time=field0&timeFormat=$Y+$j>}}

"Value must not be negative". No feedback on line number: {{ Launch2 |
uri=vap:<http://vho.nasa.gov/mission/soho/celias_pm_30sec/1998.txt?time=YY&column=GSE_X&timeFormat=$y+$b+$d+$(ignore):$H:$M:$S>}}

From VHO: {{ Launch2 |
uri=<ftp://nis-ftp.lanl.gov/pub/projects/genesis/3dmom/gim-3dl2-2002-01_v02.txt?skip=68&time=field0&timeFormat=$Y+$j+$H+$M+$S&column=field8&fill=-9999.0>}}

# Excel

German umlaut is not handled when creating column name: {{ Launch2 |
uri=<file:/media/mini/data.backup/examples/xls/2.25_carbopol_summary.xls?firstRow=51&sheet=125>
um hifreq 2\&depend0=Frequenz\&column=Komplexe\_Viskosität}}

# Aggregation

Here is aggregation with CDF subsampling. This has issues. It doesn't
reload when I change the parameter. {{ Launch2 |
uri=<http://cdaweb.gsfc.nasa.gov/istp_public/data/omni/hro_5min/%Y/omni_hro_5min_%Y%m%d_v>...cdf?HR\[::100\]\&timerange=1995+to+2000}}

No feedback when using with openDAP: {{ Launch2 |
uri=<http://cdaweb.gsfc.nasa.gov/cgi-bin/opendap/nph-dods/istp_public/data/polar/vis/%Y/po_k0_vis_%Y%m%d_v>...cdf.html?Epoch\&timerange=2001}}

Fails to Identify as aggregation: {{ Launch2 |
uri=vap+txt:<file:///opt/project/galileo/data/lrsudr/g7/eden/pws$y$j.data?timeRange=1997-049>}}

Though "Dec 2004" is requested, "Nov 2004 through Jan 2005" is loaded:
{{ Launch2 |
uri=vap+dat:<http://goes.ngdc.noaa.gov/data/avg/$Y/A105$y$m.TXT?skip=23&timeFormat=$y$m$d+$H$M&column=E1&time=YYMMDD&fill=32700&timerange=Dec+2004>}}

# File System Completions

fails: {{ Launch2 |
uri=<ftp://ftp.nmh.ac.uk/wdc/obsdata/hourval/single_year/>}}

fails to read zip, but does read locally: {{ Launch2 |
uri=<http://www-pw.physics.uiowa.edu/helios/data1/data/average/a7510-12.zip/av751229.dat?depend0=field0&rank2=1>:}}

perhaps one day this will work: {{ Launch2 |
uri=<http://www-pw.physics.uiowa.edu/helios/data1/data/average/a$y$m->...zip/av$y$m$d.dat?rank2=1:\&time=field0\&timerange=1975-oct}}

# Data Source Completions

# URIs with difficult CADENCE

The Time parameter is irregular: {{ Launch2 |
uri=vap:<file:///media/mini/data.backup/examples/xls/2008-lion%20and%20tiger%20summary.xls?sheet=Samantha+tiger+lp+lofreq&column=Elastic_Modulus&firstRow=53&depend0=Time>}}

# Issues with URIs

It would be nice to support plus notation with excel spreadsheets. Also,
this shows an issue with the excel data source which {{ Launch2 |
uri=<file:///Documents%20and%20Settings/sklemuk/Desktop/UCSF%20Voice%20Conference%202008/Product%20Summary.xls?sheet=nist%20lo&column=H>}}

This works: {{ Launch2 |
uri=<file:///c:/Documents+and+Settings/jbf/Desktop/Product+Summary.xls?sheet=nist+lo&column=H>}}

` `<message>`go `<file:///Documents%20and%20Settings/sklemuk/Desktop/UCSF%20Voice%20Conference%202008/Product%20Summary.xls?sheet=nist%20lo&column=H></message>  
` `<message>`java.lang.NullPointerException`  
`   at org.virbo.excel.ExcelSpreadsheetDataSource.getDataSet(ExcelSpreadsheetDataSource.java:89)`  
`   at org.virbo.autoplot.ApplicationModel.loadDataSet(ApplicationModel.java:1322)`  
`   at org.virbo.autoplot.ApplicationModel.updateImmediately(ApplicationModel.java:1260)`  
`   at org.virbo.autoplot.ApplicationModel.access$600(ApplicationModel.java:112)`  
`   at org.virbo.autoplot.ApplicationModel$8.run(ApplicationModel.java:1293)`  
`   at org.das2.system.RequestProcessor$Runner.run(RequestProcessor.java:201)`  
`   at java.lang.Thread.run(Unknown Source)`

# Miscellaneous URIs

Demonstrates problem with AutoHistogram: {{ Launch2 |
uri=<http://goes.ngdc.noaa.gov/data/avg/2004/A1050402.TXT>}}

# VAPs in the wild

VAP files are Autoplot configuration files, an xml version of the DOM
tree. I'd expect these to be very fragile right now, but I'll try to
support them:

From VMO, the data here contains the search date, but the time axis is
not properly located: {{ Launch2 |
uri=<http://vmo.nasa.gov/vxotmp/vap/VMO/Granule/OMNI/PT1H/omni2_1994.vap>}}
