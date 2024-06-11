# Parameters

## Common

  - **uri** an Autoplot URI or a vap file.
  - **timeRange** is the time range displayed. Note that the speparator
    is used to indicate if the end date is inclusive or exclusive:
    `2001-01-01/2001-01-02` means the end date is before 2001-01-02,
    `2001-01-01 to 2001-01-02` means the end date is before 2001-01-02,
    and `2001-01-01 through 2001-01-02` means the end date is before
    2001-01-03. Most ISO8601 forms can be used, so for example
    `2001-01-01T00:00/08:00` will show the first eight hours of the day,
    as does `2001-01-01T00:00/PT8H`. In addition, to support updating or
    near-real-time displays, the special keyword "now" refers to the
    current time, so `P10D/now` refers to the ten-day interval ending at
    the current time when the timeRange was parsed. See also [Time
    Parsing and
    Formatting](help#Time_Parsing_%2f_Formatting "wikilink").
  - **dataSetURL** controls the initial URL displayed. Note
    "<about:plugins>" and "<about:autoplot>" are supported and useful
    for debugging.
  - **column** controls the horizontal layout. Syntax is `L%+S,R%+S`,
    for example `0%+5em,100%-10em` See
    [help\#layout](help#layout "wikilink"). Use will allow for a stack
    of images created with the API with the same time axis to be aligned
    properly.
  - **row** controls the vertical layout. Syntax is `T%+S,B%+S`, for
    example `0%+2em,100%-7em` See
    [help\#layout](help#layout "wikilink").
  - **autolayout** automatically adjust the row and column to avoid
    clipping labels.
  - **font** is the font to use on the system. This must identify a font
    on the client's desktop, so good choices are generic, e.g.,
    "sans-16"
  - **renderType** explicitly specifies how the data should be rendered
      - scatter draws the data as a scatter plot
      - series connects the plot symbols
      - stairstep (used to be histogram) draws a stepped line to
        indicate the sample interval
      - fillToZero (used to be fill\_to\_zero) draws a stairstep and
        fills to the reference line when renderType=fillToZero.
      - spectrogram renders the data as a spectrogram with bilinear
        interpolation. Note if the data is not suited for this, nothing
        will be done.
      - nnSpectrogram renders the data as a spectrogram with nearest
        neighbor interpolation. Note if the data is not suited for this,
        nothing will be done.
      - hugeScatter uses a faster rendering method that can handle
        millions of points. "series" and "scatter" becomes inefficient
        with more than \~40,000 points.
  - **color** specifies the plot symbol and symbol connector color in
    \#rrbbgg format. Specify multiple componet colors with a comma
    separated list.
  - **fillColor** specifies the color in \#rrbbgg format used to fill to
    the reference. Specify multiple componet colors with a comma
    separated list.
  - **foregroundColor** is the color of the axis and labels in \#rrbbgg
    format
  - **backgroundColor** is the color of the drawing canvas background.
    (Use \#rrbbgg or none for transparent)
  - **plot.title** the title for the single panel plot.
  - **plot.{x,y,z}axis.label** the label for the x, y, or z (colorbar)
    axis.
  - **plot.{x,y,z}axis.range** the range for the x, y, or z (colorbar)
    axis. e.g. "2000-02-01 to 2000-02-15" or "200 to 800". With the
    servlet, `+` should be used in URLs instead of spaces.
  - **plot.{x,y,z}axis.log** scale type for x axis. "true" indicates use
    a log axis
  - **plot.{x,y,z}axis.drawTickLabels** "true" indicates draw labels.
    This is the default.

## Applet-only

The applet mode is not supported.

{{\#lsth:applet\_guide|Parameters}}

## Servlet-only

{{\#lsth:servlet\_guide|Parameters}}

## AutoplotServer command line

There's support for a command line server, intended to support CGI-BIN
services and other applications. It has a subset of the common
interface:

`UNIX> wget -N `<http://autoplot.org/latest/autoplot.jar>  
`UNIX> java -cp ~/autoplot.jar org.autoplot.AutoplotServer --help`  
`org.autoplot.AutoplotServer 20180726`  
`Usage: AutoplotServer `  
`  -u, --uri=   URI to plot, or if .vap then rescale to width and height `  
`  -v, --vap=   VAP to plot without scaling. `  
`  -w, --width=     width of result (default=700) `  
`  -h, --height=    height of result (default=400) `  
`  -a, --canvas.aspect=     aspect ratio `  
`  -f, --format=    output format png or pdf (default=png) `  
`  -o, --outfile=   output filename or - `  
`  -r, --timeRange=     set this to the timerange, instead of the range within the vap `  
`  --enableResponseMonitor      monitor the event thread for long unresponsive pauses`  
`  -z, --noexit     don't exit after running, for use with scripts.`  
`  -q, --nomessages     don't show message bubbles.`  
`  --autorange      autorange the Y and Z axes of each plot in the vap`  
`  --autorangeFlags     autorange the Y and Z axes of each plot where the autorange flag is set in the vap`  
`  --rescaleFonts   when the .vap is rescaled, also scale the fonts`  
`UNIX> java -cp ~/autoplot.jar org.autoplot.AutoplotServer -u '`<http://autoplot.org/data/autoplot.cdf?BGSEc>`' -o image.png`

# Methods

## Applet

{{\#lsth:applet\_guide|Methods}}

## WebStart

The webstart server serves JNLP files which configure Autoplot to run in
a number of different ways. {{\#lsth:webstart\_guide|Basic}}
