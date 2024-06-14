Purpose: introduce jyds extensions

Audience: jyds script writers using jyds scripts to implement data
sources.

# Introduction

Sometimes a jyds script is all that's needed to provide a satisfactory
data source, and a scientist wants to make it available to everyone
using Autoplot. Autoplot 2018 now allows "jyds extensions" to quickly
implement a new data source, associating a file extension, such as
".sps", with a .jyds reader. This was introduced to read .sps and spd
files used with RadioJove, where the scientist is maintaining the script
which reads the files.

# Releasing the script

  - copy must be in svn or github which is modifiable by the Autoplot
    team.
  - Autoplot team will have to approve the extension which will trigger
    (e.g. wdc is world data center files).
  - Autoplot team will have to modify code to use this site.

# Debugging

If the environment variable "jydsExtension\_<EXT>" is set, then this
alternate version of the script will be used. Logger apdss.jyds will
report what script is actually used.

```
System.setProperty("jydsExtension_sps","")
```
  
```
System.setProperty("jydsExtension_sps","`<file:/home/jbf/project/earth/svn/public/jyds/readTypeSps.jyds>`")
```

# Examples

The extension .sps is associated with the jyds script
<https://saturn.physics.uiowa.edu/svn/earth/public/jyds/readTypeSps.jyds>.
(Increase the logging for apdss.jyds to see the source.) This is done by
adding ".sps" to the META-INF file
org.autoplot.datasource.DataSourceFactory.extensions, and modifying
JythonExtensionDataSourceFactory.java to delegate to the script. TODO:
This should be modified so that no Java code is needed to configure.

