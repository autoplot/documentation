# <span id="intro"></span> Introduction

Autoplot is an interactive browser for data on the web. In the same way
that you browse content stored in HTML, JPEG, and PNG files on the web,
Autoplot allows you to interactively browse data stored in CDF, netCDF,
ASCII, and many more data file formats. You can also interact with
several types of data servers, including HAPI servers, Das2Servers, and
CDAWeb.

Autoplot tries to create a sensible plot given a URL or a name of a data
file on your computer so you can quickly get your data from one or more
data files to a presentation- or publication-ready graphic within
minutes. Plots are zoomable and annotations are easily adjusted.

Feel free to ask questions on the discussion group
[mailto:autoplot@groups.google.com](mailto:autoplot@groups.google.com)
if you need assistance, or browse the archive there at
<https://groups.google.com/forum/#!forum/autoplot>.

This document is intended to introduce scientists to the software and go
over its features. Autoplot is intended to be easy to use for new
scientists, but quite capable and suitable for those who wish to use it
for most of their science products. This document tries to be
comprehensive, but one needn't understand later sections to use the
software productively.

# Installation

Autoplot can be found at <https://autoplot.org/latest/>. The "Start
Autoplot" link brings up a download page for the latest release. The
software is available separately for each type of computer. A
"single-jar" version is available for those who already have Java on
their machines. Development releases with new features and bug fixes are
made about once a week. Though each release is tested using a suite of
automatic tests, these development releases may contain new bugs which
could interfere use, and should not be used in production environments.
Production-quality releases have been more thoroughly tested, and are
made monthly.

WebStart has been deprecated by Oracle and other methods should be used.

On Macs, a .dmg file which contains the Autoplot release and a bundled
version of the Java Runtime Environment is used. This 98Mb download is
signed and should run on any newer Mac. (The Install4J software used to
build each release supports both Intel and M1 Macs.)

Windows machines can use the "exe" release. For now you will need to
acknowledge the untrusted signature and "run anyway" to use it. Trust is
based on the number of people running it, and Microsoft does not trust
the certificate at this time.

On Linux machines, the single-jar release can be used as well. We've
prepended a bash launch script at its beginning so that if the
downloaded jar's executable bit is set, it can be launched like any
other executable file. There are also .rpm and .dmg releases which are
available, but the .rpm version has not been thoroughly tested.

# Getting Started

Once Autoplot is running, you can enter the name of a CDF file in the
address bar or try out the demonstration bookmarks. The name in the
address bar is called an "Autoplot URI" and all data in Autoplot is
identified using URIs. This is typically the name of a data file and
additional controls needed to read in the data. For example,
<https://autoplot.org/data/autoplot.cdf?BGSM> refers to the CDF file on a
website, and the BGSM parameter which will be found inside. Autoplot
will download the CDF file to its cache, load the parameter from the
file, and plot the data.

## Bookmarks

Like a web browser, Autoplot has a list of bookmarks that helps to
locate data files and servers. Autoplot is installed with a list of
"Demo Bookmarks" which provide a few initial places where data is found
so you can see that things are working and play with Autoplot right
away. For example, from the menu bar select
&quot;\[Menubar\]&rarr;Bookmarks&rarr;Demos&rarr;Demo 1&quot;, and Autoplot will plot data
from CDAWeb at NASA/Goddard.

Some other bookmarks:

  - Demo 2: Spectrograms from the POLAR/Hydra instrument.
  - Demo 5: Data from a CDF file
  - Demo 6: Use SPASE record for metadata, file reference within for
    data.
  - Demo 9: Read data from ASCII file.

## Navigation

Autoplot uses the Das2 graphics library for displaying graphics. These
are Java codes for rendering line plots, spectrograms, and other
displays on "live" axes. You can draw a box around data to zoom in, use
the middle mouse button to pan the data, and the mouse wheel to zoom in
or out. Similarly, a spectrogram's color bar can be adjusted using mouse
actions while hovering over it.

Undo and redo actions are attached to the ctrl-Z and ctrl-Y keys
(command &#8984;-Z and &#8984;-Y for Macs).


[![YouTube video player](https://img.youtube.com/vi/PcB3feFYb_4/0.jpg)](http://www.youtube.com/watch?v=PcB3feFYb_4 "YouTube video player")


## Address Bar and URIs

![addressbar.png](addressbar.png "addressbar.png")

  
In the address bar at the top of the GUI you can enter the name of a
supported [file format](#formats-read "wikilink") in a data address. If
the data address is a URL, HTTP or FTP is used to download the file to a
local directory within the folder "autoplot\_data." A fully-qualified
address will contain both the location of the file and additional
arguments to read in the data. For example, it may contain a CDF
filename followed by `?BGSM` to indicate the variable to plot. Together
these form a "URI", which is the precise address of the data. Autoplot
will help build URIs by providing graphical editors to pick the data.
Autoplot URIs are designed to give a concise way to refer to data: put a
data file in a web location, and send the URI to a colleague so they can
look at it too.

The green "Play" button will tell Autoplot to load this URI. Autoplot
will decide if the URI is partial, needing more information before it
can be plotted, and if it is, an editor panel GUI will be shown, so that
the URI can be completed. For example, when a CDF file name is entered,
Autoplot rejects the URI because the parameter to plot is needed (for
example, ...cdf?BSM). Use the GUI to complete the data selection and hit
its play button to try again. To see this, compare what happens when you
enter `https://autoplot.org/data/autoplot.cdf` in the address bar versus
`https://autoplot.org/data/autoplot.cdf?BGSM`.

The folder/magnifier button, called the "Inspect" button, will return to
the editor GUI.

Note that if you enter TAB when the address bar is selected, possible
completions will appear if they exist. This provides a quick way to
finish URIs as well.

The tiny green and blue buttons to the left of the address bar select
which of two controls is shown. The blue button shows the current time
range, which is useful when navigating long time series of data. The
green button will swap back to the address bar. Autoplot has a basic and
expert modes. In basic mode, the address bar is not visible and is
replaced with a controller for the time range. Control-T will switch to
the time range, and Control-D will switch to the data URI.

Sometimes Autoplot URIs do not refer to files. They still locate data,
but one of Autoplot's plug-ins interprets the address. For example,
`vap+cdaweb:ds=CRRES_H0_MEA&id=FLUX&timerange=1991-10-09` points to data
from the CRRES satellite provided via CDAWeb at NASA/Goddard and
`vap+audiosystem:spec=512&len=2.5` samples from the local machine's
soundsystem for 2.5 seconds.

## Example URIs: Data Files

When a data file name is entered into Autoplot, it will download the
file to make it local, and the file is opened using special readers for
the file type. CDF files and ASCII files are introduced now.

### CDF Files

A CDF URI is a web address (URL) of a CDF file, which can be a local
file (file:/tmp/myfile.cdf), and the name of a parameter to load. For
example, enter the URI into Autoplot:

<https://autoplot.org/data/autoplot.cdf?BGSM>

Entering this URI will open up the file using the CDF data source,
reading the parameter identified by "BGSM." This data is loaded into
Autoplot's internal data representation model, QDataSet, and then
displayed.

Pressing the inspect button (hourglass/folder) will enter a GUI, called
a Data Source Editor, where graphical selection of parameter is made.
One can also make other selections, such as ignoring CDF ISTP metadata,
keyword constraints to help identify parameters, and subsetting the data
using another parameter.

Note the URI given above is more formally stated as:

`vap+cdf:https://autoplot.org/data/autoplot.cdf?BGSM`

and when the vap+cdf prefix (scheme) is missing, the file extension is
used to infer the data source to use.

### ASCII Files

Tables of data in ASCII files have worked fine for many data products
for decades. Autoplot's ASCII table reader tries to utilize many forms
of these, splitting the ASCII file into records by line and then each
line is split on commas or tabs. This is a simplification of this and
many controls are provided and described below. But to get started, the
URI:

<https://cdaweb.gsfc.nasa.gov/pub/data/omni/low_res_omni/omni2_1972.dat?column=field17&timeFormat=$Y+$j+$H&time=field0&validMax=999>

breaks the lines of the file into fields using spaces. The keyword
parameters 'timeFormat' and 'time' group the three fields starting at
field0 (the first field) into a time tag treating the first column as
the year, second as the day of year, and third as hour of day. The
keyword validMax means any value over 999 should be considered invalid,
and a data break should be displayed.

## Example URIs: Data Servers

Some URIs refer to data coming from data servers rather than data files.

### CDAWeb

The CDAWeb at NASA/Goddard contains roughly 1400 data products from
around 40 different missions. Each data product corresponds to CDF files
spanning a mission, containing many plottable parameters. Instrument
teams produce CDF files and provide them to the CDAWeb which makes the
data available. An example URI is:

```
vap+cdaweb:ds=OMNI2_H0_MRG1HR&id=DST1800&timerange=Oct+2016
```
which means from the data identified as "OMNI2\_H0\_MRG1HR" plot the
parameter "DST1800", loading data to cover the time range "Oct 2016."

### HAPI Servers

HAPI is an open interface groups can implement to provide access to
their data. What makes HAPI unique is that any group can set up this
API, which has been developed by a committee of heliophysics data
providers. HAPI URIs look like:

`vap+hapi:https://cdaweb.gsfc.nasa.gov/hapi?id=AC_K0_SWE&parameters=Np,Vp&timerange=2023-11-11`

which says with the HAPI server located at
<https://cdaweb.gsfc.nasa.gov/hapi>, from the dataset AC\_K0\_SWE, load
the parameters Np and Vp. Any group can set up a HAPI server using the
documentation at
<https://github.com/hapi-server/data-specification/blob/master/hapi-2.1.0/HAPI-data-access-spec-2.1.0.md>

## Interaction

Basic user interactions include: **Left-click and drag** to zoom,
**Middle-click and drag** to pan, **Click on axis and drag** to
constrain interaction to one axis, **CTRL-Z / CTRL-Y** to undo/redo
changes, **Shift-Click** on plot to move plot box.

On a Mac, replace CTRL with CMD.

When pointer is over an axis

  - Drag axis: Middle Mouse Button Down and Drag
  - Zoom in/out: Mouse Wheel Rotate Up/Down
  - Pan: CTRL + Mouse Wheel Rotate Up/Down (Pans the axis. This allows
    for rapid scanning of the data.)

Other

  - Zoom: Left click + draw box
  - Pan: Middle click + drag
  - Reset Zoom: CTRL-R (on last plot clicked)
  - Reset Y zoom: CTRL-Shift-Y (on last plot clicked)
  - Reset X zoom: CTRL-Shift-X (on last plot clicked)
  - Move plot: Shift-Left click
  - Undo: CTRL-Z
  - Redo: CTRL-Y

More complex interaction with plots, including: mouse wheel control,
keyboard entry of axis range, context overview plots


[![YouTube video player](https://img.youtube.com/vi/Zo-QuK-KvUM/0.jpg)](http://www.youtube.com/watch?v=Zo-QuK-KvUM "YouTube video player")


Here are more videos, described below:
<https://youtube.com/@AutoplotDevelopers>

## Keyboard Shortcuts

  - Increase font size: CTRL-plus or CTRL-=
  - Decrease font size: CTRL-minus
  - Reset font size: CTRL-0
  - Show URI completions: TAB in address bar
      - Example: <https://autoplot.org/data/> + TAB will show a list of
        files in that directory
      - Example: <https://autoplot.org/data> + TAB will only show a list
        of files that you have accessed previously that match the string

## Key Menu Items

![menubar.png](menubar.png "menubar.png")  

### File &rarr; URI History

Autoplot keeps track of everything you have plotted in the file
HOME/autoplot\_data/bookmarks/history.txt. The URI history dialog is a
tool that tries to sort out the history and provides a search tool for
locating lost datasets. For example, if you know that you were plotting
a txt file, set the filter to "vap+txt" to see all the matching URIs.

### File &rarr; Export Data

Data can be exported to a number of data types. (In addition to reading
in data, some data sources will export data as well.) Only the current
selection is exported, so select the item to export, then File&rarr;Export
will bring up the dialog. From here, you can select the format (e.g. txt
for text file) and whether the original data, the processed data
(sliced, fftPower,etc), or just the visible data should be exported.

Note that while only the currently selected plot element's data is
exported, in the future you will have more options for exporting data.

### Options &rarr; Auto &rarr; Autoranging

Sometimes you want to look at different data on the same axis. This
provides a method that turns off Autoplot's autoranging. Note too that
the data tab will show the current focus' data URI. This URI can be
changed, loading new data without resetting the ranges (or
post-processing operations).

### Bookmarks

Bookmarks can be selected in two ways

1.  By selecting the `Bookmarks` menu item and then browsing a tree of
    bookmarks.
2.  By selecting `Bookmarks`&rarr;`Browse and Manage` and clicking on a
    bookmark.

Note that the second option allows you to view metadata associated with
a bookmark (if available) by clicking on the `Detailed Description`
button. In addition, the second option allows you to place a plot for a
given bookmark in a separate panel or on top of the current panel in
view.

### Tools &rarr; PNGWalk

The PNGWalk tool is an application for looking at series of images found
on websites. You can also run a pngwalk from the current product by
giving a timerange and a template for each filename (e.g. `$Y$m$d.png`).

For example:

1.  Enter `https://autoplot.org/data/versioning/data_$Y_$m_$d_v$v.qds` in
    the address bar
2.  This should bring up a GUI, because it doesn't have a timerange.
    Enter `2010-03-01`
3.  Select `Tools`&rarr;`Create PNG Walk`
    1.  Setting time format to `$Y$m$d_$H` will make hourly plots
    2.  Setting time range to `2010-03-01/2010-03-04`
4.  Note each png's span is based on the filename template you gave it.
    This should run the 72 images.

This works with any configuration where each plot knows how to get data
for any interval, such as with aggregation or the CDAWeb plugin.

See also [PNGWalks](PNGWalks.md "wikilink")

### Tools &rarr; Reload All Data

This will reload all of the displayed data.

### Tools &rarr; Manage and Browse

This submenu contains all scripts found in autoplot\_data/tools/\*.jy
and any Example scripts can be found here
<https://autoplot.org/data/tools/>.

### Tools &rarr; Additional Operations

Sometimes additional operations need to be applied to the data before
displaying. For example, suppose the data loaded is Flux which is a
three-index table of Time, Energy, and Pitch Angle. (This is often
referred to as "Rank 3" data and might be written like
Flux\[Time,Energy,PitchAngle\].) Autoplot can only display spectrograms
of data, so the data will be "sliced" before display. Autoplot does this
automatically, slicing in the middle of one of the dimensions, but you
can explicitly set the operations with this menu item. For example, you
can slice on a different dimension (energy instead of pitch angle), or
you can pick a different operation, such as averaging all the elements
of a dimension together. The are other operations, such as smooth and
detrend that are available as well.

### Tools &rarr; Cache

The Cache menu is a set of tools for managing the cache of data loaded.
When you point Autoplot to a URL like
<https://autoplot.org/data/autoplot.cdf>, Autoplot downloads the file and
stores it in a cache. (This is because most libraries need direct access
to data files, so a local copy is necessarily made.) By default this is
under the "autoplot\_data" folder in the scientist's home folder, in
fscache. This cache will grow and grow, and the "Manage Cache" tool must
be used to manually remove unneeded files.

"Reset Memory Caches" will clear fast RAM-memory caches of loaded data.
Autoplot should check data refreshness every ten seconds, but sometimes
things fail and an explicit refresh is needed.

"Manage Filesystems" is a tool for managing Autoplot's access to
filesystems. For example, if a server is unavailable when a file is
referenced, Autoplot will use a cached copy. (This is to provide offline
access to data.) The filesystem containing the file will be in an
off-line mode, meaning it can access files that have been loaded
already. If the server is back up and available again, this tool can be
used to reset the filesystem to a normal on-line mode.

The environment variable AUTOPLOT\_FSCACHE can be used to set the cache
location as well.

#### ro\_cache.txt

Note, caches can contain a file "ro\_cache.txt" (read-only cache) which
is a pointer to a local file system that contains the same files as the
remote filesystem. This allows data providers to produce .vaps that
external clients can use, without having to copy the data files into
their caches. Likewise, a collaborator may wish to mirror the site, and
they can then use a ro\_cache.txt pointer. Last, the ro\_cache.txt can
be used with the Git-based filesystem to link to a local copy of the
filesystem, so that modifications can be tested without affecting
others.

### Tools &rarr; Events List

The events list is used to load a list of times which control the
application time range. For example, suppose you are interested only in
data when we pass by the planet (perigee). You set the events list to a
list of perigee times
https://github.com/das-developers/das2meta/blob/main/orbits/junoPJ.dat, and use this
to select the perigee. Then clicking on a time will reset the
application timerange.

### Tools &rarr; Fix Layout

This will correct obvious undesired aspects of the plot, such as
overlapping labels and plots. Autoplot's layout is very flexible, more
so than is initially apparent, and because of this it can get into a bad
state. Further, its code which does the layout automatically would
oscillate between the wants of the ideal plot, and to avoid this the
result is at times not optimal. "Fix layout" allows this to be done
under the scientist's control.

## Tabs

![tabs.png](tabs.png "tabs.png")  

### <span id="axisPanel"></span>Axes

Selecting the axis tab with show a panel with basic controls for the two
axes of the plot in focus, the plot title, and the colorbar title (the
colorbar may not be visible but it always exists).


[![YouTube video player](https://img.youtube.com/vi/KrPnp3WCL60/0.jpg)](http://www.youtube.com/watch?v=KrPnp3WCL60 "YouTube video player")


Ranges for the x-, y-, and colorbar are strings that are parsed using
the current axis units (such as time or dimensionless). For example,

  - For an axes with time units: "2000 through 2010", "Sept 16 2009",
    "2009-009 10:00 to 11:00", and "2009-009T00:00 to 2009-009T10:00"
    "2012-12-14T23:00/2012-12-14T24:00".
  - For physical ranges, use the keyword "to" to delimit two real
    numbers. When the axis has a physical unit, such as "m/s" the range
    can be qualified with a unit, as in "0 to 100 cm/s."
  - An automatic test showing example ranges is
    [here](https://autoplot.svn.sourceforge.net/viewvc/autoplot/autoplot/trunk/VirboAutoplot/src/test/endtoend/Test026.java?view=markup).

All labels support "Granny Strings," which has special codes, similar to
those used in IDL, proposed by Grandel in Nystorm. For example, \!c
inserts a new line. See
[help\#Granny\_Strings](help.md#granny-strings "wikilink") for more
information. Also html escapes like \&amp;Delta; will show like &Delta;.

When selected, **Isotropic** constrains the x- and y-axis to have the
same data-to-pixel scaling. This option is ignored when the axes do not
have compatible units.

When **Legend Label** is checked, a legend is added to the plot, and an
icon for this panel is added. Note the plot also has a legendLabel
property that when set to False (\[menubar\]&rarr;Edit&rarr;Properties) will
suppress the label.

### <span id="metadataPanel"></span>Metadata

The metadata tab provides information about the data. It is a tree view
that contains a number of nodes of information.

The metadata node in the list is metadata provided by the data source.
In general, Autoplot doesn't understand the metadata and simply provides
it for reference by the user. However, if the data source also
identifies a "metadata model," this is indicated in parenthesis and
Autoplot will use the metadata to get axis labels and ranges.

The statistics node provides basic statistics about the data. For
example, it shows the mean and standard deviation, and the number of
valid points. Cadence indicates the typical spacing between points and
is used to insert breaks in time series.

The dataset node allows some inspection of the dataset itself. The size
of the dataset, its named dimensions, and their size are identified.
Metadata for plotting found within the dataset is available as well. You
can look at the digital data (though only the first twenty or so points)
as well.

Autoplot's data representation model, QDataSet, supports invalid data
place holders, called "fill data." When plotting data, this data is
skipped and the line connecting points is broken. Fill is represented in
the data with a special number, for example -1e31. Autoplot has several
ways of marking fill data. The metadata property FILL\_VALUE is the
value which marks the invalid number, -1e31, -999, etc. Note NaN is
always considered fill. The data may also have VALID\_MIN and
VALID\_MAX, which indicate the range over which the data is valid, and
values outside of this range are fill. Finally, sometimes a "weights
plane" could be used to mark fill values. This is a QDataSet with zeros
where the values are invalid. When the property WEIGHTS is equal to a
QDataSet, FILL\_VALUE, VALID\_MIN, VALID\_MAX can be ignored. If none of
these values are found, then only NaN indicates fill.

Metadata can be inserted on the plot using macros. For example, from the
bookmarks plot demo 1
(vap+cdaweb:ds=OMNI2\_H0\_MRG1HR\&id=DST1800\&timerange=2016-oct) and
replace the title with %{METADATA.GlobalAttributes.TITLE}, and when the
axis is drawn, the metadata node GlobalAttributes.TITLE replaces the
macro. If the dataset contains a USER\_PROPERTIES node,
%{USER\_PROPERTIES.prop.name} can be used to show prop.name from that
tree.

### <span id="stylePanel"></span>Style

The style tab contains controls for the style of the plotted element.

Autoplot tries to pick reasonable default settings such as data
rendering method (series versus spectrogram), but also default symbol
sizes and connectors. To further specify how a plot should appear, click
on the plot element to modify its color or symbol, for example, or for
spectrograms the colorbar (e.g. grayscale vs colors).

Note that you can set the rendering method and default settings via the
plot context menu (right-click), under Plot Style.

Autoplot will swap out controls based on the rendering method.

### <span id="scriptPanel"></span>Script

The script tab is a workspace for creating Jython scripts. Jython is the
Java version of Python, and it provides a rich environment for
developing software which combine and analyze data, and also control
workflows like running process on each file of a collection of files,
similar to IDL or Matlab. More on its use is found at
[scripting](scripting.md "wikilink"). The script tab creates an environment
optimized for creating software quickly, like an IDE for other
languages. For example, the "execute" button runs the script, and the
Context Selector controls how the script is to be used, explained below.

Right-clicking on the editor tab brings up a popup-menu of useful
functions when coding, for example &quot;Insert Code&quot;&rarr;getDataSet will insert
a getDataSet command loading the current data Autoplot is focused on.
&quot;Actions&quot;&rarr;&quot;Inspect URI&quot; will bring up the data source editor for the
URI.

The Context Selector controls how the script will be used. There are two
types of Autoplot scripts, "Application Context" and "Data Source
Context." Application Context scripts control the Autoplot application
itself, with access to the dom (the current state of Autoplot) and can
tell Autoplot to save the canvas to a .png file. The Data Source Context
is a more limited scripting environment, only able to load data. A Data
Source Context script is saved with a .jyds extention, and is loaded
into the canvas as if it were a data file.

The script panel is intended to be useful for other ascii-file tasks,
such as counting the number of characters in columns of an ascii file.
Note that when selecting text the number of characters and lines are
indicated.

### <span id="consolePanel"></span>Console

The console tab is where output from scripts and logging messages from
Autoplot are printed, and an interactive command prompt is found. For
example, at the "AP\>" prompt, enter "print 'hello'" and the text
"hello" is printed on the console. This allows data to be used
interactively, and gives a place where commands can be tested.

Autoplot uses "Loggers" throughout the system, which allow various parts
of the system to report on named channels. The print command prints on
the channel "console.stdout," while downloading a file writes to the
channel "das2.filesystem.http". Most channels will only be of interest
to developers, but you can see these channels by clicking on the
"Console Settings" button.

The "Console Settings" button controls how the console operates. Each of
the logging channels has a verbosity level, and messages that should not
be seen under normal conditions are issued at a quieter level than
"INFO" such as "FINE." Error messages are issued at more verbose levels
(such as WARNING) and will be printed on the console. Additional
information can be printed with each line, such as the logger name, and
log level. "timing" will show the elapsed seconds since each message was
printed. "threads" shows an identifier for concurrent thread of the
message, and GUI when the message was issued from the event thread.

Jython scripts can use the logging system. (This is fixed in the next
dev release, 20161020.)

```
from org.das2.util import LoggerManager
logger= LoggerManager.getLogger('analysis')
logger.info('opening file data.dat')
logger.fine('file data.dat is 140 bytes long')
logger.warning('warning!')
print 'print message'
```
The AP prompt contains an Jython session which can be used for quick
calculations and to test statements. The keyboard up arrow can be used
to get to previously-entered commands. The keyboard tab key will show
completions. Try "print datum('15hr') / datum( '5s')"

The console text can be saved to a file as well. Typically this will be
a text file containing the text in the console, though note there is a
limit to the size of the console, and some messages may no longer be
available. If the provided filename ends with .xml, then all logging
information is saved, providing complete feedback information to others.

# Adding Plots

`Right click`&rarr;`Add Plot` can be used to add additional plots to the
canvas. Axes from multiple plots can be bound together so that adjusting
one triggers a change in others. This video shows how to add a second
plot and bind the y-axes together. Note that Autoplot tries to bind time
axes together automatically, since this is a common mode of operation.

Keyboard shortcuts:

  - Add plot: Right click on canvas and select Add Plot
  - Next plot element: CTRL-TAB
  - Previous plot element: CTRL-Shift-TAB
  - Add a plot below: CTRL + Play Button (green arrow button)
  - Add overplot: Shift + Play Button (green arrow button)


[![YouTube video player](https://img.youtube.com/vi/UGA8SiDBZX8/0.jpg)](http://www.youtube.com/watch?v=UGA8SiDBZX8 "YouTube video player")


## <span id="layoutPanel"></span>Layout

![layout.png](layout.png "layout.png") The Layout Panel (enable with
Options&rarr;Enable Feature&rarr;Layout Tab) provides access to all of the plots
and plot elements on the canvas. This allows you to swap plot position,
delete plot elements, add groups of plots, etc.  

### Plots

The Plots area contains a simplified view of the plots on the page. Each
plot has a context menu that allows the plot to be edited or deleted.
Also a group of plots can be added below, for example a block of 3 by 3
plots.

Multiple plots can be selected by holding the control button (command on
Macs) down while clicking. Two plots can be selected and Plots&rarr;Swap
Position will exchange their positions. Also multiple plots can be
edited at once, for example to set all the titles the same and then make
tweaks for each plot.

### <span id="dataPanel_1"></span>Bindings

This Bindings area contains a list of bindings for the application.
These are properties that are bound together. For example, a stack of
plots with a common x axis all have their x axes' range bound to the DOM
property "app\_0.timerange". If one right-clicks on a binding, it can be
deleted.

### Plot Elements

Plot elements have the job of rendering the data onto a plot. The Plot
Elements section allows them to be individually controlled and deleted.
Note when a vector is plotted (e.g. Bookmarks&rarr;Demo 5), then a plot
element is added for each component, and these are all children of an
inactive parent component. The inactive component can be used to control
all the children at once. For example, adjust the line thickness of the
parent and all the children will be modified.

## Data

The Data Panel (enable with `Options`&rarr;`Enable Feature`&rarr;`Data Panel`)
contains controls for processing the dataset after it is loaded.

For example, the fill value can be set manually when the dataset has
failed to identify it.

The **Data Source** subpanel controls the data source node that has
focus. A second URI controller is provided for reference, and can be
used to control the data loaded as well. Additional operations can be
applied to the data immediately after loading, such as indicating fill
values, or when for plotting slices against one another.

<span id="dataPanel_2"></span> **Data Post Processing** specifies the
operations that should applied before displaying the data. Originally
introduced to allow for slicing of high-dimension (high "rank") data
sets like Flux\[Time,Energy,Angle\], this also has a number of filters
that are described below.

When the Operations field is "|slice\<dim\>(\<index\>)" the data is
sliced to provide a view (like a cross-section) of the data. Note the
mouse wheel will allow the index of the slice to be adjusted
interactively.

When a vector component is plotted, Operations simply identifies the
component to plot, and this is implicitly the "|unbundle(c)" operation.

The magnifying glass with three vertical bars (|||) icon enters a GUI
that allows these to be adjusted. This allows several adjustments to be
made at once, such as slicing the data then running the result through a
histogram.

**Additional Operators** When the operations field starts with the pipe
(|) character, it is a list of filters that are to be applied to the
data. These filters include (for example):

`|histogram` perform an "auto" histogram of the data that automatically
sets bins.

`|log10` take the base-10 log of the data.

`|slice0(index)` slice the data on the zeroth dimension (often time) at
the given index.

`|slice1(index)` slice the data on the first dimension at the given
index.

`|collapse0` average over the zeroth dimension to reduce the
dimensionality.

`|transpose` transpose the rank 2 dataset.

`|fftPower(size)` plot power spectrum by breaking waveform data in
windows of length <em>size</em>.

`|smooth(size)` boxcar average over the rank 1 data.

`|diff` finite differences between adjacent elements in the rank 1 data.

`|accum` running sum of the rank 1 data. (opposite of diff).

`|grid` grid the rank2 buckshot but gridded data into a rank 2 table.

`|flatten` flatten a rank 2 dataset. The result is a n,3 dataset of
\[x,y,z\]. (opposite of grid)

`|negate` flip the sign on the data.

`|add(amount)` add a constant to the data. Note this can be datums like
"15sec".

`|multiply(amount)` multiply the data by add a constant.

`|cos` cos of the data in radians. (No units check)

`|sin` sin of the data in radians. (No units check)

`|toDegrees` convert the data to degrees. (No units check)

`|toRadians` convert the data to radians. (No units check)

These filters can be chained together like so: `|slice1(10)|histogram`.
The GUI in Autoplot v2015a contains a GUI for working with this string.
In the DOM, this is the same as the "component" property of a
plotElement.

More about [filters](filters.md "wikilink") can be found here.

## Script

The script panel (enable with Options&rarr;Enable Feature&rarr;Script Panel)
provides a convenient place for writing and reviewing the Jython scripts
to control the application and load data. It provides a simple
completion and right-click to see additional options. This is intended
to provide full access to advanced users.

Note a .jyds file executed in the "data source context" and loads data
from a number of places and performs operations to create a new dataset.
.jy files are executed in the "application context" and control labels,
add components, run batches and plot ad-hoc datasets. .jyds scripts are
unaware of the application itself or the plotting that is done with the
data it produces. Further, .jyds scripts must be saved to a file, and
references to these files can be saved in .vap files.

Another use case for scripting is to add new functionality to the GUI.
Scripts that run in the application context can be added to the tools
bookmarks, and will appear in the tools menu when the app is reloaded
(or getViewWindow().reloadTools() is run). For example, run the script:
<https://autoplot.org/data/tools/flashFocus.jy>. This will show the
script in a dialog with an execute button. (The scripts can do malicious
things like delete files, so you must review the script\!) Note in the
review dialog, that there's a checkbox to add to the tools menu. The new
menu item "Flash Focus" should appear. The script will cause the focus
plotElement to flash three times.

Jython scripting is being finalized and documented. More documentation
is coming soon.

# <span id="layout"></span>Modifying Layout

![DOM GUI (Accessed via Edit&rarr;Edit DOM) showing entries for layout.
Autolayout must be de-activated for changes to apply
(Options&rarr;Auto&rarr;Autolayout)](layoutdom.png
&quot;DOM GUI (Accessed via Edit&rarr;Edit DOM) showing entries for layout. Autolayout must be de-activated for changes to apply (Options&rarr;Auto&rarr;Autolayout)&quot;)

Autoplot's **canvas** consists of a number of **plots** which are the
two-dimensional spaces on which data is rendered. **Plot elements**
connect data to the plots, by identifying the data source, plot, and
method for rendering data. A plot can contain a number of plot elements,
as is the case when two datasets are drawn on the same axes, (also
referred to as an **overplot**.) A color bar is connected to all plots
so that multiple spectrograms can be rendered using the same color map.
The color bar is hidden when it is not needed.

The [cookbook](cookbook.md "wikilink") page describes quite a few useful
tricks, such as resizing plots and putting exponents in labels.

Autoplot uses rows and columns to specify the location of components on
the drawing canvas. These objects are controlled with strings that
efficiently specify the location. For example, the horizontal (column)
layout from the left is specified as a percentage plus a shift from the
left `L%+S`, where

  - L is the percentage of canvas to place the left side of the plot box
    (only data, no labels)
  - S is the shift (in px or em)

To have the labels on the y-axis rendered outside of the canvas, use
```
0%+0
```
The layout may be specified in the URI sent to the Autoplot server. In
this case, the left and right positions are comma separated, as in
`L%+S,R%+S`. The default is `0%+8em,100%-6em`. For the bottom and top
positions, the default is `100%-3em,0%+2em`.

Note that rows and columns are children of the marginRow and
marginColumn. Instead of specifying the normal position with respect to
the canvas, these rows and columns position are specified with respect
to the marginRow and marginColumn. The autolayout feature automatically
adjusts the position of the marginRow and marginColumn to make the plot
fit on the page.

  

# Saving Plots

The state of the application, including information about the plot
layout, labels, and data URIs that specify where data is loaded can be
saved in a VAP file using "File \> Save As".

A VAP file does not contain the data used to produce the plot, but only
references (URIs) to it<sup>+</sup>. To save data along with a VAP file,
select "Embed Data" when saving. The file created is a zip file
containing the VAP and the data required to display the VAP. See
[developer.vapzip](developer.vapzip.md "wikilink").

<div style="font-size:85%">

<sup>+</sup>Note that if a VAP file has URIs to files on the local
filesystem, the VAP will only work on systems with data in the same
directory location.

</div>

## Time Ranges in VAP Files

Timeranges or time values occur in multiple places in a VAP file:

  - URIs (vap+cdaweb:ds=AC\_H2\_SEP\&id=H1\&timerange=2005-02-04)
  - on axes (<datumRange units="us2000" value="2005-02-04"/>),
  - within defaults for each plotElement, and
  - for the overall application (in the "timeRange" property).

The timeRange property, found at the end of the VAP file, is what sets
the time range. This is what allows arguments to VAP files, e.g.,
`/tmp/foo.vap?timerange=2012-03-04`, to override the time ranges and
values specified in the file. Even though the data URIs may refer to
other times, their ability to browse to other times (their "Time Series
Browse" capability) is used to load data for the correct time.

# <span id="ascii_main"></span>Reading Data Files

## Reading ASCII

An editor can be used to help develop a URI with the appropriate
parameters for Autoplot to read and plot data in a ASCII file. The list
of parameters that may be used in a URI is given
[below](#ascii-table "wikilink"). A table is displayed showing how the
reader would parse the file. Darker lines that are not broken into
columns are lines identified as non-records, such as header lines.

Details on how the ASCII table reader is implemented is described at
[ascii\_data\_source](ascii_data_source.md "wikilink").


[![YouTube video player](https://img.youtube.com/vi/TcR0jtxlWrw/0.jpg)](http://www.youtube.com/watch?v=TcR0jtxlWrw "YouTube video player")


### Header tab: identify records and non-records

Skip Lines: the number of lines to skip before attempting to parse
records. Press "Select" then click on the first parseable line.  
Comment Prefix: lines starting with this are treated as non-records.

### Times tab: specify how times are parsed

Time Format: format for interpreting times. For example, `$Y+$m+$d`
means the first three fields are interpreted as year, month, and day
separated by a space. `$Y$m$d` means the first field is an 8-digit date.
Press "Select" and highlight the fields in one of the records. This will
copy the fields up into the Time Format text field. Then in the text
field, highlight each field and use the drop list to identify the field
type. If the field is already ISO8601 compliant, a manual specification
of the time format is not required. See
[\#Wildcard\_codes](#wildcard-codes "wikilink") for a full list of time
codes.

Note that fractional times may be given in the ASCII file, e.g.,
`$Y+$m+$d+$H` with

```
2014 01 02 12.5 -44.1
```
will be interpreted as a value of -44.1 at 12:30 on January 2nd, 2014.

Note too that all times are implicitly UTC, and other timezones are not
supported.

### Data tab: identify data to plot and interdependence

Column: the column to plot. Note if the first record is column labels,
then these labels can be used to identify columns. Press "Select", then
click on a field to select the column. If a several adjacent fields are
selected, then a rank 2 table is plotted (e.g. as a spectrogram)

Depends On: the column that tags the column to plot. This is the
independent parameter upon which the dependent parameter depends. Press
"Select" then click on the field to select the column.  
Time checkbox: identify the "Depends On" as times.

Data can also be exported as an ASCII tables. Presently data is
formatted to a comma-separated-values (csv) file, and no formatting
options are provided. Use Autoplot's &quot;File&rarr;Export Data&quot;, then select a
file name with a .csv, .dat, or .txt extension.

## Reading CDF

CDF files are a special file format developed at NASA/Goddard and used
to store data in a binary format, but with named parameters within the
file. These parameters have metadata containing labels and units, but
also indicating relationships between variables. Dependent parameters
like "Density" are declared to be dependent on an independent parameter
like "Time" or "Epoch." In this way the files store data in a more
abstract form than ASCII and other file formats, and Autoplot can
leverage this information.

![cdfEditorPanel.jpg](cdfEditorPanel.jpg "cdfEditorPanel.jpg")

### Select variable parameter

Select the variable to be plotted. Note when a parameter has components,
such as a 3-component B-field, then individual components (Bz) can be
plotted by opening the folder. This is the list of parameters that have
been marked as "data" and not "support data" in the metadata. For
example, the timetags variable "Epoch" is not shown. To see all
parameters, select the "show all" checkbox.

In the middle of the panel is information about the variable. These come
from the CDF metadata "CATDESC" and "VAR\_NOTES". Minor problems found
in the CDF may be indicated here, for example if two variables don't
have the same number of records.

### Advanced Sub-panel

"Load subset" allows a subset of the records to be loaded. For example,
0:100 will load just the first 100 records. ::2 will load every second
record.

"Only load data where" will load a second variable and filter the data
when this condition is true. For example, "within" "1e0 to 1e9" will
only load the FEDU data when HOPE\_ENERGY is with in this range. (TODO:
make more useful example.)

"Interpret Metadata" allows non-conforming CDFs to be used. For example,
a variable with poorly formed metadata cannot be plotted, and this
allows these conventions to be ignored and data plotted.

# Exporting Data

Data can be exported using \[menubar\]&rarr;File&rarr;Export Data. This will take
the data that has the focus set by the last mouse click and export
either the data as it was originally loaded in or as it is displayed.
For example, if Flux\[Time,Energy,Angle\] is loaded, a slice is
displayed. The scientist can either export the original 4-D data, or
export a slice of just Flux\[Time,Energy\].

Autoplot's plug-in data sources can also provide methods for formatting
data, and the list of available methods for writing data are displayed.
Autoplot checks to see if the data will "fit" into the format, and
disable the option when it will not. For example, Density\[Time\] could
not be exported as a .png image, but Image\[Rows,Columns,3\] could.

Plug-in data sources may also provide a GUI which controls how the
formatting is done.

There is a second option where Autoplot is able to format many datasets
at once, in the "export all" dialog. This will show all the loaded URIs,
and will then load them all into one "bundle" dataset for export.

## Use within scripts

When scripting, the command "formatDataSet" is used. The command takes
two arguments, a dataset and a URI. The URI is similar to the URI which
would read the data, where its arguments are used to control how the
data is exported. (A URI string is used because a future version of
Autoplot will allow data to be exported to databases and websites, but
this has not yet been explored.) URI parameters for scripting are
described below. The following script shows how data is loaded from a
CDF file and formatted to an ASCII file.

```
ds= getDataSet( 'https://autoplot.org/data/ac_h2_mfi_20060101_v05.cdf?Magnitude' )
formatDataSet( ds, '/tmp/mag.txt' )
```
## Formats Supported

The parameters shown can be used in scripts, and the default value is
sometimes shown, to provide an example value.

### .idlsav

The scientist can export data to IDLSAV files. Rank 1 and rank 2 data
are now supported.

  - tunits=t1970. The time units for the data. t1970, the default, means
    the number of non-leap seconds since 1970-01-01T00:00Z. "seconds
    since 2019-01-02T00:00Z" (or whenever) is often used as well, so
    that the times are just seconds since midnight.

Note that rank 2 and higher data is transposed between this and the
org.autoplot.idlsupport.APDataSet ("IDL/Matlab Bridge") result. This is
because org.autoplot.idlsupport.APDataSet is used to provide access to
data in Matlab and Python as well, while exporting to IDLSAV is
optimized for IDL access.

### .mat

Matlab files can be used to export rank 1 and rank 2 data.

  - tunits=t1970. The time units for the data. t1970, the default, means
    the number of non-leap seconds since 1970-01-01T00:00Z. "seconds
    since 2019-01-02T00:00Z" (or whenever) is often used as well, so
    that the times are just seconds since midnight.

### .das2stream

Format streams for caching data or to explore responses for the
das2server.

  - version
  - fracsec
  - precision
  - type="ascii". Use ascii or binary for data transfer.

### .dat .txt (ascii tables)

  - tformat="ISO8601"
  - header="none". add a header to the data, for example "rich" header
    describes all sorts of metadata.
  - format
  - depend0Units units for times, such as t1970 or "seconds since
    2019-01-02T00:00Z"
  - doDep

### .nc (NetCDF)

  - type=double. the data type to use.
  - arg\_0 name for the variable.
  - doDep
  - metadata
  - append=F. add to the existing file.

### .cdf

The append option allows a cdf file to be built up. Alternatively, if it
is more convenient to have all the data in memory at once, then a bundle
of data can be exported.

  - type=double. the data type to use, for example float.
  - append=F. add to the existing file.
  - bundle=F. format each of the bundled datasets.
  - timeType=tt2000. or epoch
  - compressed=F. compress the data within the CDF.
  - arg\_0 is the parameter name.

### .wav

wav sound files.

  - scale=T. scale the data so that the full dynamic range is used.
  - byteOrder big or little.
  - type the data type, like short.
  - timeScale=1.0. rescale the times. timeScale=2 means "speed up the
    sound"
  - timetags=F. if T, then create a second ASCII file which shows the UT
    time vs index.

### .hapi

This formats responses supporting HAPI servers. HAPI server developers
may want to use this to see what properly formatted responses should
look like, and this is used with the AutoplotServlet and
AutoplotDataServer to provide responses.

This plug-in is somewhat odd, because the file given converted to a
folder name by changing the ".hapi" extension to "/hapi", and then
formatting each part of the response.

# Forming URIs

## Aggregation

Data coming from files can typically be combined, or aggregated. For
example, a single CDF file can be read (using the CDF plug-in) with the
URI:

`vap+cdf:ftp://cdaweb.gsfc.nasa.gov/pub/istp/ace/swe/2008/ac_k0_swe_20080620_v01.cdf?Np`

If this is one of a series of files, the variable `Np` can be plotted
across several files using the notation:

`vap+cdf:ftp://cdaweb.gsfc.nasa.gov/pub/istp/ace/swe/$Y/ac_k0_swe_$Y$m$d_v$v.cdf?Np&timerange=2008-June`

Most of the letters used for the wildcards for time are the same as the
Unix `date` command, for example `$Y` means a four-letter year while
`$y` means a two-letter year.

Any file-based reader that returns time for the first dimension can be
aggregated. Note &quot;Tools&rarr;Aggregate...&quot; will attempt to create an
aggregation spec from a file URL.

<span id="aggregator_main"></span>

### Aggregation GUI

![AggregationGUI.jpg](AggregationGUI.jpg "AggregationGUI.jpg")
Aggregation URIs will have an additional controller in the data source
editor. This allows timeranges to be browsed and selected. The field
"Time Range for Aggregation" controls the span that will be aggregated.
This is a time range parsed like other timeranges in Autoplot: 2010 is a
year, 2010-Jan is a month, 2010-Jan-01 is a day, 2010-Jan-01 07:00 to
08:00, and so on. Below are three droplists that allow an interval to be
selected. The GUI will query the server to see which intervals are
available. First select from the available years, then from available
months within that year, and then a day. "Copy" will then copy the value
into the time range text field. The reduce checkbox enables the
experimental data reduction feature where data is reduced to axis
resolution as it is read in.

### Wildcard codes

Aggregation URIs will contain from the following wildcard codes:

  - $Y four-digit year
  - $y two-digit year
  - $j three-digit day of year
  - $m two-digit month
  - $b three-letter month (English locale only)
  - $d two-digit day of month
  - $H two-digit hour
  - $M two-digit minute
  - $S two-digit second
  - $(milli) three digit milliseconds since second boundary. (please use
    subsec instead of this)
  - $(micro) three digit microseconds since millisecond boundary.
    (please use subsec instead of this)
  - $(subsec;places=3) three digits are milliseconds. $(subsec;places=6)
    means the 6 digits are microseconds.
  - $v version number, decimal sort. $(v;alpha) is for alpha sort, and
    $(v;sep) for "x.y.z" Note sometimes the filename will contain a V
    before this, and this should be just the number like so: V$v
  - $o orbit number, arguments like $(o;id=crres) make this useful. see
    <https://autoplot.org/developer.orbitTimeSpec#Orbits_in_Time_Ranges>
  - $x ignore, match anything but don't interpret the field.

A version wildcard is allowed. Versioned URIs have the form:

`vap+cdf:https://cdaweb.gsfc.nasa.gov/data/ace/swepam/level_2_cdaweb/swe_k0/$Y/ac_k0_swe_$Y$m$d_v$v.cdf?Np&timerange=2022-July`

Also, parenthesis can be used to modify fields. For example:

  - $Y$m$d-$(H;span=12) indicates the hour is the beginning of a 12 hour
    interval indicated by the name.
  - $Y$m$d\_$H$(M;span=10) indicates the files are in ten-minute blocks.
  - $(m;Y=2011)$d indicates the year field is implicit. TODO: bugs
    prevent this from working, since we look for $Y to detect
    aggregations...
  - $Y$m$d\_$H$M$S.$(milli;span=250)

See also
<https://github.com/hapi-server/uri-templates/wiki/Specification>, which
includes a more complete description.


[![YouTube video player](https://img.youtube.com/vi/QI2ggl_iv64/0.jpg)](http://www.youtube.com/watch?v=QI2ggl_iv64 "YouTube video player")


## Time Parsing / Formatting

One code for parsing and formatting times into strings is used
throughout Autoplot to:

  - parse times within a file
  - parse times in a filename (and URI)
  - generated times in scripts

Note this is different than the code that parses ranges to control axes.
That one must guess the format, then parse. This one is given a time
format, and then and parse strings to get timeranges or vice-versa.

Example times:

  - $Y-$m-$d 2010-06-23
  - <file:///tmp/$Y$m$d.dat> <file:///tmp/20100623.dat>

Field types (see [\#Wildcard\_codes](#wildcard-codes "wikilink") for
full list and definitions):

  - $Y $m $d $H $M $S $(milli) $(micro)

Field qualifiers:

  - $(H;span=4) digit indicates beginning of 4 hour interval
  - $(m;Y=2004) The year 2004 is implicit

Note %{m;Y=2004} may be used instead.

### Automatic Time Parsing

A number of places in Autoplot allow for implicit time range parsing.
For example, typing "May 2014" on a time axis is interpreted as
2014-05-01 through 2014-05-31. This allows users to easily convey intent
to the software without the burden of entering each field. This control
is intended to be more informal, and to provide reasonable
interpretations of how time ranges might be represented.

A number of special keywords are supported as well. For example, "now"
refers to the current time, and this can be used to ISO8601 durations to
create range specifications like "now-PT24H/now" to refer to the
previous 24 hours. Also orbits are identified for a number of
spacecraft, and intervals can be created with "orbit:SCID:ORBITID" where
SCID is the spacecraft and ORBITID identifies one of its orbits. For
example, orbit:rbspa-pp:4 refers to orbit 4 of the RBSP-A spacecraft,
which is the time range 2012-08-31 12:13 to 21:12. The "select time
range" GUI has a tab to create time ranges of this type.

Here are a number of entries and their interpretations:

| Implicit String                           | Interpreted Start                       | Interpreted Span                                         |
| ----------------------------------------- | --------------------------------------- | -------------------------------------------------------- |
| 2000-01-01T13:00Z to 2000-01-01T14:00     | 2000-01-01T13:00:00.000Z                | 60.0 min                                                 |
| 2000-01-01 13:00 to 14:00                 | 2000-01-01T13:00:00.000Z                | 60.0 min                                                 |
| 2000-01-02                                | 2000-01-02T00:00:00.000Z                | 24.0 hr                                                  |
| 2000-002                                  | 2000-01-02T00:00:00.000Z                | 24.0 hr                                                  |
| 2000-02                                   | 2000-02-01T00:00:00.000Z                | 29.0 days                                                |
| 2000-feb                                  | 2000-02-01T00:00:00.000Z                | 29.0 days                                                |
| 2000                                      | 2000-01-01T00:00:00.000Z                | 366 days                                                 |
| 2000-01-01 to 2000-01-05                  | 2000-01-01T00:00:00.000Z                | 4.0 days                                                 |
| 2000-01-01 through 2000-01-05             | 2000-01-01T00:00:00.000Z                | 5.0 days                                                 |
| 2001-01-01 span 10 days                   | 2001-01-01T00:00:00.000Z                | 10.0 days                                                |
| 2000-01-01T13:00Z/PT1H                    | 2000-01-01T13:00:00.000Z                | 60.0 min                                                 |
| 20000101T1300Z/PT1H                       | 2000-01-01T13:00:00.000Z                | 60.0 min                                                 |
| 2000-01-01T00:00Z/P1D                     | 2000-01-01T00:00:00.000Z                | 24.0 hr                                                  |
| 2007-03-01T13:00:00Z/P1Y2M10DT2H30M       | 2007-03-01T13:00:00.000Z                | 437.11 days                                              |
| 2007-03-01T13:00:00Z/2008-05-11T15:30:00Z | 2007-03-01T13:00:00.000Z                | 437.11 days                                              |
| P1Y2M10DT2H30M/2008-05-11T15:30:00Z       | 2007-03-01T13:00:00.000Z                | 437.11 days                                              |
| 2007-009/2007-021                         | 2007-01-09T00:00:00.000Z                | 12.0 days                                                |
| 2007-05-15/2007-05-30                     | 2007-05-15T00:00:00.000Z                | 15.0 days                                                |
| 2007-03-01/P5D                            | 2007-03-01T00:00:00.000Z                | 5.0 days                                                 |
| P5D/2007-03-06                            | 2007-03-01T00:00:00.000Z                | 5.0 days                                                 |
| 2000-01-01T13:00/PT1H                     | 2000-01-01T13:00:00.000Z                | 60.0 min                                                 |
| 20000101T13:00Z/14:00Z                    | 2000-01-01T13:00:00.000Z                | 60.0 min                                                 |
| 1000                                      | 1000-01-01T00:00:00.000Z                | 365 days                                                 |
| 9000                                      | 9000-01-01T00:00:00.000Z                | 365 days                                                 |
| 2000-01-01T00:00:00 span .000001 sec      | 2000-01-01T00:00:00.000Z                | 1.0 microseconds                                         |
| 2000-01-01T00:00:00 span .000000001 sec   | 2000-01-01T00:00:00.000Z                | 0.0010 microseconds                                      |
| 2002-01-01T10:10:10 span .000000001 sec   | 2002-01-01T10:10:10.000Z                | 0.0 microseconds                                         |
| Aug 1969 through Sep 1970                 | 1969-08-01T00:00:00.000Z                | 426 days                                                 |
| 2004-12-03T20:19:59.990/PT.02S            | 2004-12-03 20:19:59.990 to 20:20:00.010 | within 30.0 micros (0.0 microseconds -0.25 microseconds) |
| 2004-12-03T20:19:56.2/PT.2S               | 2004-12-03T20:19:56.200Z                | .2 seconds                                               |
| 2014-08-29T13:27:43.253Z                  |                                         |                                                          |
| P1D                                       | (1 day ending at the current time)      | 1 day                                                    |
| PT1H                                      | (1 hour ending at the current time)     | 1 hour                                                   |
| orbit:rbspa-pp:403                        | 2013-01-27T18:58:17.392Z                | 8.9789 hr                                                |
| orbit:rbspa-pp:403-406                    | 2013-01-27T18:58:17.392Z                | 1.4965 days                                              |
| 1972/now-P1D                              | 1972-01-01 00:00 to (24 hours ago)      |                                                          |
| now-P10D/now-P1D                          | (10 days ago) to (1 day ago)            |                                                          |
| lastday-P1D/lastday                       | yesterday (UTC), beginning of the day   | 1 day                                                    |

# Cookbook

The [cookbook](cookbook.md "wikilink") page describes quite a few useful
tricks, such as resizing plots and putting exponents in labels.

# Advanced Topics

## Granny Strings

All labels may include "Granny" strings defined by Grandle and Nystrom
[1](http://www.csb.yale.edu/userguides/graphics/explorer/html/doc/ref/stan/nagtext.htm).
A few of these are

  - \!A superscript
  - \!B subscript
  - \!E superscript with smaller font size
  - \!D subscript with smaller font size
  - \!N normal position
  - \!C carriage return (newline)
  - \!S push current position and size on to stack.
  - \!R pop position and size from stack.

so that `!A2!Ns!A-2!N` results in m<sup>2</sup>s<sup>-2</sup>.

Labels may include Unicode (indicated using its entity number, e.g.,
`&#197;`). In addition, the named html entities listed at
<http://www.fileformat.info/format/w3c/htmlentity.htm> may be used. The
list includes:

  - Greek letters (use without quotes): "\&Alpha;" "\&Beta;" "\&Delta;"
    "\&alpha;" "\&beta;" "\&delta;" "\&pi;" "\&rho;" "\&omega;"
  - Math symbols: &quot;\&amp;sum;&quot; (&sum;) &quot;\&amp;plusmn;&quot; (&plusmn;)

## TimeSeriesBrowse and other Capabilities

Autoplot allows each data source to advertise additional capabilities
beyond data loading. For example, the most commonly used capability is
TimeSeriesBrowse.

### TimeSeriesBrowse

TimeSeriesBrowse is the feature provided by some data sources which
allows data from any interval to be loaded. For example, a day's worth
of data is displayed on the screen, the scientist can click on a button
to advance to the next day, and the data source will then load data for
this interval.

The aggregating data source provides this capability. When
<https://autoplot.org/data/agg/efi/$Y/po_k0_efi_$Y$m$d_v$v.cdf?POTENT&timerange=2000-01-01>
is loaded, the data source tells Autoplot that it can load data for
other intervals as well.

Conventionally, data sources supporting this will use the keyword
"timerange" to control the time. For example the CDAWeb data source also
supports time series browse:

```
vap+cdaweb:ds=PO_K0_EFI&id=POTENT&timerange=2000-01-01
```
### Updating

Data sources can provide other capabilities, such as updating. This
capability will cause Autoplot to periodically check back with the data
source to see if updates can be loaded. For example, file-based URIs
often support filePollUpdating=5, which will check for updates in any of
the files every five seconds.

## Caching

  - FileSystem cache - The data files are kept on your local file
    storage. HTTP HEAD requests are used to check if new versions are
    available, limited to once per 10 seconds.
  - Reference cache - Many data sources use the reference cache to keep
    track of loaded data. As long as someone is using data, and a
    reference to it exists in machine memory, the reference will stay
    valid. If no one is using data, the Java "garbage collector" is free
    to remove it from memory.
  - DataSource cache - Some data sources use a mechanism called caching
    to cache extra data that is loaded.

Note \[menubar\]&rarr;Tools&rarr;&quot;Reload All Data&quot; will reset all in-memory
caches. Files will be reloaded if the remote file is updated (which will
happen anyway).

If the data source is jyds, and inputs and script has not changed,
execution may be faster because output values are cached. To see this in
action, run a script and then hit the play button again. The second
execution will be faster.

Some data sources cache data, where several quantities that were
expensive to calculate were calculated, so instead of throwing them away
we cache them in case someone else needs them. Suppose there is a
JythonDataSource script that loads three quantities and then produces a
derived quantity. Often the quantities used to derive are interesting as
well, and will be plotted alongside the derived quantity.

## Failsafe Installation

### Windows

Download <https://autoplot.org/jnlp/latest/autoplot.jar> to your desktop
and then double click it. Autoplot should launch if you have Java
installed.

Some versions of Java will run with limited memory (e.g. 192MB instead
of 1GB), so check that this will be sufficient; if not, start using the
command line using:

```
java -Xmx4G -jar autoplot.jar
```
### Linux and OS-X

On the command line, download Autoplot using either wget or curl:

`wget&nbsp;-N&nbsp;`&lt;https://autoplot.org/jnlp/latest/autoplot.jar&gt;  
`curl&nbsp;-O&nbsp;`&lt;https://autoplot.org/jnlp/latest/autoplot.jar&gt;

and then start it with

```
java -jar autoplot.jar  
```
Note that IcedTea/OpenJDK versions of Java may work, but we recommend
using Oracle's version of Java
[2](http://www.java.com/en/download/index.jsp).

To launch Autoplot with more memory, use

```
java -Xmx16G -jar autoplot.jar
```
### 32bit JVMs

A 32 bit JVM can be used, but it must be run with 1GB of memory or less.
A 64bit JVM is recommended.

### Errors

Sometimes updates in Autoplot's dependencies cause this error:

```
Unsigned application requesting unrestricted access ...
```
To fix, start `javaws -viewer` and delete all CDF and Autoplot
applications and then delete all CDF and Autoplot resources. Web Start
is touchy software and resetting things almost always seems to help.

## Plug-ins

### Data Sources

Plug-in data sources are used to load data into Autoplot using a URI
specification. The URI is used to identify the plug-in and then the
plug-in uses the URI and its parameters to read in the data (into
Autoplot's internal data model, [QDataSet](QDataSet.md "wikilink")). Some
plug-in data sources have graphical (GUI) editors that make it easier to
compose URIs. For these plug-ins, clicking the folder icon next to the
address bar will launch the editor, otherwise the URI completions is
used to provide the user with the available parameters.

For example, the ASCII Table reader URIs have the form

```
vap+dat:<file>?<params>
```
and the params identify how to parse the ASCII table with parameter
names like skipLines and delim. The

```
vap+dat:
```
explicitly requests a plug-in (a guess is made if not given). (Details
on how the ASCII table reader is implemented is described at
[ascii\_data\_source](ascii_data_source.md "wikilink").)

Note data from servers that use query parameters (with URLs containing
?) cannot be read directly, since the query parameters are interpreted
by the Autoplot reader plug-in. Either read the data to a local file
(changing the name so that it does not contain a question mark) and read
that, or a Jython script (.jyds) can be used to read the data.

### Discovery

A discovery plug-in helps the user develop a valid URI to enter into the
address bar.

Discovery plug-ins are activated by entering their vap prefix (e.g.
vap+cdaweb:) into the address bar and are typically accessed using a GUI
by selecting File&rarr;&quot;Add Plot From ...&quot;.

In some cases, these plug-ins use knowledge of conventions used for the
layout of a data bases to allow the user to browse all available data
from a given data provider. In other cases, these plug-ins help the user
plot data from one or more data providers, data directories, and/or data
files without having to enter a complex URI into the address bar.

Data providers interested in making their plug-ins discoverable should
see [Adding\_Data\_Sources](Adding_Data_Sources.md "wikilink").

#### CDAWeb

URI prefix: vap+cdaweb:

![Accessing list of CDAWeb data from Autoplot.](cdaweb.png
"Accessing list of CDAWeb data from Autoplot.")

![(Click image to expand.) Autoplot's listing of data from CDAWeb that
is shown when selecting `File&rarr;Add Plot From&rarr;CDAWeb` or by clicking this
\[<https://autoplot.org/autoplot.jnlp?vap+cdaweb>: link\] ](CDAWebDB.png
&quot;(Click image to expand.) Autoplot's listing of data from CDAWeb that is shown when selecting File&rarr;Add Plot From&rarr;CDAWeb or by clicking this [https://autoplot.org/autoplot.jnlp?vap+cdaweb: link] &quot;)

The [CDAWeb group](https://cdaweb.gsfc.nasa.gov/) at
[NASA/Goddard](https://gsfc.nasa.gov) provides a large volume of data in
[CDF](https://cdf.gsfc.nasa.gov) files which Autoplot can read. This
plug-in knows how to query the database to see what is available and
provides a GUI for searching and filtering the list.

To see the list,

  - Click this \[<https://autoplot.org/autoplot.jnlp?vap+cdaweb>: link\]
    to start Autoplot with the list shown, or
  - in Autoplot, select `File`&rarr;`Add Plot From`&rarr;`CDAWeb` as shown in the
    top image to the right.

  

#### das2server

URI prefix: vap+das2server:
![das2ServerEditorPanel.png](das2ServerEditorPanel.png
"das2ServerEditorPanel.png")

Das2 servers are used to supply data to Das2 applications for the Plasma
Wave Group and its collaborators. Since Autoplot is a Das2 application,
it's easy to make these data sets available for plotting in Autoplot.
Note quite a few of these IDs were introduced for small studies and no
longer work. The group is working to add additional metadata to identify
working products. Data sources that identify an example range should
work for this range, and they will be adding automated tests to ensure
this.

Note the Das2 Server sends data to Autoplot via das2streams or QStreams.

  

##### parameters

  - **\_res** explicitly set the data loading resolution, for example
    \_res=10s will always request 10s data. This is confused with
    "resolution" and is supported because resolution will be reset to
    the axis resolution.

## Formats Read

The data source type is determined using the mime type in the HTTP
headers; if the mime type is not specified, then the file extension is
used. The data source type can be explicitly specified by prefixing the
URI with "vap" plus an extension followed by a colon. For example:
`vap+dat:`<https://autoplot.org/data/autoplot.asc> tells Autoplot to
treat the data returned by this URI as ASCII table formatted.

Once the data source type (most often the file format type) is
identified, the URI's parameter string is interpreted. Different URI
types may have different parameter arguments. Additional formats may be
added - see the tutorial for adding a data source to Autoplot:
[Adding\_Data\_Sources](Adding_Data_Sources.md "wikilink")

Note that if a parameters string is not given, the parameters in the
file or data stream can often be listed by clicking the folder icon to
the right of the address bar, or by pressing Tab to trigger completions.

### ASCII Table

The ASCII Table reader reads in a flat ASCII file with one record per
line. Each line of the file is identified as a record or non-record.
Autoplot URIs are the name of the ascii file and parameters that specify
how to parse the file, listed below. A
[GUI](help.md#ascii-editor "wikilink") is also provided that allows the URI
to be created graphically. This does not provide access to all the
available controls, but is much easier to use.

  - extensions: .dat, .txt
  - URI prefix: vap+dat, vap+txt
  - example URLs:

<ftp://nssdcftp.gsfc.nasa.gov/spacecraft_data/omni/omni2_1963.dat?column=field17&timerange=1963>  
<http://goes.ngdc.noaa.gov/data/avg/2004/A1050412.TXT?skip=23&timeFormat=$y$m$d+$H$M&column=E1&time=YYMMDD>  
<ftp://nssdcftp.gsfc.nasa.gov/spacecraft_data/omni/omni2_$Y.dat?column=field17&timerange=1963&timeFormat=$Y+$j+$H&time=field0&validMax=999>

#### Parameters

  - **fixedColumns** an optimized parser should be used since each row
    of the file has a fixed column width. By default the row are split
    into columns using a delimiter. The value may take several forms:
      - value contains ",": specify column locations as in "0-10,20-34"
      - value is int: specify the number of columns in each row. Actual
        may be less.
      - value is unspecified: the first row is split to determine the
        column locations.
  - **columnCount** override the number of columns.
  - **column** identifies the field in each record to treat as the
    dependent variable. By default the columns are named field0, field1,
    field2, etc.
  - **depend0** identifies a field as the independent variable.
  - **rank2** when in the URL indicates that the dataset produced should
    be a rank 2 dataset, and the number of fixed columns indicates the
    number of elements per row. When the value contains a colon (:),
    this indicates a range. The range is
    <firstColumn>:<lastColumn exclusive> or
    <firstColumn>-<lastColumn inclusive>.
      - value may be empty, meaning use all columns
      - 1: means the second row and up.
      - \-5: means the last five rows.
      - 20:24 means the four rows starting at the 21st row.
      - field3:field6 three columns
      - B\_x\_gsm-B\_z\_gsm three columns.
  - **depend1Labels** indicates the first record contains the labels for
    the rank 2 dataset. (<firstColumn>:<lastColumn exclusive>)
  - **depend1Values** indicates the first record contains the values for
    the rank 2 dataset (so it is displayed as a spectrogram).
    (<firstColumn>:<lastColumn exclusive>)
  - **skip** is an integer indicating the number of lines that should be
    skipped before processing begins.
  - **fill** is the number that indicates missing or fill data.
  - **timeFormat** specifies the time format, based on the Unix `date`
    command. "ISO8601" means the times are ISO8601 conforment, or use
    template with fields from
    [\#Wildcard\_codes](#wildcard-codes "wikilink").
  - **time** specifies the field that is the time record. This also sets
    the independent variable.
  - **delim** identifies the delimiter character. By default, the first
    record is inspected for commas, tabs and then whitespace.
  - **comment** prefix string that indicates records to ignore.
  - **fill** values to be treated as fill data.
  - **where** constraint for the records, for example with a timerange
    or containing a string.
      - where=field2.lt(100)
      - where=field2.eg(1)
      - where=field2.eq(rbspa) ordinal data can be used with eq.
      - where=field2.within(4+to+40)
      - where=field2.matches(Heater+Status+(On%7COff)) The plus is
        turned into a space, and %7C is a pipe character.
  - **label** concise label for the data
  - **title** one-line title for the data

#### Coming with v2017a

  - **X** **Y** **Z** Specify columns for X,Y,Z triples.

#### Notes

**column identifiers**

Columns are referenced by field identifiers, and the reader will create
valid identifiers when the header is not valid. So for example BX-GSM is
BX\_GSM, etc. "field0" will always refer to the first column, etc.

**range notation**

Ranges of columns are specified for several keywords, such as
depend1Labels and rank2. These are specified as follows:

  - **1-3** columns 1 through 3
  - **field1-field3** columns by generic field name
  - **BX-BZ** columns by field name (BX and BZ are example column
    identifiers, see notes above)
  - **1:4** columns 1 through 3 (colon is exclusive to be consistent
    with Jython, etc.)
  - **-5:-1** last columns, but not the very last one.
  - **-5:** last columns

### Comma Separated Values

Autoplot implements special handling needed for proper CSV files,
supporting for example multi-line strings containing commas for quoted
fields.

#### Arguments

  - **column=field4** which column to use as the dependent values
  - **depend0=field1** which column to use as the independent values
  - **skip=5** skip five lines before parsing
  - **bundle1=:** as with the ascii table reader, bundles of data can be
    read in at once to return a rank 2 dataset.

### Binary table

BinaryTableReader reads in datasets from binary files. Data are assumed
to be in records of fixed-length.

  - extension: .bin
  - URI prefix: vap+bin
  - example URI:
    vap+bin:<file:///media/mini/data.backup/examples/bin/fromidl.bin?type=float&fieldCount=2&column=1>
  - supports formatting: yes, rank 1 and 2, written out as doubles.
  - parameters
      - **byteOffset** int, number of bytes skip before reading the
        data. default is 0.
      - **byteLength** int, total number of bytes to read. default is
        the content length.
      - **recLength** int, the number of bytes per record.
      - **recOffset** int, the byte offset into the record.
      - **fieldCount** int, number of fields per record, when recLength
        is not specified. default is 1.
      - **column** int, field number for the dependent parameter, then
        recOffset is not specified.
      - **dims=\[48,64\]** int array, specify dimensions of rank 2 table
        within each record.
      - **rank2=:** string like ":" or "5:15" to specify the positions
        to read in as table.
      - **type** data type for the dependent parameter. double, float,
        long, int, short, byte, ubyte. Default is ubyte.
      - **depend0Offset** int, byte offset into each record for the
        independent parameter.
      - **depend0** int, field number for the independent parameter when
        depend0Offset is not specified. Default is no independent
        parameter and the byte offset is the independent parameter.
      - **depend0Type** data type for the independent parameter. double,
        float, long, int, short, byte.
      - **byteOrder** data type byte order (endianness). little or big.
        Default is little.
      - **validMin**, double minimum valid value
      - **validMax**, double, maximum valid value
      - **recFormat**, string, format specifier for each record.
          - "d,13f" 8-byte double followed by 13 (4-byte) floats
          - "i,s,ub" int, short, unsigned byte
          - "x,ub,ui" skip byte, unsigned byte, unsigned int

#### Use-cases

**Reverse engineer binary format** How to reverse engineer a binary file
with the binary reader:

  - Plot the data using the default 1-byte data.
  - Look for the courser repeating pattern, which are probably records.
    Timetags will typically identify records, because they are far from
    zero. Set recLength= this length. rank2 can be used to look at each
    records bytes in a spectrogram.
  - Look for a repeating pattern. This implies a data type. For example,
    if every fourth point is a peak, then try type=float. If the period
    is 15 bytes long, then try to identify the data type of the first
    field by using recLength=15\&type=float, recLength=15\&type=double,
    etc. Once the first field's data type is appearent, it's easy to see
    if the recLength is correct. Use recOffset to look at other bytes
    within each record.
  - If you're getting repeating data with large exponents, then try
    byteOrder=big
  - Once the byteOrder is determined, then it's much easier to identify
    fields.
  - Example where the query parameters were figured out by the above
    approach:
    [3](vap+bin:https://space.physics.uiowa.edu/plasma-wave/voyager/data/pra/v1790205?reportOffset=yes&rank2=6:262&recLength=528&type=ushort&byteOrder=big)

**UTF16 to ASCII** Netbeans writes out a Unicode file of its output
window using 16-bit unicode. (I could tell this because ascii values were interleaved with
zeros.) `iconv` failed to convert the file, so I tried converting it
with Autoplot:

```
ds= getDataSet('vap+bin:file:///tmp/output1249405460816')
# skip every other record, skipping the zeroth record.
ds2= ds[1::2]  
# save it out as a binary stream.
formatDataSet( ds2, 'vap+bin:file:///tmp/output1249405460816.txt?type=ubyte' )
```
### CDF

Reads in a variable from a [Common Data
Format](https://cdf.gsfc.nasa.gov/) file.

  - mime type: application/x-cdf-file (Note some servers advertise a
    content type of application/x-netcdf.)
  - extension: .cdf
  - Example URL:
    [4] vap+cdf:https://cdaweb.gsfc.nasa.gov/sp_phys/data/ace/swepam/level_2_cdaweb/swe_k0/2012/ac_k0_swe_20121229_v01.cdf?He_ratio
  - Supports formatting: Yes, rank 1 and 2, though not yet ISTP
    compliant.
  - Parameters
      - The parameter is the name of the cdf variable.
      - If not specified, a list of possible variables is given.
  - Wildcards and aggregation

In the following, we tell autoplot that the file name has a four-digit
year, a two-digit month, and a two-digit day. Then we ask it to plot
data on the day 20000109 using the time wildcards described in
[5](https://autoplot.org/autoplot/index.php/Main_Page#Wildcards_and_Aggregation).

The first part of the url is

<https://cdaweb.gsfc.nasa.gov/istp_public/data/polar/hyd_h0/>

the file part of the url is

```
2000/po_h0_hyd_$Y$m$d_v01.cdf?ELECTRON_DIFFERENTIAL_ENERGY_FLUX&timerange=20000101
```
to specify more than one day, use

```
2000/po_h0_hyd_$Y$m$d_v01.cdf?ELECTRON_DIFFERENTIAL_ENERGY_FLUX&timerange=20000101 - 20000103 (end is not inclusive)
```
to allow access to data that crosses a year boundary, use

```
$Y/po_h0_hyd_$Y$m$d_v01.cdf?ELECTRON_DIFFERENTIAL_ENERGY_FLUX&timerange=20001231 through 20010101
```
### NcML

NcML is an XML representation of netCDF metadata.

  - Example URL:
    [6](https://autoplot.org/autoplot.jnlp?https://autoplot.org/data/autoplot.ncml?skt_surface)

### SPASE

  - SPASE: If the URL or filename corresponds to a SPASE XML file with a
    NumericalData element, an attempt is made to plot the first
    AccessURL in the AccessInformation section. (In the future, default
    behavior will be to look for a URL in the Granule element and to use
    the information in the NumericalData node to populate the metadata
    tree.)

<!-- end list -->

  - Example URL:
    [7](https://autoplot.org/jnlp.cgi?https://autoplot.org/data/autoplot.xml)

### VAP

**VAP**: a **V**iRBO **A**uto**p**lot files save the state of the
application. This is just like a PowerPoint file which is your whole
presentation, or an HTML document which is the whole page of a browser,
this contains plot positions, data source references, and style
settings.

Note if a data source URI is entered on the address bar, the whole
application is reset to the new vap file settings. However, if File&rarr;&quot;Add
Plot From..." is used to access a vap, data URIs from within the vap are
accessible.

  - Example URL:
    [8](https://autoplot.org/jnlp.cgi?https://autoplot.org/data/autoplot.vap)

### Das2Streams and QStreams

  - Das2Streams and QStreams: Das2Streams are self-describing, streaming
    format developed and used by the Plasma Wave Group at the University
    of Iowa. "Streaming" is the requirement that at any point along the
    stream, you have all the data you need have a valid and complete
    stream. They are generally useful for serializing and deserializing
    data in das2's internal data model, and Autoplot's QDataSet model.
    The design goal is any dataset that can be represented in Autoplot
    can be serialized into a das2Stream. "QStream" refers specifically
    to a das2Stream with a QDataSet on it, and has the extension .qds.
    Legacy das2Streams have a .d2s extension.
  - Mime type: application/x-das2stream
  - Extensions: .d2s .das2stream .qds
  - Example URLs:
    [9](https://autoplot.org/jnlp.cgi?https://autoplot.org/data/proton_density.qds)
    [10](https://autoplot.org/jnlp.cgi?https://autoplot.org/data/proton_velocity_rtn.qds)
  - Supports Formatting: yes, rank 1, 2, 3 to QStream
  - parameters
      - arg\_0 is the named parameter within the stream, if not
        specified then default parameter is used.
  - output parameters
      - **type**
          - **binary** means format to binary stream

### CEF File Reader

Reads data in the [Cluster Exchange
Format](http://www.space-plasma.qmw.ac.uk/csds/welcome.html) CEF for
Cluster. This is experimental, but should work fine for at least 1-D
data.

  - Example URL:
    [11](https://autoplot.org/jnlp.cgi?https://autoplot.org/data/C1_CP_CIS-CODIF_HS_H1_PSD__20010226_050000_20010226_061000_V070529.cef?3d_ions__C1_CP_CIS-CODIF_HS_H1_PSD)

### netCDF file reader

Reads in a variable from a
[netCDF](http://www.unidata.ucar.edu/software/netcdf/) file.

  - mime type: application/x-netcdf
  - extension: .nc, .ncml, .hdf5, .h5
  - Example URL (described on the [unidata web
    page](http://www.unidata.ucar.edu/software/netcdf/examples/files.html)):
    [12](https://autoplot.org/jnlp.cgi?http://www.unidata.ucar.edu/software/netcdf/examples/tos_O1_2001-2002.nc?tos)
  - parameters
      - The parameter is the name of the netcdf variable.
      - If not specified, a list of possible variables is given.

Times can be encoded in NetCDF files as ISO8601 times, using a 2-D array
of characters. The second dimension should be between 14 and 30
characters, for example 20110101T00:00 is 14 chars long,
2011-Jan-01T00:00:00.000000000 is 30 characters long.

### HDF5 (HDF) files

  - extension: .hdf5, .h5

The NetCDF reader has the ability to read many HDF5 files as well. There
are a few data schemes (grids) which will are not readable. Note older
HDF files are probably not readable.

### OPeNDAP

Reads in data from [OpenDAP](http://opendap.org) servers. When data
files are served from an OPeNDAP server, subsets of a variable in a file
may be requested.

  - mime type:
  - extensions: .dds and .dods
  - Example URL:
    [13](https://autoplot.org/jnlp.cgi?http://cdaweb.gsfc.nasa.gov/cgi-bin/opendap/nph-dods/istp_public/data/genesis/3dl2_gim/2003/genesis_3dl2_gim_20030501_v01.cdf.dds?Proton_Density)
  - Parameters
      - The parameter following the question mark is the name of the
        OPeNDAP variable. If not specified, a list of possible variables
        is given.
      - Numbers in brackets optionally control the cadence in the
        notation \[min:step:max\] or \[min:max\]. See the [OPeNDAP/DODS
        documentation](http://www.opendap.org/user/quick-html/quick_1.html).

### Excel Spreadsheet

Data is read from a Microsoft Excel spreadsheet using [Jakarta
POI](http://poi.apache.org/).

  - mime type: application/vnd.ms-excel
  - extension: .xls
  - Example URL:
    [14](https://autoplot.org/jnlp.cgi?https://autoplot.org/data/autoplot.xls?column=A)
  - Supports formatting: yes, rank 1 and 2
  - parameters
      - **column** is the name of the column (e.g. "C"), and in brackets
        the starting and ending rows.
      - **depend0** is the name of the column identifying the X values
        for each value.
      - **plane0** is a third parameter. Use with caution, this will
        probably go away.
      - **firstRow** is the first row to read (1 is the first row)
      - **sheet** is the name of the sheet within the workbook to read.
      - **recCount** limit the number of records to read.

### TSDS

Data is read from a [TSDS](http://tsds.net) server.

  - Mime type:
  - Extension: tsds (use vap+tsds:<http://>...)
  - Example URL:
    [15](https://autoplot.org/jnlp.cgi?vap+tsds:http://timeseries.org/get.cgi?StartDate=20030301&EndDate=20030401&ext=bin&out=tsml&ppd=1440&param1=OMNI_OMNIHR-26-v0)
  - parameters
      - None
  - Dependencies
      - BinaryDataSource

### FITS

Flexible Image Transport System
[16](http://fits.gsfc.nasa.gov/fits_intro.html). This is using a library
that limits what it can access. Soon a new implementation will enable
more data sources.

  - extension: .fits .fts
  - Example URLs:
    [17](https://autoplot.org/jnlp.cgi?https://autoplot.org/data/hsi_qlimg_5050601_001.fits)
    [18](https://autoplot.org/jnlp.cgi?https://autoplot.org/data/hsi_fsimg_5050612_001.fits)

### Images

This data source reads images using java's ImageIO library. The images
are mapped to a QDataSet internally.

  - mime type:
  - extension: .gif .jpg .png

<!-- end list -->

  - Example URL
    [19](https://autoplot.org/jnlp.cgi?https://autoplot.org/data/image/Capture_00158.jpg?channel=greyscale)

<!-- end list -->

  - Parameters
      - **channel** specifies how components should be combined to
        produce the rank 2 dataset.
          - If channel is not specified, then a rank 3 dataset with
            original image channels results.
          - Example channels include:
          - red, green, blue
          - hue, saturation, value (brightness)
          - greyscale is faster to calculate than value
      - **plotInfo=0** grab the axis information from the richPng
        metadata. See <https://autoplot.org/richPng>. (Note log=1 doesn't
        work with 24-bit color images.)
      - **xaxis=\[valmin,pixmin,valmax,pixmax\]** apply the axis
        transform on the horizontal axis.
      - **yaxis=\[valmin,pixmin,valmax,pixmax\]** apply the axis
        transform on the vertical axis.
      - **fog=90** apply 90% opaque fog to the image before displaying.
      - **blur=5** apply a 5=pixel wide blur kernal
      - **rotate=0** rotate the image clockwise degrees.

### Wav Files

Plots the waveform within wav files.

  - extension: .wav
  - supports formatting: yes, rank 1 to 16 bit PCM. xtags must be
    seconds or UT time.

Example URLs:
[20](https://autoplot.org/jnlp.cgi?https://autoplot.org/data/trainMono.wav)
See also [\#Multiple\_plot\_panels](#multiple-plot-panels "wikilink")

  - Parameters:
      - **channel** the channel to plot (by default, only the 0th
        channel is plotted as a time series).
      - **offset** the number of seconds into the file to start at
      - **length** the number of seconds to plot

### Jython Files (jyds)

Jython scripts can be used to create new datasets by combining other
datasets. See also [https://autoplot.org/scripting
scripting](https://autoplot.org/scripting_scripting "wikilink").

  - extension: .jyds
  - Example URLs:
      - Plot the difference between two images:
        [21](https://autoplot.org/jnlp.cgi?https://autoplot.org/data/imageDiff.jyds)
      - Read a complicated ASCII file and plot the result:
        [22](https://autoplot.org/autoplot.jnlp?https://autoplot.svn.sourceforge.net/svnroot/autoplot/autoplot/trunk/JythonDataSource/src//wdc_kp_ap.jyds)
      - More examples:
        [23](https://autoplot.svn.sourceforge.net/svnroot/autoplot/autoplot/trunk/JythonDataSource/src/)
      - Demonstrates time series browse:
        [24](https://autoplot.org/jnlp.cgi?https://autoplot.org/data/tsbDemo.jyds)
  - Parameters:
      - <name>=<expr> defines parameters for use within the script.
        Scripts use getParam method to get method parameters.
      - <expr> after running the script, this expr is evaluated and
        plotted. The default expression is "data".

Example Script (/home/user/script.jyds):

```
amplitude= getParam( 'amp', 1.0, 'the amplitude of the waveform' )
data= amp * sin( linspace( 0, PI*2, 100 ) )
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

`vap+jyds:file:///opt/project/cassini/new_hfr_level2_level3/2010_091_180/n2/P2010118.17?script=file:///home/jbf/project/cassini/jared/autoplot/readL2Files3.jyds`

Here the "script=" switch points to the script. This is useful to define
a parser for a file type, which allows aggregation to be used.

### Inline

Data and short jython commands can be embedded in a URI for
demonstrations or quick-and-dirty annotations. An editor is
automatically generated for scripts. Any parameter read from the
getParam function will be provided in the GUI.

  - extension (prefix): vap+inline:
  - Example URIs:
      - vap+inline:1,2;3,4;5,6;7,2;9,0 \# five 2-D points
      - vap+inline:1,3;2,4 \# the points \[1,3\] and \[2,4\]
      - vap+inline:ripples(100,100) \# demo function from jython support
      - vap+inline:linspace(0,1,100),linspace(0,1,100),ripples(100,100)
        \# jython expressions allowed
      - vap+inline:ripples(100,100)+randn(100,100)/10 \# jython
        expressions allowed
      - vap+inline:ripples(100,100)+randn(100,100)/10\&RENDER\_TYPE=nnSpectrogram
        \# specify QDataSet properties
      - vap+inline:getDataSet('<https://autoplot.org/data/autoplot.ncml>')\&RENDER\_TYPE=nnSpectrogram
        \# "decorate" other datasets (TODO: bugs when ? in URI)

## PNGWalk Tool

The PNG Walk Tool provides efficient browsing of a series of images.
Autoplot has a menu item for generating PNG walks. More information
about this can be found at [PNG\_Walks](PNG_Walks.md "wikilink").

## Run Batch Tool

The Run Batch Tool generates inputs for Jython scripts, and manages
batch runs. More info at [batch](batch.md "wikilink").

## Annotations

Annotations are additional labels that can be added to the canvas. More
information about this can be found at
[Annotations](Annotations.md "wikilink").

## Axis Autorange Hints

Autoplot allows additional hints when autoranging, such as the center of
the autorange or the width. See
[AxisAutoRangeHints](AxisAutoRangeHints.md "wikilink").

## Managing the Cache

Autoplot caches remote files to the local directory
$HOME/autoplot\_data/fscache. Not only is having local copies necessary
for many formats, such as CDF files, but this allows Autoplot to be used
when no internet connection is available. This area will grow as more
data is read, and presently there is no mechanism to automatically
remove infrequently used resources. Autoplot provides a GUI that can be
used to manage this cache, see \[menubar\]&rarr;Tools&rarr;Cache&rarr;&quot;Manage Cached
Files."

### Data Providers

#### ro\_cache.txt

Data providers will want to know that you can set up a link between your
local file cache and the local file location of the data, so that the
local cache is not used. For example,
<http://jfaden.net/~jbf/1wire/data/furnace.$Y$m$d.d2s> is a resource I
want to make available to everyone, but in
/home/jbf/public\_html/1wire/data I have the data locally. In my local
file cache, I would use the link file to avoid downloading the data to
my local cache, making a second copy. When Autoplot looks for the
resource, it will use files from here before downloading.

```
jfaden.net> cat /home/jbf/autoplot_data/fscache/http/jfaden.net/~jbf/ro_cache.txt
/home/jbf/public_html
```
#### keychain.txt

Often we need to run batch processes, and the keychain.txt allows data
providers to store credentials for batch processing. Note only a minimal
amount of thought has gone into this, so please be careful with these
facilities and use them at your own risk\!
[developer.headless](developer.headless.md "wikilink") talks about this
more.

## Applet

  - The Applet mode is no longer supported \*

The Autoplot applet requires Java 1.7 or higher and that your browser
has Java enabled. The applet typically takes less than 2 seconds to load
if the background pre-loading is successful. If the background
pre-loading is not successful, the applet will take about 10 seconds to
load the first time.

If you are having problems starting the applet, see the [Applet
Guide](applet_guide "wikilink") or ask for help by sending an email to
the Autoplot forum at <http://groups.google.com/group/autoplot>.

The Autoplot applet has a number of features that are disabled, due to
security restrictions enforced by web browsers. When using the applet,
you cannot save data to disk or save a pdf or png file of your image.
For more information on Java applets, see
<http://en.wikipedia.org/wiki/Applet> or <http://java.sun.com/applets/>.

# Server Mode

Autoplot provides a server mode, where external programs can connect to
Autoplot for plotting and data reading services. See
<https://autoplot.org/server>. This is not well-used, and the two
following modes might be more useful.

Autoplot can be run from the command line to produce graphics for
CGI-based websites.

It can also be run as a servlet with a Java web server such as
Apache/Tomcat. A war file is available which works with these servers.
See <https://autoplot.org/servlet_guide> .

# Abbreviations

  - CDF Common Data Format
  - CEF Cluster Exchange Format
  - JYDS Jython Data Source. Jython script used to load data into
    Autoplot.
  - JY Jython Script. Jython used to operate Autoplot as a batch mode.
  - RTE Run-Time Exception. This is an error that occurs that the user
    should not see, and is given the opportunity to submit the bug to
    developers.
  - RFE Request For Enhancement, or feature request.
  - TCA Time Correllated Axes, which are axes with ephemeris information
    attached to each tick.
  - TSB Time Series Browse capability, which is the ability for a data
    source to load data at different time intervals.

See also <https://autoplot.org/glossary>

# Logging

Autoplot uses multiple-channel logging, so instead of printing
everything to the console, messages are sent to named channels with
verbosity levels. This means that normally Autoplot quietly processes,
hiding thousands of messages which are useful for debugging problems
when things don't work. The verbosity is controlled on the console tab,
via the "Console Settings" button. Pressing this will show a set of
loggers and allow their verbosity to be controlled.

For example, suppose you are developing CDF files for your instrument,
but things are not working as you would expect. You define a valid range
with the VALID\_MIN and VALID\_MAX metadata, but Autoplot is not
respecting these. The verbosity of the logger "apdss.cdf" (Autoplot
dataset source) is increased to FINER, meaning messages issued while the
CDF file is loaded at the FINER, FINE, INFO, and WARNING levels will be
displayed. Load the CDF file again and a message showing the problem
(maybe that VALIDMIN should have been used) is now visible.

The log console also has an option to highlight messages matching a
search string. Often you'll increase the verbosity, getting many
messages, and you'll be interested in one message. This is a regular
expression, but simple strings that don't contain brackets or other
special symbols should work fine.

Note too that when Autoplot matches a string, it will grab the stack
trace showing where the message is issued in the source code. This can
be useful when developing Jython Scripts, as the Jython script location
can be found in the stack trace as well. Any messages issued with the
simple "print" command will appear in the channel "console.stdout".
Presently the tooltip for the "AP\>" prompt contains the stack trace,
and look for "pycode" to find the line number.

