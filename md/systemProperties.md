Purpose: describe system properties that can be set.

This should be a copy of code in AutoplotUtil.java, and this file is
created in USER/autoplot\_data/config/system.properties .

```
# Autoplot loads these system properties on startup.  See http://autoplot.org/systemProperties.  These are used to provide alternate
# behavior to groups and to allow users to experiment with new features.

# reference cache allows some URIs to be resolved once per plot.
#enableReferenceCache=true

# use new LANL-requested Nearest Neighbor rebinning that looks at bin boundaries.
#useLanlNearestNeighbor=true

# do check on index and rank with commonly used datasets, at a slight performance cost.
#rangeChecking=true

#email RTEs by default, instead of HTTP POST, when firewall prohibits put calls.
#autoplot.emailrte=true

# use wget to download data instead of Java's built-in network protocols. Should be command line or empty.
#AP_WGET=/usr/local/wget

# use curl to download data instead of Java's built-in network protocols. Should be command line or empty.
#AP_CURL=/usr/bin/curl

# provide option in save dialog to embed data within a zip file.
#allowEmbedData=true

# don't show icon in legend when there is only one renderer
#reluctantLegendIcons=true

# monitor the event thread for hangs.
#enableResponseMonitor=true

# turn off certificate checks.
#noCheckCertificate=true
```
Note that some of these properties are now enabled by default. For
example, referenceCaching is a mature feature that is enabled by
default.

These are read in the code (or Jython scripts) using System.getProperty
calls like:

