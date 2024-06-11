Audience: Scientists using Jython scripting

Purpose: Describe usage of the Jython annotation command.

See also: <http://autoplot.org//Annotations>

# Introduction

The annotation command creates annotations on the canvas from programs.

# Basic Usage

`annotation( text='Plot 1', fontSize=1.4 )  `

will put an annotation on canvas, replacing it if one already exists.

`annotation( index, text='Plot 2', fontSize=1.4 )  `

where index is the annotation number.

## namedParams

All of these are optional:

  - **text** The message, allowing Granny codes
  - **textColor** text color
  - **background** background color
  - **foreground** foreground color
  - **fontSize** size relative to parent (1.2em) or in pts (8pt)\\n
  - **borderType** draw a border around the annotation text
    none,rectangle,roundedRectangle.
  - **anchorBorderType** draw a border around the anchor box.
  - **anchorPosition** One of NE,NW,SE,SW, N,E,W,S, outsideN,outsideNNW
  - **anchorType** PLOT means relative to the plot. DATA means relative
    to xrange and yrange
  - **rowId** row to anchor, or empty for the entire page
  - **columnId** column to anchor, or empty for the entire page
  - **xrange**, **yrange** anchor box when data coordinates
  - **pointAt** comma separated X and Y to point the annotation arrow
    at.
  - **pointAtOffset** length like "1em" to back off the pointer so that
    the subject can be seen.

NOTE: arguments should be flexible, so findgen(5) can be used as well as
\[0,1,2,3,4\], and timegen('2018-001T00:00Z','24hr',3) instead of
\['2018-001T00:00Z','2018-002T00:00Z','2018-003T00:00Z'\], and Color.RED
as well as 'Red' and 0xFF0000.

### colors

Color can be a Java color object (Color.GREEN), or a string which can be
converted into a color. Examples include:

**`'DarkRed`**`' X11 color names are resolved.  See `<https://en.wikipedia.org/wiki/X11_color_names>`, and note spaces should be removed from names.`  
**`'0x00FF00`**`' RGB colors specified in hex.`  
**`'0xA000FF00`**`' ARGB, where A is the "alpha" or transarency channel, and 0 is completely invisible and 255 (FF) is completely opaque.`  
**`Color.RED`**` Java color object.`

# Advanced Usage

`annotation = annotation( index=1 )`  
`annotation.text= 'New Title'`

The "1" indicates that the annotation at index 1 should be used for
this. This similar to the plot command which also has an index. This is
so that annotations and plots are replaced instead of added again and
again as the script is rerun.
