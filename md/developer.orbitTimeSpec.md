# Purpose

Define spec for having orbits as time ranges

# Audience

Scientists wishing to browse by orbit

# Quick Introduction

Often it's more appropriate to browse a series of data by orbit, since
each the orbits identify similar intervals and intervals like days have
little meaning. Because of this Autoplot is able to handle orbit numbers
the same way it does times. For example, the string "February 2012"
means the time interval 2012-02-01T00:00 to 2012-03-01T00:00, and "next"
means "March 2012," even though they have different numbers of days. The
string "orbit:rbspa-pp:30" means the perigee to perigee orbit id 30 of
the RBSP-A spacecraft. The are orbits are identified in the file
<http://www-pw.physics.uiowa.edu/rbsp/orbits/rbspa_pp>, and those for
"orbit:rbspb-pp:30" are found in
<http://www-pw.physics.uiowa.edu/rbsp/orbits/rbspb_pp> .

# Spec

The following string refers to one orbit of the CRRES spacecraft:
"orbit:crres:509". These orbits are defined here:
<http://das2.org/Orbits/crres.dat>. Autoplot uses the following logic to
resolve an orbit:

  - where you have the orbit string "orbit:<SCID>:<ORBITID>" look for
  - <http://das2.org/Orbits/><SCID> and
  - on the classpath Orbits/<SCID>.dat

The file should contain a set of lines with three values: "<st> <et>
<NUM>" where <st> and <et> are ISO8601 (eg $Y-$m-$dT$H:$M) times. Note
this is the events file format, and also that lines not containing these
three fields are ignored. This allows the orbits files to exist within a
wiki page, using \<pre\> and \</pre\> to indicate the table is
preformatted. I found also that orbits are often described as "<NUM>
<st> <et>", so this is supported as well. The code looks for three
whitespace-delimited fields, with the middle one an ISO8601 time, and
either the first or last field an ISO8601 time.

"orbit:<http://das2.org/Orbits/crres.dat:509>" is supported as well.
Schemes "<file://>", "<http://>", "<https://>", and "<ftp://>" are
supported here. Note this does not use Autoplot's data loading, so data
may not exist in zip files or via sftp, and must be a text file.

# Orbits in Time Ranges

We also need to be able to create times (and filenames) using orbits for
timeranges. For example, you should be able to create a pngwalk by
orbit, so you might want to name each file by the orbit number. In this
case we might format the names of the files like so:

```
product_$4(o,id=rbspa-pp).png
```

instead of

```
product_$Y$m$d.png
```

The default field length will be 5 characters and the default pad will
be underscore. The digit prefixing the field (4) identifies the length,
and the pad keyword identifies pad character (only \_ and 0 are
supported):

```
product_$4(o,id=rbspa-pp,pad=0).png
```

## Multiple Orbit Ranges

Surely people will want to be able to specify multiple orbits. As with
multiple years, the field is repeated and the second is exclusive. TODO:
check on this.

# Examples

## Different Time Ranges

Note you can get the template for this in the Autoplot Time Range
Selector by right clicking, then Examples. You will need to press enter
to accept the time. Here are some more examples:

  - orbit:rbspa-pp:30, which is the same as
  - orbit:<http://www-pw.physics.uiowa.edu/rbsp/orbits/rbspa-pp:30>
  - Available orbits: <http://www-pw.physics.uiowa.edu/rbsp/orbits/> and
    <http://das2.org/Orbits/>.
  - And: <https://github.com/das-developers/das2meta/tree/main/orbits>

## Run PNGWalk with Orbit-based timeranges

We want to run a png walk with parameters plotted orbit by orbit.

  - \[Autoplot Menu Bar\]-\>Tools-\>Create PngWalk
  - Time Format: $(o,id=crres)
  - Time Range: 1991-Feb

