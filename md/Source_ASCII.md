## Reading ASCII

An editor can be used to help develop a URI with the appropriate
parameters for Autoplot to read and plot data in a ASCII file. The list
of parameters that may be used in a URI is given
[below](#parameters "wikilink"). A table is displayed showing how the
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

  - extensions: .dat, .txt
  - URI prefix: vap+dat, vap+txt
  - example URLs:

<ftp://nssdcftp.gsfc.nasa.gov/spacecraft_data/omni/omni2_1963.dat?column=field17&timerange=1963>  
<http://goes.ngdc.noaa.gov/data/avg/2004/A1050412.TXT?skip=23&timeFormat=$y$m$d+$H$M&column=E1&time=YYMMDD>  
<ftp://nssdcftp.gsfc.nasa.gov/spacecraft_data/omni/omni2_$Y.dat?column=field17&timerange=1963&timeFormat=$Y+$j+$H&time=field0&validMax=999>

#### Parameters
The GUI composes URIs, but for completeness the control parameters in ASCII
URIs are described below.

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

## See Also
See also [ascii_data_source.md].
