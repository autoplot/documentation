The canvas layout can be stored for future use in a .vap file.  This is an xml file 
containing the plot and plot element configurations, and the URIs loaded to make 
the plot.  These product files are like a .doc file is to Microsoft Word, or 
an HTML file with .jpg references.  When all the data products are from public 
servers, the .vap file can be sent to collegues so that they can have a look at the 
same display.  Another common use is to have a public website to can share standard 
plot configurations with others.  

The .vap files are saved and loaded using the file menu.  If a .vap file name or URI
is entered in the address bar, it will be loaded the same way.  Often .vap files
are associated with the Autoplot application in the browser (this will happen automatically
for most installations), so that clicking on a .vap file URL will run Autoplot with the
configuration. 

.vaps can be tweaked when they are loaded as well.  For example, suppose you have a
.vap which loads data from several servers for a day.  It is common to tell Autoplot
to load this vap but for another day.  For example, if the vap file is 
http://autoplot.org/data/autoplot.vap then http://autoplot.org/data/autoplot.vap?timerange=2000-01-12
will load the same data but for 2000-01-12.  Note the File&raar;"Open Vap File" has 
a gui control to pick a different time.
