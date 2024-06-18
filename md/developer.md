Purpose: Links for miscellaneous developer pages.

# Development Versions

The development versions are released "early and often" to accelerate
maturing of code. They are located here:
[Autoplot\_Change\_Log](Autoplot_Change_Log.md "wikilink")

  - <http://autoplot.org/jnlp/latest/autoplot.jar> is the "production
    version" which is done roughly monthly, has had extensive testing,
    and passes all Jenkins tests. If a new problem is discovered by
    someone using this, I stop what I'm doing until this is fixed.
  - <http://autoplot.org/jnlp/devel/autoplot.jar> is the "development
    version" which is made roughly weekly, or if a change is requested
    by someone. Typically all the Jenkins tests are passing, but new
    problems may be encountered and testing is not as thorough. This is
    the version that I typically use as I work on campus.
  - <https://ci-pw.physics.uiowa.edu/job/autoplot-release/lastSuccessfulBuild/artifact/autoplot/Autoplot/dist/autoplot.jar>
    is the automatic "nightly" build (often more often) which is used to
    get a new feature out for immediate use or fix a problem, but has
    typically no human testing. Jenkins tests are run against this, but
    a test can fail and this release will be available regardless.

The Jenkins interface is at
<https://ci-pw.physics.uiowa.edu/job/autoplot-release/>

# Use methods

Autoplot is typically run as a "thick client" on the scientist's
workstation. The \~25MB application is downloaded and run on top of the
Java platform. This is not the only way to use the application, however,
and this section covers other modes.

## Servlet

See [servlet\_guide](servlet_guide.md "wikilink"). Autoplot can be run in a
server mode in which case the user specifies a URL to file in a web
browser and a PNG image is returned. Notes for developers of the servlet
are here: [developer.servlet](developer.servlet.md "wikilink")

## WebStart

See [webstart\_guide](webstart_guide.md "wikilink").

## Jython

Autoplot uses Jython (Python in Java) for scripting data sources and the
application itself. Selecting Options-\>Enable Feature-\>Script Panel
will reveal a tab named "script". See
[developer.scripting](developer.scripting.md "wikilink").

## IDL/MATLAB

See [developer.idlMatlab](developer.idlMatlab.md "wikilink").

## Command line

### WebStart

To start Autoplot from the command line, use

`javaws&nbsp;`&lt;http://autoplot.org/autoplot.jnlp&gt;

To start Autoplot with an initial URI in the address bar, use the CGI
script on Autoplot.org which resolves to a jnlp containing the URI:

`javaws&nbsp;`&lt;http://autoplot.org/autoplot.jnlp?http://autoplot.org/data/autoplot.cdf?Magnitude&gt;

Note, however, that as of 2018 it looks like Webstart is no longer going
to be supported with Java 11 and up. Autoplot currently supports Java 7
and will soon require Java 8, but webstart support will be removed at
some time in the next five years.

### Non-Webstart

Note: documentation needs URLs for non-64-bit libcdfNativeLibrary binary
files. Note on note: in the current version, vap+cdfj will resolve
vap+cdf if the native libraries aren't available.

`wget&nbsp;-O&nbsp;/tmp/ap/autoplot.jar&nbsp;&nbsp;`&lt;http://autoplot.org/jnlp/latest/autoplot.jar&gt;  
```
java -jar /tmp/ap/autoplot.jar  # see that Autoplot works
```

#### Command-Line Arguments

You can launch with command line arguments as well, like so:

`java&nbsp;-cp&nbsp;autoplot.jar&nbsp;org.autoplot.AutoplotUI&nbsp;`&lt;http://autoplot.org/data/autoplot.cdf?Magnitude&gt;  
```
java -cp autoplot.jar org.autoplot.AutoplotUI --help
```

#### Notes on data server

The following documentation refers to the application used to serve
data. This needs to be cleaned up.

To see command line options, type

``` bash
java -Djava.awt.headless=true -cp autoplot.jar org.autoplot.AutoplotServer
```
`
```

#### Linux

On Linux systems the default install of Java is not complete. On a
Debian-based system, use

```
apt-get install openjdk-8-jre
```

and call java using

```
/usr/lib/jvm/java-8-openjdk/bin/java
```

``` bash

wget "http://autoplot.org/jnlp/latest/autoplot.jar"

java -Djava.awt.headless=true -cp autoplot.jar org.autoplot.AutoplotServer -u "http://autoplot.org/data/autoplot.cdf?BGSM" -f png -o BGSM.png
```
`
```

#### Mac

``` bash
curl http://autoplot.org/jnlp/latest/autoplot.jar > autoplot.jar

# Test operation:
java -Djava.awt.headless=true -cp autoplot.jar org.autoplot.AutoplotServer -u "http://autoplot.org/data/autoplot.cdf?BGSM" -f png -o BGSM.png
```
`
```

will create [:Image:BGSM.png](:Image:BGSM.png.md "wikilink")

# Development

## Feature requests

Autoplot was initially developed as part of a NASA VxO grant for the
ViRBO project. Development will continue and we welcome requests for new
features. Submit requests to <http://sourceforge.net/projects/autoplot>
or send an email to the list given at
<http://groups.google.com/group/autoplot>.

## Report a bug

The preferred method of reporting a bug is through the [sourceforge bug
tracker
system](http://sourceforge.net/tracker/?atid=970682&group_id=199733&func=browse).
The feature "Log Console" records internal logging messages and catches
stdout and stderr. This information is useful for debugging, and the
console's Save button saves these messages to a file.

## Automated Testing

Autoplot uses Jenkins for managing automated testing and reporting.

  - Once each night and shortly after any commit of source code,
    hundreds of tests are performed to detect if a change has been made
    that breaks some aspect of the system. These are currently broken up
    into roughly 50 functional areas in these the tests here:
    **<https://papco.org/jenkins/>**. These make static images of vap
    products, test layout, test the IDL/Matlab interface, do PNGWalk
    generation, etc. This is not a thorough test, but it often catches
    errors that before would have been reported in a desperate email the
    week before a meeting.
  - <https://ci-pw.physics.uiowa.edu/> also does FindBugs analysis that
    analyses the code for suspicious and oddly-worded code, and has
    identified a number of mistakes as well.
  - <https://ci-pw.physics.uiowa.edu/job/autoplot-release/> provides a
    convenient means for making one-of releases and greatly simplifies
    the release process.

## Manual Testing

We have a script for human-driven testing here:
[developer.tests](developer.tests.md "wikilink"). These are procedures for
tests that don't translate into automatic tests, such as GUI operations
and multiple-platform testing.

## Email List

For discussion about Autoplot, send email to autoplot@googlegroups.com.
You may browse the email archive at
<http://groups.google.com/group/autoplot>

## Presentations

  - AGU 2010 poster: [ppt](:Media:agu2010.ppt.md "wikilink")
  - QDataSet Poster talks about how data is represented:
    [ppt](:Media:InsideAutoplot-20110531.ppt.md "wikilink")

## Source Code

  - The source code for Autoplot is located at
    <http://autoplot.svn.sourceforge.net/viewvc/autoplot/autoplot/> (GPL
    license)
  - Instructions for building are located here: [Build from
    Source](Autoplot_from_source "wikilink") (with notes for Eclipse,
    NetBeans, and Ant)
  - svn at
    <https://autoplot.svn.sourceforge.net/svnroot/autoplot/autoplot/>
    (and add "trunk" for the main trunk, or you'll get all the tagged
    versions too.)
  - The source code for das2 library is located at <http://das2.org>.
    (GPL license)
  - Details about the internal workings of das2 may be found on their
    [wiki](http://www.das2.org/wiki/)
  - Details about the QDataSet data model may be found at
    [QDataSet](QDataSet.md "wikilink")

## List of URIs for Testing

Here is a [List Of URIs](Test_dataset_urls.md "wikilink") for testing.
These include links that demonstrate that things work, and may quickly
demonstrate sources that don't work. Feel free to add to the list,
adding a comment if it doesn't work properly.

## Notes on Debugging

Here is a [place](developer.tipsAndTricks.md "wikilink") for thoughts on
techniques for debugging, for the senior developer's reference, and for
those who would like to get into the code.

# Who's Using Autoplot

  - [ViRBO](http://virbo.org) to view data files and data streamed from
    its time series server
  - [VMO](http://vmo.gsfc.nasa.gov) to view granules of data using
    webstart mode
  - [RBSP Emfisis instrument
    team](http://www-pw.physics.uiowa.edu/rbsp/) to look at data packets
    coming from GSEOS, and eventually science analysis
  - [Juno Wave instrument team](http://www-pw.physics.uiowa.edu/juno/)
    look at level zero data, science analysis
  - Scientists at U. Iowa working on Cassini use Autoplot to read data
    into Matlab for analysis
  - [RBSP ECT instrument team](http://www.lanl.gov/) as a part quality
    control workflow, and eventually science analysis
  - [Space Physics Data Facility](http://spdf.gsfc.nasa.gov) to view
    data using autoplot in webstart mode
  - [Radio and Plasma Wave Group at The University of
    Iowa](http://www-pw.physics.uiowa.edu/) For analysis, publication
    graphics, and custom applications for verifying and working with
    data
  - [The ACE Science Center](http://www.srl.caltech.edu/ACE/ASC/) to
    generate server-side graphics
  - [Center for Space Physics at Boston
    University](http://spacedata.bu.edu/mics_k1.html) for browsing
    CAMMICE/MICS data
  - [Virtual Model Repository](http://vmr.engin.umich.edu/) to generate
    server-side graphics using command-line server
  - [APL](http://www.jhuapl.edu) is using Autoplot internals to develop
    applications
  - [EMWRAP](http://aten.igpp.ucla.edu/emwrap/index.php/Main_Page) at U.
    Iowa is using Autoplot for display and testing of science products.

# Design Documents

## Misc.

  - [developer.idlMatlab](developer.idlMatlab.md "wikilink") IDL/MATLAB
    interface
  - [developer.novice](developer.novice.md "wikilink") discussion of a
    basic/expert user mode.
  - See [Special:Allpages](Special:Allpages.md "wikilink") for a list of
    all pages on this wiki.
  - [QDataSet](QDataSet.md "wikilink") beginnings of a QDataSet tutorial
    and QDataSet technical description. QDataSet is the internal data
    model.
  - [developer.scripting](developer.scripting.md "wikilink") Help with
    scripting
  - [developer.guiConventions](developer.guiConventions.md "wikilink") GUI
    Conventions
  - [developer.URI\_syntax](developer.URI_syntax.md "wikilink") Describes
    Autoplot data set URI construction, rules, and conventions.
  - [developer.URI\_completion](developer.URI_completion.md "wikilink")
    Description of the completion engine used to create valid URIs, to
    assist humans and perhaps allow for data mining...
  - [developer.Title\_and\_Label\_Templates](developer.Title_and_Label_Templates.md "wikilink")
    proposal for how titles and labels can use templates to insert
    metadata.
  - [developer.inlineData](developer.inlineData.md "wikilink") proposal for
    URIs that contain data for quick plotting and tags.
  - [developer.axis\_auto\_property](developer.axis_auto_property.md "wikilink")
    proposal for adding "auto" property to axis so autoranging is finely
    controlled.
  - [developer.DataSource\_API\_Change](developer.DataSource_API_Change.md "wikilink")
    proposed for DataSources that would allow for database and other
    non-file-based DataSources.
  - [developer.panel\_rank\_reduction](developer.panel_rank_reduction.md "wikilink")
    spec for how panels can reduce data that's handed to them, and
    implementation notes.
  - [developer.userDirectory](developer.userDirectory.md "wikilink") layout
    of the user data directory. Right now this is just data, but I want
    to put other things here too.
  - [developer.bindingTypes](developer.bindingTypes.md "wikilink") initial
    thoughts about the need for more binding types.
  - [developer.helpsets](developer.helpsets.md "wikilink") conventions for
    developing and maintaining help documents.
  - [developer.datasourceURI.extensions](developer.datasourceURI.extensions.md "wikilink")
    propose new features for data sources
  - [developer.dataset.filters](developer.dataset.filters.md "wikilink")
    work out spec for user-defined filters for QDataSet, Autoplot and
    TSDS.
  - [developer.python.indexing](developer.python.indexing.md "wikilink")
    document the logic for PyQDataSet.\_\_getItem\_\_ index parameter.
  - [developer.addingHelpFiles](developer.addingHelpFiles.md "wikilink")
    adding help documents
  - [developer.respondingToEvents](developer.respondingToEvents.md "wikilink")
    need to establish conventions for how to respond to events
    (valueIsAdjusting, etc).
  - [developer.multiDataSetConventions](developer.multiDataSetConventions.md "wikilink")
    thoughts about conventions for data readers to read in Z(X,Y) from
    any data source.
  - [developer.bugSequences](developer.bugSequences.md "wikilink")
    Sequences which have been known to demonstrate bugs. These are
    probably good to check periodically.
  - [developer.autolayout](developer.autolayout.md "wikilink") New version
    of the autolayout that removes gaps and overlaps between panels.
  - [developer.logging](developer.logging.md "wikilink") clean-up of the
    under-used and inconsistent logging system.

## Autoplot 2012b

Autoplot 2012a has had a feature set that hasn't required a new vap
version. This is in part because I was being lazy, because I can't
guarantee that new versions are pushed out. It's final version was 1.07.
There have been a number of feature requests that affect the vap, and I
should do these all at once.

### URIs for Renderers

For a while it's been clear that a more generic way of controlling plot
rendering is needed. Currently, properties are added to the vap, readers
and writers are made to handle those properties, and bindings made to
implement the properties in das2. This works fine when a small set of
properties is controlled, but as the number of degrees freedom
increases, so must the complexity. Take for example a contour plot. This
is clearly going to need a string to control contour positions. Then
take the request to have separate fill-to-reference lines for above and
below (grey if below 0.0V, red if above 5.0V). Last consider that we
want to allow custom renderers that need some generic control. For all
the reasons URIs have been effective for loading data, they will be
effective for painting data. Note too, that ideally users would never
see these, they are simply there to provide flexible control that allows
Autoplot to delegate responsibility for implementing graphics to third
parties.

So for example:

```
rend+contour:levels=10,20,30,40&fillBelow=lightGrey,grey,darkGrey,red
rend+series:fillAboveColor=red&fillAboveReference=5.0V&fillBelowColor=grey&fillBelowReference=0.0V
```

I'd like to get this in place for people that want to play with it, but
it will be limited until there are GUIs, etc, and that's a big job. So
I'll be adding things to the style node as well for now.

### Axis Position / Overlay Plots, not just plotElements

We will support two plots being drawn on top of one another, so that two
Y axis can control plotElements. das2 already supports this, but it is
not saved in the vap.

### Fill Above UpperReference, Fill Below LowerReference

To implement warning levels such as grey if below 0.0V, red if above
5.0V. The legacy fill-to-reference will still be supported as a third
property that is drawn first.

### Slicer Type

Some time I just need to put this squirrelly feature in, and see what
problems it creates

### Annotation Objects

To support titles and plot annotations, a set of annotations for
decorating a plot. These would include:

  - canvas title (text)
  - callout for features (arrows, lines, text)

### Colors in Vap Files

I just noticed that blue is value="\#ff" in the vap file.
ColorSerializeDelegate should provide the names of common colors.

### org.das2 in Vap Files

Also, there are things like

<property name="colortable" type="enum:org.das2.graph.DasColorBar$Type" value="color_wedge"/>

We should get rid org.das2 references from the vap file.

### Override Units

Reiner would like to be able to override units in the Data tab, the same
way you can override valid range and fill. This would help out ascii
files, which have limited support for units.

### Physical Units system

It would be nice to finally implement a physical units system, so that
cm divided by sec would be cm/s... We've talked about doing this for
years.

### allow XSLT modifiers to create DOMs

Bob would like to use XLST to specify DOMs, so you could say
foo.xslt\&uri1=...\&uri2=...\&uri3=...

### Declare TimeSeriesBrowse connections

Right now these are calculated automatically at runtime. They should
probably be explicit in the file. For example, Reiner has products that
would have no time axes, but need to run on pngwalks.

## Autoplot 2011

It would be useful to identify the feature set of the Autoplot2011
branch.

### TimeSeriesBrowse

  - TimeSeriesBrowse will reconnect itself to application timerange if
    the result is not a timeseries.
      - (TODO: this doesn't work when you reload the file.)
  - Automatic aggregation detection. Plotting "20100101.dat" will look
    for "$Y$m$d" and use the aggregation automatically. \[NOTYET\]

### Data Sources

  - pure-java cdf reader handles ".cdf" (NOT YET)
  - inline specification of filters, such as
      - vap+bin:[file:///tmp/foo.wav?column=1\&recLength=3|histogram](file:///tmp/foo.wav?column=1&recLength=3%7Chistogram)
        (NOT YET)
  - introduce the general way to specify depend datasets, such as: (NO,
    2012)
      - vap+bin:<file:///tmp/foo.dat?recLength=45&depend0.column=0&column=2>
        , instead of
      - vap+bin:<file:///tmp/foo.dat?recLength=45&depend0offset=0&column=2>
  - introduce other standard parameters for easily modifying the
    dataset, like title, label, rendertype, etc.
  - csv is handled by 3rd party and correct csv reader. (YES, DONE)

### Graphics

  - legend position, and legend outside plot (DONE, though not yet in
    vap)
  - plots.xaxis.ticklen (DONE)
  - improve cadence logic, there's a "corner case" of just four corners
    that I don't handle, where the histogram resolution is too fine so
    the non-zero peaks are spaced regularly.
  - new annotations in labels
      - %{VERSION} from QDataSet
      - %{CONTEXT} shows any context, e.g. slice position, associated
        with a dataset.
      - %{COMPONENT} shows slice positions, components, or additional
        processing.
  - Time Axis annotations (ephemeris, TCA. It goes by a number of
    names).
  - RGB image renderer (DONE)
  - Events bar renderer (DONE)
  - rank 0 renderer that allows data to be reported. (DONE, digital
    supports this)
  - digital renderer used for enumeration data.
  - Improve list of available renderers to only those that handle
    dataset scheme, checkmark next to active render type.

### GUI

  - Optional x-axis (time) range controller on canvas tab. (done)
  - Option to use $Y-$j day of year for ticks instead of $Y-$m-$d (done)
  - Links over to help documentation (done)
  - Flip y axis (Garcia) (NOTYET)
  - Labels option to only face two directions, many publishers require
    this. (Bill K.) (NOTYET)

### Layout

  - Automatic layout inserts extra spaces for multiline plots and axes.
    (Need to specify how this is going to work.)
    [developer.autolayout](developer.autolayout.md "wikilink")
  - Handle stack plots that don't have x ticks.
  - plot above/plot below, insert plot below, insert plot above. (done)
  - convert current plot to M by N
  - easy way reduce/enlarge height

### DOM version 1.8

Everyone has figured out there there are lots of accessible Das2
features that don't make it into the DOM. Bob has requested that
"everything" be in the DOM, and to the extent that this is possible,
I'll do this. These features include:

  - legend position (NOTYET)
  - plots.xaxis.ticklen (NOTYET)
  - overriding cadence (NOTYET)
  - Flip y axis (Garcia)
  - Labels option to only face two directions (THIS MISSED the 2011
    branch, but is a trivial change. I'll probably introduce it for
    2011a\_8 as a user preference.

### User Options

  - basic/expert mode hides large sections of the DOM to help to get
    started. \[DONE\]
  - basic mode will:
      - hide the controller nodes
      - show \[?\] in section labels to link to documentation
      - hide the "data" "script" "console" tabs
      - show "add plot from...cdaweb..." in basic mode
  - expert mode will:
      - show the "data" "script" "console" tabs
      - show \[?\] in section labels to link to documentation
  - see [developer.novice](developer.novice.md "wikilink")

## Autoplot 2010

### Major Limitations of Current Autoplot

A couple of easily described limitations of autoplot present a nice use
case and hopefully help to specify the beefy version.

  - Only one dataset can be viewed at a time.
      - no stack plots
      - no overplots
      - no correlation plots
  - Some properties can be changed, but changes are not saved.
      - row, column layout
      - contour numbers

The more configurable the application becomes, the more pressing the
need for a beefy system for storing application state. This has been a
lingering problem with das2 for years.

### Scalability from Delegation

The way complex state is achieved is to delete object state storage out
to the objects. The application knows how to store itself by delegating
to the objects that implement it.

### DOM Tree for Autoplot

Upper-case nodes represent nodes with children, lower case nodes are
leaf nodes that can be set. 'Italics' are simply comments about the
node. An example node may exist below a parent to show an example child,
and an ID will show how it might be accessed.

*Style* is a node below many nodes, which contain properties that affect
the application view but not the model. DOMs may be deserialized while
ignoring these, leaving user preferences in place. Further "Style
Sheets" may be applied to a DOM with affecting the interpretation the
application state.

EmSpec is a string like *50%+5em*, which are to be interpreted relative
to a column or row. *20%* means 20% of the way from min to max. *5em*
means 5 ems, the height of the font. *20px* or *20pt* means 20 pixels.

Propose/Specify DOM for autoplot application.

{{\#tree:openlevels=0|root=Autoplot DOM Tree:|

  - Application
      - Style
          - dateformat '%Y-%j', spec to use for formatting dates.
          - cachesize, float, size in megabytes of the file cache.
          - locale, string, localization code.
          - antialias, boolean, do antialias where possible
          - textAntialias, boolean, do antialias text
          - visualCues, boolean, animate state transisions, etc.
          - autoContext, boolean, allow context plot.
          - autoRange, boolean, autorange data.
          - focus, string, object id having focus
      - DataSetSelector
          - Style
              - recent\[\]
          - Editor
              - text
          - goButton
          - go()
      - MenuBar
          - Menu
              - File
              - Edit
              - BookmarkButtons\[\]
                  - Manage Bookmarks
      - Bookmarks\[\]
      - Window\[\]
          - print()
          - Canvas
              - Style
                  - font
                  - background
                  - foreground
              - Plots\[\]
                  - Plot 'plot\_1'
                      - Style
                          - drawGrid
                          - drawMinorGrid
                      - title
                      - Xaxis
                          - Style
                              - ticklen 'EmSpec length of ticks'
                          - range
                          - title
                          - units
                      - Yaxis
                          - Style
                              - ticklen 'EmSpec length of ticks'
                          - range
                          - title
                          - units
                      - ColorBar 'colorbar\_1'
                          - Style
                              - colorbarType 'greyscale, rainbow, etc'
                              - fillColor
                              - ticklen 'EmSpec length of ticks'
                          - range
                          - title
                          - units
                      - Renderer\[\]
                          - SpectrogramRenderer 'spectrogram\_1'
                              - Style
                                  - rebinType
                              - dataSourceId
                      - primaryMouseModule
                      - MouseModules\[\]
                          - CrossHairDigitizer *crosshair\_digitizer*
                              - Style
                                  - tooltip
                                  - multiline
              - Components *other components on a canvas*
                  - ContextPlotConnector 'connector\_1'
                  - Annotation 'annotation\_1'
                      - Style
                          - font
                          - foregroundcolor
                          - backgroundcolor
                      - text
              - Columns\[\]
                  - Column 'column\_1'
                      - min, emSpec
                      - max, emSpec
              - Rows\[\]
                  - Row 'row\_1'
                      - min, emSpec
                      - max, emSpec
      - MouseModuleFactories\[\] *palette of available mouse modules*
      - DataSources\[\] *data sources in the application*
          - DataSource 'datasource\_1'
              - url
              - Config *DOM for configuring DataSource, one-to-one
                mapping with URL*
      - BindingContext\[\]
          -   - BindingContext 'binding\_context\_1'
                  - updatePolicy ''immediate, or support for update
                    button'
                  - Bindings\[\]
                      - Binding 'binding\_1'
                          - SrcProperty
                          - DestProperty
                          - BindingConvertor

}}

### First Implementation

Here's how the DOM is shaping up:

{{\#tree:openlevels=0|root=Autoplot DOM Tree:|

  - Application
      - controller, applicationController, the object for controlling
        the application
          - focusSuri
      - options
          - drawAntialias, boolean, do antialias on the data
          - textAntialias, boolean, do antialias text
          - overRendering, boolean, load and paint data outside plot
            bounds to improve pan appearance
          - autoContext, boolean, allow context plot.
          - autoRange, boolean, autorange data.
          - color, Color, default symbol color.
          - fillColor, color for fill-to-reference
          - foreground, Color, axis and labels color.
          - background, Color, canvas background color.
          - drawGrid, boolean, draw grid at major ticks
          - drawMinorGrid, boolean, draw grid at minor ticks
      - canvas, the current focus canvas
          - size, Dimension, the size of the canvas
          - row, String, the spec positioning the outside bounds of the
            plot
          - column, String, the spec positioning the outside bounds of
            the plot
          - fitted, boolean, canvas size is determined by parent
            container.
      - plot, Plot, the current focus plot
          - title
          - xaxis, Axis, the xaxis properties
              - range, DatumRange, the range of the axis (DatumRange is
                min, max, and Units )
              - log
              - label
          - yaxis
          - zaxis
      - plots\[\], array of all plots in the application
          - plots\[1\] 'plot\_1'
      - panel, the current focus panel
          - controller, PanelController, its controller.
          - plotId, String, the name of the plot containing the panel.
          - renderType, RenderType, enum of the methods for rending data
            (Spectrogram, Scatter, Series, etc.)
          - plotDefaults, Plot, autoranging settings for the loaded
            dataset
          - style, PanelStyle, rendering options
              - colortable, Colorbar.Type
              - rebinMethod, RebinnerEnum, enum of BinAverage,
                NearestNeighbor, etc.
              - color
              - reference, Datum
              - fillToReference, boolean
              - fillColor, Color
              - plotSymbol, PlotSymbol
              - symbolSize, double
          - dataSourceFilter, DataSourceFilter, the uri and post-load
            operations
              - controller, DataSourceController
                  - dataSet, the loaded dataset
                  - fillDataSet, the dataset after post-load operations
              - suri, the uri
              - sliceDimension
              - sliceIndex
      - bindings, BindingModel\[\], properties that are tied together
          - binding\[0\], application.timeRange \<--\>
            plot\_1.xaxis.range
      - connectors, Connector\[\], connects two plots (e.g. for context
        overview.)
          - connector\[0\], Connector, plotA to plotB
      - timeRange, DatumRange, range for the stack of panels.

}}

Some differences to note:

  - less hierarchical than first conceived. It's easier to manage when
    the model's structure doesn't change, so have plots contain panels
    by reference rather than object hierarchy. panel.plotId contains the
    plot that contains it. This also means moving a panel is just
    resetting the plotId.
  - many controllers. Back in the Spring I expected there would be one
    massive controller, but it works nicely to have a controller for
    each node.
  - controllers in the tree. Right now, the controllers are accessible
    in the tree with each node's getController method. This may change
    since it pollutes the model with the controller. But it does make it
    very easy to find things.
  - application.options rather than application.style. This is closer to
    the legacy structure and this may change as the idea of "style
    sheets" is introduced. Options are per-user inter-session
    persistent.

### Controller for Autoplot

The controller contains methods for controlling the DOM.

#### Methods

  - bind( 'Canvas\[0\].Plot\[0\].Xaxis.range', property(
    DOM.getElementById('annotation\_1'), 'text' )
  - property( Object o, String property )
  - insertRow( ) *adds below the current focus*
  - insertColumn( )
  - focusElement( )
  - addDataSource( DataSource )

### Use Cases

  - plot with two datasets overlayed.
  - correlation between two datasets.
  - add ContoursRenderer
  - add TimeRangeSelector
  - add page for collecting digitize times
  - run daily plots for year
  - style sheets demo similar to CSS Zen Garden

### Layout Specification

"Rows" and "columns" are used to control the position of plots. Autoplot
uses strings "5em,100%-10em" to control the position of these objects.
The comma delineates min and max specifications, which correspond to
top,left and bottom, right for rows and columns respectively. The text
"100%-10em" means 100% of the way from the way left (min) to right
(max), and the -10em means come back 10 em heights.

# Autoplot Objects

## DOM Controllers

The DOM Controllers are objects that manage nodes of the DOM. For
example, when the slice index of a DataSourceFilter node is changed, the
controller slices the original dataset to create a new dataset, and
fires off an event notification of the new dataset.

DataSourceController: Converts the DataSourceFilter node URI string into
a dataset. (Filter comes from that this once would slice as well, but
that function may be removed. We may allow one node to simply filter
another node.)

PlotElementController: A PlotElement has references to a
DataSourceFilter,a Plot node, and render type string identifying the
rendering method. This takes the QDataSet produced by the
DataSourceController and renders it onto the plot. Note that this may
also filter the data. When vectors are displayed, several PlotElements
are added for each component. Also, each PlotElement contains default
plot ranges and labels.

PlotController: The Plot node has range and label settings. This
controller will detect when autoranging should occur and combines the
plot ranges into a default plot range.

TimeSeriesBrowseController: When a DataSource indicates it has the
TimeSeriesBrowse capability, this controller is created to manage
loading new data when new ranges are displayed.

ApplicationController: Its job is to simply add and remove listeners as
the dom is manipulated, to keep track of the application's history, and
to implement load and save.

Note a number of things are handled as part of the Das2 graphics library
or Java:

  - Updates to the plot when axes are moved or labels changed via
    property editor.
  - Connectors between plots are painted and managed by das2.
  - Bindings are simply Java Beans Bindings between property nodes.

## DOM Nodes

### syncTo

syncTo method should set all the properties of a node to those of
another node. This should include the id. This should include references
to id's.

### diffs

diffs returns an array of diff descriptor objects that can do and undo
the diff. The returned diffs should include the id. The returned diffs
should include changes in references to other

### copy

copy is a deep copy of the node, including id and references. However,
this is often implemented with clone() it's extremely important that the
controller not be copied. Most copy implementations will explicitly set
the controller to null.

