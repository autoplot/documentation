In the 2011 version of Autoplot, the ascii file parser can now parse the
file's "rich headers" which provide more metadata than the Ascii parser
did before. Note the parser should parse existing documents just the
same as before, but these rich headers allow ascii files to be created
and used that allow more precise representation of the data. For
example, ascii files could have a label and units specified for each
column, like so:

```
# time density(/cc)
2011-01-01T00:00 0.12
2011-01-01T00:01 0.14
```

When data providers have the freedom to pick a data format, they may
choose to use rich ASCII headers. These use JSON-formatted structures to
identify metadata for each column, such as labels and units, but also
fill data, suggested axis ranges, log/lin axis settings. Also
dependencies between columns can be declared.

```
# { "time": { LABEL: "Time_UTC", UNITS:"UTC" },
#   "density": { LABEL: "Density", SCALE_MIN:0.01, SCALE_MAX:100, SCALE_TYPE:LOG, UNITS:"/cc" } }
# time density
2011-01-01T00:00 0.12
2011-01-01T00:01 0.14
```

# format

```
# {
#    `<NAME_I>`: { `<PROP_J>`:`<VALUE_J>`, ... }
# }
```
`#&nbsp;`&lt;NAME_0&gt;`&nbsp;`&lt;NAME_1&gt;`&nbsp;`&lt;NAME_2&gt;  
&lt;DATA_0&gt;`&nbsp;`&lt;DATA_1&gt;`&nbsp;`&lt;DATA_2&gt;  
```
...
```

NAME\_I should be a Java or C style identifier. (Exceptions like "L\*"
work, but will be assigned a slightly different name for the QDataSet,
which must have a conforming name.)

Where PROP\_J is from QDataSet and can be:

```
VALID_MIN, number, inclusive of the valid values.  VALID_MIN=0 means 0 is valid but -1 is not.
VALID_MAX, number, inclusive of the valid value.   VALID_MAX=1000 means 1000 is valid (TODO: verify this.)
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

## \_JSON\_ATTRIBUTES

The root-level JSON object called "\_GLOBAL\_METADATA" identifies
properties of the ascii file that follows. This may include the nodes:

```
  DELIMITER   COMMA or WHITESPACE
  FORMAT  fortran style specifier
  METADATA_STANDARD  ISTP or QDataSet.  Default is Autoplots QDataSet
  ENDIAN - BIG or LITTLE if binary, ignored if text.
```

Note ENDIAN is present only because we want to reserve the option to
allow the file following the JSON header to be binary data, used in
conjunction with the FORMAT specifier. This binary data would begin
following the last newline character (13 or 10) following the last hash
(\#) symbol.

## Enumerations

The LANL CRRES dataset has a number of enumerations in it, and it would
be nice if we could improve support for this:

  - Make sure this can easily be plotted, and the events bar comes up by
    default.
  - Need to define way to specify colors. e.g. ENUM\_COLORS=\[ "red",
    "yellow", "green", "\#FFEE00" \]

Purpose: Develop a spec for rich headers for ascii data files. This
continues a discussion started around Nov 17, 2010 about specifying a
richer format for ascii headers. This discussion involved Jeremy,
Reiner, Jonathon, and Mike from LANL.

# Resolutions So Far

  - JSON to be used as a format for the headers. Comment character is
    added to each line.
  - QDataSet tags should be used when appropriate.
    (TITLE,UNITS,LABEL,etc)

# Examples

SCALE\_MIN/SCALE\_MAX would be used often (precise):

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
  - decorate other people's existing products.

# Connecting JSON Record to Table Column

{ <name>: { props } } where name is the legacy name for the column.

Two tags connect describe rank 2 data:

DIMENSION=\[5\] indicates this will take 5 columns. By default they are
named NAME\_x, where x=0,1,2,... and NAME is the name of the dataset or
by the column names when they start with the same letters. E.g. BGSM\_X
starts with BGSM. DIMENSION=\[10,10\] means 100 elements are specified
for the rank 3 dataset. A 1-D array may be specified as a scalar
(DIMENSION=5).

ELEMENTS=\[ 'e0', 'e1', 'e2' \]. These identify the column names, and
the columns must be adjacent.

```
# E_SPEC {
#   DIMENSION= 5,
#   ELEMENTS=[ 'e1', 'e2', 'e3', 'e4', 'e5' ]
#}
TIME e1 e2 e3 e4 e5
 
```

Jon/Reiner: We talked about having "global" properties, such as the
rec\_count and record format.

```
# { "": { REC_COUNT:1440, FORMAT="ISO8601,f5.2" }, 
#    "TIME": { LABEL: "Time_UTC", "COLUMNS": 0},
#   "DENSITY": { LABEL: "Density", SCALE_MIN:0.01, SCALE_MAX:100, SCALE_TYPE:LOG, "COLUMNS":1 } }
# TIME DENSITY 
2011-01-01T00:00 0.12 
2011-01-01T00:01 0.14
```
  
  
```
# B_gsm: { UNITS:nT, DIMENSION=3, ELEMENTS={ Bx, By, Bz }, "START_COLUMN":1}
```

# Examples

  - <http://jfaden.net:8080/hudson/job/autoplot-test030/lastSuccessfulBuild/artifact/19820105_1981-025_CPA_l2_fcf-001.txt>
  - <http://jfaden.net:8080/hudson/job/autoplot-test030/lastSuccessfulBuild/artifact/CRRES_mod_20121213.txt>
  - <http://jfaden.net:8080/hudson/job/autoplot-test030/lastSuccessfulBuild/artifact/proton_density.dat>

# 20160610

  - This has evolved quite a bit, and is in production at LANL.
  - We started a github site to contain examples, so we can lock it
    down.
  - <https://github.com/JSONheadedASCII/examples>

Jeremy's thoughts for the day:

  - Earlier specs (above) were way too permissive. Only strict JSON
    should be used, and only one JSON block.

# 20160621

Jeremy Faden, Steve Morley, and Brian Larson met to sync up the
specification for Rich ASCII. LANL calls this "JSON Headed ASCII" and it
loosely refers to the same spec as Rich ASCII. They use this format
extensively in their processing at LANL.

  - There should be a JSON\_SPEC block that contains metadata for
    parsing. This would include fields like DELIMITER, FORMAT,
    METADATA\_STANDARD (ISTP is supported, for example), and ENDIAN for
    when binary format specifiers are used.
      - DELIMITER - COMMA or WHITESPACE (default)
      - FORMAT - Fortran style specifier
      - METADATA\_STANDARD - ISTP or QDataSet (default)
      - ENDIAN - BIG or LITTLE (default)
  - Any block which contains VALUES or START\_COLUMN describes data.
  - Any block not containing these is metadata, and systems are
    encouraged to convey this for human interpretation.
  - "Rank 3" data will be supported, where DIMENSION={5,6} would mean
    that the 30 numbers are actually a stream of 2-D arrays.
  - When the METADATA\_STANDARD is not specified, QDataSet tags (NAME,
    TITLE, LABEL, TYPICAL\_MIN, TYPICAL\_MAX, VALID\_MIN, VALID\_MAX,
    FILL\_VALUE, etc) are used. Should METADATA\_STANDARD='ISTP' then
    their tags are used (FILLVAL, LABLAXIS, VAR\_NOTES, etc).
  - Encoding for the JSON portion will always be UTF-8.
  - Binary formats should be hidden for now, where this is a possible
    extension. The binary form would start following the newline and
    carriage return characters (10 and 13) after the closing JSON brace.
  - Autoplot may allow the JSON spec to be external to the data, so that
    one JSON spec could describe multiple files, and also so that a JSON
    spec might be added to an existing product, but this extension is
    not a required feature to be implemented by libraries.

# See Also

  - <https://github.com/JSONheadedASCII>

