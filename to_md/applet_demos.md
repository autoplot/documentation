See also [applet\_guide](applet_guide "wikilink"), Video
[1](http://aurora.gmu.edu/autoplot-applet/dist-packed/OnePanelApplet-bgloadAll-movie.html),
and [\#Spectrogram](#Spectrogram "wikilink")

# Time Series Browse

Example use of time series browse server. The server is set up to allow
the user to interactively browse long time ranges of very high
resolution data. The bottom panel shows a 1-second time series over 11
years. To zoom, use your mouse to draw a box around some data.

As you zoom in on the bottom panel, you will be able to see the
mechanism that allows this \~ 365x86400x11 point (\~ 2.5 GB if numbers
are represented as 8-byte floats) time series to be viewed
interactively. The plotting program recognizes that there are only a
certain number of pixels available to render the plot on the user's
screen. Instead of requesting all of the data points and then rendering
them, the plotting program simulates what would be rendered on the
screen by requesting fewer data points from the server. The server is
set up to allow fast responses to the required data operations (min,
max, and average in a time window) needed to support this type of data
request.

Top panel: Daily averages of 1-second data.

Bottom panel: Unaveraged data.

Use the box-zoom feature of Autoplot to figure out why the
daily-averaged data in the top panel has spikes whereas the full
resolution does not show spikes. Answer below.

<addhtml>

<html>

`   `<applet  width="100%" height="500px" id="applet2" 
             code="org.virbo.autoplot.AutoplotApplet"
             codebase="http://aurora.gmu.edu/autoplot-applet/dist-packed/lib/packed"
         archive="AutoplotAppletAll.jar.pack.gz">  
`     `<param name="dataSetURL" value="tsds.http://timeseries.org/get.cgi?StartDate=19980101&EndDate=20081231&ext=bin&out=tsml&ppd=1&param1=NGDC_NOAA15_SEM2-33-v0" />  
`     `<param name="codebase_lookup" value="false">  
`     `<param name="column" value="5em,100%-5em">  
`     `<param name="font" value="sans-16">  
`     `<param name="row" value="3em,100%-3em">  
`     `<param name="renderType" value="fill_to_zero">  
`     `<param name="color" value="#ffffff">

<param name="plot.title" value="Same as bottom panel but daily averaged">

`     `<param name="fillColor" value="#aaaaff">  
`     `<param name="foregroundColor" value="#ffffff">  
`     `<param name="backgroundColor" value="#000000">  
`     `<param name="statusCallback" value="appletStatus">`;`  
`   `</applet>

`  `<applet  width="100%" height="500px" id="applet2" 
             code="org.virbo.autoplot.AutoplotApplet"
             codebase="http://aurora.gmu.edu/autoplot-applet/dist-packed/lib/packed"
         archive="AutoplotAppletAll.jar.pack.gz">  
`     `<param name="dataSetURL" value="tsds.http://timeseries.org/get.cgi?StartDate=19980101&EndDate=20081231&ext=bin&out=tsml&ppd=86400&param1=NGDC_NOAA15_SEM2-33-v0" />  
`     `<param name="codebase_lookup" value="false">  
`     `<param name="column" value="5em,100%-5em">  
`     `<param name="font" value="sans-16">  
`     `<param name="row" value="3em,100%-3em">  
`     `<param name="renderType" value="fill_to_zero">  
`     `<param name="color" value="#ffffff">  
`     `<param name="fillColor" value="#aaaaff">  
`     `<param name="foregroundColor" value="#ffffff">  
`     `<param name="backgroundColor" value="#000000">  
`     `<param name="statusCallback" value="appletStatus">`;`  
`   `</applet>

</body>

</html>

</addhtml>

# Answer

Spikes appear in the daily-averaged data on days when there were very
few data valid data points and the valid data points are mostly positive
or negative.

# Spectrogram

<addhtml id="3">

<html>

<head>

</head>

<body>

`   `<applet  width="100%" height="400px" id="applet0" 
             code="org.virbo.autoplot.AutoplotApplet"
             codebase="http://autoplot.org/applet/20090820/"
         archive="AutoplotAppletAll.jar.pack.gz">  
`     `<param name="dataSetURL" value="vap+tsds:http://timeseries.org/get3.cgi?StartDate=19930101&EndDate=20031231&ppd=1&ext=bin&out=ncml&param1=Kanekal_SAMPEX_elo_1hour-1-v0" />  
`     `<param name="codebase_lookup" value="false">  
`     `<param name="font" value="sans-14">  
`     `<param name="row" value="3em,100%-4em">  
`     `<param name="column" value="5em,100%-8em">  
`     `<param name="plot.yaxis.label" value="10 times L-shell">

<param name="plot.title" value="SAMPEX ELO Flux (2-6 MeV electrons)">
<param name="plot.zaxis.label" value="#/str-s-cm^2-MeV">

`     `<param name="renderType" value="spectrogram">  
`     `<param name="color" value="#ffffff">  
`     `<param name="fillColor" value="#aaaaff">  
`     `<param name="foregroundColor" value="#ffffff">  
`     `<param name="backgroundColor" value="#000000">  
`     `<param name="statusCallback" value="appletStatus">`;`  
`   `</applet>

</html>

</addhtml>
