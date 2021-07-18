# URIs
Autoplot URIs are compact representations of data.  These allow files to record what data
is used, for example in a .vap file, but also allow data to be loaded in one line
of code, and for one scientist to tell another to look at something in an email.  

## History
Autoplot keeps a history of every URI ever plotted.  This is useful when you have a study
which you return to once a year and you need to know what data was used.  File->"Open URI History"
starts up a dialog for browsing, where the URIs are split into groups by day and week.  You 
can filter here too, because often part of a URI is known.  ("I know it was data from the
RBSP mission", so you filter by "RBSP".)

## Usage 
URIs are used all over Autoplot.  Here are some example uses:

* Send reference to data to a colleage
* Save a history of everything ever plotted
* Create a test bed of data to plot in nightly tests
* inline script URIs contain other URIs embedded within.
* Load data into Matlab, IDL, or Python scripts
* Instruct Autoplot script to load data into a variable in a script.
