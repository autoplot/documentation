Purpose: Outline progress and issues with introducing new filters
dialog.

Audience: Developers and interested scientists.

# The Issue

The filters are an attempt at generalizing the slicing of the first go
at Autoplot into a more general set of filters. Back in 2007, high-rank
data (ds\[time,energy,pitch\]) would be sliced automatically and the
title would indicate that slice was done. Later versions of Autoplot
would allow arbitrary filters, identified as a "process string" stored
in the property plotElement.component. "|slice1(3)" would be an example
of how the slicing was re-implemented, and users could now also run
complex filters like "|fftPower(512)".

The GUI has not been generalized, however, and users get a GUI to
support the legacy ability to slice on any dimension, but other filters
do not have GUI elements.

Scientists could also chain filters together. For example,
"|slice1(3)|multiply(-1)" will pull out the smaller dataset and then
display the result times -1.

## Words for things

Making things more confusing is the lack of thought to what these are
called. The words "filter" "process" and "operation" have all been used
to describe the same thing.

# The Solution

We are working to add GUIs for each of the filters, and to make
discovery of filters more intuitive.

There will be a set of small GUIs to control each step of the filter
chain. For the example "|slice1(3)|multiply(-1)" there would be a small
GUI to select the slice index and dimension, and then a small one to
contain the number by which the data is multiplied. The multiply GUI
could have useful values, such as "-1,2,180/PI" etc.

Each GUI implements a small interface, similar to the PanelEditors. This
includes the methods:

`void setFilter( String filter )`  
`String getFilter()`

Also to preserve the existing functionality of the slice GUI, we would
need:

`void addPropertyChangeListener()   to register a listener to the GUI, that will be called when a change is indicated to the rest of the system`  
`void setInput( QDataSet ds )  to allow the droplist to display named dimensions.`

## Words for things

"Filter" refers to an operation that takes one dataset argument and some
number of scalar or string arguments. These are often expressed in the
form "|filter()", indicating that the first argument is a dataset.
"Filters" are a chain of Filters.

"Mash Up" refers to a process that takes one or more datasets and
combines them into one dataset. This process can be visualized as a tree
of unary, binary, and N-argument operations, such as divide which is a
binary operator.

# Notes

  - This was implemented in Fall 2014.
  - See .../QDataSet/src/org/virbo/filters (package name change coming)
