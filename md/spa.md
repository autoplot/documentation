Draft of SPA Newsletter Announcement

# Newsletter Announcement

Autoplot release announcement

Autoplot [1](http://autoplot.org/) is an interactive browser for data on
the web; given a URL of a data file, it tries to create a sensible plot
of the contents in the file. Autoplot was developed to allow quick and
interactive browsing of scientific data files that are often encountered
on the web. Interactive and stylized special views of data that combine
data from multiple resources can be saved and shared as bookmarks.

A large suite of bookmarks containing multiple panels using data from
many data providers is available by selecting from a list of bookmarks
in the Autoplot folder of the Bookmarks menu.

This release introduces three types of bookmarks:

1\. Raw - Selecting a raw bookmark will result in an automatic
single-panel display of data from a given data provider. (Some GUI
interaction may be required for some bookmarks.) Click the right or left
arrows to view the day after or day before the day in view.

2\. Special Views - Stylized plots using data from many data providers.
For examples, see the ViRBO sub-folder. Examples of Data Views include
stack plots of measurements from Polar, Cluster, ACE, THEMIS, and NPOES.
Data Views are generally created by scientists using the Expert GUI mode
and Raw Bookmarks and then contributed to ViRBO's Special Views
repository. A tutorial for creating special views will be presented at
the Summer 2012 GEM workshop.

3\. Overviews - A data set for which the initial view is of the full
time range of available data. Draw a box on a time range to zoom in on a
specific time interval.

To try Autoplot, click [this
link](http://autoplot.org/autoplot.jnlp?mode=basic&open=bookmarks:http://autoplot.org/bookmarks/heliophysics.xml),
which initiates a \~10-second installation process that works on most
operating systems and browsers.

See <http://autoplot.org/help#Installation> for browser-specific
installation hints, [help](help.md) for usage instructions,
and send email to <http://groups.google.com/group/autoplot> for help.

When the installation is complete, browse bookmarks by selecting a
bookmark under the Bookmarks menu item (the bookmarks may take a few
seconds to appear after Autoplot starts). To see more information about
a bookmark, select Bookmarks-\>Browse and Manage and click the button
labeled Detailed Description.

Autoplot was developed under the NASA Virtual Observatories for
Heliophysics program in a collaborative effort among several
institutions, including support or code contributions from ViRBO, VMO,
RBSP-ECT, and the Radio and Plasma Wave Group at The University of Iowa.

# Testing

## Test links and comments

Start after deleting all bookmarks.

  - <http://autoplot.org/autoplot.jnlp?mode=basic&open=bookmarks:http://autoplot.org/bookmarks/heliophysics.xml>

Make this be an alias to the above:

  - <http://autoplot.org/autoplot.jnlp?config=heliophysics>

and have the following re-write to the above

  - <http://autoplot.org/autoplot-heliophysics.jnlp>

and then have

  - <http://autoplot.org/config#heliophysics> describe the configuration
    and default bookmarks?

## Issues

This shows a bug in the cgi script:

  - <http://autoplot.org/autoplot.jnlp?open=bookmarks:http://autoplot.org/bookmarks/heliophysics.xml&mode=basic>

but this works

  - <http://autoplot.org/autoplot.jnlp?mode=basic&open=bookmarks:http://autoplot.org/bookmarks/heliophysics.xml>

<!-- end list -->

  - Jeremy will change so that bookmarks inherit parent folders
    description-url if one is not specifed.
  - Aggregation across zip files does not work. Bug will be fixed.
  - <ftp://virbo.org/POES/n15/$Y/poes_n15_$Y$m$d.cdf.zip/poes_n15_$Y$m$d.cdf>?
    results in 550 Failed to change directory error.
  - Need some indication for how to un-grey the Data Set selector in
    basic mode? Or, should data set selector switch you to expert mode?
    (**to discuss**)
  - 2010-01-01 shows up in Time Range bar (Should say "Select bookmark
    or File-\>Add Plot From"?)
  - When clicking on Bookmarks, I see \[loading\] then Demos ... then
    Autoplot \[loading\] appears after a few seconds. There is about 3
    seconds where no indication is given that more loading is taking
    place.
  - After launching I click Autoplot-\>ViRBO-\>Special Views-\>SWPC and
    see the data selector but I never explicitly switched.
  - What is the syntax for P1D? Will P10D work?
  - Bob needs to add "See ..." for Special Views.
  - We are going to get a complaint about metadata for bookmarks. Could
    we have a <metadata> tag associated with each bookmark-folder?
  - Should I remove Autoplot-\>Demos?

{{\#lst:help|Installation}}

