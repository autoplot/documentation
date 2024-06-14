Autoplot can parse "Rich ASCII," which are data files containing data
and metadata in a prescribed format developed jointly with Los Alamos
National Labs, in their SpacePy software. (Note it is also called
JSON-Headed ASCII.) These rich headers allow ascii files to be created
and used that allow more precise representation of the data. For
example, ASCII files could have a label and units specified for each
column, like so:

```
# {
#    "Epoch": {
#       "START_COLUMN": 0,
#       "UNITS": "UTC"
#    },
#    "density": {
#       "FILL_VALUE": -1.0E31,
#       "LABEL": "density (cm**-3)",
#       "START_COLUMN": 1,
#       "UNITS": "cm**-3",
#    }
# }
2015-03-21T00:00:00.476Z 2.0834
2015-03-21T00:00:06.976Z 2.0829
```

The following properties can be attached to each variable:

```
VALID_MIN, number, inclusive of the valid values.  VALID_MIN=0 means 0 is valid but -1 is not.
VALID_MAX, number, inclusive of the valid value.   VALID_MAX=1000 means 1000 is valid, but 1000.00001 is not.
FILL_VALUE, number, value to consider invalid.   FILL_VALUE=0 means 0 is invalid.
SCALE_MIN, number, suggest scale range
SCALE_MAX, number, suggest scale range
SCALE_TYPE, string, suggest scale type: 'linear' or 'log'
LABEL, string, short label for the column, used for the Y axis of plots.  The NAME is used by default.
TITLE, string, title of the column, used above plots for example.  LABEL is used by default.
RENDER_TYPE, string, "scatter" "nnSpectrogram" "series" "spectrogram"
UNITS, string, units string that is made into canonical das2 units.  A list of defined units will be made available.  
   Note units like "seconds since 2010-01-01T00:00" can be used for times.  These are non-leap-seconds since the UT time.
   "UTC" should be used to indicate that the time is an ISO8601 formatted time (2016-06-16T01:23).
```

Structural properties allow for more complex data:

```
DIMENSION, array of ints
  "[]" (default is a scalar)
  "[1]" is also interpreted as a scalar.
  "[3]" (three element vector) 
  "[20,30]" (qube of 60 elements).
ELEMENT_NAMES, array of strings, C-style (encouraged) identifier for each element.  
ELEMENT_LABELS, array of strings, Human-readable label for each column of the parameter.
DEPEND_1, string, refers to another column's NAME to assign values for the rank 2 qube of data.
DEPEND_0, string, refers to another column's NAME to assign values for the of data.  By default, the first column is used, but this can override.
ENUM, array of string, enumerated data type.  0=the first element, 1=second element, etc.
```

Any root-level JSON object that describes data will contain either:

```
START_COLUMN, integer, starting column for the data, where 0 is the first column, or
VALUES, array of doubles, values are defined in the rich header and not in the table below.  This is typically used for DEPEND_1.
```

All other root-level JSON objects are considered to be metadata. Note
too that each JSON object can contain arbitrary tags to be interpreted
as metadata.

# Examples

SCALE\_MIN/SCALE\_MAX:

```
# { "TIME": { "LABEL": "Time_UTC", START_COLUMN=0, UNITS="UTC" },
#   "DENSITY": { "LABEL": "Density", "SCALE_MIN":0.01, "SCALE_MAX":100, "SCALE_TYPE":"LOG", START_COLUMN=1, UNITS:"cc**-3" } }
# TIME DENSITY 
2011-01-01T00:00 0.12
2011-01-01T00:01 0.14
```

Dimension property embeds higher rank data:

```
# { "Time": { "UNITS":"UTC" }
#   "B_gsm": { "UNITS":"nT", DIMENSION=[3] } }
2011-01-01T00:00 0.12 0.13 0.14
2011-01-01T00:01 0.14 0.15 0.16
```

Dimension property embeds higher rank data, ELEMENTS allows components
to be accessed

```
# { "Time": { "UNITS":"UTC" }
#   "B_gsm": { "UNITS":"nT", DIMENSION=[3], ELEMENTS={ "Bx", "By", "Bz" } }
2011-01-01T00:00 0.12 0.13 0.14
2011-01-01T00:01 0.14 0.15 0.16
```

# Use Cases

  - encode data that is impossible to derive using parser: e.g.
    VALID\_MIN
  - enrich existing products to make them more useful

# Examples

  - <http://jfaden.net/jenkins/job/autoplot-test030/lastSuccessfulBuild/artifact/19820105_1981-025_CPA_l2_fcf-001.txt>
  - <http://jfaden.net/jenkins/job/autoplot-test030/lastSuccessfulBuild/artifact/CRRES_mod_20121213.txt>
  - <http://jfaden.net/jenkins/job/autoplot-test030/lastSuccessfulBuild/artifact/proton_density.dat>

# See Also

  - <https://github.com/JSONheadedASCII>

