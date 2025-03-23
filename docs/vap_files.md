The canvas layout can be stored for future use in a .vap file.  This is an xml file 
containing the plot and plot element configurations, and the URIs loaded to make 
the plot.  These product files are like a .doc file is to Microsoft Word, or 
an HTML file with .jpg references.  When all the data products are from public 
servers, the .vap file can be sent to collegues so that they can have a look at the 
same display.  Another common use is to have a public website to share standard 
plot configurations with others.  

# loading .vap files
The .vap files are saved and loaded using the file menu.  If a .vap file name or URI
is entered in the address bar, it will be loaded the same way.  Often .vap files
are associated with the Autoplot application in the browser (this will happen automatically
for most installations), so that clicking on a .vap file URL will run Autoplot with the
configuration. 

.vaps can be tweaked when they are loaded as well.  For example, suppose you have a
.vap which loads data from several servers for a day.  It is common to tell Autoplot
to load this vap but for another day.  For example, if the vap file is 
http://autoplot.org/data/autoplot.vap then http://autoplot.org/data/autoplot.vap?timerange=2000-01-12
will load the same data but for 2000-01-12.  Note the File&rarr;"Open Vap File" has 
a gui control to pick a different time.

# saving .vap files
When saving a .vap file, you have the option to "embed the data" within the output.  
This writes not a .vap file, but a .zip file containing the .vap file and the data used
to make the plot.  The file will have a .vap.zip extension, which can then be used on the road 
without having to load the data again.  To load the data you can point at the 
vap file within the .zip, and Autoplot will pull out resources as needed.  (Any zip file
can be "mounted" and browsed as if it were a file system.)

Note that if you are plotting data from files which have been saved to your computer,
then the .vap will contain references to data that will only work on your computer.  This
is another case where it might be easier to share a .vap.zip file, because the local
data from your computer will be embedded within the file.


