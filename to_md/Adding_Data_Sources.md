This document is outdated. Autoplot is generally repacked into a two jar
files, one for Autoplot and its libraries and one for the third party
jar files. Otherwise the document is still useful.

# Autoplot Internals Overview

The core of Autoplot is four jars

  - QDataSet, the data model
  - DataSource, gets data into the data model
  - DataSourcePack, various implementations of DataSource, including
    AsciiTable and das2Stream.
  - Autoplot, the application based on all of the jars.

Other jar files are used to read data from different file formats (e.g.,
CDF, and netCDF) or are used for UI functions (e.g., jars for writing
PNG files). To see the list of jar files used, save
<http://www.autoplot.org/autoplot.jnlp> as a text file and read its
contents.

## QDataSet

  - QDataSet is the data model, which is a Java interface
  - QDataSet implementations, e.g. DDataSet wraps a double array
  - QDataSet is the data model used in das2 since the Autoplot2010
    branch.
  - Operators
      - slice
      - data reduction
      - aggregation
  - Utilities
      - ascii table parser
      - data set builder

## Metadata Handling

Metadata is conveyed using a tree built from Map objects. The root
"node" is Map\<String,Object\>, and the objects can be another
Map\<String,Object\> branch or
[immutable](http://en.wikipedia.org/wiki/Immutable_object) objects that
are leaves.

## DataSource

  - `DataSource`s know how to model other data models as QDataSets.
  - `DataSource`s also provide a metadata of Map\<String,Object\> with
    name=value leaves.
  - `DataSourceFactory`s
      - translate from URI to DataSource
      - provide completion model to generate valid URIs
      - have a reject method that rejects incorrect or incomplete URIs
  - Data sources often have GUIs that assist in creating valid URIs.
  - DataSourceRegistry
      - table of lookups: extension to DataSourceFactory and mime-type
        to DataSourceFactory
  - DataSetURI
      - uses DataSourceRegistry, DataSourceFactory to create DataSource
        from URI
      - provides filesystem completion or dataSource completion by
        delegation.
  - MetaDataModel
      - translates various metadata models into canonical QDataSet
        metadata model.
      - for example, ISTPMetaDataModel allows cdfs to be interpreted via
        local file access or via openDAP.
  - org.autoplot.aggregator
      - AggregatingDataSource aggregates another DataSource using das2
        FileStorageModel
      - AggregatingDataSourceFactory uses a delegate DataSourceFactory
        and a representative file.
  - DataSetSelector GUI component that provides user interface to
    completion model. This is the address bar in the Autoplot GUI.
  - DataSource.getCapability adds various capabilities, such as
    TimeSeriesBrowse. See
    [developer.capabilities](developer.capabilities "wikilink")

## Existing Data Sources

  - various DataSources know how to model other data models as
    QDataSets, for example:
      - ASCII--uses internal QDataSet ASCII table parser to read in
        table
      - Binary--binary files.
      - Excel--uses external Jakarta Poi library to read data from Excel
        spreadsheets.
      - das2Stream--das2 streams allow streaming of data and metadata.
        Bob Weigel's TSDS server can send these streams.
      - netCDF--adapts NetCDF data model.
      - OpenDAP--open DAP is a web API for accessing remote data.
      - SPASE--allows SPASE record to wrap another data source, and
        provide metadata for it.
      - Fits--Fits files used in astronomy
      - Wav--.wav files. This is the result of this tutorial.
      - CDF--ISTP CDF files
      - CEF--Cluster Exchange Format files
      - Jython--Jython code is used to compose datasets.

## Autoplot

  - ApplicationModel is the legacy internal Model and Controller (as in
    [MVC](http://en.wikipedia.org/wiki/Model-view-controller)) of the
    Autoplot application. (The state and things the application can do.)
  - the package "dom" implements the "DOM" tree containing the
    application state.
  - AutoplotUI is a GUI View of the model.
  - the package "state" has classes for undo/redo support, and saving
    application state into .vap files.
  - the package "transferrable" supports copy image to OS clipboard.
  - the package "server" is the back-end server that provides access to
    console to support scripting.
  - the package "scriptconsole" is a GUI for browsing and executing
    jython code. It also contains LogConsole, which provides access to
    log messages.

# Overview of Tutorial

In this tutorial, we will add the ability to plot .wav files to
Autoplot. First, we will create a dummy data source and register it with
autoplot. Then we will actually read the data and return the waveform.
Last we'll add an additional capability and see how completions are
added.

So we can avoid the tedium of jar files and compiling java code, this
tutorial assumes you are using Netbeans 6.5+ and can build Autoplot as
described in [Autoplot\_from\_source](Autoplot_from_source "wikilink")
and
[Autoplot\_from\_source\#Building\_in\_Netbeans](Autoplot_from_source#Building_in_Netbeans "wikilink").

# Create a Dummy DataSource and Register the DataSource Type

Before writing the code to deal with the wav format, we'll create the
data source with a dummy implementation and confirm that it gets
properly registered with Autoplot.

## Set up project

  - Create a new project "WavDataSource"
  - Open WavDataSource project properties and click on "Libraries"
      - Click "Add Project" and add QDataSet
      - Click "Add Project" and add DataSource
      - Click "Add Project" and add DasCore

## Define two classes

Create a new package "org.autoplot.wav". All class references are within
this package.

### WavDataSource

  - Create a new class `WavDataSource` that extends
    `AbstractDataSource`. (An abstract class is a class that is mostly
    implemented, and subclasses finish the work.)
  - Define a constructor that accepts URI and calls super constructor.
  - Provide an implementation of the abstract method `getDataSet`. This
    is a dummy method for testing; the real implementation is presented
    in the next section.

<!-- end list -->

``` java
public QDataSet getDataSet(ProgressMonitor mon) throws Exception {
    return DataSetUtil.replicateDataSet( 30, 1.0 );
}
```

### WavDataSourceFactory

  - Create a new class `WavDataSourceFactory` that extends
    `AbstractDataSourceFactory`.
  - Implement `getDataSource(URL url)` to simply return `new
    WavDataSource(url)`

## Register with Autoplot

This is the tricky part, since no java type checking is done and it's
easy to make mistakes.

  - Make a text file
    META-INF/org.autoplot.datasource.DataSourceFactory.extensions that
    would contain the name of your factory class that has a no-argument
    constructor, followed by the extensions (e.g. wav).
  - Alternatively, the plugin can be registered by mime type using the
    text file
    META-INF/org.autoplot.datasource.DataSourceFactory.mimeTypes.
    **Note:** mime types are only used with http urls. DEPRECATED: don't
    use this, it will probably go away.

The META-INF directory should appear in the project's src folder.

For Autoplot to locate and load your new data source, WavDataSource.jar
must appear in the classpath. When running from NetBeans, the easiest
way to do this is to add the WavDataSource project as a library in the
Autoplot project properties.

## Test

  - run autoplot
  - for URL, enter "<file:///foo.wav>"
  - 30 1.0's should be plotted.

# Implement the DataSource

We will do all the work in the getDataSet method of WavDataSource.

## wav file format

A wav file is a big binary array, with encoding information in the first
64 bytes of the file. We will use java's AudioSystem class to parse the
header. For this example, we will only support mono (one channel)
formats. Also, we will not implement the QDataSet interface for now, and
we will use java.nio which handles endian encodings.

## Get a local copy of the file, create QDataSet

``` java
public QDataSet getDataSet(DasProgressMonitor mon) throws Exception {
    File wavFile = DataSetURI.getFile(this.uri, mon);
 
    AudioFileFormat fileFormat = AudioSystem.getAudioFileFormat(wavFile);
    AudioFormat audioFormat = fileFormat.getFormat();
    FileInputStream fin = new FileInputStream(wavFile);
    ByteBuffer byteBuffer = fin.getChannel().map(MapMode.READ_ONLY, 64, wavFile.length() - 64);

    int frameSize = audioFormat.getFrameSize();
    int frameCount = (byteBuffer.limit() - byteBuffer.position()) / frameSize;
    int bits = audioFormat.getSampleSizeInBits();
    boolean unsigned= audioFormat.getEncoding().equals(AudioFormat.Encoding.PCM_UNSIGNED );
      
    if ( unsigned ) {
        throw new IllegalArgumentException("Unsupported wave file format: " + audioFormat + ", need signed.");
    }
    if (audioFormat.getChannels() > 1) {
        throw new IllegalArgumentException("Unsupported wave file format: " + audioFormat + ", need mono.");
    }
    if (bits != 16 && bits != 8) {
        throw new IllegalArgumentException("Unsupported wave file format: " + audioFormat + ", need 8 or 16 bits.");
    }
 
    QDataSet result;
 
    if (bits == 16) {
        if (audioFormat.isBigEndian()) {
            byteBuffer.order(ByteOrder.BIG_ENDIAN);
        } else {
            byteBuffer.order(ByteOrder.LITTLE_ENDIAN);
        }
        ShortBuffer shortBuffer = byteBuffer.asShortBuffer();
        short[] buf = new short[frameCount];
        shortBuffer.get(buf);
        result = SDataSet.wrap(buf);
    } else {
        byte[] buf = new byte[frameCount];
        byteBuffer.get(buf);
        result = BDataSet.wrap(buf);
    }

    return result;
}
```

If you are interested in the QDataSet data model, you'll want to look at
the [QDataSet](QDataSet "wikilink").

## Test

Run Autoplot again and this time point it to a .wav file. Windows "Sound
Recorder" can be used to produce the file, or use this one:
[1](http://autoplot.org/data/trainMono.wav)

# Adding Metadata to the DataSource

## Return arbitrary Metadata that is presented in the metadata tab

Override method "getMetaData(org.das2.util.monitor.ProgressMonitor)":

``` java
public Map<String,Object> getMetadata(ProgressMonitor mon) throws Exception {
    File wavFile = DataSetURI.getFile(this.uri, mon);
    AudioFileFormat fileFormat = AudioSystem.getAudioFileFormat(wavFile);
    AudioFormat audioFormat= fileFormat.getFormat();
    Map<String,Object> properties= new HashMap<String,Object>(  );
    properties.put( "encoding", audioFormat.getEncoding() );
    properties.put( "channels", audioFormat.getChannels() );
    properties.put( "frame rate", audioFormat.getFrameRate() );
    properties.put( "bits", audioFormat.getSampleSizeInBits() );
    return properties;
}
```

## Assigning time tags with the QDataSet model

To specify physical time tags with the QDataSet model, we can attach
time tags to the created data set. To the getDataSet method, we add:

``` java
  
MutablePropertyDataSet timeTags= DataSetUtil.tagGenDataSet( frameCount, 0., 1./audioFormat.getSampleRate() );
timeTags.putProperty( QDataSet.UNITS, Units.seconds );
result.putProperty( QDataSet.DEPEND_0, timeTags );
```

In the QDataSet model, the property DEPEND\_0 contains a dataset with
the values of the independent variable. See
<https://saturn.physics.uiowa.edu/svn/das2/dasCore/community/autoplot2010/trunk/dasCoreDatum/src/org/das2/datum/Units.java>
for a list of units.

# Adding parameters to the URI

Let's add the ability to look at just a part of the .wav file. We'll
define two keywords, offset and length to our dataset URIs. For example,
<file:///data/mywav.wav?offset=1.0&length=0.2> means start at 1.0
seconds into the wav file, and clip after 0.2 seconds.

## Getting the Parameters

Since we are extending AbstractDataSource, the parameters are available
in the Map\<String,String\> params. It should be clear to the reader how
this would be implemented, and here is the source:
[WavDataSource.java](https://vxoware.svn.sourceforge.net/svnroot/vxoware/autoplot/trunk/WavDataSource/src/org/autoplot/wav/WavDataSource.java)

## Completion

The DataSourceFactory can provide a set of completions so that users can
more easily use the data source. In our class WavDataSourceFactory, we
now override getCompletions:

``` java
public List<CompletionContext> getCompletions(CompletionContext cc) {
    List<CompletionContext> result= new ArrayList<CompletionContext>();
    if ( cc.context.equals(CompletionContext.CONTEXT_PARAMETER_NAME ) ) {
        result.add( new CompletionContext( CompletionContext.CONTEXT_PARAMETER_NAME, "offset" ) );
        result.add( new CompletionContext( CompletionContext.CONTEXT_PARAMETER_NAME, "length" ) );
    } else if ( cc.context.equals(CompletionContext.CONTEXT_PARAMETER_VALUE ) ) {
        String paramName= CompletionContext.get( CompletionContext.CONTEXT_PARAMETER_NAME, cc );
        result.add( new CompletionContext( CompletionContext.CONTEXT_PARAMETER_VALUE, "<double>" ) );
    }
    return result;
}
```

The completions identified here are used to automatically generate a GUI
to create URIs.

# What's Next

This tutorial uses existing implementations of QDataSet that force the
data to be read into memory. This limits the size of the wav file that
can be browsed to about 30 seconds at 8000Hz. One could easily create a
QDataSet implementation that wraps the memory-mapped ByteBuffer, so data
is only swapped into physical memory as it is accessed. (See java.nio
for information about ByteBuffer.)

Note that this is implemented in Autoplot source.

You can also:

  - define the reject method in WavDataSourceFactory to reject when the
    parameters aren't properly specified.
  - define a graphical editor which aids URI construction instead if
    completions. (Note an automatic editor based on completions is
    coming.)
      - also see the tutorial extension below

# Creating a Graphical URI Editor

After producing functional WavDataSource and WavDataSourceFactory
classes, an Editor Panel can be created as well. In this example we use
the Netbeans (Java IDE) GUI builder, but it can be developed in Eclipse
or other environments.

## Summary of Steps

  - First, create a class called "WavDataSourceEditorPanel" in the same
    package as the first two classes.
  - Before implementing anything, we must create an extensions file so
    that our Panel will be used in Autoplot.
  - Finally, we will implement the necessary methods to produce a
    working editor panel.

## Create a WavDataSourceEditorPanel

Create the class in the same package as before.

  - If you are using NetBeans, you may wish to use the GUI builder in
    constructing this class
  - WavDataSourceEditorPanel should implement the DataSourceEditorPanel
    interface, and extend the JPanel class

## The Extensions File

Next, we must create another file in the package's "META-INF" folder.
Open a new text file, and save it as
"org.autoplot.datasource.DataSourceEditorPanel.extensions". Then simply
add the text: <i>"org.autoplot.wav.WavDataSourceEditorPanel wav"</i>.
This will allow Autoplot to find the class we are about to write and
display it for editing Wav files.

## Implementing the Editor

First we must design a simple GUI to handle parameters for the Wav file.
Since we are only dealing with two parameters: offset and length, we
only need two labels and two text fields in our GUI.

After this, we must implement five methods from the
DataSourceEditorPanel interface: `getPanel`, `setURI`, `getURI`,
`reject`, and `prepare`.

### reject

This method determines if the given URI is acceptable for editing. Below
is a simple implementation for the reject method. It simply detects if
the given URI is a directory. This code can easily be modified to accept
a URI that is incomplete and provide a default file path.

``` java
public boolean reject(String uri) throws Exception {
    URISplit split = URISplit.parse(uri);
    FileSystem fs = FileSystem.create(DataSetURI.getWebURL(DataSetURI.toUri(split.path)).toURI());
    if (fs.isDirectory(split.file.substring(split.path.length()))) {
        return true;
    }
}
return false;
```

Note data sources that do not reject an empty URI like
"vap+<em><dsid></em>:" are called "discoverable" and are added to the
Autoplot menu at File-\>Add Plot From-\>\<<em>dsid</em>\>.

### prepare

The prepare method for an editor panel can be designed to do a number of
things to get the Editor ready. Since we only have a simple GUI, not
much is needed in this case. This method returns true under normal
condition. Note this method is provided a progress monitor, so long
operations, such as downloading a file, should be done here.

``` java
public boolean prepare(String uri, Window parent, ProgressMonitor mon) throws Exception {
    URISplit split = URISplit.parse(uri);
    File f = DataSetURI.getFile(new URL(split.file), mon);
    return true;
}
```

### getPanel

Simply implement this method with "`return this;`"

### setURI

This method is used to initialize the GUI. Since our GUI has two text
fields with which to modify the URI, we will want these to display the
current parameter values upon opening the URI editor.

``` java
public void setURI(String uri) {
    this.sURI = uri;//store the value of the String input
    URISplit split = URISplit.parse(sURI);
    File f = DataSetURI.getFile(new URL(split.file), new NullProgressMonitor());
    Map<String, String> params = URISplit.parseParams(split.params);
    String oF = params.get("offset");
    String lF = params.get("length");
    jTextField1.setText(oF);
    jTextField2.setText(lF);
}
```

Where jTextField1 and jTextField2 are the two `jTextField`s that display
the parameter values.

### getURI

The method "getURI" returns the URI for the current GUI settings. Note
Autoplot assumes this is a working URI, and will exhibit strange
behavior if it is not.

``` java
public String getURI() {
    URISplit split = URISplit.parse(sURI);
    Map<String, String> params = new LinkedHashMap();
    String offset = jTextField1.getText().trim();
    String length = jTextField2.getText().trim();
    if(!offset.equals("")) params.put("offset", offset);
    if(!length.equals("")) params.put("length", length);
    split.params = URISplit.formatParams(params);
    return URISplit.format(split);
}
```

<hr>

There are many ways to extend the WavDataSourceEditorPanel to include
additional functionality, including:

  - More parameters can be included, such as 'channel'
  - A more complex GUI may be implemented using something other than the
    `jTextField`s used here
  - The methods can be modified to accept only a directory URI instead
    of a full filepath

![WavDataSourceEditorPanelImage.png](WavDataSourceEditorPanelImage.png
"WavDataSourceEditorPanelImage.png")  
Preview of a WavDataSourceEditorPanel
