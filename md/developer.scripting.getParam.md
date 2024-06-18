Purpose: Discuss how getParam is used to create the GUIs, and how this
will be improved.

Audience: Autoplot developers and clients wanting to understand how
getParam is used to create GUIs.

# Current State

  - scrapes through the code looking for getParam lines, and these are
    parsed to get input parameters.

# Proposed new solution

Automatically simplify code to make it executable within 300 ms. This is
a describable process. The simplified code is run, and getParam calls
trigger the addition of GUI elements. See JythonUtil.removeSideEffects,
JythonUtil.getGetParams

# Example Test Codes

## Simplest that is currently working

```
resourceURI= getParam( 'resourceURI', '`<ftp://satdat.ngdc.noaa.gov/sem/poes/data/raw/ngdc/2013/noaa19/poes_n19_20130409_raw.nc>`', 'example file to load' )
parm= getParam( 'parm', 'mep_pro_tel0_cps_p3', 'parameter to load', [  'alt', 'lat', 'lon' )
```
## Here's the problem

```
resourceURI= getParam( 'resourceURI', '`<ftp://satdat.ngdc.noaa.gov/sem/poes/data/raw/ngdc/2013/noaa19/poes_n19_20130409_raw.nc>`', 'example file to load' )
parm= getParam( 'parm', 'mep_pro_tel0_cps_p3', 'parameter to load', [  'alt', 'lat', 'lon', 'mep_pro_tel0_cps_p1', 'mep_pro_tel0_cps_p2', 'mep_pro_tel0_cps_p3', 'mep_pro_tel0_cps_p4', 'mep_pro_tel0_cps_p5', 'mep_pro_tel0_cps_p6',  'mep_pro_tel90_cps_p1', 'mep_pro_tel90_cps_p2', 'mep_pro_tel90_cps_p3', 'mep_pro_tel90_cps_p4', 'mep_pro_tel90_cps_p5', 'mep_pro_tel90_cps_p6', 'mep_ele_tel0_cps_e1', 'mep_ele_tel0_cps_e2', 'mep_ele_tel0_cps_e3', 'mep_ele_tel90_cps_e1',  'mep_ele_tel90_cps_e2',  'mep_ele_tel90_cps_e3',   'mep_omni_cps_p6', 'mep_omni_cps_p7', 'mep_omni_cps_p8',  'mep_omni_cps_p9' ] )
```
## simple case resolves variables

```
parms= [ 'alt', 'lat', 'lon']
parm= getParam( 'parm', 'alt', 'parameter to load', params )
```
## continuation supported

```
parms= [ \
 'alt', \
 'lat', \
 'lon']
parm= getParam( 'parm', 'alt', 'parameter to load', params )
```
## branches supported

```
sp= getParam( 'species', 'ele', 'protons or electron species', ['ele','pro','omni'] )

if ( sp!='omni' ):
   t90= getParam( 'angle', 'tel0', 'angle', [ 'tel0', 'tel90' ] ) 

if ( sp=='ele' ):
   ch= getParam( 'ch', 1, 'channel to plot', [ 1,2,3 ] )
elif ( sp=='omni' ):
   ch= getParam( 'ch', 1, 'channel to plot', [ 6,7,8,9 ] )
else:
   ch= getParam( 'ch', 1, 'channel to plot', [ 1,2,3,4,5,6 ] )
```
# See Also

<https://sourceforge.net/p/autoplot/feature-requests/320/>

