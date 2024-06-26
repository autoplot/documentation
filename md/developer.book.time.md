It's worthwhile to have a section to talk about how time is handled in
Autoplot.

# Units, LocationUnits, and TimeLocationUnits

Times are stored in Autoplot as a type of Datum, which is a number and a
unit representation of the number. Location units have a basis, like
"north from equator", and Time Location Units have a basis instant in
time. This means that there is no single way that times are represented.
They might be expressed in microseconds since 2000-01-01T00:00Z, or they
might be in days since 1970-01-01T00:00Z. This allows data to be
preserved in many formats. For example, CDF data in recent missions is
tagged by CDF\_TT2000, which is the number of nanoseconds since
2000-01-01T00:00:00.000000000Z, including leap seconds. This data can be
read into Autoplot and represented using the same numbers, and a units
converter converts the data to different epochs if needed.

Most time formats skip leap seconds. This has the benefit that
calculation of decomposed times (Year, Month, Day, Hour, ...,
Nanosecond) can be done without depending on a table of leap seconds
which could become outdated. Note however that events which occur during
the leap second are not properly represented, and subtractions used to
calculate distances will be missing the leap second as well.

# Other topics suggested by Ivar

  - different formats (cdfTT2000, ...)
  - internal representation/expected precision
  - converting between formats
  - creating epoch variables/arrays (sec. 9.13 in cookbook, ...)
  - addition/subtractions issues
  - an index of epoch-related functions
  - input/output (including time sting parsing and output formatting)
    (sec. 7.2 in cookbook, ...)
  - events lists (sec. 2.3 in cookbook, ...)

