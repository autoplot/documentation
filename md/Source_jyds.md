
### Jython Files (jyds)

Jython scripts can be used to create new datasets by combining other
datasets. See also [https://autoplot.org/scripting
scripting](https://autoplot.org/scripting_scripting "wikilink").

  - extension: .jyds
  - Example URLs:
      - Plot the difference between two images:
        [21 https://autoplot.org/data/imageDiff.jyds](https://autoplot.org/data/imageDiff.jyds)
      - Read a complicated ASCII file and plot the result:
        [22 https://github.com/autoplot/dev/blob/master/demos/jyds/wdc_kp_ap.jyds](https://github.com/autoplot/dev/blob/master/demos/jyds/wdc_kp_ap.jyds)
      - Demonstrates time series browse:
        [24 https://autoplot.org/data/tsbDemo.jyds](https://autoplot.org/data/tsbDemo.jyds)
  - Parameters:
      - <name>=<expr> defines parameters for use within the script.
        Scripts use getParam method to get method parameters.
      - <expr> after running the script, this expr is evaluated and
        plotted. The default expression is "data".

Example Script (/home/user/script.jyds):

```
amplitude= getParam( 'amp', 1.0, 'the amplitude of the waveform' )
result= amplitude * sin( linspace( 0, PI*2, 100 ) )
```
This is called like so:

```
/home/user/script.jyds?amp=2
```
An editor is provided that will allow editing of the script, and when
getParam( name, default, description, \[ constraints \] ) is used, an
entry form is generated for the parameters.

Note if the parameter "timerange" is used, then Autoplot will call the
script with new time ranges as the time axis is adjusted.

URIs can also use the resourceURI part to point to a resource that is
parsed by the script, such as:

`vap+jyds:https://www.ngdc.noaa.gov/stp/space-weather/geomagnetic-data/INDICES/KP_AP/2018?script=https://github.com/autoplot/dev/blob/master/demos/jyds/wdc_kp_ap.jyds`

Here the "script=" switch points to the script. This is useful to define
a parser for a file type, which allows aggregation to be used:

`vap+jyds:https://www.ngdc.noaa.gov/stp/space-weather/geomagnetic-data/INDICES/KP_AP/$Y?script=https://github.com/autoplot/dev/blob/master/demos/jyds/wdc_kp_ap.jyds`

