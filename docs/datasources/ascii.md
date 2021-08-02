# ASCII Files

First, it tries to figure out what the field delimiter is.  If it sees a bunch of commas 
on each line, it will use commas.  It looks for tabs, and it looks for white space.  
Once it's decided what the field-delimiter is, it will try to figure out which lines 
contain data.  It does this by scanning through the file and looking for lots of 
lines with the same number of fields.  Then, "field<x>" will be the field to load 
in, and if field0 looks like time it'll use them.  That's the simple part, and 
the "automatic" part.  It does this quite reliably, in fact there are hundreds of 
files which have parsed the same way through years of tweaks.  
  
You can also tell it what to use for the delimeter, and how to parse each record.  For 
example you can give it a regular expression and parse the captured fields.  You can 
have a parser that always grabs characters 3 and 4 and parses them as an int.  There's 
also nominal data, where it'll load in strings or events lists. 
