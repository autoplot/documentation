Purpose: Describe RTE reporting.

# Introduction

RTE (Runtime Exception) reporting has proved a very effective way to
maintain Autoplot. When users hit a runtime exception, they can submit a
report that provides Autoplot developers with information about the
error.

# How is the report generated

The RTE report is an XML document that is uploaded to a server, which is
presently <http://papco.org/RTEReceiver/LargeUpload.jsp>. Some servers
don't allow posts, so the user may save the report to a file that is
sent via email.

# What is recorded

  - applicationId= autoplot
  - user comments, which are free text entered by the user to describe
    the bug.
  - userName, guessed from java properties
  - email, if the user provides
  - the current URI autoplot has in the focus bar
  - buildinfos, which are tags that can be used to recover the source.
    (Not tested.)
  - platform info, including: java.version, java,vendor, os.name,
    os.arch, os.version, runtime.freeMemory, etc.
  - exception that raised the dialog, including the stack trace
  - .vap file of the current state
  - states, which are undo information showing how they got there
  - screenshot, optional.

# How to use this report

## get the screenshot

The screenshot is encoded with uuencode, and the command uudeview is
useful:

```
unix> uudeview rte_0751346092_20120808_212159_usern.xml
Loaded from rte_0751346092_20120808_212159_usern.xml: '' (UNKNOWN.001):  part -1   Base64                                                                      
Found 'UNKNOWN.001' State 16 Base64 Parts 1 OK
unix> mv UNKNOWN.001 UNKNOWN.001.png
unix> eog UNKNOWN.001.png
```

## load the vap

The vap file within the report can be loaded by renamimg the exception
report and loading it:

```
unix> cp rte_0751346092_20120808_212159_usern.xml rte_0751346092_20120808_212159_usern.xml.vap
```

and then in autoplot load this vap. This works because the vap-loading
code looks for exception report files and handles them specially. Also
you can prefix the URL with "vapfile:" to force load of a resource as a
vap file.

