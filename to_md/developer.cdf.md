Purpose: Show how CDF Metadata appears on the Autoplot display.

Audience: Data product developers

See also: <http://autoplot.org/developer.cdfguide> which also talks
about the CDF format.

# Introduction

CDF is a data format created at NASA/Goddard to store data produced in
space physics. Each file is like a small database, and conventionally
files for each interval together form a long time series. This is
intended to serve as a primer to develop these files. These files are
rarely read and written directly, instead NASA provides libraries for
working with these files.

For example, the CDF file data\_20060101.cdf contains data collected on
2006/01/01. It contains named parameters "Magnitude" "Epoch" and BGSM.
Each of these parameters contains 24 records. Magnitude is the magnitude
of the symbol, and Epoch contains the time tags for each measurement.
BGSM is a vector collected at the same time.

Each variable has metadata attached. For example BGSM has an attribute
"CATDESC" that is a title for the data "Magnetic field vector in GSM
coordinates (1 hr)" and it also has units specified in an attribute
"UNITS" which is "nT." Note attributes can be any data type, for example
FILLVAL is the value that marks missing data.

Metadata also identifies relationships between variables. For example
BGSM and Magnitude both have DEPEND\_0="Epoch" indicating they are
dependent parameters on the independent parameter Epoch. LABL\_PTR\_1 is
used with BGSM to a variable containing three string labels for each
component.

# Attributes

<http://spdf.gsfc.nasa.gov/istp_guide/vattributes.html>

# Global Attributes

There are attributes for the file itself, called global attributes. Note
when data is combined from files to make a time series, implicitly the
Global Attributes should be the same for each file.

# Where things appear on Autoplot

  - The source\_name is derived from Global Attribute "Source\_name",
    removing the characters after the "\>". So "AC\>Advanced..." becomes
    "AC"
  - The descriptor is derived from Global Attributes "Descriptor" the
    same way, so "Descriptor=MAG\>ACE Magnetic Field Instrument" becomes
    "MAG"
  - Autoplot's plot title is derived from Attribute CATDESC. If
    source\_name, and descriptor are available, then the title is
    "source\_name/descriptor CATDESC." In the example, the title used is
    "AC/MAG Magnetic field vector in GSM coordinates (1 hr)"
  - The y-label is LABLAXIS for line plots.
  - The colorbar label, for spectrograms, is comes from LABLAXIS and the
    DEPEND\_1 parameter's LABLAXIS is used to label the axis.
  - UNITS identify the units. Autoplot allocates new Units objects to
    represent new unit types. A small set of units have conversions
    defined as well.
  - VALIDMIN is the minimum valid value.
  - VALIDMAX is the maximum valid value.
  - SCALEMIN is a suggested axis minimum. If this does not seem
    consistent with data, Autoplot performs the autoranging.
  - SCALEMAX is a suggested axis maximum. If this does not seem
    consistent with data, Autoplot performs the autoranging.
  - DISPLAY\_TYPE is either "time\_series" or "spectrogram"
    "time\_series" hints that the plot should be Autoplot's "series"
    mode. "spectrogram" hints that it should be "spectrogram" mode.

# Filename Conventions

Daily files is typical. Target less than 600MB per file. For example,
use 10 minute files when each file would have been 1.2G.
data\_$Y$M$D\_$H$M\_v01.cdf.
