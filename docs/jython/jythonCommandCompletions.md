When completions are triggered on the plot command, a static 
page is shown.  It would be nice to allow for completions on keywords 
with documentation explain use.

Now if the Jython command has the tags `__completions__`, it will be a string which
is parsed as JSON.  This JSON explains each keyword.

For example, plot now uses the following:

~~~~~
{ 
    "position": [
        {
            "name": "pos",
            "description": "if not data, then the plot position"
        },
        {
            "name": "x",
            "description": "the x coordinate"
        },
        {
            "name": "y",
            "description": "the y coordinate"
        },
        {
            "name": "z",
            "description": "the z coordinate"
        }
    ],
    "keywords": [
        {
            "name": "xtitle",
            "description": "set the label for the x-axis"
        },
        {
            "name": "ytitle",
            "description": "set the label for the y-axis"
        },
        {
            "name": "ztitle",
            "description": "set the label for the colorbar"
        },
        {
            "name": "index",
            "description": "plot index"
        },
        {
            "name": "title",
            "description": "title for the plot"
        },
        {
            "name": "renderType",
            "description": "explcitly set the render type, to scatter, series, nnSpectrogram, digital, etc"
        },
        {
            "name": "color",
            "description": "the line colors."
        },
        {
            "name": "fillColor",
            "description": "the color when filling volumes."
        },
        {
            "name": "colorTable",
            "description": "the color table to use, like white_blue_black or black_red."
        },
        {
            "name": "symbolSize",
            "description": "set the point (pixel) size"
        },
        {
            "name": "symbolFill",
            "description": "none, outline, or solid (solid is default)"
        },
        {
            "name": "lineWidth",
            "description": "deprecated--the line thickness in points (pixels)"
        },
        {
            "name": "lineThick",
            "description": "the line thickness in points (pixels)"
        },
        {
            "name": "lineStyle",
            "description": "the line style, one of solid,none,dotfine,dashfine</td></tr>"
        },
        {
            "name": "symbol",
            "description": "the symbol, e.g. dots triangles cross"
        },
        {
            "name": "isotropic",
            "description": "constrain the ratio between the x and y axes."
        },
        {
            "name": "legendLabel",
            "description": "add label to the legend</td></tr>"
        },
        {
            "name": "title",
            "description": "title for the plot"
        },
        {
            "name": "xpos",
            "description": "override horizontal position of plot, eg. '50%+1em,100%-2em'"
        },
        {
            "name": "ypos",
            "description": "override vertical position of plot, eg. '0%+1em,25%-2em', 0 is top"
        },
        {
            "name": "xdrawTickLabels",
            "description": "False turns off the x tick labels for the plot"
        },
        {
            "name": "ydrawTickLabels",
            "description": "False turns off the y tick labels for the plot"
        },
        {
            "name": "xtickValues",
            "description": "explicitly control the tick locations."
        },
        {
            "name": "ytickValues",
            "description": "explicitly control the tick locations."
        },
        {
            "name": "xautoRangeHints",
            "description": "hints to the autorange, see http://autoplot.org/AxisAutoRangeHints"
        },
        {
            "name": "yautoRangeHints",
            "description": "hints to the autorange, see http://autoplot.org/AxisAutoRangeHints"
        },
        {
            "name": "zautoRangeHints",
            "description": "hints to the autorange, see http://autoplot.org/AxisAutoRangeHints"
        },
        {
            "name": "renderer",
            "description": "add custom renderer, a class extending org.das2.graph.Renderer, see http://autoplot.org/CustomRenderers"
        },
        {
            "name": "rightAxisOf",
            "description": "specify a plot where a new plot with a new yaxis."
        },
        {
            "name": "topAxisOf",
            "description": "specify a plot where a new plot with a new xaxis above."
        },
        {
            "name": "overplotOf",
            "description": "a plot or plot element with which this should share axes.  Note something should reset the plot!"
        }
    ]
}

~~~~~

This will be supported starting at v2022a_4.
