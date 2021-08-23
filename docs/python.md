# Using Autoplot in the Python Environment, using JPype.

Audience: Autoplot users who would like to use the software to read data into Python, and to use other Autoplot codes from these environments

See also: help.jython which is the Java-based version of Python which is used to script Autoplot.

# Introduction
Both IDL and MATLAB make it extremely easy to use Java code in these environments. Autoplot is able to read data from a variety of input sources using compact URIs to specify data locations, making it useful accessing digital data. For example, it's difficult to read data from an Excel worksheet into IDL, but since Autoplot can read this data, it becomes just as easy to read data from this source as it is a table of ASCII data. Further, Matlab can read data from CDF files, but its low-level CDF interface makes Autoplot attractive, because you can access data with just several lines of code. Last, Autoplot can automatically retrieve and manage data from remote sites via FTP and HTTP, so this mechanism can be used in IDL and MATLAB as well.

Autoplot contains a number of codes that are useful, in addition to reading data. For example, Autoplot is able to write data to a number of data formats, and this code is useful in Matlab as well.

JPype is a Python library that bridges Java to native Python, and it is used to provide this functionality to Python as well.

# Installing JPype and Autoplot
Install jpype which allows Python to call Java codes and migrate data in and out of the Java Virtual Machine:
 
~~~~~
pip install jpype
~~~~~

Install Autoplot software:
~~~~~
pip install autoplot
~~~~~

# Connecting to Python
Python is able to add the jar after the session is started, with the plugin jpype. You'll have to use your JRE location (Java 7 is required), and autoplot.jar can be downloaded from http://autoplot.org/latest/autoplot.jar:

~~~~~
>>> from jpype import *
>>> startJVM(getDefaultJVMPath(),'-Djava.class.path=/tmp/autoplot.jar')
>>> APDataSet= JClass("org.autoplot.idlsupport.APDataSet")
>>> apds=APDataSet()
APDataSet v1.7.0
Java Version 1.8.0_282
~~~~~

This object "apds" can be used to download data:
~~~~~
apds.setDataSetURI( 'http://autoplot.org/data/swe-np.xls?column=data&depend0=dep0' )
apds.doGetDataSet()
print( apds.toString() )
~~~~~

The package "autoplot" provides some convenience methods.  Once installed
with "pip install autoplot" try:
~~~~~
from autoplot import javaaddpath
from jpype import JClass
javaaddpath('http://autoplot.org/latest/autoplot.jar')
APDataSet= JClass("org.autoplot.idlsupport.APDataSet")
apds=APDataSet()
~~~~~
This will download the latest version of Autoplot and use it.
