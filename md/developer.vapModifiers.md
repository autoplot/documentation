Description: Autoplot vap references can have modifiers that apply
tweaks to the vap files, and we are considering allowing xslt transforms
to provide greater support for this.

Audience: autoplot power users

# Introduction

Autoplot has always allowed modifiers to vap files, the primary use case
being the one where an existing product is used to look at different
timeranges. Suppose the file

&lt;http://autoplot.org/data/autoplot-applet.vap&gt;`&nbsp;`

looks at timeranges from 2003-05-01 through 2003-05-31, then

<http://autoplot.org/data/autoplot-applet.vap?timerange=2003-05-10>

would use the same vap, except just the day 2003-05-10 is shown.

What Autoplot does is to load the dom from the vap file, then any
transformations following the question mark (?) are applied to the dom.

# Allowing for XSLT transforms

Allowing for XSLT transforms would provide a useful way to create VAPs.
For example, an empty template vap could be populated with URIs and
labels. XML files that are configurations for other systems could be
transformed into a vap file.

# Syntax

Vap file modifier:

<vapFile>`?xslt=`<xsltFile>`&`<xsltFileArgs>  

and <xsltFileArgs> is a list of ampersand-delimited arguments, for
example:

```
color=yellow&background=black
```
Note in this case, the vapFile should be a valid vapFile. (Anything with
a .vap extension ought to be a vap.)

Autoplot should be able to work without a vap file, where just the xslt
is used to create the DOM.

<xsltFile>`?`<xsltFileArgs>

In this case, Autoplot will trigger off the .xslt extension to invoke
its handling code. I would also suggest a couple of special named
parameters, as with Autoplot URIs:

```
resourceURL is the name of a file to be transformed that is not a .vap file.
arg_i be the ith unnamed argument.
```
# Examples

<http://autoplot.org/data/autoplot.vap?xslt=http://autoplot.org/data/text.xslt&title='My+data>`"`

