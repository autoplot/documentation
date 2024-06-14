Purpose: try to enumerate and have some control over releases.

# v2017a

This is a bunch of major and long-overdue changes.

  - bundle(X,Y) supported as a primary data type. Typically Y(X) is used
    to support scatter data, even though there is no functional
    relationship between X and Y.
  - Jython 2.7 supported.
  - org.virbo.autoplot -\> org.autoplot namespace change.
  - improve Units support with SIUnits library that supports
    multiplication and division.
  - <https://sourceforge.net/p/autoplot/bugs/1783/>, where rank 0
    numbers are reported as "label=value".
  - <https://sourceforge.net/p/autoplot/bugs/1771/>, where the user has
    their preferences which reset will always return to.
  - <https://sourceforge.net/p/autoplot/bugs/1753/>, review
    datum/dataset/datumRange operations.
  - <https://sourceforge.net/p/autoplot/bugs/1704/>, consider removing
    indexed properties.
  - consider <https://sourceforge.net/p/autoplot/feature-requests/564/>.
    Maybe a "label" property next to timeRange in the dom.

