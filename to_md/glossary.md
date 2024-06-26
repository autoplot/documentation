Purpose: Provide definitions to specific words used in Autoplot's
documentation.

Audience: developers and interested scientists.

# Glossary

## Data Representation

**dataset** Structured set of numbers having scientific meaning. This
contains both dependent and independent parameters, such an array
Density values which are a function of Time: Density\[Time\]

**metadata** Data about the data. For example, the data are numbers
representing Density which is a function of Time; and but metadata might
include the labels "Density" and "Time" and which spacecraft collected
it. Metadata is often split into "use" and "discovery" metadata, where
use would be things you need to know to use the data, such as the units
and axis labels; while discovery is what was used to find the data, such
as the spacecraft and instrument name.

**QDataSet** Autoplot's method for representing a dataset, or data
model. It allows representing trivial data such as the scalar "6.2",
Density tabulated as a function of time, spectrograms, or complex joins
of tables. See [QDataSet](QDataSet "wikilink").

**rank** the number of indices of a QDataSet. E.g. Density\[Time\] is a
rank 1 dataset with the one index corresponding to time;
Flux\[Time,Energy\] is a rank 2 dataset.

**dataset geometry** the structure of the dataset, including its rank
and dimension lengths.

**join dataset** like an array of datasets, where each of the elements
has a dataset with like properties. For example, an instrument that has
several sampling modes would produce this sort of data. See ragged
dataset.

**simple bundle dataset** rank N dataset containing a number of rank N-1
datasets. For example, ds= bundle( time, density, temperature ) where
time, density and temperature results in a rank 2 bundle dataset, with
ds\[m,3\] elements.

**qube** Constraint to arrays that each element is the same thing, e.g.
a 4x5 Array is 4 5-element arrays. This is opposed to Java arrays which
are the more general array of arrays, where each array can have
different length ("ragged arrays" or "city skyline"). In QDataSet, this
extends to the metadata, where each element has the same type of
metadata. Most formats are constrained to qubes. For example, any
variable in a CDF file is a qube. The das2server

**ragged dataset** Opposite of a qube dataset, where each slice of a
join may have a different geometry (e.g. 1st is 1144 by 43, 2nd is 1144
by 18, etc.)

**interface** vs **implementation** An interface is how you interact
with an object, and the implementation is how the object is coded to
provide that interface.

**backing** or **backed** The native data store for the dataset. Since a
QDataSet is an interface, clients needn't worry about the mechanics of
the data storage in arrays or memory-mapped files. For example, a
2-index QDataSet may be backed by a single-index double array or by a
file that has been memory-mapped into Java.

**mutable** or **writable** QDataSets are immutable, meaning that once
created they cannot be modified. However, it is common that functions
will return versions of the data that can be modified. Further
complicating things, Jython's datasets are often mutable, and duck
typing means that it's easy for users to assume that all datasets are
mutable.

**buckshot data** data with the independent data distributed randomly.
This is opposed to gridded data, where the independent data is taken at
somewhat regular intervals.

**gridded data** data with the independent data distributed regularly,
such as in the rows and columns of a spectrogram.

**context** term used preserve information, as in "out of context." For
example if a spectrogram is sliced at an energy, then the slice location
(e.g. 300eV) is the context for the new dataset, and it can be displayed
alongside the data so that the data is not presented out of context.
Similarly, the Plot objects have a context property, which allows them
to control a context, typically a timerange when comparing two slices of
a time series, so no time axis is visible.

**timerange** an interval of time, formatted and parsed in concise
string messages, like "2016-05-05" for May 5, 2016. See
[http://autoplot.org//help\#Time\_Parsing\_.2F\_Formatting more about
times](http://autoplot.org//help#Time_Parsing_.2F_Formatting_more_about_times "wikilink").
These are a special case of DatumRange, which is an interval in a
physical dimension, with a minimum to a maximum.

**schemes** QDataSet is a syntax, where the interface constrains how
things can fit together, and the scheme is how data is arranged within
QDataSet. For example, a rank 1 dataset having a rank 1 dataset for
DEPEND\_0 is a "simple time series" scheme, and a rank 2 dataset with
DEPEND\_0 and DEPEND\_1 is known as a "simple spectrogram."

## Data Operations

**flatten** take an arbitrary dataset and make in into rank 2 ds\[n,m\]
where n is the total number of points, and m is the number of physical
dimensions.

**grid** take flattened data and attempt to form gridded data in a rank
2, 3, or 4 qube.

**slice** extract the elements of one of the dimensions reducing the
rank by 1. For example slice0(0) takes ds\[3,4,5\] and returns ds\[4,5\]

**reduce** reduce the resolution of a dataset, combining measurements.
This might be by averaging or by returning the maximum of grouped
numbers.

**collapse** remove a dimension by combining measurements in the
dimension, typically using linear averages.

## Data Formats

**CDF** Common Data Format developed at NASA

**HDF5** Hierarchical Data Format is a binary format with abstractions
like named multi-dimensional qube arrays of data.

**NetCDF** Data Format now based on HDF5 that is used in earth sciences.

**ASCII Table** A text file with records delimited by new lines, and
fields within each record delimited by spaces, commas or column
position. Each record must contain the same number of records, and those
that do not are considered to be comment lines and are ignored. The
first line can contain field labels and units.

**OpenDAP** Not really a format but a protocol for communicating data
over the web.

**Rich ASCII** Ascii file with special JSON metadata at the beginning,
providing additional metadata and data relationships similar to CDF.
This is also called "JSON headed ASCII" in SpacePy.

**Rich PNG** PNGs created by Autoplot (and possibly other systems) that
contains axis transformations and labels in a roughly 1 KB of additional
size. This allows users to "grep" for axis labels and use the pngwalk
tool to look up coordinates. [1](http://autoplot.org/developer.richPng)

## URIs

**URI** Uniform resource identifier, and in Autoplot these specifically
refer to data sets. For example,
vap+cdf:<http://autoplot.org/data/autoplot.cdf?BGSEc> refers to data in
a NASA CDF file, and
vap+inline:linspace(0,5\*PI,100)\&sin(linspace(0,5\*PI,100)) refers to a
sine wave.

**file** is used to represent a local file or anything that could be
downloaded and used as a file. For example,
<http://autoplot.org/data/2010_061_17_41_40.txt> is a file.

**folder** is a container for files. For example,
<http://autoplot.org/data/> is a folder.

**filesystem** a heirarchy of folders and the files contained within.
Autoplot is able to treat a local folder and http location
(http://autoplot.org/data/) as filesystems. Supported filesystem types
include FTP, HTTP, SFTP, and .zip files.

**switch** Like an IDL keyword, switch is used to refer to named
parameters in URIs and Python function calls. For example, in
"<http://autoplot.org/data/2010_061_17_41_40.txt?column=field8&where=field8.gt(1e-16)>"
the switch "where" is used to extract a subset of the data.

**vap file** an xml file containing an Autoplot canvas configuration,
like a .doc file is to Microsoft Word or .html is to Firefox.

**events file** ASCII file containing three columns: start time, end
time, and event label. These are used to identify orbits, control PNG
Walk generation, and mark events. (See events list.)

## Within the application

**DOM** Taken from web terminology, it is the configuration of the
application.

**canvas** the 2-D space on which the application resides.

**plot** a rectangular areas using two axes to form a 2-D space, and a
third colorbar axis controlling data to color.

**plotElement** controls how data is painted onto a plot using the
plot's axes, keeping track of the data, plot, and render type.

**property** a controllable aspect of a plot, plotElement, or any DOM
component.

**binding** a connection between two properties of the DOM. For example,
each plot typically has its x-axis' range property bound to the
application timeRange property, so a stack of plots all show the same
time range.

**connector** component that relates two axes, drawing lines to show
where they reside with respect to one another. For example, the "context
overview" shows the top plot as a short, more detailed interval,
connected to a longer interval plot below.

**renderer** is the Das2 component that paints data onto plot. Examples
include "spectrogram" and "eventsBar". Autoplot picks the renderer
appropriate for the data, but the scientist (or script) can override
this. This shows rendering types:
<http://autoplot.org/developer.renderTypes>

**keyword** See named parameter. IDL uses this name for its similar
idiom, and keyword is sometimes used as a synonym.

**switch** See named parameter. Unix commands uses this name for its
similar idiom, and switch was used for a while to describe Jython named
parameters.

**named parameter** a Jython function parameter which is defined by name
rather than position, similar to IDL keywords. For example, in "plot(
ds, index=1 )" index is a named parameter, and ds is a positional
parameter.

## Developer Notes

**browse trigger** code which is triggered by a URI in the
DataSetSelector with the "inspect" button pressed.

**inspect button** folder and magnifier.

**play button** green triangle pointed west.

**GUI** graphical user interface.

**data source editor** Editor provided for a particular data source,
such as CDF files, which edits URIs.

## Institutions

These are workgroup and institution references are found in
documentation and bug tickets.

**LANL** Los Alamos National Labs. Los Alamos, New Mexico, USA

**NMC** New Mexico Consortium. Los Alamos, New Mexico, USA

**GMU** George Mason University.

**APL** Applied Physics Labs. Laurel, Maryland, USA

**ESA** European Space Agency

**NASA** National Aeronautics and Space Administration. Greenbelt, MD

**U. Iowa** The University of Iowa, Iowa City, Iowa, USA

**UNH** University of New Hampshire. Durham, New Hampshire

**UMN** University of Minnesota in Minneapolis, Minnesota.

**Aerospace** The Aerospace Corporation.

**UCLA** University of California, Los Angeles, California, USA

**SWRi** Southwest Research Institute.

**CDAWeb** The workgroup at NASA/Goddard which created and manages the
CDF file specification and data sets.

## Not Categorized

**TSB** Time Series Browse, the capability for a data source to span
long time intervals (years) but typically browsing is done by day.
Autoplot uses the TimeSeriesBrowse capability to query for new time
ranges. Datasets can also have a resolution which will load a reduced
version of the data, and will always have an intrinsic resolution which
is the limit of how fine the resolution can be.

**TCA** Time Correlated Annotations are das2-specific name for
additional information added to x-axis ticks when browsing through time.
This is often called ephemeris data. See
<http://autoplot.org/cookbook#Add_Axis_Annotations> for how these are
added.

**Axis Annotations** ephemeris data attached to the x axis major ticks,
in addition to the time values at each tick.

**Annotations** Text which can be attached to plots, data, and the
canvas, for adding titles or pointing out features.

**Matlab** Data analysis software often used in engineering but often in
Space Physics as well.

**IDL** Data analysis software often used in Space Physics and Medicine.

**Jython** Python implemented in Java. This is the Python Autoplot uses.
All Java libraries are available to it, but Python codes such as SciPy
are not ([yet](http://jyni.org/)).

**ISO8601** ISO spec for formatting time that everyone should know and
we can all agree on, where Year comes first then less significant
components follow. For example, 2014-01-01T00:00Z is a well-formatted
time. The specification also defines time spans, and this is supported
somewhat as well. <http://en.wikipedia.org/wiki/ISO_8601>

**JSON** Structured ASCII format, often used where XML shouldn't be
used. XML data is all strings with explicit schemes, where JSON is
String,Float, and Integer types with duck typing.

**gzip** Compression format that has the feature that it can be
streamed, is freely available, and is supported in most programming
environments.

**zip file** Hierarchical files and folders contained in one file.

**jar file** a .zip file used to distribute Java software.

**jumbojar** a jar file containing all the software needed to run the
application, which also contains a unix bash script at the beginning of
the file, that will launch the software on Linux.

**single jar** another name used for jumbojars.

**human-readable** Expression used often in documentation to indicate
the result should only be interpreted by humans and never machines. For
example, toString output should never be parsed, as it can be changed to
improve the human interface.

**events list** list of time intervals of interest. In Autoplot these
ranges are often accompanied with an RGB color and text label. They are
used to control the xaxis to jump around to convenient times, enumerate
orbit numbers, and to control pngwalk generation.

**orbits list** a special case of an events list enumerating the orbits
of a spacecraft. Typically these are contiguous in time, but need not
be.

**orbits file** special case of a csv or text file, where it is three or
four columns, having startTime, endTime, \[rgbColor,\] label.

**orbit time range** string encoding a time interval from an orbits
file, like "orbit:junoPP:7"

**ad-hoc orbit time range** orbits time range, with the filename, like
"<http://das2.org/Orbits/de1.dat>"

**data mashing** the practice of taking several datasets and combining
them to create a new dataset. For example, take B magnitude and
calculate FCE by dividing, or taking a noisy dataset and filter on a
quality index.

**dashup** the working name for the Autoplot utility for doing data
mashing. "Mashup" is the final name.

**filters** alias for the processes in the process stream. Autoplot
allows users to "pipe" data through a set of processes.

**process chain** better name for the processes applied to the data
before plotting. Filters have the problem that one filter type might be
to filter data more than 1000.

**GUI** Graphical user interface, the buttons, text areas, and other
components that make and control an application.

**Data Source** A source of data for Autoplot, namely the software that
can take a URI and produce a QDataSet, and often provides GUI controls.

**Data Source Editor** The GUI used to control URIs for a Data Source.

**event** an interval in time, often with associated label and color.
See **events list**

**event** a Java object representing a human action (e.g. button press)
or timer expiring.

**URI** uniform resource identifier, in Autoplot's case identifying a
data source and its configation.

**Idempotence** a function which once applied will always have the same
result, like abs or mod, or makeMonotonic.

# Synonyms

Dataset "size" and "dimensions" are both used to mean the same thing.
"Geometry" refers to the overall structure. The "size" command returns
an array of lengths for each dimension of the qube dataset.
"ELEMENT\_DIMENSIONS" returns an array of lengths as well, and should be
renamed "ELEMENT\_SIZE".

Unfortunately "variables" and "parameters" are used interchangeably.
"variable" should refer to a named quantity in a script, and parameter
should refer to an interface. A script has parameters which controls
variables within. A CDF file has "parameters" but these are also called
variables in other contexts.
