Purpose: describe how vap versioning is done.

The vap file itself is versioned, providing the ability for a new
Autoplot to write vap files which an old version can read. For example,
the "scale" property is added to the Axis node, but old versions of
Autoplot won't know what this is and will fail.

Currently Autoplot writes out v1.07 files, and 1.08 exists as a marker
that auto-ranging should be performed as prescribed in the file.

v1.09 introduces the scale property, but earlier Autoplot versions fail
when reading these because the binding code doesn't allow for bindings
to unknown properties. Autoplot v2017a\_4 will correct this by dropping
bindings to properties it doesn't know with a warning. Release 20171021a
will handle this by writing a v1.08 file, but will remove the bindings
between scale.

