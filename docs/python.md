# Using Autoplot in the Python Environment, using JPype.

Audience: Autoplot users who would like to use the software to read data into Python, and to use other Autoplot codes from these environments

See also: help.jython which is the Java-based version of Python which is used to script Autoplot.

# Introduction
Both IDL and MATLAB make it extremely easy to use Java code in these environments. Autoplot is able to read data from a variety of input sources using compact URIs to specify data locations, making it useful accessing digital data. For example, it's difficult to read data from an Excel worksheet into IDL, but since Autoplot can read this data, it becomes just as easy to read data from this source as it is a table of ASCII data. Further, Matlab can read data from CDF files, but its low-level CDF interface makes Autoplot attractive, because you can access data with just several lines of code. Last, Autoplot can automatically retrieve and manage data from remote sites via FTP and HTTP, so this mechanism can be used in IDL and MATLAB as well.

Autoplot contains a number of codes that are useful, in addition to reading data. For example, Autoplot is able to write data to a number of data formats, and this code is useful in Matlab as well.

JPype is a Python library that bridges Java to native Python, and it is used to provide this functionality to Python as well.
