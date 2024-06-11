Purpose: Fully describe the Create PNGWalk Feature, and the PNGWalk
Tool.

Audience: Scientists

See also: <http://autoplot.org/PNG_Walks>

# Introduction

PNG Walks are a set of images which together study a mission which
cannot be captured in one image. These are typically daily plots from a
many-year mission. We want to be able to quickly flip through images to
find unusual events, for example. If we were to do this using Autoplot
interactively, we might be limited by the time the data takes to load.
In this case we can set up the PNGWalk to run over night, and then use
the PNGWalk Tool to flip through plots in the morning.

Autoplot is able to both produce PNG Walks and look at them. To look at
them, the PNG Walk Tool is used, which lets you flip through images
quickly, looking at thumbnails and using the mouse wheel.

# Create PNG Walk

  - Template used to specify the file names and implicitly the interval
    size.
  - Orbits can be used to create files by orbits.

## Autorange Some, But Not All, Axes

Autoplot v2018a\_3 now allows some of the axes to autorange, while
others are fixed. In the vap (or current configuration), edit each axis
so that its "autorange" property is set if you intend for it to be
autoranged. Axes where this is not set are left alone.

See also <http://autoplot.org/AxisAutoRangeHints>, which allows
additional hints (like include zero or select width from a set of
possibilities) to be set.

# PNG Walk Tool

  - Any set of images can be loaded, they need not be the same size or
    time tagged.
  - The "QC" (Quality Control) tool can be used to annotate images when
    the files are local.
  - clicking on the image will give plot coordinates. This is done by
    looking for special metadata within the PNG files.
  - The QC tool can also be used to create tutorials, where a script
    grabs captions from the QC files.

# Basic PNGWalk

  - A set of files in a directory. These are loaded with ".../\*.png"
    for example. png, jpg, and gif images are supported.
  - the directory can be a local folder, a web folder, or within .zip
    file (as any Autoplot data can be).
  - thumbs subdirectories can exist but are not required.
      - thumbs100 are thumbnails roughly 100 pixels corner to corner
      - thumbs400 are thumbnails roughly 400 pixels corner to corner
      - directories should contain thumbnail images with the same
        filename as the full-size image.
      - if the file is not found, a thumbnail is generated from the
        full-size image (but not stored).
  - "QC" files are files containing annotations for the files. This will
    be the image filename, plus .ok or .problem extensions.
      - the QC tool can be used to read and further annotate files.
      - annotation is only supported for local files and when ftp is
        used.
  - png files can contain axis information, so that pixel-to-data
    transformations can be done.
