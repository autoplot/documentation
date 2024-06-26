Purpose: Outline chapters for a Das2 "book." The goal would be to create
a 20-30 page book outlining the capabilities of the Das2 and QDataSet
libraries.

Audience: das2 developers

# Introduction

## Motivation for Das2

  - Provide license-free environment for providing science graphics.
  - Objects reflect concepts of Space Physics graphics, allowing
    applications to be assembled instead of written.
      - Spectrograms and Line plots
      - Mouse Events cross-hair digitizer data lookup
      - FileStorageModel for modelling database of files file storage
      - Data Model provides uniform data access

### Relationship to IDL and Matlab.

  - The problem with IDL. If everyone is up-to-date with current
    versions, then there is no problem.
  - More and more people are using Matlab and SciPy, and don't even have
    an IDL license. Further fragmentation of the field.
  - IDL doesn't provide out-of-the-box solutions, there's always more
    work to be done to make it work for Space Physics, and for a
    particular group's needs.

## Basic Capabilities

  - Spectrograms and lineplots
  - Axes are live, and can be adjusted with the data rendering following
    along.

## Java Platform and Webstart

  - Java 7 is the platform for Das2.
  - Java is freely available at <http://java.com>, and is often
    installed on new machines.
  - Webstart is the mechanism for launching most Das2 applications, and
    allows clients to click on a web link and have the software come up.

# Graphics

  - Java2D Graphics
  - Rendering
  - DasAxis and DasPlot
  - DasCanvasComponents

# Das2 applications

  - Small Java programs that set up the das2 components and bind them
    together. The goal is to write applications quickly by connecting
    building blocks, instead writing code that handles the numbers.
  - Examples
      - Voyager Lowrate plotter
      - Cassini App
      - SatDen Saturn Density optimizer
      - Autoplot

# Datums and Units

  - Units are an enumeration identifying physical units
  - Modelling science data with double + Unit == Datum
  - Times are a Datum with Units like "microseconds since
    2000-01-01T00:00Z" (Units.us2000)
  - TimeParser class for fast time parsing.
  - DatumRanges.
  - UnitsConverters
  - EnumerationUnits allow for nominal data
  - Stevens' Levels of Measurement
    <http://faculty.webster.edu/woolflm/statwhatis.html>
  - Basis and SI Units are coming.

# QDataSet

  - Implementation vs Interface
  - from the Datum up to Bundles and Join Data Sets
  - Examples of limitations QDataSet addresses.
  - Schemes
  - ArrayDataSet and BufferDataSet
  - DataSetBuilder

# QDataSet operations

  - Slicing
  - Add,Subtract,Divide,etc.
  - smoothing
  - FFTPower
  - Connecting to Jython in Autoplot. binding operators.

# Streaming Data

  - Das2Streams. Built for the old data model, Das2Streams represent
    data that can be plotted on the screen. (E.g. spectrograms,
    lineplots, typically time series)
  - QStreams. Developed along with QDataSet, these are more much more
    flexible than das2streams.

# Das2Server

  - discovery and branding. Goal is to allow the client to be loosely
    coupled to the server.
  - All data is transmitted as Das2Streams and QStreams.

# Utilties

  - FileSystems
  - FileStorageModel
  - ProgressMonitors

# Events

  - DataPoints and Ranges
  - Box selections
  - Beans Binding and MVC.
