# ASCII Files
First, it tries to figure out what the field delimiter is.  If it sees a bunch of commas 
on each line, it will use commas.  It looks for tabs, and it looks for white 
space.  Once it's decided what the field-delimiter is, it will try to figure out which 
lines contain data.  It does this by scanning through the file and looking for lots of 
lines with the same number of fields.  Then, "field<x>" will be the field to load 
in, and if field0 looks like time it'll use them.  That's the simple part, and 
the "automatic" part.  It does this quite reliably, in fact there are hundreds of 
files which have parsed the same way through years of tweaks.  
  
You can also tell it what to use for the delimeter, and how to parse each record.  For 
example you can give it a regular expression and parse the captured fields.  You can 
have a parser that always grabs characters 3 and 4 and parses them as an int.  There's 
also nominal data, where it'll load in strings or events lists. 

## Reading in the One Column
First, one can read in one column of an ASCII file using "column=field<n>".  When 
column names are found as the first row of the file the column name may be used 
as well.  For example for the file twocolumn.dat,
  
~~~~~
time,temperature
2020-02-02T00:00,78.3
2020-02-02T00:01,78.4
2020-02-02T00:02,78.2
~~~~~
  
one can read the temperature column using
~~~~~
https://github.com/autoplot/documentation/blob/master/docs/datasources/examples/twocolumn.dat?column=temperature
~~~~~
Note that if the first column (field0) is an ISO8601 time, then it is automatically read in as a timetag for each measurement.
  
## Reading in the Entire File as a Bundle
The entire file can be read in as a "bundle", which is a two-element array of data, 
ds[ntime,ncol], with the first index for the record and the second for the
column.
  
NOTE THERE'S A BUG WHERE THE UNITS ARE NOT READ IN PROPERLY!
  
## Parsing with Regular Expressions
A regular expression is a well-known and standard tool in text parsing, and can be 
used in Autoplot to parse unusual text files.  Regular expressions, or regex strings,
allow for "capturing groups" which become the fields of each record.  For example,
suppose you have a file regex1.dat like:
  
~~~~~
# fake data
site=3 temp=3.4
site=4 temp=5.6
site=5 temp=7.3
~~~~~
  
You could then use the regular expression "site=(.+).temp=(.+)" and then use

~~~~~
https://github.com/autoplot/documentation/blob/master/docs/datasources/examples/regex1.dat?pattern=site=(.+).temp=(.+)&field1
~~~~~
  
Each record (line) which matches the regular expression pattern will have its capturing groups set to field0, field1, etc.
  
These can also be named capturing groups. In this case, the following URI might be used:
~~~~~
https://github.com/autoplot/documentation/blob/master/docs/datasources/examples/regex1.dat?pattern=site=(?<site>.+).temp=(?<temp>.+)&site
~~~~~
  

