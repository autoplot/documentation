# Audience

Script developers and those using the Data Pointer in applications like
digitizing.

# Introduction

The Data Point Recorder (DPR) is a built-in component which receives
data points and collects them to form a new data set. For example, with
Plasma Waves data at the University of Iowa, we track the bottom cut-off
of a spectrogram, from which we can infer the local plasma density. The
scientist marks points along the bottom by clicking their mouse, and
then a digitizer tab will contain the points. Once each day is
completed, the data points are then saved to a file.

# Scripts and Programs that use the DataPointRecorder

The DPR is created and addDataPoint is called to insert data.

sorted means that points are sorted in X as they are inserted. Note that
as a file is read in, the data will not be resorted.

snapToGrid means the points will be rounded to regular grid locations.
For example, if any point within a minute should be tagged with the
start of the minute, snapToGrid would be set to True, and XTagWidth is
set to 60 seconds.

dpr.addAccessory(JComponent) allows additional controls to be added. For
example, in the PNG Walk Tool's use of the DPR, a control for the marker
type (crosshair or vertical line) is added.

# Output File Format

The output written is a tab-delineated ascii file, where times are
encoded as ISO8601. The first line are column headers and in parenthesis
are the units, so Y() means the column is called Y and is dimensionless.

# Notes

The value -1e31 is always treated as a fill value. (Units.FILL\_DOUBLE
can be used in scripts.) See also the mouse modules which create data
from mouse clicks and other gestures.
