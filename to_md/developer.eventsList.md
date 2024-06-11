Purpose: describe events list format.

Audience: interested scientists

# Introduction

Events lists are useful but under-supported abstraction. Users can
create an ascii file and then use it as an events list, but they need to
use the eventsListColumn keyword to cause it to be parsed as such. This
document proposes that they become more accessible by getting rid of the
need for the keyword, and allowing a special scheme to be recognized
automatically.

## What is an events list?

An events list is a list of time intervals, which is often associated
with a label and color for plotting. The events bar is used to render an
events list onto the canvas, and a mouse click on an event will cause
the message to be displayed in a tooltip.

# Formats that will be interpreted as an events list

## ASCII file

An ASCII file with the first two columns as ISO8601 times and no more
than four columns, will be treated as an events list. For example an
ASCII file containing multiples of any of the following records would be
treated as an events list:

`2015-07-11T00:00 2015-08-11T00:00`  
`2012-09-05T18:00:25.676Z 2012-09-06T02:59:24.361Z       18`  
`2015-07-11T08:00, 2015-07-11T12:00, 0x00FF00, "Garage Sale"`

When four columns are found, and the third column could be interpreted
as an RGB color, it is interpreted as such.

## CDF file

When ordinal data has DEPEND\_0 with DELTA\_PLUS and DELTA\_MINUS, then
this is interpreted as an events list. (TODO: find example that
demonstrates.)

# Pitfalls

I've hesitated in making this choice because I'm pretty sure I've seen
ASCII files with two times that are not a range. For example, you have a
file with spacecraft time and then ground receive time, and then a bunch
of associated data. I'm pretty sure this file had more than four
columns, so Autoplot would not assume the interpretation, and for that
matter additional keywords would allow the old interpretation to work.

## TODO

Consider PNGWalk Tool's annotation facility and events lists. Perhaps if
the label is a URL, starting with <http://>, then we can look up the
http.
