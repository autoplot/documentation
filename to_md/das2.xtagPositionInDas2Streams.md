Purpose: Consider how to handle understanding of the x position in
das2streams. Some readers serve the data with the beginning of the bin,
and some use the center of the bin.

Audience: das2 Developers (This page will be moved once we have a better
wiki).

# Introduction

In a weekly meeting we were talking about how the x tags is represented
in das2streams. Many of the das2streams tag the center of the bin, and
the das2 code assumes this as well as most of the stream processors.
However a good number of them tag the beginning of the bin, because this
is how das1 streams worked.

das2 renders data (by default) using bilinear interpolation. Four points
bracketing a region will be used to fill in the region. This works
because the tags are at the center of the accumulation interval for the
measurement, and the center best describes this location. Similarly,
when a line plot draws a connecting line between to points, the same
assumption is made.

The old das1 streams were rendered to the screen using the last point
received at any given time, which is consistent with the old model that
the tag was the beginning of the interval.

# Codes that make the middle assumption

  - binAverageSeconds assumes that the point is in the middle of the
    bin. X values are averaged together to make a new X value in the
    output.
  - spectrogram renderer assumes that interpolation can be done between
    two points. The cadence is only calculated to detect breaks in the
    data.
  - spectrogram renderer in nearest neighbor mode needs the cadence to
    figure out the beginning and ends of the bin.

# Solutions

  - das2streams should allow metadata to indicate the sampling time. For
    example, there's a xTagWidth width that is often used for the
    cadence, and we could add additional data like:
      - xTagPosition which would be one of "center" or "begin"
      - xBinRange which can be a DatumRange, for example "-30 to 30
        seconds" "0 to 60 seconds" or "-7 to 7 percentIncrease"
