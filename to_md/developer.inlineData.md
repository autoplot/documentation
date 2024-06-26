Purpose: explore URI syntax for containing data, inparticular to support
plotting in javascript with an applet. For example, a yagi calculator
calculates element dimensions, then autoplot in an applet is used to
display the antenna layout. Also, SeriesRenderer is given a rank 0
number so that a reference line is drawn.

This also forces a clean-up of the datasources API, which still uses
URLs, excluding databases and this simple use case.

Limitations. It looks like many servers have a limit of 256 characters.
I couldn't find any limitations in the URI spec. For large datasets,
another mechanism should be used.

`vap+inline:3,4;3,6;5,6`  
`vap+inline:2000-001T00:00,23.5;2000-002T00:00,23.5;2000-003T00:00,23.5`  
`vap+inline:1,2,3&DEPEND_0=1,2,3&UNITS=hours since 2000-001T00:00`

# Use Cases

  - In jython, construct dataset ytags with inline dataset.

` ytags= getDataSet( 'vap+inline:exp(findgen(20))&UNITS=eV&SCALE_TYPE=log&LABEL=Energy' )`

  - Decorate existing datasets. This removes the xtags from the dataset
    (not released):

` vap+inline:getDataSet('`<http://autoplot.org/data/autoplot.cdf?BGSM>`')&DEPEND_0=None`

# Examples

vap+inline:2000-001T00:00,23.5;2000-002T00:00,23.5;2000-003T00:00,23.5

vap+inline:2000-001T00:00,2000-002T00:00,2000-003T00:00;23.5,23.5,23.5

vap+inline:1,2,3\&DEPEND\_0=1,2,3\&DEPEND\_0.UNITS=hours since
2000-001T00:00

vap+inline:exp(findgen(20))\&UNITS=eV\&SCALE\_TYPE=log\&LABEL=Energy

vap+inline:ripples(1440)\&DEPEND\_0=timegen('2003-05-01','1 min',1440)

vap+inline:t=linspace(0,2\*PI,200)\&cos(2\*t),sin(3\*t),t

vap+inline:ripples(10,10)\&RENDER\_TYPE=digital
