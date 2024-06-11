Show in human-ready form the logic of AutoplotUtil.guessRenderType. See
also <http://autoplot.org/developer.renderTypes>

# RENDER\_TYPE is specified in dataset

time\_series → hugeScatter when length\>80000

time\_series → series otherwise

spectrogram → user preference for nnSpectrogram or spectrogram

XXX\>YYY → RenderType.valueOf(XXX);

# Guess it from dataset geometry

JOIN\_0 \!=null && length()==0 → Series

SemanticOps.isRank2Waveform(fillds) → hugeScatter

ds.rank()==2 && isBundle && bds.length()==3 && bundle.property(
DEPEND\_0, 2 )\!=null → colorScatter

ds.rank()==2 && isBundle && bds.length()==3 && bundle.property(
DEPENDNAME\_0, 2 )\!=null → colorScatter

ds.rank()==2 && isBundle && bds.length()==3 &&
ds.property(QDataSet.DEPEND\_0)==null &&
bundle.property(QDataSet.CONTEXT\_0,2)\!=null → colorScatter

ds.rank()\>=2 && isBundle && bds.length(0)==3 && lastIsOrdinalUnit →
eventsBar

ds.rank()\>=2 && isBundle && bds.length(0)==4 && lastIsOrdinalUnit →
eventsBar

unitIsOrdinal && noDep0 → digital

unitIsOrdinal && dep0 → eventsBar

# Notes

There is no scheme that resolves to: stairSteps, fillToZero, image,
pitchAngleDistribution, vectorPlot, orbitPlot or contour.

# Explicitly Setting the Render Type within the Data Set

Datasets can suggest a method for rendering, and Autoplot will always
use this now.

`ds.putProperty( RENDER_TYPE, 'fillToZero' )`

## Proposed extensions

I've been trying to figure out how the dataset can have more control
over how it is rendered. For example, AE should always be 4=yellow,
\<4=green, \>4=red. The jython script that loads this could put in hints
to get this close.
<http://www-pw.physics.uiowa.edu/~jbf/autoplot/users/kris/kp.jyds>

`ds.putProperty( RENDER_TYPE, 'fillToZero>color=yellow&fillColor=yellow' )`

The "fillToZero" refers to a type, and after the greater than sign are
further qualifications.

For example, the image reader can request the greyscale channel, but the
colorbar used to render this is default RGB.

`ds.putProperty( RENDER_TYPE, 'spectrogram>table=greyscale' )`

Reserved words should come from the plotx function, but I'll enumerate
them here:

  - spectrogram
  - interpolate=none,nn,bilinear
  - table=greyscale,blackred,blackgreen,blackblue,
  - color=0xRRGGBB,red,blue,etc.
  - fillColor=0xRRGGBB,red,blue,etc. darker brighter
  - reference=0.0 datum for reference, with fillColor
  - thick=1 in pts/pixels
  - symbolSize=3 in pts/pixels
  - style=dashFine,dotFine,solid. TODO what does the "fine" refer to?
  - symbol=circles,triangles,cross,ex,star,diamond,box,none
  - fillStyle=fill,outline

`ds.putProperty( RENDER_TYPE, 'stairSteps?color=yellow' )`  
`ds.putProperty( RENDER_TYPE, 'series?color=blue&interpolate=nn' )`

Also see the property plotElement.renderControl, which should use these
as well.
