Purpose: outline a short getting started guide for new CDF authors.

Audience: people getting started with creating CDF files who wish to
contribute ideas.

See also: <http://autoplot.org/developer.cdf> which is focused on
metadata to Autoplot display.

# Introduction

This is not a getting started with CDF guide, but instead it is notes
for one that doesn't yet exist.

# List of Confusing Ideas to Cover

  - rVar/zVar difference -- use zvars
  - representing timetags: Epochs, TT2000 -- use TT2000 and be done with
    it.
  - metadata that connects variables (DEPEND\_0)
  - valid data and plot hints
  - ISTP metadata and skeleton files
  - structure for common examples
  - How to create quick CDF data files from IDL
  - working with SPDF to make your data available to the community

# Outline

  - Introduction to CDF file format
      - History and goals
      - What is it? Binary format that contains a named arrays and
        associations between arrays and metadata.
      - Uses compared to ascii data, etc.
      - CDAWeb is like a database but data is ingested in chunks and can
        be copied out into chunks.
  - Reading CDF files
      - Reading in Autoplot
      - IDL and Matlab
      - Using CDAWeb make your data available to the world
  - Writing CDF files from scratch
      - creating and installing data.
      - first metadata to specify title, fill values and scale settings
      - installing times. TT2000.
      - linking data DEPEND\_0
      - multidimensional datasets.
      - varying vs non-varying data.
      - what's not talked about
          - sparse data
          - blocking
          - compression
  - Using skeletons.
      - Separation of roles. Let the scientist specify the metadata, and
        the programmers handle the data.
      - a complete processing system
      - validating product with skteditor.
  - Ingesting data into CDAWeb
      - naming CDF files. Filenaming conventions, mission, instrument,
        dates, and versioning.
      - what about missing files? Should an empty file be made?
  - Example schemes for data
      - spectrogram
      - sparse data
  - Limitations -- people have asked a lot about how big can CDF files
    be? I suggest \<300 MB, but I know Autoplot has handled 1GB files.
  - WriteMyCDF
  - Reading and Writing in Java.

# CDF as Archival Format

  - variables should be single blocks. This provides efficient access
    with NIO.
  - or cdfs should be compressed by variable, but in this case we use
    chunks to provide random access.
  - Timetags are stored in TT2000 format, and are not compressed.
    (Uh-oh, does this contradict last two?)

# Other resources

Does Bob McGuire have a powerpoint that shows some of these ideas that
we could link to?

Tami (CDAWeb) has a page showing different types of data in CDF files:
<http://spdf.gsfc.nasa.gov/istp_guide/variables.html>
