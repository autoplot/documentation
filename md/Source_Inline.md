### Inline

Data and short jython commands can be embedded in a URI for
demonstrations or quick-and-dirty annotations. An editor is
automatically generated for scripts. Any parameter read from the
getParam function will be provided in the GUI.

  - extension (prefix): vap+inline:
  - Example URIs:
      - vap+inline:1,2;3,4;5,6;7,2;9,0 \# five 2-D points
      - vap+inline:1,3;2,4 \# the points \[1,3\] and \[2,4\]
      - vap+inline:ripples(100,100) \# demo function from jython support
      - vap+inline:linspace(0,1,100),linspace(0,1,100),ripples(100,100)
        \# jython expressions allowed
      - vap+inline:ripples(100,100)+randn(100,100)/10 \# jython
        expressions allowed
      - vap+inline:ripples(100,100)+randn(100,100)/10\&RENDER\_TYPE=nnSpectrogram
        \# specify QDataSet properties
      - vap+inline:getDataSet('<https://autoplot.org/data/autoplot.ncml>')\&RENDER\_TYPE=nnSpectrogram
        \# "decorate" other datasets (TODO: bugs when ? in URI)

Note the data mash-up just creates an inline URI.