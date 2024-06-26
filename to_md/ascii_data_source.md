The ASCII table parser has enough controls and features that it should
have its own page. This page describes in detail what it can do and how
it is used.

# What it can do

Autoplot's ascii parser looks in ascii files for tables of data. It
breaks up the file into records and fields, and records with the correct
number of fields are treated as data. Presently a record is always a
newline-delimited line. (^M, ^J, and ^M^J are all treated as newline
delimiters.) The record is generally broken up by tabs or whitespace
into fields. When a line has the "right" number of fields, it is
considered a data record. "Right" is in quotes because the user can
explicitly control the number of fields, or the code can also guess the
number of fields, essentially looking in the file for the data records.
When a line contains the right number of fields, but the fields are not
parsable, it tries to extract labels for the fields from the record.
Non-records can contain metadata as well, and this is described later.
Last, field parsers are "pluggable" so for example, times and nominal
data can be parsed as well.

So in short, this:

  - parses tables with the same number of fields in each record
  - ignores lines that do not appear to be records
  - grabs labels and units from a line that has the correct number of
    fields, but fields are not parseable.
  - has pluggable field parsers to handle times and nominal data
  - has pluggable record parsers to handle fixed columns and regular
    expressions as well.

## What it cannot do

  - parse records with variable field counts.
  - parse records that span multiple lines. (Presently, this wouldn't be
    too difficult to support.)
  - parse multiple tables

# Records and non-records

A record is a line that breaks up into the correct number of fields, and
doesn't start with a comment character. Sometimes comments are treated
as data fields in this case, but when they do not parse, the record is
disposed of. There can be failures, for example:

` data file created 1/2/2011`  
` 1 2 3 4 `  
` 2 3 4 5 `  
` 1 2 3 4`

![ascii\_data\_source\_wiki\_1.png](ascii_data_source_wiki_1.png
"ascii_data_source_wiki_1.png")

causes problems because the first line, which is a comment but isn't
explicitly marked as such, is treated as a record of column headers.
There is a control to skip a number of lines before parsing.

Generally there should be a space between implicit comments, or better
yet prefix comments with hash marks when possible. Note too that the
number of fields determines how if a line is a record or not. So if you
have spaces in column headers and spaces are used to delimit files, then
the column header will be missed.

Note this parser will not be able to parse all files. Hopefully, though,
it's capable of parsing many files, and simple improvements can be made
to it so that it handles more files.

## Parsing Column Headers and Units

The parser tries to create useful labels and names for each column. The
name is a URI-friendly string used to identify columns, which can also
be used as a variable name. The label is a human-readable label for the
column. Here are a few rules for them:

  - column headers cannot follow valid data records
  - density(nT) -\> name="density" label="density" unit="nT"
  - Ch1(34.4-68.3) -\> column name="Ch1" label="Ch1(34.4-68.3)"
    unit=dimensionless

Note that if a label cannot be used, then "field<n>" is used for the
column. Right now, there are limitations on what is used for a label,
including the characters: a-z, A-Z, 0-9, and " \_\[\]()". (TODO: I'm not
sure why this restriction exists.)

# Field parsing

The parser provides codes for automatically configuring parsing. These
will break on field delimiters as it works with most files, yet still
has acceptable performance. (Note that the fixed columns parser has the
best performance.) Fields will be broken up on delimiters found in
records, first looking for commas, then tabs, and then whitespace when
commas and tabs are not found. Note the ASCII parser can be configured
to use a particular delimiter when the guess fails.

Each field has its own parser for converting text into a number. The
default is just a number parser (Java's Double.parseDouble). Often
though, the field is an ISO8601 formatted time, or time of some other
format, and special field parsers are available for this. In Autoplot's
ASCII table data source, checking time in the GUI will use this instead.
Note that an ISO8601 time in the first column is automatically handled.

To be more precise, the das2 Units are identified for each column, and
the unit is responsible for interpreting each field. When time is
detected, a das2 time unit is specified for the column, and the parser
works. Note when the AsciiParser is used directly (not through the ASCII
data source), ordinal values can be handled as well.

# Use in Autoplot

Note Autoplot's ASCII Table Data Source is a wrapper for QDataSet's
ASCII parser, org.virbo.dsutil.AsciiParser. It abstracts the table read
from the ascii file a bit further, pulling out individual records and
also combining records to form times.

# Source Code

The source code for further review is here:

[AsciiParser.java](https://autoplot.svn.sourceforge.net/svnroot/autoplot/autoplot/branches/autoplot2010/QDataSet/src/org/virbo/dsutil/AsciiParser.java),
the code that parses ascii tables.

[AsciiTableDataSource.java](https://autoplot.svn.sourceforge.net/svnroot/autoplot/autoplot/branches/autoplot2010/DataSourcePack/src/org/virbo/ascii/AsciiTableDataSource.java)
the Autoplot plugin data source that wraps AsciiParser.java and provides
parsing of dates when dates span multiple fields.
