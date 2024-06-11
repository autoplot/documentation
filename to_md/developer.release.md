Purpose: Describe how Autoplot is released

Audience: Autoplot developers

# Introduction

Autoplot's release has grown incrementally over the years. For example,
the screenshot with each release, was put in after a user would get
confused about which version he was running. Since then the screenshot
has been one a favorite part of the release procedure, digging through
screenshots to identify the release. This describes the current
procedure for the release, and updates for the 2015 development.

Note in this document ROOT is used to identify the root of the Autoplot
distribution, and is generally working copy of
<https://svn.code.sf.net/p/autoplot/code/autoplot/trunk>.

# Release Script

The hudson server at
<http://apps-pw.physics.uiowa.edu/hudson/job/autoplot-release/> is used
to create releases. This provides a pushbutton to run a standard
procedure for creating a release. The pushbutton asks for the release
tag, which is a string that identifies a release. The current version is
checked out of the svn from sourceforge and the das2 svn, and the a
script is run to build both the JNLP release as well as the single jar
release. Note this procedure runs nightly as well, and a tag is
automatically assigned to the version.

# Screenshots and Branding

The screenshots are used to "brand" the release, by which we mean to
make a release easily recognizable. The file
ROOT/VirboAutoplot/src/screen.png is the screenshot used for any
release. Note this is generally a 60% reduced screenshot of the
application, and the script
<http://autoplot.org/data/tools/createScreenShot.jy> takes the
screenshot and erases the background for you. (Note this script should
also do the 60% reduction, but for now gimp or similar is used. TODO:
add this.)

The web page used to describe the release is
ROOT/VirboAutoplot/src/index.html. This includes a series of bullet
points describing bugfixes and new features.

# Versioning

Releases are versioned with one of two strings. Development versions are
tagged with the current date and a sequence letter (20150121a). The
sequence letter is meant only to make it trivial to update later in the
day. Production versions are tagged with a year, branch sequence letter,
and a version sequence letter (v2015a\_1). For example v2015a\_1 means
this was the first production release of the 2015a branch. The branch
sequence was meant to allow for having multiple branches in one year,
but this hasn't been necessary. The idea was that a new production
branch could introduce a bunch of new functionality, so there would be
two periods of adding new features in the year for the 2015a and 2015b
branches.

# Bugfixes and new features

A bugfix corrects a mistake and does not introduce new functionality,
and a new feature introduces new functionality but may introduce new
bugs. Development releases will have new features, along with bugfixes,
while production releases should only be bugfixes. Ideally any
production release will contain a superset of the functionality of the
previous production release. New branches of the production release will
contain more new features that have been proven in development releases,
while older revisions in the branch will contain just bugfixes.

# Webstart releases

Webstart is a mechanism developed at Sun Microsystems for managing Java
applications. It provides just enough functionality to be more useful
than it is annoying, but about half of the users just use the single-jar
release. Autoplot is broken up into two parts, the stable and the
volatile parts. Clients then only need to download the stable part once
and then updates are provided in the small volatile updates. These are
two jar files, the stable being approximately 20 MBytes and the volatile
being about 7 MBytes. Ideally the stable jar would only be updated once
per major production branch. Note the single-jar release contains
everything.

Webstart will push new revisions out to users automatically, if one of
the jar files is updated. This mechanism proved to be extremely
unreliable when used with mediawiki on the autoplot.org server, and for
this reason we would always make new releases. User's webstart caches
would be filled with successive versions and would need periodic
purging. We believe this problem is fixed, and starting with the 2015
branch, the webstart update mechanism will be used.

## Notes on Webstart

In the JNLP file:

  - jnlp/information/title is just a label for the app. This is what is
    used in the menu.
  - devel releases will not try to associate cdf and vap files.
  - codebase for devel and latest releases are always
    <http://autoplot.org/jnlp/devel/> and
    <http://autoplot.org/jnlp/latest/>
  - shortcut and offline-allowed should be consistent, and I think the
    nightly builds will not use these.
  - jnlp/shortcut online="false" so that it doesn't check back with the
    server. Clients will come to the website for updates.

# Single-jar releases (jumbojar)

Further down in the release web page users will find a link to the
single-jar version. Some users have added a script to their systems that
use this release along with Java options for increasing the memory size.

# Procedure

## Verify Fidelty

  - <http://jfaden.net:8080/hudson/> contains hundreds of tests that
    verify most of the aspects of the software.
  - <http://apps-pw.physics.uiowa.edu/hudson/job/autoplot-findbugs/>
    will show red when more serious flaws are detected, and these should
    be addressed quickly. The yellow flags, which are generally
    harmless, should be kept between 60 and 80 flags. (Note when
    findbugs was first run on the code, there were over 600 flags.)

## Building Autoplot for one user

Often you need to commit a correction and get the release out to one
user. For example, last night one user saw a problem that no one else
was seeing, and I was able to push releases out to him with feedback
messages on the console.

Log in to
<http://apps-pw.physics.uiowa.edu/hudson/job/autoplot-release/> and put
the build button. TAG should be assigned the release tag, for example
20150121a or v2015a\_1, but for single-user releases, just leave the
default tag that identifies the build number. Note the release will have
this tag available internally, as well as the SVN version and time
stamp.

## Building for a development release

Describe the release and provide branding. Make sure new features and
bugfixes are described. Any change in the code that is not a "trivial"
change (trivial commits should be committed with the "trivial" prefix)
should be described. A new screenshot will make the release easier to
identify.

To release on Autoplot.org:

  - ssh -i \~/.ec2/ec2-keypair.pem
    ubuntu@ec2-54-235-176-122.compute-1.amazonaws.com. A key is needed
    to access this server.
  - cd /var/www/autoplot/jnlp
  - wget -O dist.zip
    <http://apps-pw.physics.uiowa.edu/hudson/job/autoplot-release/lastSuccessfulBuild/artifact/autoplot/VirboAutoplot/dist/*zip*/dist.zip>
  - unzip dist.zip
  - vi dist/autoplot.jnlp
  - mv dist TAG
  - note the target of the link devel, call this OLDTAG
  - rm devel; ln -s TAG devel
  - vi OLDTAG/autoplot.jnlp to reset to OLDTAG, and not the current.

## Making a development release into a production release

  - vi OLDTAG/autoplot.jnlp to reset to latest, and not the devel.
  - rm latest; ln -s TAG latest
