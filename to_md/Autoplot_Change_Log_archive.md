# 20140421b

  - <http://autoplot.org/jnlp/20140421b/>
  - introduce butterworth filter
  - rendering bug 1129 fixed.
  - lanlNN support time-varying Y-Tags in spectrograms.

# v2013b\_11

  - <http://autoplot.org/jnlp/v2013b_11>
  - various minor bugs
  - various minor features after MMS meeting

# v2013b\_10

  - <http://autoplot.org/jnlp/v2013b_10>
  - JNLP cleanup to improve startup.
  - NetCDF and HDF spaces were not handled properly.
  - various minor bugs

# v2013b\_8

  - <http://autoplot.org/jnlp/v2013b_8>
  - minor new features such as events list tool.
  - all tabs are properly initialized on events thread.

# 20140221e

  - <http://autoplot.org/jnlp/20140221e/>
  - introduce events list tool, which makes it easy to navigate a list
    of events.
  - createEvent is more consistent with events file format.
  - das2 data source leaves progress monitor spinning with ephemeris
    data.

# v2013b\_7

  - <http://autoplot.org/jnlp/v2013b_7>
  - minor improvements to JythonDataSource, including support for
    "(a,b)=myfunc()" in data set selector.

# 20140204a

  - <http://autoplot.org/jnlp/20140204c/>
  - minor corrections to Jython Data Source.
  - color scatter bug pointed out by Scott is fixed.
  - flipped property added to the vap files.

# v2013b\_6

  - <http://autoplot.org/jnlp/v2013b_6/>
  - corrections to fix v2013b\_5 and its misrendering of data.
  - 1148: correction to reference cache, guards against dataset
    mutabilility.
  - layout tab allows drag to swap plot position.
  - RBSP orbits updated to 2014-02-03

# v2013b\_5

  - <http://autoplot.org/jnlp/v2013b_5>
  - Botched release with attempt to make rendering more efficient.
  - reference cache finally fixed, by making read-only copy of mutable
    datasets.

# v2013b\_4

  - <http://autoplot.org/jnlp/v2013b_4>
  - Introduce make immutable switch to finally correct mismatch between
    ideal design and real implementation.
  - DataSetSelector focus on macs.
  - "CDF URI needs an argument" with CDF and re-enter on java webstart.

# 20131112a

  - <http://autoplot.org/jnlp/20131112a/>
  - empty cdf throws NoDataInIntervalException instead of runtime
    exception to support scripting.
  - first general support for VOTables
  - 1095: experimental handling of ReferenceCache was flawed.

# v2013a\_17

  - <http://autoplot.org/jnlp/v2013a_17/>
  - Series mode has a more useful rendering of data when there are \>
    200000 points.

# 20131106a

  - <http://autoplot.org/jnlp/20131106a/>
  - 1124: deadlock observed on a mac
  - 1122: horiz slice on mageis-l2 data fails
  - 1120: large dataset handling by SeriesRenderer

# 20131030a

  - <http://autoplot.org/jnlp/20131030a/>
  - scripts like CreatePngWalk could hang when a runtime error occured
    because the exception handler was not set up.
  - .jy parameters panel would mess up timeranges.
  - vertical and horizontal slices have slope mouse module.
  - .d2t and .qdst resolve to das2stream reader, after new extensions
    were introduced for ascii versions.

# 20131021a

  - <http://autoplot.org/jnlp/20131021a/>
  - return code from createPngWalk.

# v2013a\_16

  - <http://autoplot.org/jnlp/v2013a_16>
  - minor bugfixes
  - introduce "now" for timerange strings
  - pngwalks from event lists

# v2013a\_15

  - <http://autoplot.org/jnlp/v2013a_15/>
  - getParam implementation in jython based on simplified syntax tree.

# 20130915a

  - <http://autoplot.org/jnlp/20130915a>
  - minor bugfixes and rte fixes.
  - 320: jython syntax tree used for scraping for getParam calls, also
    tree path is considered.
  - 322: bookmarks button for "Add axis annotations" dialog

# 2013a\_12

  - <http://autoplot.org/jnlp/v2013a_12>
  - Fonts embedded in PDF output.
  - cancel properly handled in aggregation
  - same as 2013a\_11 release, but also bugfix in Java/CDF with
    one-element dimensions.

# 20130807b

  - <http://autoplot.org/jnlp/20130807b/>
  - PDF switch allows fonts as shapes or not.
  - Taller/Shorter buttons on the layout tab

# v2013a\_10

  - <http://autoplot.org/jnlp/v2013a_10/>
  - bugfix with events scheme ascii file
  - clean up of tearoff tabbed pane
  - bugfix lock up with LANL vap fixed by tighten thread safety.
  - support "import autoplotapp as app"
  - support slice at time |slice0('2012-03-05T00:00') to explore this
    type of slicing

# 20130730c

  - <http://autoplot.org/jnlp/20130730c>
  - experimental wget-based filesystem to provide http to those behind
    challenging firewalls.

# 20130724a

  - <http://autoplot.org/jnlp/20130724a>
  - used for demo at LANL

# v2013a\_9

  - <http://autoplot.org/jnlp/v2013a_9>
  - correction to the fix to remove flickering.
  - other minor bugfixes

# v2013a\_8

  - <http://autoplot.org/jnlp/v2013a_8>
  - more fixes, including vectors from CDAWeb and a round fixes for
    annoying bugs like:
      - flickering when adjusting the slice index
      - don't use valid range from CDF as typical range when typical
        range is missing.
      - |multiply(-2) didn't work
      - fixes to bounding boxes when in script mode so elements are
        completely drawn.
      - \-3010.00 in ascii file was triggering code that looked for
        ISO8601 years.
  - and new features:
      - datum as index for slice0 location
      - recent history handles wildcards like "rbsp\*.vap"

# v2013a\_7

  - <http://autoplot.org/jnlp/v2013a_7>
  - post-GEM meeting fixes.

# v2013a\_5

  - <http://autoplot.org/jnlp/v2013a_5>
  - Release for GEM 2013
  - Scripts (.jy) can now have parameters, similar to .jyds scripts.
  - bugfix with CDF UNITs causes problems

# 2013a\_1

  - <http://autoplot.org/jnlp/v2013a_1>
  - first release of new branch in name only.
  - improved support for ISO8601 time strings.

# v2012b\_29

  - <http://autoplot.org/jnlp/v2012b_29/>
  - numerous bugfixes

# 20130412e

  - <http://autoplot.org/jnlp/20130412e>

# v2012b\_28

  - <http://autoplot.org/jnlp/v2012b_28>

# v2012b\_27

  - <http://autoplot.org/jnlp/v2012b_27>
  - Ascii reader's non-ascii check didn't count tabs as ascii.
  - Add additional ticks dialog keeps its own history.
  - export ascii table properly handles time-varying y tags that are
    actually constant.
  - spectrogram verifies monotonic timetags so non-monotonic tags marks
    as monotonic won't mess it up.
  - "user@" inserted into URLs that needed authentication messed up
    PngWalk Tool's "view in autoplot" button.

# v2012b\_25

  - <http://autoplot.org/jnlp/v2012b_25>
  - bugfix in export data when data is processed.
  - minor new features including limit selectable exports to valid
    options.

# v2012b\_24

  - <http://autoplot.org/jnlp/v2012b_24>
  - botched bug in the slice1 keyword for the binary CDF reader.

# v2012b\_23

  - <http://autoplot.org/jnlp/v2012b_23>
  - various bugfixes

# 20130307c

  - <http://autoplot.org/jnlp/20130307c>
  - fixed <http://www.rbsp-ect.lanl.gov/> completion
  - fixes problem with slicing where recent code changes broke the
    slicer
  - runtime error about bad format code "v" in completion
  - AutoplotDataServer would truncate datasets when an exception was
    encountered.
  - progress monitors and long warning messages were not erased properly
    for short plots.

# 20130227d

  - <http://autoplot.org/jnlp/20130227d>
  - various bugfixes.

# v2012b\_22

  - <http://autoplot.org/jnlp/v2012b_22>
  - a number of bug fixes and minor new features

# v2012b\_21

  - <http://autoplot.org/jnlp/v2012b_21>
  - a number of bugfixes since the pre-AGU release.

# 20121221a

  - <http://autoplot.org/jnlp/20121221a>
  - release preceeding v2012b\_21

# 20121219a

  - <http://autoplot.org/jnlp/20121219a>
  - fix old bug in layout where panels wouldn't quite be the same size.

# 20121215a

  - <http://autoplot.org/jnlp/20121215a>
  - 3596098: canvas image on layout tab is always repainted, never
    cached
  - clean up of bookmarks, when bookmark is dragged to or from remote
    folder.
  - GUI can finally be shrunk to small sizes, time range editor droplist
    was setting minimum size

# 20121121a

  - <http://autoplot.org/jnlp/20121121a>
  - introduce reduce in aggregation
  - rename jnlp title to add space in "Autoplot (20121121a)"
  - allow rank 2 depent\_1 and bundle\_1 switching.

# v2012b\_20

  - <http://autoplot.org/jnlp/v2012b_20>
  - jython editor handles long default parameter values without messing
    up GUI
  - clean up applet and servlet compile scripts

# v2012b\_19

  - <http://autoplot.org/jnlp/v2012b_19>
  - bugfix in hugeScatter where occasionally it would fail to repaint
  - events renderer mouse allows for multiple event messages
  - local paths ending with /tmp would fail.
  - cdf-java will attempt to use swap memory outside of JVM, then use
    JVM memory if that fails.

# 20121113a

  - <http://autoplot.org/jnlp/20121113a>
  - hugeScatter repaint bug finally corrected
  - eventsBar shows overlapping events in mouse popup

# v2012b\_18

  - <http://autoplot.org/jnlp/v2012b_18>

# 20121108a

  - <http://autoplot.org/jnlp/20121108a>
  - CDF-Java fails when memory outside the JVM is not available, now CDF
    is read directly into JVM memory
  - Time Range Tool doesn't loose orbit number when reentering GUI.
  - TCA Ephemeris doesn't block when loading, progress indicator
  - sparse records in CDFs

# v2012b\_17

  - <http://autoplot.org/jnlp/v2012b_17>
  - Time range editor GUI
  - sparse records in CDFs

# 20121030a

  - <http://autoplot.org/jnlp/20121030a>
  - introduces TimeRangeEditor
  - allows jython scripts to register hooks that can reject quit
    request, so digitized work is not lost.

# 2012b\_16

  - <http://autoplot.org/jnlp/v2012b_16>
  - bugfix in pngwalk tool generate, where underscore was always added
    when invoking for review
  - lspec routine handles fill in timetags.
  - orbit 00003 and 3 were not recognized are not considered equal in
    all codes, resulting in pngwalk failure.
  - minor bugfixes

# 2012b\_15

  - <http://autoplot.org/jnlp/v2012b_15>
  - http files without parents can be accessed again, which was
    inadventently broken in v2012b\_3
  - minor bugfixes

# v2012b\_12

  - reduce number of threads as a stopgap to fix problem where one vap
    can overload a server (Dan's server with 12 data sources)
  - CDF fixes

# 2012b\_8

  - <http://autoplot.org/jnlp/v2012b_8>
  - fix bug noticed by Seth where DEPEND\_1/BUNDLE\_1 datasets would not
    range correctly
  - miscellaneous bugfixes.
  - introduce rank2 waveform support.

# v2012b\_5

  - <http://autoplot.org/jnlp/v2012b_5>
  - introduce waveform scheme for QDataSets, where waveform is rank2
    dataset with base for DEPEND\_0 and offsets for DEPEND\_1,
    introduced for speed.
  - bugfix: remote compressed bookmarks were broken since mid-August.

# v2012b\_4

  - <http://autoplot.org/jnlp/v2012b_4>
  - new production release. Earlier versions (v2012b\_3) were released
    but were not pushed.

# 20120914

  - <http://autoplot.org/jnlp/20120914a>
  - miscellaneous bugfixes, including:
      - single-tick bug on short plots
      - JythonMain bug where some scripts would fail because of
        automatic imports
  - split plot function in \[layout\]-\>plots-\>add plots
  - current render type is indicated.

# 20120912

  - <http://autoplot.org/jnlp/20120912c/>
  - misc bugfixes
  - minor GUI improvements:
      - checkbox to turn off title
      - checkbox on plot type indicates current setting
      - ctrl-S saves vap.

# 20120907

  - <http://autoplot.org/jnlp/20120907c>
  - minor new features such as:
      - title now has checkbox and can be turned off without erasing
        useful context.
      - clicking on background selects hidden parent plot element.
  - fix layout looks at visible property.

# rbsp-ect-20120905b

  - <http://autoplot.org/jnlp/rbsp-ect-20120905b>
  - Named so to work around bug/problems with LANL firewall
  - bugfix in ftp filesystem where cache failed to load new versions of
    files
  - bugfix in jyds where TimeSeriesBrowse capability was incorrectly
    fixed.
  - bugfix in labelling when series plots are used to render rank 2 data
    after slicing.
  - total, smooth, and collapse operators all preserve metadata.

# v2012b\_3

  - <http://autoplot.org/jnlp/v2012b_3>
  - more testing and cleanup of http filesystem.
  - Jython editor improvements

# v2012b\_2

  - <http://autoplot.org/jnlp/v2012b_2/>

# 20120816

  - <http://autoplot.org/jnlp/20120816b/>

# v2012b\_1

  - fairly radical changes in how threads are managed, this version is
    quite experimental and contains known bugs not present in the 2012a
    branch.
  - <http://autoplot.org/jnlp/v2012b_1>

# v2012a\_12

  - <http://autoplot.org/jnlp/v2012a_12>
  - Use CDF library 3.4.1 to avoid initial delay
  - CDAWeb source gets data from
    "<http://cdaweb.gsfc.nasa.gov/sp_phys/data/>"
  - NetCDF cleans up resources, fixing problems observed on Windows.
  - Introduce boolean variables for .jyds scripts.

# v2012a\_11

  - <http://autoplot.org/jnlp/v2012a_11>
  - cdaweb thread problems demonstrated on Windows.

# v2012a\_10

  - <http://autoplot.org/jnlp/v2012a_10>
  - v2012a\_9 released but never released because of problems with FTP
    on windows.
  - cdaweb gets data from http to avoid problems with FTP on windows.
  - FTP cleaned up. Files were left open, causing visible problems on
    windows.
  - several RTE users submitted were fixed.
  - valid\_range in data tab fixed when vap is loaded.

# v2012a\_9

  - <http://autoplot.org/jnlp/v2012a_9>
  - 3533882: reset of timerange when move plot caused by handler
    ignoring binding
  - bugfix when remote http host is in accessible, runtime error
    prevented offline use.
  - Profiling used to remove memory leaks. Now all CDF quantities can be
    plotted in one session.
  - ytagWidth is used from the first table of a rank 3 join dataset. Now
    we use the maximum of all tables.
  - $o and $(o properly detected in pngwalk tool

# v2012a\_8

  - <http://autoplot.org/jnlp/v2012a_8>
  - bugfixes after batch run of all CDA datasets
  - tweak rules for getRepresentativeFile in FileStorageModel. Check for
    valid date (year\<9000) and handle where unprocessed empty folders
    exist.
  - various minor bugfixes
  - work with O'Brien and Weigel on LSpec routine.
  - Script version of the servlet is back, with new security checks
  - introduce orbitPlot type.

# v2012a\_7

  - <http://autoplot.org/jnlp/v2012a_7>

# v2012a\_6

  - <http://autoplot.org/jnlp/v2012a_6>
  - version presented at the RBSP meeting, May 15th 2012.
  - source was tagged at
    <http://autoplot.svn.sourceforge.net/svnroot/autoplot/autoplot/tags/v2012a_6/>
  - v2012a\_5 was a botched release that showed obvious problems
  - corrections and minor tweaks
  - cleanup round of pngwalk, performance issues associated with image
    reduction and excessive caching.
  - TimeRange selector shows if no one is listening.
  - remote-remote bookmarks are all read at once
  - improvements to support das2servers, and reduction of data from URIs
    on server side.

# v2012a\_4

  - <http://autoplot.org/jnlp/v2012a_4>
  - corrections and minor tweaks

# v2012a\_3

  - <http://autoplot.org/jnlp/v2012a_3>
  - first version to be pushed out on the front page of autoplot.org
  - minor corrections and tweaks

# v2012a\_2

  - minor corrections and tweaks

# v2012a\_1

  - first release of new production branch
  - this was not pushed onto the main page because of E.G.U. meeting.

# 20120406c

  - <http://autoplot.org/jnlp/20120406c>
  - bugfixes and minor features
  - use production release of CDF3.4.0
  - orbits in pngwalks
  - first filters GUI button
  - plot from bookmarks manager

# 20120331b

  - <http://autoplot.org/jnlp/20120331b>
  - bugfixes and minor features
  - orbits in pngwalks
  - first filters GUI button
  - plot from bookmarks manager

# 20120320

  - <http://autoplot.org/jnlp/20120320a>
  - corrections to filesystems create, cleanup when failures occur.
  - support "orbit:<http://das2.org/wiki/index.php/Orbits/rbspa-pp:29>"
    so anyone can create and publish orbits files
  - bugfix: remote bookmarks load with "bookmarks:..." at the command
    line.
  - hash long names in downloadResourceAsTempFile
  - reload all data button
  - first export to IDLSAV and HDF5
  - last dev release before updating production branch to "v2012a\_1"

# 20120310

  - <http://autoplot.org/jnlp/20120310>
  - Introduction of CDF time type TT2000, which includes leap seconds.
  - bugfix to the filesystems create, tighten up synchronization so one
    can be created independently from others.
  - initial support for using orbit numbers to control times
    "orbit:crres:591"
  - minor cleanup of pngwalk tool

# v2011a\_11

  - <http://autoplot.org/jnlp/v2011a_11> on 2012-02-25
  - v2011a\_10 was a botched release because I left a test the RTE
    report so RTEs could not be reported
  - bugfix $Y$(m,span=6)$d and resetZoom\[XYZ\] null pointer exception
    when no dataset is plotted.

# v2011a\_10

  - <http://autoplot.org/jnlp/v2011a_10> on 2012-02-24
  - v2011a\_9 was a botched release and was never linked or announced.
  - various tweaks and clarifications to GUI requested by Reiner at
    LANL.
  - clarification of feedback gui failure in LANL firewall environment.
  - delay construction of axes and style guis to improve startup on a
    mac.
  - bugfixes in autorange
  - initial support for TT2000 in Java/CDF reader (vap+cdfj:...).
    C-based reader will be next update.
  - initial support for \[Menubar\]-\>View-\>Reset Zoom-\>Reset Y
  - other more minor bugs

# v2011a\_8

  - <http://autoplot.org/jnlp/v2011a_8> on 2012-02-09
  - A change in v2011a\_7 caused datasets to fail to automatically bind
    to the application timerange.
  - stress testing revealed some interesting memory leaks. These are
    addressed.
  - data sources with TimeSeriesBrowse, that have a URI without the
    timerange, are accepted by binding automatically to the application
    timerange.
  - other more minor bugs

# v2011a\_7

  - <http://autoplot.org/jnlp/v2011a_7>
  - bugfixes for Windows when using ftp
  - rfe: tearoff tabs can be dropped into undocked tabs
  - jython scripts with TimeSeriesBrowse caching improved, script=
    switch supported in editor.
  - occasional deadlock (frozen application) found and fixed.
  - severe memory leak fixed that would affect scripts loading and
    unloading data
  - minor changes to menu bar, see View and Help menus.

# 20120125a

  - <http://autoplot.org/jnlp/20120125a>
  - bugfixes for Windows when using ftp
  - rfe: tearoff tabs can be dropped into undocked tabs
  - jython scripts with TSB caching improved.

# v2011a\_6

  - <http://autoplot.org/jnlp/v2011a_6>
  - updates to the production release, including a number of Jython
    improvements.

# 20120109b

  - bugfixes and minor new features released for testing.

# v2011a\_1

  - <http://autoplot.org/jnlp/v2011a_1>
  - new production version.

# 20111214b

  - <http://autoplot.org/jnlp/20111214b>
  - prerelease for new production version.

# 20111203

  - <http://autoplot.org/jnlp/20111203>
  - remove overlaps bug when em offsets were not taken into account
  - finish off bugs with remote bookmarks
  - file-\>open File split into separate for data files and vap files
  - restoring a large vap file onto a small screen now prompts for
    scaling or scrollbars

# 20111122

  - <http://autoplot.org/jnlp/20111122>
  - quite a few bugfixes and minor new features

# 20111028c

  - <http://autoplot.org/jnlp/20111028c/>
  - bugfixes in CDAWeb plugin where modified all.xml would no longer
    parse properly because they corrected local file references.
  - FTPBeanFileSystem presents login dialog when anonymous ftp is not
    allowed.
  - findbugs analysis used to clean up code

# v2010v\_19

  - <http://autoplot.org/jnlp/v2010b_19/>
  - prepare for bugfix in CDAWeb all.xml file. This bugfix will break
    old versions of Autoplot's CDAWeb reader.
  - bugfix: support autoplot2011 v1.07 vap files

# 20111018

  - <http://autoplot.org/jnlp/20111018/>
  - bugfixes to stabilize for production use
  - bugfixes with CDAWeb plugin, and support for more popular virtual
    variables.
  - Improved XML encoding of bookmarks files
  - \--basic command line option

# v2010b\_18

  - <http://autoplot.org/jnlp/v2010b_18/>
  - minor bugfixes:
      - some remaining internationalization problems (Java localizes
        numbers like 3,14 when decimal point should always be used)
      - XML format errors of RTE reports (clients would not see the
        error)
      - timeout when uploading error report
  - bugfix:CDAWeb would fail if it was entered before any data had been
    plotted.
  - ability to read 2011 bookmarks files

# 20110924

  - <http://autoplot.org/jnlp/20110924/>
  - bugfixes to stabilize for production use
  - basic mode introduced to simplify GUI for browsing applications

# 20110910

  - <http://autoplot.org/jnlp/20110910/>
  - bugfixes to stabilize for production use

# v2010b\_17

  - <http://autoplot.org/jnlp/v2010b_17>
  - minor bugfixes.

# 20110821

  - <http://autoplot.org/jnlp/20110821/>
  - bugfixes from the production release
  - minor features from the production release
  - column labels in ascii files improved for "30.0-45.0eV"

# v2010b\_16

  - <http://autoplot.org/jnlp/v2010b_16>
  - bugfixes for MMS/Themis files include improved feedback in CDF reads
  - move some minor 2011 features back to 2010.
  - runtime error submission includes vap and undo list.

# 20110727

  - <http://autoplot.org/jnlp/20110727/>
  - bugfixes from the production release

# v2010b\_15

  - <http://autoplot.org/jnlp/v2010b_15>
  - bugfixes to undo after multiple plots are added.

# 20110722

  - <http://autoplot.org/jnlp/20110722/>
  - undo images

# 20110707

  - <http://autoplot.org/jnlp/20110707>
  - faster startup

# 20110624

  - <http://autoplot.org/jnlp/20110624>
  - introduce "script:<file>"
  - improvements to "script:" and "pngwalk:" completions
  - bugfixes in das2server

# v2010b\_14

  - <http://autoplot.org/jnlp/v2010b_14>
  - botched v2010b\_13 release was missing extension not recognized
    bugfix.
  - move over code from 2011 version that inserts agg timerange from
    xaxis to avoid rejecting.

# v2010b\_13

  - <http://autoplot.org/jnlp/v2010b_13>
  - bugfix: dialog when extension isn't recognized.
  - bugfixes with CDAWeb
  - history dialog migrated over from the 2011 branch.

# 20110616

  - <http://autoplot.org/jnlp/20110616>
  - bugfixes from the production branch and on the development branch
  - User options for day-of-year labels and nearest neighbor rebinning
    for spectrograms.
  - Improve time series browse support in "internal" datasets.
  - Improve time series browse support in Jython data sources.

# 20110604

  - <http://autoplot.org/jnlp/20110604>
  - prototype ability to hide address bar. Options-\>Address Bar-\>Time
    Range Selector
  - menu of the menu bar GUI elements moved to style tab

# 20110524

  - <http://autoplot.org/jnlp/20110524>
  - update to the production version containing bugfixes from production
    branch.
  - array-of-vectors scheme supported.
  - first coding of events bar support

# v2010b\_12

  - <http://autoplot.org/jnlp/v2010b_12>

# v2010b\_11

  - <http://autoplot.org/jnlp/v2010b_11>
  - update to the production version containing bugfixes for:
      - CDF\_UCHAR supported
      - extraneous "vap:" qualifier confusing
      - null pointer exception in completion.
      - raise the Autoplot window when "View in Autoplot" is pressed on
        pngwalk window.
      - remove extra flashes when just one plot is visible.
      - check for invalid make pngwalk specs like "$Y$m$d\_$H$m" (2 m's)
  - and also:
      - python script editor includes example scripts.

# v2010b\_10

  - <http://autoplot.org/jnlp/v2010b_10>
  - update to the production version containing bugfixes for:
      - runtime errors in pngwalks handled properly
      - null pointer exception in completion.
      - at (@) symbols in username for authenticated URLs
      - decimal year (1976.0000) handled in ascii parser.

# 20110427

  - <http://autoplot.org/jnlp/20110427>
  - improve support for rich headers, including support in ascii gui
    selector.

# 20110422

  - <http://autoplot.org/jnlp/20110422>
  - improve support for rich headers, including support in ascii gui
    selector.

# v2010b\_9

  - <http://autoplot.org/jnlp/v2010b_9>
  - use mirror of CDF libraries

# 20110408

  - <http://autoplot.org/jnlp/20110408>
  - bugs and minor features migrated from production branch
  - CDF libraries mirrored to Autoplot.org

# 20110407

  - <http://autoplot.org/jnlp/20110407>
  - bugs and minor features migrated from production branch
  - first version of the recent history dialog (File-\>Open Recent...)

# 20110405

  - <http://autoplot.org/jnlp/20110405>
  - bugs and minor features migrated from production branch

# v2010b\_8

  - <http://autoplot.org/jnlp/v2010b_8>
  - update fixes a number of minor bugs
  - hidden plots for binding are handled properly in add plot below.
  - more improvements to user feedback, try to avoid RTE for normal
    operations.
  - JythonDataSource editor fixed.

# 20110325

  - <http://autoplot.org/jnlp/20110325>
  - update to the production version of Autoplot. "v2010b\_6"
  - fairly big bugfixes, including:
      - colorbar disconnected when move spectrogram
      - null pointer exceptions
      - Java/CDF exceptional branches updated to match C version
  - detect file not found and give a more pleasant message.
  - reduce Findbugs bug detections.

# 20110324x

  - <http://autoplot.org/jnlp/20110324x>
  - update to the development version of Autoplot2011.
  - merge over bugfixes from autoplot 2010 branch.

# 20110311

  - <http://autoplot.org/jnlp/20110311>
  - update to the development version of Autoplot2011.
  - controls for ticklen/direction, OutsideNE label position.
  - merge in bugfixes from production version
  - bugfixes in rich headers for ascii files

# 20110307

  - <http://autoplot.org/jnlp/20110307>
  - <http://autoplot.org/jnlp/v2011b_5>
  - update to the production release
  - uses new version of Java CDF library
  - rank 2 Y tags handled properly in spectrogram
  - minor bugfixes

# 20110219x

  - <http://autoplot.org/jnlp/20110219x>
  - development release has new URI selector component

# 20110215x

  - <http://autoplot.org/jnlp/20110215x>
  - development release made for Ivar to fix a bug with Cluster CDF he's
    plotting
  - also contains new Ascii rich headers.

# 20110212

  - <http://autoplot.org/jnlp/20110212>
  - update to the production release
  - round of GUI cleanup, including focus of range selectors pointed out
    by Aaron
  - bugfixes in CDAWeb GUI, usuability improvements.
  - jython conflicts cleaned up a bit, introducing listDirectory and
    coerceToDs to replace list and coerce.

# 20110121

  - <http://autoplot.org/jnlp/20110121>
  - update to the production release
  - cdaweb data source masters logic corrected
  - off-line support for ftp.
  - clean up source to allow checkout onto filesystems that ignore upper
    and lower case.
  - other minor bugfixes.

# 20110114

  - <http://autoplot.org/jnlp/20110114>
  - bugfixes of pngwalk, including all views have decorations for
    quality control.
  - bugfix in cdf-java where epoch16 is used.
  - other minor bugfixes.

# 20110110

  - <http://autoplot.org/jnlp/20110110>
  - update to the production version includes support for nested
    bookmarks.
  - minor bugfixes.

# 20101221

  - <http://autoplot.org/jnlp/20101221>
  - production release of new branch that uses QDataSet throughout,
    including das2 graphics
  - introduces direct support for CDAWeb
  - more aggressive GUI improvements
