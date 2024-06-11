Each interface captures the content of a particular type of science
content.

Jot list of data types of potential interest:

Note: all data interfaces are implied to be immutable (no mutator
methods on the interface; client usage can expect no changes)

linear data

  - number of values
  - values (1-D)
  - x-axis values(not necessarily a gauge\!) (time
  - possibly gauged (time, or more generally non-strictly monotonic
  - different flavors: scatter plot data, line plot data
  - uncertainties
  - units
  - name of x variable; name of y variable
  - description
  - fill value
  - max x-gap for connecting dots OR max gap function of x OR max gap as
    function of index
  - plotting metadata: plot color, symbol, line thickness, axis labels

Simplest Interface: XYData

  - size()
  - getX(i)
  - getY(i)

Then have a separate interface with:

EnhancedXYData extends XYData

  - isFill(index)
  - xunits, yunits (TBD probably some object)
  - name of x variable; name of y variable
  - labeler for axis values
  - Optional<UncertProvider> getUncertProviderX()
  - Optional<UncertProvider> getUncertProviderY()

interface UncertProvider {

` double getUncertPlus(i)`  
` double getUncertMinus(i)`

}

EnhancedXYDataWithUncert extends XYData

spectrum / 1D histogram

  - has x bins
  - has y data values for each bin
  - has uncertainties?

spectrogram / 2D histogram

  - not just with functions of time

trajectory

Plot Types in Autoplot:
