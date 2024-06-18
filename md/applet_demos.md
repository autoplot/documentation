See also [applet\_guide](applet_guide.md "wikilink"), Video
[1](http://aurora.gmu.edu/autoplot-applet/dist-packed/OnePanelApplet-bgloadAll-movie.html),
and [\#Spectrogram](#spectrogram "wikilink")

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



<html>

`&nbsp;&nbsp;&nbsp;`&lt;applet  width=&quot;100%&quot; height=&quot;500px&quot; id=&quot;applet2&quot; 
             code="org.virbo.autoplot.AutoplotApplet"
             codebase="http://aurora.gmu.edu/autoplot-applet/dist-packed/lib/packed"
         archive="AutoplotAppletAll.jar.pack.gz">  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;dataSetURL&quot; value=&quot;tsds.http://timeseries.org/get.cgi?StartDate=19980101&amp;EndDate=20081231&amp;ext=bin&amp;out=tsml&amp;ppd=1&amp;param1=NGDC_NOAA15_SEM2-33-v0&quot; /&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;codebase_lookup&quot; value=&quot;false&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;column&quot; value=&quot;5em,100%-5em&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;font&quot; value=&quot;sans-16&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;row&quot; value=&quot;3em,100%-3em&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;renderType&quot; value=&quot;fill_to_zero&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;color&quot; value=&quot;#ffffff&quot;&gt;

<param name="plot.title" value="Same as bottom panel but daily averaged">

`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;fillColor&quot; value=&quot;#aaaaff&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;foregroundColor&quot; value=&quot;#ffffff&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;backgroundColor&quot; value=&quot;#000000&quot;&gt;  
```
     `<param name="statusCallback" value="appletStatus">`;
```
`&nbsp;&nbsp;&nbsp;`&lt;/applet&gt;

`&nbsp;&nbsp;`&lt;applet  width=&quot;100%&quot; height=&quot;500px&quot; id=&quot;applet2&quot; 
             code="org.virbo.autoplot.AutoplotApplet"
             codebase="http://aurora.gmu.edu/autoplot-applet/dist-packed/lib/packed"
         archive="AutoplotAppletAll.jar.pack.gz">  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;dataSetURL&quot; value=&quot;tsds.http://timeseries.org/get.cgi?StartDate=19980101&amp;EndDate=20081231&amp;ext=bin&amp;out=tsml&amp;ppd=86400&amp;param1=NGDC_NOAA15_SEM2-33-v0&quot; /&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;codebase_lookup&quot; value=&quot;false&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;column&quot; value=&quot;5em,100%-5em&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;font&quot; value=&quot;sans-16&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;row&quot; value=&quot;3em,100%-3em&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;renderType&quot; value=&quot;fill_to_zero&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;color&quot; value=&quot;#ffffff&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;fillColor&quot; value=&quot;#aaaaff&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;foregroundColor&quot; value=&quot;#ffffff&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;backgroundColor&quot; value=&quot;#000000&quot;&gt;  
```
     `<param name="statusCallback" value="appletStatus">`;
```
`&nbsp;&nbsp;&nbsp;`&lt;/applet&gt;

</body>

</html>



# Answer

Spikes appear in the daily-averaged data on days when there were very
few data valid data points and the valid data points are mostly positive
or negative.

# Spectrogram



<html>

<head>

</head>

<body>

`&nbsp;&nbsp;&nbsp;`&lt;applet  width=&quot;100%&quot; height=&quot;400px&quot; id=&quot;applet0&quot; 
             code="org.virbo.autoplot.AutoplotApplet"
             codebase="http://autoplot.org/applet/20090820/"
         archive="AutoplotAppletAll.jar.pack.gz">  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;dataSetURL&quot; value=&quot;vap+tsds:http://timeseries.org/get3.cgi?StartDate=19930101&amp;EndDate=20031231&amp;ppd=1&amp;ext=bin&amp;out=ncml&amp;param1=Kanekal_SAMPEX_elo_1hour-1-v0&quot; /&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;codebase_lookup&quot; value=&quot;false&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;font&quot; value=&quot;sans-14&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;row&quot; value=&quot;3em,100%-4em&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;column&quot; value=&quot;5em,100%-8em&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;plot.yaxis.label&quot; value=&quot;10 times L-shell&quot;&gt;

<param name="plot.title" value="SAMPEX ELO Flux (2-6 MeV electrons)">
<param name="plot.zaxis.label" value="#/str-s-cm^2-MeV">

`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;renderType&quot; value=&quot;spectrogram&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;color&quot; value=&quot;#ffffff&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;fillColor&quot; value=&quot;#aaaaff&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;foregroundColor&quot; value=&quot;#ffffff&quot;&gt;  
`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&lt;param name=&quot;backgroundColor&quot; value=&quot;#000000&quot;&gt;  
```
     `<param name="statusCallback" value="appletStatus">`;
```
`&nbsp;&nbsp;&nbsp;`&lt;/applet&gt;

</html>



