This outlines the lost changes and the block of changes committed after
the great SourceForge crash of 2015:

Email from SourceForge:

    SourceForge experienced a storage fault on 2015-07-16. Service restoration
    has been in-progress since that time, and our latest full status update is online at:
    http://sourceforge.net/blog/sourceforge-infrastructure-and-service-restoration-update-for-724/
    
    Subversion data has generally been restored to the 2015-07-14 backup. We have identified
    497 Subversion repositories which received commits after 2015-07-13 and before the storage fault.
    Your project, autoplot, is one of those repositories.
    
    To determine which repositories are missing recent commits, we compared the
    revision count currently in your repository on disk (Current revision on disk)
    to the revision count seen by our repository tracking (Current revision in database).
    The repository tracking database does not house a full copy of your commit data.
    We determined data needed to be committed again because the Current revision
    on disk is less than the Current revision in database.
    
    Analysis of your repository compared to our SCM repository tracking data shows:
    Current revision on disk: 17127
    Current revision in database: 17139
    
    Recent commit events tracked in database:
    r17109 jbfaden Mon Jul 13 2015 11:37:09 GMT+0000 (UTC) 1428 hide the filters name, which was leaking i...
    r17110 jbfaden Mon Jul 13 2015 11:37:44 GMT+0000 (UTC) 1428 hide the filters name, which was leaking i...
    r17111 jbfaden Mon Jul 13 2015 11:38:39 GMT+0000 (UTC) this test looks important.
    r17112 jbfaden Mon Jul 13 2015 12:45:14 GMT+0000 (UTC) reject method must see if the file could be int...
    r17113 jbfaden Mon Jul 13 2015 13:22:43 GMT+0000 (UTC) make room for the colorbar in test140.
    r17114 jbfaden Tue Jul 14 2015 11:39:46 GMT+0000 (UTC) version 20150714.0636
    r17115 jbfaden Tue Jul 14 2015 11:42:46 GMT+0000 (UTC) clean up and indicate the hostname as well.
    r17116 jbfaden Tue Jul 14 2015 11:43:06 GMT+0000 (UTC) clean up and indicate the hostname as well.
    r17117 jbfaden Tue Jul 14 2015 14:00:08 GMT+0000 (UTC) 1428 hide the filters name, which was leaking i...
    r17118 jbfaden Tue Jul 14 2015 14:00:15 GMT+0000 (UTC) 1428 hide the filters name, which was leaking i...
    r17119 jbfaden Tue Jul 14 2015 16:24:49 GMT+0000 (UTC) bugfix: initial create whitelist.txt file would...
    r17120 jbfaden Tue Jul 14 2015 22:40:39 GMT+0000 (UTC) bugfix 1408: log the URI after the dialog box i...
    r17121 jbfaden Tue Jul 14 2015 23:18:10 GMT+0000 (UTC) release notes
    r17122 jbfaden Wed Jul 15 2015 01:00:44 GMT+0000 (UTC) scroll to selection. expand components when th...
    r17123 jbfaden Wed Jul 15 2015 01:14:11 GMT+0000 (UTC) check for all support_data variables.
    r17124 jbfaden Wed Jul 15 2015 01:16:29 GMT+0000 (UTC) release notes
    r17125 jbfaden Wed Jul 15 2015 11:58:46 GMT+0000 (UTC) release notes
    r17126 jbfaden Wed Jul 15 2015 12:23:21 GMT+0000 (UTC) release notes
    r17127 jbfaden Wed Jul 15 2015 12:23:29 GMT+0000 (UTC) release notes
    r17128 jbfaden Wed Jul 15 2015 15:50:59 GMT+0000 (UTC) demo general path rendering speed test.
    r17129 jbfaden Wed Jul 15 2015 18:20:20 GMT+0000 (UTC) Initial coding linear version of the code. tur...
    r17130 jbfaden Wed Jul 15 2015 18:43:06 GMT+0000 (UTC) go back to width=3 to recover N**2 log N result.
    r17131 jbfaden Wed Jul 15 2015 20:30:59 GMT+0000 (UTC) make a note about anti-aliasing restoring linea...
    r17132 jbfaden Wed Jul 15 2015 22:50:53 GMT+0000 (UTC) bugfix: remove code that was applying the windo...
    r17133 jbfaden Thu Jul 16 2015 00:44:26 GMT+0000 (UTC) Operations name change
    r17134 jbfaden Thu Jul 16 2015 00:57:17 GMT+0000 (UTC) Operations name change
    r17135 jbfaden Thu Jul 16 2015 12:36:13 GMT+0000 (UTC) allow server=0 to indicate that the port will b...
    r17136 jbfaden Thu Jul 16 2015 12:36:40 GMT+0000 (UTC) allow server=0 to indicate that the port will b...
    r17137 jbfaden Thu Jul 16 2015 12:38:49 GMT+0000 (UTC) restore server ability to import items. I'm no...
    r17138 jbfaden Thu Jul 16 2015 13:50:59 GMT+0000 (UTC) add test to measure performance of the series r...
    r17139 jbfaden Thu Jul 16 2015 13:51:51 GMT+0000 (UTC) support null for z in plot(chNum,label,x,y,z,re...
    
    
    Since commits were made to your repository after our restore point, it will be necessary
    for you to coordinate within your team to ensure these changes are recommitted.
    
    We recommend you make a backup of your existing repository checkout, then make
    a fresh checkout of the repository in another directory, copy over any changes
    and commit. Depending on the number of developers on your team and the granularity
    of change tracking you need for these uncommitted changes, you may need to tune
    this process for your project. Please coordinate with the other developers on
    your project team before committing.
    
    If you have any follow-up questions or concerns, please contact the
    SourceForge Support team by submitting a ticket at:
    https://sourceforge.net/p/forge/site-support/new/
    
    Thank you,
    
    SourceForge Support

# SVN Logs

SVN had one last release where I could see the changes immediately
before the release:

```
`
```
    restore server ability to import items.  I'm not sure why this was disallowed earlier this spring. (detail)
    allow server=0 to indicate that the port will be picked automatically. (detail)
    allow server=0 to indicate that the port will be picked automatically. (detail)
```
`
```
# Other machines

I had changes on my home workstation as well, and these now need to be
merged in. I am:

  - svn co -r 17127
    <https://svn.code.sf.net/p/autoplot/code/autoplot/trunk> autoplot
  - cd autoplot

```
2008  svn info .
```
`2009&nbsp;&nbsp;svn&nbsp;copy&nbsp;.&nbsp;`&lt;https://svn.code.sf.net/p/autoplot/code/autoplot/sourceforge_crash2015&gt;  
`2010&nbsp;&nbsp;svn&nbsp;mv&nbsp;`&lt;https://svn.code.sf.net/p/autoplot/code/autoplot/sourceforge_crash2015&gt;`&nbsp;`&lt;https://svn.code.sf.net/p/autoplot/code/autoplot/branches/sourceforge_crash2015&gt;  
```
2011  svn switch `<https://svn.code.sf.net/p/autoplot/code/autoplot/branches/sourceforge_crash2015>` .
2012  ls
2013  svn status
2014  cd ..
2015  cd autoplot_uncommitted_head/
2016  ls
2017  find . -name '.svn'
2018  find . -name '.svn' -exec rm -fr {} \; -prune
2019  find . -name '.svn'
2020  ls VirboAutoplot/
2021  find . -name 'build' 
2022  find . -name 'build' -exec rm -fr {} \; -prune
2023  find . -name 'build' 
2024  ls VirboAutoplot/
2025  find . -name 'dist' 
2026  find . -name 'dist' -exec rm -fr {} \; -prune
2027  ls VirboAutoplot/
2028  cd VirboAutoplot/
2029  cd ..
2030  rsync -av autoplot_uncommitted_head/ autoplot/
2031  ls
2032  cd autoplot
2033  ls
2034  svn status
2035  find . -name 'nbproject'
2036  find . -name 'nbproject' -exec svn revert {} \; -print
2037  svn status
2038  svn status | grep java
2039  svn diff VATesting/src/org/autoplot/test/Test_054_FftFilter.java
2040  svn diff QDataSet/src/org/virbo/dataset/DataSetOps.java
2041  svn diff dasCore/src/org/das2/components/DataPointRecorder.java
2042  svn diff JythonSupport/src/org/virbo/jythonsupport/PyQDataSet.java
2043  find . -name 'nbproject'  -print
2044  find . -name 'nbproject'  -print -exec rm -r {}/* ; 
2045  find . -name 'nbproject'  -print -exec rm -r {} ; 
2046  find . -name 'nbproject'  -print -exec rm -r {}/* \; 
2047  ls -l ./*/nbproject/
2048  ls ./*/nbproject/*
2049  rm -r ./*/nbproject/*
2050  kill %1
2051  rm -fr ./*/nbproject/*
2052  svn update
2053  svn diff
2054  svn status
2055  svn diff VirboAutoplot/src/org/virbo/autoplot/AutoplotUI.java
2056  ls VATesting/Test_*.png
2057  rm VATesting/Test_*.png
2058  svn status
2059  rm -r VirboAutoplot/pngwalk*
2060  rm -r VirboAutoplot/temp-classes/
2061  rm -r VirboAutoplot/temp-src/
2062  ls
2063  svn status
2064  rm VirboAutoplot/hs_err_pid*
2065  svn status
2066  rm VATesting/Test_*.vap
2067  rm APLibs/lib/ScienceDataInterfaces.jar *
2068  ls
2069  ls -lrt
2070  svn status
2071  svn update
2072  svn status
2073  rm -r VirboAutoplot/output-listOfTimes
2074  rm -r VirboAutoplot/autoplot.jar 
2075  rm VATesting/hs_err_pid29*
2076  svn status
2077  rm APLibs/svn-commit.tmp APLibs/lib/guava-18.0.jar APLibs/lib/QDataSetScienceDataInterface.jar 
2078  ls
2079  ls -lrt
2080  svn status
2081  rm -r VirboAutoplot/temp-volatile-*
2082  svn status
2083  rm -r dasCore/lib/CopyLibs
2084  svn status
2085  cp VATesting/src/org/autoplot/misc/SeriesRendererRenderingSpeed.java /home/jbf/ct/autoplot/study/rendererSpeed/
2086  cp VATesting/src/org/autoplot/misc/GeneralPathRenderingSpeed.java /home/jbf/ct/autoplot/study/rendererSpeed/
2087  rm VATesting/src/org/autoplot/misc/GeneralPathRenderingSpeed.java VATesting/src/org/autoplot/misc/SeriesRendererRenderingSpeed.java 
2088  svn status
2089  rm -r META-INF
2090  ls
2091  svn status
2092  svn info
2093  svn commit -m "commit changes since the sourceforge crash of 2015, which will need to be merged back into the trunk."
2094  svn diff VirboAutoplot/src/external/PlotCommand.java
2095  svn diff -r{17127:17131} VirboAutoplot/src/external/PlotCommand.java
2096  svn diff -r{17127:17130} VirboAutoplot/src/external/PlotCommand.java
2097  svn diff -r17127:17131 VirboAutoplot/src/external/PlotCommand.java
2098  history
```
# breakdown of changes 17128

I thought it would be useful to summarize that big commits.

  - cdfn and cdfj loggers combined to "cdf" since there's just one cdf
    source.
  - bug where cdf editor had no visible variables because of bugs with
    CDF editor (Mark, Matt at UNH).
  - bug where labels were array \[N\] instead of \[1,N\] corrected.
  - ds\[rank0ds\] handled in Jython
  - flattenRank2 handles rank 1 DEPEND\_1.
  - correction where FFT window was applied twice corrected.
  - qds supports BIN\_PLUS and BIN\_MINUS properties, WEIGHTS.
  - verify the qstream packet length is less than 1000000, to aid in
    debugging.
  - warning icon persists, where it was cleared mistakenly before.
  - scriptContext formatDataSet allows error bar.
  - imports are allowed with server port again. Simon needs them and I
    don't see any significant security risk.
  - updates to many of the example scripts.

## features

  - improvements to DashupTool.
  - automatic support for events list in ascii file.
  - update the port reported when the server is on, to support automatic
    selection of port with --server=0.

# breakdown of changes 17132

  - Ops.labels renamed to Ops.labelsDataset, to avoid name clashes.
  - completions within command, like plotx(<C>) where we need to look up
    the documentation for plotx.
  - more support for color argument in plotx, see
    <http://sarahandjeremy.net:8080/hudson/job/autoplot-test037/lastSuccessfulBuild/artifact/getColorDemo.jy>
  - plot and plotx command are finally one and the same.
  - rte\_0759798375
  - check for null in setSymbolConnector, setColor, setFillColor.

## features

  - plotx command legendLabel named parameter added.
  - plots linestyle added.

