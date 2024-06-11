This is the development release list. After testing several releases, a
release becomes final.

# Hudson

Daily builds: [1](http://autoplot.org/autoplot.jnlp?version=hudson)

# v2018a\_2

  - <http://autoplot.org/jnlp/v2018a_2/>
  - update to botched v2018a\_1 release (it wasn't clear which SVN
    version was used)

# 20180113a

  - <http://autoplot.org/jnlp/20180113a/>
  - Tweaks to QC in PNGWalk Tool
  - 1946: correction to histogram rendering

# 20180106a

  - <http://autoplot.org/jnlp/20180106a/>
  - tweaks to ascii editor to improve usability.
  - synchronize checks cadence to limit interpolation.

# v2017a\_6

  - <http://autoplot.org/jnlp/v2017a_6/>
  - minor bug fixes such as reading the recent times on the event thread
    and correcting metadata for cdf\_tt2000 variables.

# 20171216a

  - <http://autoplot.org/jnlp/20171216a/>
  - rte\_0155056645: IndexOutOfBounds caused by new quick monotonic
    check
  - 1912: corrections to trim which would skip points or leave points in
    with waveform data.
  - Corrections to SAMP support to allow multiple simultaneous requests.
  - rte\_0211810917: where a single-column ASCII file could not be read
  - a bunch of new controls for plot command, such as tick locations and
    right-axis plots.
  - the script plot command returns the plot and plotElement affected.
  - new logos\!

# 20171116a

  - <http://autoplot.org/jnlp/20171116a/>
  - correction of Java signature
  - Jython codes can define "custom renderers" which paint data onto the
    plot. See <http://autoplot.org/CustomRenderers> .
  - create PNGWalk allows running with the interactive Autoplot, instead
    of via vap file to a background process, to allow Jython extensions.
  - allow MashUp Tool to be used on a Mac, because dragging from the
    functions area doesn't work. See <http://autoplot.org/dashup> .
  - single column ASCII files can be read again.

# v2017a\_5

  - <http://autoplot.org/jnlp/v2017a_5/>
  - correction of Java signature

# v2017a\_4

  - <http://autoplot.org/jnlp/v2017a_4/>
  - PDF output improvements more precise pixel-to-point scaling.
  - "Run Batch" allows times to be loaded from events file.
  - CSV automatically switches from comma to semicolon.
  - eventsConjunction function returns where two events lists have
    overlaps.
  - new axis "scale" property supports binding between axes.

# v2017a\_3

  - <http://autoplot.org/jnlp/v2017a_3/>
  - Autoplot server has --nomessages to turn off message warning
    bubbles.
  - changes to better support SAMP.
  - improvements to completions.
  - X11 color names added, transparent colors supported.
  - More plot symbols added.

# v2017a\_2

  - <http://autoplot.org/jnlp/v2017a_2/>
  - corrections to Jython refactoring.
  - preserve the scientist's timerange in GUIs, some would reset to
    dataset default range.
  - SAMP interface handles URLs to servers.
  - 60+ bugfixes since v2017a\_1
  - 20+ new features since v2017a\_1.

# v2017a\_1

  - <http://autoplot.org/jnlp/v2017a_1/>
  - internal renaming of codes refactoring, old Jython scripts should
    still work.
  - bugfixes

# 20170707c

  - <http://autoplot.org/jnlp/20170707c/>
  - corrections to package refactoring of jython scripts.
  - 1661: revisit format to CDF on Windows
  - 1854: clean up code which relied on file.toString to construct URLs
    for the NetCDF library
  - 1836: ds.putProperty( QDataSet.UNITS, None )
  - start SAMP adds a status tab.

# 20170628a

  - <http://autoplot.org/jnlp/20170628a/>
  - refactored release moves package names to org.autoplot and
    org.das2.qds.

# 20170602b

  - <http://autoplot.org/jnlp/20170602b>
  - rte\_2052946987: index-out-of-bounds when data is reduced and all
    data is outside the visible region. Thanks, Kris\!
  - colorbar control points allow resize, useful when there is a hidden
    plot and common colorbar. Thanks, Ivar\!
  - 1839: append of two rank zero datasets should be a rank 1 dataset.
    Thanks, Kristoff\!
  - rte\_0153443069: CSV parser editor GUI would fail with
    NullPointerException because handling was delegated a sloppy code.
    Thanks, Mimai\!

# v2016a\_16

  - <http://autoplot.org/jnlp/v2016a_16>
  - allow different credentials to be used on different paths on the
    same server.
  - 1818: pngwalk of Omni DST vs KP skips each December.

# 20170521a

  - <http://autoplot.org/jnlp/20170521a>
  - Old events scheme check (time,deltaTime,color,str) was broken since
    last production release v2016a\_15. Thanks, Chris\!
  - Data Point Recorder sorting is disabled while data is loaded from a
    file, for speed. Thanks, Darrelle\!
  - Catch when "orbit:<file:///>..." was used where "<file:///>..."
    should have been used for an orbit file, which would block entry to
    the time range editor. Thanks, Ivar\!
  - Add tools menu to PNGWalkTool, and action to write PNG Walk to PDF
    file, and write sequence as animated GIF.

# 20170509a

  - <http://autoplot.org/jnlp/20170509a>
  - round of improvements to the PNG Walk Tool, including show only
    QC-marked files and zoom on image.
  - jnlp needed Codebase attribute to run without complaint. Thanks,
    IcedTea\!
  - Wind waves showed where dbAboveBackground mishandled valid range
    metadata.

# v2016a\_15

  - <http://autoplot.org/jnlp/v2016a_15>
  - PDS-PPI node now gets data from <http://pds-ppi.igpp.ucla.edu>.
  - pngwalk tool accepts \&timerange=2016 to subset the pngwalk
  - Jython editor now allows tabs to be used instead of spaces, when
    "tabIsCompletion" is false.
  - JUNO Perijove intervals added.

# v2016a\_14

  - <http://autoplot.org/jnlp/v2016a_14>
  - bugfixes since the last production release
  - innocent v2017a features introduced that don't affect function, like
    Java8 javadocs.

# 20170320a

  - <http://autoplot.org/jnlp/20170320a>
  - bugfixes leading up to next production release
  - CDF and HDF reader allows DEPEND\_0 and Y values to be specified

# 20170227a

  - <http://autoplot.org/jnlp/20170227a>
  - Null pointer when selecting time field type but time format column
    has never been set.
  - 1789: PngWalkTool correct feedback about writing to writable
    FileSystem.
  - 1754: Correctly support download of
    <http://autoplot.org/data/AMSR_E_L3_SeaIce6km_B06_20070307.hdf.gz>,
    where the .gz and Apache confuses things.
  - 1785: unable to format bundle (B-field X,Y,Z) to CDF. (Append is now
    handled properly).
  - export-to-wav has timeScale parameter for scaling time tags, useful
    for auralizing B-Field data. Thanks, Kris\!

# v2016a\_13

  - <http://autoplot.org/jnlp/v2016a_13>
  - support CDAWeb, which now uses https for transactions.

# 20170113a

  - <http://autoplot.org/jnlp/20170113a>
  - orbit plot properties are set properly from .vap files
  - script correctly use positional (not named) parameters from command
    line.
  - spectrograms with no valid ytags would cause a runtime error popup.

# v2016a\_10

  - <http://autoplot.org/jnlp/v2016a_10>
  - last release of the v2016a branch
  - fixes HAPI server client, which was doing web transactions on the
    event thread, potentially causing problems with slow servers or
    network
  - aggregation avail=T attempted to download granule metadata when it
    is not used.
  - render topDecorator is cleared when reset is called.
  - mouse modules (crosshair,etc) allow up,down,right,left keys for
    precise control.

# 20170102a

  - <http://autoplot.org/jnlp/20170102a>
  - 1740: two-columns of iso8601 do not read properly as events list
  - 1746: dasPlot created off event thread would occasionally cause RTE
    11148\*.
  - ascii file dep0units can be used to explicitly set the units, and
    does this correctly for times now as well.

# 20161109b

  - <http://autoplot.org/jnlp/20161109b>
  - improvements to run batch facility.
  - minor corrections to HAPI support.
  - change color to black from custom
  - Bookmarks when a single plot is already plotted
  - don't go into the completions editor when there is no extension.
  - break into stack of plots reconnects time series browse to new
    x-axis.

# v2016a\_9

  - <http://autoplot.org/jnlp/v2016a_9>
  - rte\_1736345160: improperly-localized strings caused RTE in layout
    tab's "make taller" and other buttons. Thanks, Andre\!
  - rte\_0095613254: if the vap+cdf: was missing from the URI,
    Tool-\>"Mash Data" would fail.
  - data set selector component setValue would add "%20" when there was
    an extra space at the end when cut-n-paste URIs.

# v2016a\_8

  - <http://autoplot.org/jnlp/v2016a_8>
  - First production release of HAPI server support.
  - update to new security certificate to correct jnlp release.
  - "Scheme BK" font is embedded and available on all platforms.
  - bugfix: likely thread lock bug when many pngwalk of many plots
    accessing the same resource.
  - bugfix: clipping of top and bottom ticks
  - various bugs with the Data Mashing tool, corrections to support for
    time series browsing of mashed datasets.
  - bugfix: command line for single-jar release would fail with some
    switches like "--help"

# 20161029a

  - <http://autoplot.org/jnlp/20161029a>
  - binary support for HAPI servers.
  - bugfix where FileSystem.create would incorrectly lock, causing
    occasional hang (1%) when multiple threads access the same
    filesystem.
  - 1699: flickering on FiltersChainPanel dialog.
  - vap+das2Server and vap+das2server were not treated as equivalent,
    causing "add plot from" initialization feature to fail.

# 20161008a

  - <http://autoplot.org/jnlp/20161008a>
  - fix clipping that occurs with some fonts
  - include Scheme font
  - support reduceMean (collapse1) with slice when possible.
  - other various minor bugs
  - improvements to the new HAPI server support.

# v2016a\_7

  - <http://autoplot.org/jnlp/v2016a_7>
  - blurTsbUri would fail when a data source type was removed
    (vap+hapi), but one of its URIs was still in the history.
  - 1677: interpolate2D should allow interpolation along edges when the
    opposite edge contains fill, performance improvements.

# 20160909c

  - <http://autoplot.org/jnlp/20160909c>
  - The spectrogram averaging code didn't properly handle NaN's used as
    fill values, causing data loss as you zoomed out.
  - Jython codes using if blocks were not properly simplified when
    automatically creating GUI control panels.
  - the layout panel would occasionally fail to repaint after recent
    bugfix where it would paint excessively.
  - rfe247, proposed years ago, where you can edit the URI without
    resetting everything else (on the data tab).
  - dataset index bounds checking flag is enabled by default now,
    improving error message precision.

# 20160902b

  - <http://autoplot.org/jnlp/20160902b>
  - two column text file of ISO8601 times can be used as an events list.
    (Thanks, Brian\!)
  - 1667: color icons not shown in events list tool.
  - 1666: Jython ds\[i,j\] would return rank 1 when i was integer and j
    was rank 0 dataset. (Thanks, Ivar\!)
  - .nc files can contain string times like "1997223000009297", plus new
    support for validMin (Thanks, Babtiste\!)
  - data mash-up dialog includes sin, cos, and other trig functions
    (Thanks, Craig and Yuko\!)
  - hilbert function added. (Thanks, Craig\!)
  - rfe521: aggregation of images is supported with new rules for
    aggregation
  - rfe523: format to wav now scales data by default (thanks, George\!)

# 20160827a

  - <http://autoplot.org/jnlp/20160827a>
  - production branch v2016a\_6 contained a bug where pan feature was
    jumpy
  - append to CDF works on Windows now
  - unnecessary paints removed
  - aggregation works with image files
  - inverse fft added
  - CDF reader replaceLabels=T will use the Y values instead of channel
    labels (14.4 eV instead of "ch01")

# v2016a\_6

  - <http://autoplot.org/jnlp/v2016a_6>
  - 1646: correction to overplot of TSB of TSB without timeaxis flips
    back to timeaxis, where a TSB would fail to bind to the xaxis.

# 20160730a

  - <http://autoplot.org/jnlp/20160730a>
  - 1649: plotting a data set below would reset the timerange
  - 1643: pngwalk file basename property would fail when when both
    product and folder contained "JNO-IONS"
  - 1646: overplot of Y(T) vs X(T) (TSB without timeaxis) flips back to
    timeaxis momentarily, causing problems with bound axes.
  - bugfix in medianFilter, which was never tested thoroughly.

# 20160723b

  - <http://autoplot.org/jnlp/20160723a>
  - 1635: xaxis fails to unbind.
  - 1637: binary source fails to read large JADE files bigger than
    250,000,000 bytes
  - recent change for setItem for datasets in Jython needed to account
    for sloppy codes.

# v2016a\_5

  - <http://autoplot.org/jnlp/v2016a_5>
  - 1630: copy plots down initializes DSF TSB properly

# 20160714c

  - <http://autoplot.org/jnlp/20160714c>
  - 1624: local .gz files are now uncompressed automatically.
  - reduce memory requirement for bundles by avoiding copy.
  - CSV and ASCII table reader use skipLines consistently

# 20160706b

  - <http://autoplot.org/jnlp/20160706b>
  - with Jython dataset indexing, where a Jython array used for an index
    was misused.
  - occasional ConcurrentModification error with Jython scripting
    finally fixed\!
  - UInt24 and Nybble support in the binary data source

# 20160701a

  - <http://autoplot.org/jnlp/20160701a>
  - more hooks for the PNGWalkTool, for building applications with
    scripts.
  - occasional ConcurrentModification error with Jython scripting
    finally fixed\!

# v2016a\_4

  - <http://autoplot.org/jnlp/v2016a_4>
  - NullPointerException when File-\>"Add plot from" was used
    immediately. Whoops\!

# v2016a\_3

  - <http://autoplot.org/jnlp/v2016a_3>
  - more hooks to allow for scripting the pngwalk
  - support for groups in HDF files.

# 20160623a

  - <http://autoplot.org/jnlp/20160623a>
  - back out flawed correction to the "Add Plot" dialog when only one
    URI is used.
  - pngwalk tool digitizer improves support for pngwalks without
    timeaxis.
  - corrections to Rich ASCII file support.
  - tweaks to the guess cadence code that often shows breaks for log Y
    axis, when there shouldn't be.
  - MMS CDF file with very negative long fill value for TT2000 was
    treated inconsistently and mucking up autoranging.

# v2016a\_2

  - <http://autoplot.org/jnlp/v2016a_2>
  - add control for the colorbar in the plot command.

# v2016a\_1

  - <http://autoplot.org/jnlp/v2016a_1>
  - 113 described bugfixes since December's production release
  - 63 described new features

# v2015a\_11

  - <http://autoplot.org/jnlp/v2015a_11>
  - improve feedback with warnings about 32bit Java on the about dialog,
    link to page explaining.

# 20160123a

  - 1511: unproductive reset of time axis when second plot URI is
    changed.
  - 1512: CDF files work more consistently on 32 bit Java installations.
  - <http://autoplot.org/jnlp/20160123a>

# 20160114a

  - PNGWalk tool allows sparse data without limits.
  - <http://autoplot.org/jnlp/20160114a>

# 20160108a

  - CDAWeb plugin uses web services to more accurately identify needed
    files.
  - CDAWeb plugin shows data availability.
  - <http://autoplot.org/jnlp/20160108a>

# 20151207b

  - <http://autoplot.org/jnlp/20151207b>
  - bug 1500: two autoplots, two editors pointing at same file
  - add code to ensure that ephemeris data is monotonic and
    non-repeating. LANL script for RBSP ephemeris is fixed, but this
    will be more tolerant of future mistakes
  - Canvas size GUI supports "7 inch" or "30 centimeters" for
    dimensions, not just pixels.

# 20151206a

  - <http://autoplot.org/jnlp/20151206a>
  - restore to maximized vap, instead of suggesting scrollbars, when
    maximized app is saved.
  - experiment with copy and paste plots.
  - 467: add accessory to allow override timerange when loading vap
    files.

# v2015a\_10

  - <http://autoplot.org/jnlp/v2015a_10>
  - corrections to dashup tool and, or operators
  - add hidden plot would intercept mouse events, making the connected
    plots difficult to work with.
  - introduce rank0 transform methods to support Jython rank 1 iterator
    returns rank 0 datasets instead of doubles, breaking Juno/Waves
    planning script.
  - 1486: minor corrections to layout tab to improve usability

# v2015a\_9

  - <http://autoplot.org/jnlp/v2015a_9>
  - colors dialog allows picking the color from the screen, from other
    applications and plot images.
  - huge scatter lines thicken as you zoom in closely.
  - updates to the Java signatures.

# 20151106a

  - <http://autoplot.org/jnlp/20151106a>
  - bugfixes with annotations
  - component property changes lock application properly for scripts.
  - AUTOPLOT\_DATA/config/colors.txt allows new colors to be added to
    palette.
  - dashup removeValues introduced. Finish off the original list of
    functions.

# 20151028a

  - <http://autoplot.org/jnlp/20151028a>
  - new certificates for WebStart
  - Jython editor detects external changes.
  - Slice and unbundle preserve more metadata

# v2015a\_8

  - <http://autoplot.org/jnlp/v2015a_8>
  - bugfix 1462: NullPointerException in the huge scatter renderer when
    cadence cannot be derived

# v2015a\_7

  - <http://autoplot.org/jnlp/v2015a_7>
  - bugfixes since the v2015a\_6 release:
  - corrections to support for the leap second, such as rendering axis
    tick at 23:59:60
  - corrections to contour renderer.
  - allow waveform cadence to change in fftPower. window correction was
    incorrectly applied.
  - xls files would have times shifted by local time zone.
  - aggregations can start with non-time wildcard like $x, and no longer
    need any time digits.
  - improvements to memory management and rendering speed.
  - Jython plot command is now the same as the plotx command, accepting
    keywords.
  - scripts can drive multiple windows and can position the windows,
    other enhancements to prepare for classroom use.
  - Improved support for HDF5.
  - improved support for huge (\>2GB) CDF files.

# 20150828a

  - <http://autoplot.org/jnlp/20150828a>
  - pngwalk can be generated from list of times with arbitrary
    filenames.
  - 1433: double-check on cadence for FFTs was too restrictive.
  - HDF5 supports where keyword

# 20150821a

  - <http://autoplot.org/jnlp/20150821a>
  - user preferences preserved when running pngwalks.
  - HDF5 editor panel.
  - opposite property for axes.

# 20150729a

  - <http://autoplot.org/jnlp/20150729a>
  - jython plot and plotx are one-and-the-same
  - new named parameters for plot command

# v2015a\_6

  - <http://autoplot.org/jnlp/v2015a_6>

# 20150716a

  - <http://autoplot.org/jnlp/20150716a>
  - Correction for fftPower, where Hann window was not applied
    correctly.
  - Automatic support for events lists in two- to four-column ascii
    files.

# 20150619b

  - <http://autoplot.org/jnlp/20150619b>
  - 1347: finally make the result from reducex have uniform timetags.
  - 1415: plotting one day of data from a yearly aggregation. The exact
    URI timerange now appears.
  - format to CDF with append multiple sets of timetags.

# 20150612c

  - <http://autoplot.org/jnlp/20150612c>
  - slices have properly hidden next/previous buttons
  - GUI title indicates if problemmatic 32bit Java is used.
  - put the script arguments on the address bar and in history.

# v2015a\_5

  - <http://autoplot.org/jnlp/v2015a_5>
  - more macros in labels, like %{METADATA.GlobalAttributes.PI\_NAME}
  - Bugfix in Webstart release, where caching would prevent updates.
  - Keep track of scripts, so they only need to be okayed once,
    enhancing security.
  - 1402: recent change in ascii URIs breaks editor when DEPEND\_0 is
    not the zeroth column.
  - Tools-\>Filters... added

# 20150521c

  - <http://autoplot.org/jnlp/20150521c/>

# v2015a\_4

  - <http://autoplot.org/jnlp/v2015a_4>
  - another correction to the data panel, caused by a botched bug fix.
  - corrections to the inline data source

# 20150423a

  - <http://autoplot.org/jnlp/20150423a>
  - bugfix to data panel, where filter would sometimes load incorrectly.

# 20150420a

  - <http://autoplot.org/jnlp/20150420a>
  - putPropertyFilterEditorPanel and putProperty filter.
  - style panels for more render types.
  - improvements to the jython editor.
  - hang detector can be enabled via
    autoplot\_data/config/system.properties, property
    enableResponseMonitor=true
  - new JavaCDF library, export to more CDF types.
  - scan button fix with waveform data.

# 20150203a

  - <http://autoplot.org/jnlp/20150203a>
  - corrections for Juno meeting, including events file reference in vap
    file, and baseurl in .pngwalk file.
  - revert aggregation/monotonic logic, which was causing too many
    problems, and add ensureMonotonic command.

# 20150124a

  - <http://autoplot.org/jnlp/20150124a>
  - minor corrections to the filters GUI
  - fftPower hints that log axis should be used.
  - medianFilter allows 3 to be used for the boxcar width.

# v2015a\_1

  - <http://autoplot.org/jnlp/v2015a_1>
  - first production release of v2015a branch includes new filters chain
    GUI.
  - release method pushes new releases to clients.

# 20150114a

  - <http://autoplot.org/jnlp/20150114a/>
  - 2015 branding
  - pow and sqrt were available but missing from the list of available
    filters
  - 1304: Partial vap support introduced bug where linestyle setting
    would be reset for time series browsing.
  - 1301: redo mechanism that resolves the same file downloaded from two
    Autoplot instances.
  - fix the labels data with Rank 2 DEPEND\_1, where stack of lineplots
    were not given unique labels

# 20141221a

  - <http://autoplot.org/jnlp/20141221a/>
  - introduction of new filters GUI

# 20141208e

  - <http://autoplot.org/jnlp/20141208e/>
  - add inches output to the canvas size in inches, listener to get
    update
  - minor bugfixes

# 20141205a

  - <http://autoplot.org/jnlp/20141205a/>
  - URI bar updates so that dates are more consistent in vap products.
  - improve feedback when a timerange must be selected from two
    timeranges.
  - cleanup to PDF writing to support bold and italic fonts.
  - bugfix where ephemeris wouldn't load for Joe.
  - get rid of Thread.sleep use, which was bad practice.

# 20141126a

  - <http://autoplot.org/jnlp/20141126a/>
  - result of aggregations will now always be monotonically increasing
    (bugfixes).
  - The old CDF-Java library is removed. The next release will also
    remove the native library.
  - Improved feedback when PDS-PPI node is not available.
  - update RBSP orbits
  - corrections to FITS reader

# 20141118a

  - <http://autoplot.org/jnlp/20141118a/>
  - result of aggregations will now always be monotonically increasing.
  - cdaweb file names are translated properly.

# 20141110c

  - <http://autoplot.org/jnlp/20141110c/>
  - initial digitizer on pngwalk tool
  - cdf where improvements

# 20141031c

  - <http://autoplot.org/jnlp/20141031c/>
  - improvements to the pngwalk GUI
  - initial digitizer on pngwalk tool

# v2014a\_14

  - <http://autoplot.org/jnlp/v2014a_14/>
  - signature fixed
  - misc bugfixes

# 20141020c

  - <http://autoplot.org/jnlp/20141020c>
  - new filter |setDepend0Cadence('30s') added, to specify explicitly
    when Autoplot fails to guess.
  - marx orbits added
  - improvements to ImageDataSource for Dave's plot where orbits are
    overlaid on mars surface

# v2014a\_13

  - <http://autoplot.org/jnlp/v2014a_13>
  - bugfix: new users would would get runtime error because of bug in
    autoplot\_data directory setup

# 20141010a

  - <http://autoplot.org/jnlp/20141010a>
  - minor tweaks
  - correction to merge routine.
  - demo 1 is now new OpenDAP server.
  - editor should not show tools automatically.

# 20141009a

  - <http://autoplot.org/jnlp/20141009a>
  - Tools are all trusted now, avoiding confirm dialog
  - Fix brand-new user runtime error as autoplot directories are created
  - jython documentation blocks shown in popups.

# 20140925b

  - <http://autoplot.org/jnlp/20140925b>
  - experiment with automatic support for .gz for individual files over
    http
  - bookmarks files are updated with compose then rename to avoid
    corruption.
  - bugfix to the bookmarks, no asterisk meaning needs update.

# v2014a\_12

  - <http://autoplot.org/jnlp/v2014a_12>
  - tweaks to Jython script panel
  - RBSP orbits to 2014-10-19
  - generalize mean, mode, stddev, and variance to support any rank
    dataset by using DataSetIterator. Support fill data.

# 20140920a

  - <http://autoplot.org/jnlp/20140920a>
  - bugfix in CDF where test Maven files were misread because of old
    kludge.
  - tools are now stored in bookmarks/tools.xml, allowing remote
    bookmarks files of tools and hierarchies.

# 20140916a

  - <http://autoplot.org/jnlp/20140916a>
  - reload all reloads the TCA
  - 1250: Ephemeris (TCAs) from TSBs at the mission beginning and NRT
    handled poorly.
  - rfe387: support gzip encoding in downloadResourceAsTempFile.
  - rfe386: interpolation routines must only extrapolate modestly.

# v2014a\_11

  - <http://autoplot.org/jnlp/v2014a_11>
  - bugfix in locking which would mess up pngwalk generation
  - 1255: slow rendering of flash feedback could basically hang
    application.
  - 1253: bugfix in locking which would mess up pngwalk generation

# 20140905b

  - <http://autoplot.org/jnlp/20140905b/>
  - bugfix in locking which would mess up pngwalk generation

# v2014a\_10

  - <http://autoplot.org/jnlp/v2014a_10/>
  - bugfix in ytags reported by histogram2d

# 20140829b

  - <http://autoplot.org/jnlp/20140829b/>
  - last dev before v2014a\_10
  - histogram and histogram2d indices corrected by 1-half bin.
  - misc bugfixes.

# 20140815b

  - <http://autoplot.org/jnlp/20140815b/>
  - pdsppi maturing
  - 2-line Y-axis label center justified by default, option to set
    justification added.
  - misc bugfixes.

# 20140808a

  - <http://autoplot.org/jnlp/20140808a/>
  - pdsppi supports discovery
  - AutoplotServer images are set to .vap file height and width by
    default
  - Kristoff pointed out where Jython GUI wouldn't reset properly when
    dom.plots\[0\].yaxis.range was used as default.

# v2014a\_9

  - <http://autoplot.org/jnlp/v2014a_9/>
  - pngwalk can write pdfs instead of png files.
  - update RBSP orbit numbers to 2014-08-13.

# 20140724a

  - <http://autoplot.org/jnlp/20140724a/>
  - bugfix in the completions-based editor, used by HDF5 and NetCDF.

# 20140722e

  - <http://autoplot.org/jnlp/20140722e/>
  - tweaks/clean up to make jython scripts environments more consistent
  - pitch angle distribution rendering
  - URI format/parse to use + in timerange parameters instead of %20, so
    the URIs are more legible.

# 20140719b

  - <http://autoplot.org/jnlp/20140719b/>
  - changes in http handling to support GitHub.
  - minor improvements to CEF handling.
  - improvements to pitch angle distribution plotting.

# v2014a\_8

  - <http://autoplot.org/jnlp/v2014a_8/>
  - 1216: series renderer mis-configured for large datasets rendering.
  - 1224: Time Series Browse load when timerange is context (not
    x-axis),then zoom in on timerange.
  - jyds would use 2010-01-01 (the default timerange) incorrectly.
  - OpenDAP looks for missing\_value and title metadata, preparing to
    update demo 1 bookmark.
  - add butterworth and medianFilter to the filters

# v2014a\_7

  - <http://autoplot.org/jnlp/v2014a_7/>
  - vap files can be streamed into Autoplot, supporting servers.
  - improvements to metadata in VOSPASE files from PDSPPI node.
  - improvements to xls export to support appending and writing to
    multiple sheets.

# 20140606a

  - <http://autoplot.org/jnlp/20140606a/>
  - aggregate all breaks with jyds script with timerange param
  - File-\>print is performed off the event thread, avoiding possible
    hangs
  - jython script can be run from any Autoplot window

# v2014a\_6

  - <http://autoplot.org/jnlp/v2014a_6/>
  - miscellaneous bugfixes.
  - memory leaks for batch processing
  - allow the main window for jython scripts to be reset.
  - popup dialog asks which timerange to use when it is ambiguous.

# v2014a\_3

  - <http://autoplot.org/jnlp/v2014a_3/>
  - last of three first releases of the 2014 branch.
  - v1.08 files fix problems with autorange properties in vap files.
  - include Nand's new Java CDF reader in the stable jars, export to CDF
    from single-jar release.

[Autoplot\_Change\_Log\_archive](Autoplot_Change_Log_archive "wikilink")
