Inline URIs are ones which contain data or instructions for loading data.  For example,

 vap+inline:1,2,3,4,5,1,2,3,4,5,1,2,3,4,5
 
will plot the numbers three times to make a sawtooth.  
 
 vap+inline:2021-07-18T02:18Z 

is just an instant in time, useful for drawing a vertical line to mark an event.
This can also contain bits of Jython code to load and manipulate data.  Here,

 vap+inline:ds=getDataSet('vap+cdaweb:ds=OMNI2_H0_MRG1HR&id=THETA-V1800')&toRadians(ds)&timerange=Oct+2016
 
loads angle data in degrees and converts it to radians.
 
There's an editor to assist in creating vap+inline URIs.  Note that the last tab is the "mash up" GUI
which allows you to graphically combine data.

<img src='../image/mashup.png' width=150>
