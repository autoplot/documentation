Granny text strings are used thoughout Autoplot to encode text and extentions.  It started
initially with the goal of rendering IDL's strings with control characters like '!A' for up
and '!N' to return to the baseline.  These codes were defined by Grandle and Nystrom (1980).
Extensions have been added over the years, for example allowing bits of HTML and also
special "Painters" which can insert icons or plot symbols so legends can be made.

A special editor is provided to assist in creating the strings, and this document serves
to definitively describe what can be done.

# To Be Done
LaTeX rendering is an obvious feature, and is used in both IDL and Python, and has been 
used in special cases in Autoplot.  There is a pure-Java LaTeX rendering engine, so this
is quite possible. 
