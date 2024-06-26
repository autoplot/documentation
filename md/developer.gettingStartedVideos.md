Purpose: describe a series of videos to highlight and demonstrate
Autoplot features.

(demo 5 means "Bookmarks-\>Demos-\>Demo 5")

Each section would correspond to a video, and the target length for each
video would be about 20 seconds. No audio, text bubbles indicate what's
about to happen. Text bubbles can pause the video, so we should decide
whether we should use this or just have a delay...

# Launching Autoplot with Webstart

# Navigation

  - box zoom
  - zoom on X and Y, Z axis
  - pan on X
  - mouse wheel on X
  - comment about how this works on all axes.
  - control-Z (command-Z) is undo, control-Y is redo.

# Loading data from a CDF File

  - File-\>Open File...
  - Select parameter to plot
  - Use address bar to browse remote listing. (See demo 3 for address)
  - Select remote file, which is automatically downloaded to
    $HOME/autoplot\_data/.

# Loading data from an ASCII File

  - Enter in name of OMNI file (See demo 7?)
    (vap:<ftp://nssdcftp.gsfc.nasa.gov/spacecraft_data/omni/omni2_1971.dat>)
  - Ascii Editor panel pops up, select column 17, which is DST (verify
    this, documentation is in sibling file).
  - plot comes up of parameter, fill values plotted and no timetags
  - back into editor panel
      - Guess button next to data-\>fill value
      - go to times tab, select field0-field2.
      - replace numbers in time format field with "$Y+$j+$H" using
        convenient "select field type..."
      - exit to plot again
  - plot has time tags and data gaps now
  - replace omni\_1971.dat with omni\_1972.dat to show that this
    configuration works for other omni files (and this is why URIs are
    effective)

# Aggregation

  - "file aggregation is combining the data from a series of files into
    one data set."
  - start with the URI from last video.
  - change "1972.dat" to "$Y.dat" and hit enter.
  - This goes back into editor panel, but now there is "Aggregation Time
    Range"
  - Enter "1970 to 1975"
  - Hit scan next to see that more data is loaded if it matches the
    aggregation spec

# Advanced Navigation

  - holding control while mouse wheel pans axis.
  - axis tab, enter 1982 to go to that year. "1982 Jan" will go to that
    month
  - \[right-click on plot\]-\>Add Plot-\>Context Overview
  - drag on curtain opening to pan around.

# Setting Titles and Legend Labels

# Multiple Panels

  - find a stereo wav file, (short with good separation between the
    channels. I can provide...)
  - plot the wave file. channel=0 is the default.
  - File-\>Add Panel...
      - add "?channel=1" to the URI.
      - Plot Below.
  - xaxis will be bound if the range is similar. (This is poor logic and
    will probably change.)
  - if the xaxes are not bound, then right click on the new plot xaxis,
    then "bind to plot above"
  - yaxis, "bind to plot above"
  - show how they move together

# Advanced Multiple Panels

  - The address bar has a shortcuts for add panel.
      - control + play button adds a new plot.
      - shift + play button adds an overplot, which is a new panel on
        the same plot.
  - plotting vector quantities like B-GSM automatically adds more panels
    for each component.
  - plot demo 5.
  - right-click on z\_component, move to plot below
  - reset application deletes all the extra plots and data panels to
    return to the initial state.

# Bindings

  - Bindings connect properties together, like a short-circuit.
  - application has a special property timeRange for binding all the x
    axis ranges together.
  - Nice use case where I needed a better tool for looking over hudson
    tests, so I could bind PNGWalkTools together to look at the current
    state against the standard.

# Application Focus

  - the application has a focus, which set by clicking on a data plot.
    Yellow flash indicates focus change.
  - plot demo 5
  - click on traces to change focus
  - the layout tab shows the focus panel (and the plot it is within.)
      - undock/slide it to show it side-by-side
      - click on traces to change focus
  - note the invisible parent panel that ties the three component panels
    together.
      - The parent deletes its children if they are no longer needed
      - changing properties of the parent will push the changes to the
        children.
  - ("panel" seems to be a confusing name. Canvas contains Plots, Plots
    contain panels.) (Name-that-abstraction contest? e.g. PlotElement,
    pel, or element )
  - style, metadata, axes tabs follow focus
      - select Z component and make it thicker.
  - clicking play resets the URI of the current focus data source.
  - operations are often with respect to focus. e.g. Add Panel... Plot
    Below means below the focus panel.

# Application DOM

  - the DOM is the entire application state.
  - Edit-\>Edit DOM allows browsing the DOM and setting properties.
  - inspect bindings
  - edit all panel.style properties to set them at once.
      - Select each node, then right-click "Edit Selected".
      - setting value in the first column sets all of the values at
        once.
      - then individual properties can be changed.
  - plot demo 5
      - Select 3 child nodes, "Edit Selected"
      - set line width to 0.5
      - set Bz to 2.0 and black.

# Tearoff Tabbed Pane

  - autoplot tabs can be removed for side-by-side views.
  - often you want to look at the plot while adjusting parameters or
    looking at metadata.
  - right click on the tab, "undock"
  - or just tear it off by dragging it to the desired location.
  - dock it again with right-click, "dock"
  - "slide right" constrains the new window to be next to the original,
    reducing window clutter.

# Bookmarks and Recent URIs

# Make PNG Walk

  - load demo 3
  - Make PNG walk for "2000 Jan", go get a coffee
  - show how PNG walk allows control of Autoplot with "launch autoplot"
    button.
  - show structure of result directory, that it contains images,
    thumbnails, and vap file.

# Cache Management

  - Tools-\>Cache-\>Edit Cache
  - right-click on filename to plot it
  - select multiple nodes to delete them

# Scripting

Jasper was asking about how to combine variables almost immediately when
I was introducing him to Autoplot, and I realized my usual talk doesn't
talk about scripting at all.

# What's a URI and why they exist

URIs are central to Autoplot, and probably worth talking about. The
video could talk about the evolution from PaPCo's data representation
(first 4 integers, then 16 strings were added, then arbitrary data) to a
string "URI" to represent state. Overhead of parsing and formatting
means standard codes must be provided, but this was done years ago. URIs
are compact and easily transmitted and stored. They are extensible (e.g.
skipLines added to an ascii reader).

# more complex script where functionality is added to the pngwalk tool

Ivar talked about how useful the pngwalk is for creating workflows. This
video would show how to create a pngwalk with a tool to create a
workflow.

