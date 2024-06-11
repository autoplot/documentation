# Purpose

Autoplot's testing has a feature where it will scrape a web page looking
for Autoplot URIs and vap files, and will test them regularly. Add links
to your products to this page, and they will be tested regularly.

You must prefix Autoplot URIs with
"<http://autoplot.org/autoplot.jnlp>?" for the test to use the address,
and any vap reference is tested.

Results from this test are visible at
<http://jfaden.net/jenkins/job/autoplot-test147/lastSuccessfulBuild/artifact/>.

# Jeremy's Links

  - <http://autoplot.org/autoplot.jnlp?http://jfaden.net/~jbf/autoplot/vap/geothermal20130106.vap>

<!-- end list -->

  - <http://autoplot.org/autoplot.jnlp?http://jfaden.net/~jbf/autoplot/vap/c3_pp_cis.vap>
  - <http://autoplot.org/autoplot.jnlp?http://jfaden.net/~jbf/autoplot/vap/demos/polar/hydraVis.vap>
  - <http://autoplot.org/autoplot.jnlp?http://jfaden.net/~jbf/autoplot/vap/demos/medianFilter.vap>
  - <http://autoplot.org/autoplot.jnlp?http://jfaden.net/~jbf/autoplot/vap/demos/tsbFun.vap>

## CSV ASCII

  - <http://www-pw.physics.uiowa.edu/pds/GOPW_2001/DATA/12_EUROPA/FPE_1997_12_16_V01.CSV?delim=;&column=field20&depend0=field0>

## NetCDF

<http://www-pw.physics.uiowa.edu/~jbf/autoplot/data/examples/nc/randomNc4.vap>

## Render Types

<http://autoplot.org/autoplot.jnlp?vap+cdaweb:ds=OMNI2_H0_MRG1HR&id=DST1800&timerange=2016-09-29+08:32+to+2016-10-30+08:32&x=Epoch&y=KP>

## Cadence Tests

<http://jfaden.net/~jbf/autoplot/tests/test147/cadenceBreak20180807.qds>

## inline URIs

Inline URIs contain data without any more data loading.

  - <http://autoplot.org/autoplot.jnlp?vap+inline:4,3,4,3>
  - <http://autoplot.org/autoplot.jnlp?vap+inline:1,4;2,3;3,4;4,3>
  - <http://autoplot.org/autoplot.jnlp?vap+inline:1.6e2,4.6e4;2.6e2,3.6e4;3.6e2,4.6e4;4.6e2,3.6e4>

Highlite a region in time. Note by default there is some transparency:

  - <http://autoplot.org/autoplot.jnlp?vap+inline:ds=createEvent>('2014-01-01+1:04+to+1:05',0x000000,'error')\&ds
  - <http://autoplot.org/autoplot.jnlp?vap+inline:2013-044,5kg;2013-045,6kg;2013-046,7kg;2013-047,8kg>

# TSDS Links

(Commented out, edit this page to change)
