Purpose: discuss memory issues with Autoplot and develop plans for
dealing with memory problems.

# Introduction

Autoplot runs within the JVM, which immediately restricts the memory
available. This is compounded by Windows, which limits the JVM memory to
1GB. This is made worse by the maxim of first get it right, then make it
optimal. Because of this, datasets are often loaded twice, producing
copies of the same data in memory.

# Note to Autoplot Users

Supposing you've using Autoplot and constantly running out of memory,
there are several things you can do to address this. First, Autoplot can
be launched with additional memory using webstart and the server that
creates configurations for webstart. For example,
<http://autoplot.org/autoplot.jnlp?max-heap-size=4G> will launch
Autoplot allowing it to use up to 4GB of memory. Starting with
20180804a, you can also use the autoplot\_4GB.jnlp to launch any version
with 4GB. Note 32 bit machines are limited to about 1GB of memory and
this is not an option. Second, if the single-jar file is used
(autoplot.jar), it can be edited to launch with more memory by editing
the script to add -Xmx4G. Since the file is part ascii and part binary,
many editors will muck up the file, so do this with care.
(http://ridiculousfish.com/hexfiend works on a mac, vi on linux.)

# Per-datasource Caching

Some of the data sources provide thier own caching. For example, the CDF
readers cache the timetags, assuming that multiple timeseries will be
read from the same file. JythonDataSource caches all the datasets
calculated so that the script is only run once.

These have been minimally implemented intentionally, the reason being
that serious performance penalities are avoided, but ultimately a
uniform caching layer should be added to Autoplot. This is tricky and
non-trivial, and bugs will be difficult to diagnose. For example, some
of the Jython scripts know that they can mutate the data, but this would
often mutate the data that is within the cache. (QDataSet is immutable,
but often mutable ArrayDataSet implementations are used.)

## CDF Files

It looks like the CDF-Java reader (vap+cdfj) caches timetags (variables
with CDF\_EPOCH, CDF\_EPOCH16 or CDF\_TT2000). The cache is flexible,
but only these are cached. Also I noticed code where it looked like
CDF\_TT2000 was not cached.

## JythonDataSource

The script is run, and the jython session object is cached so we can
query for other variables.

# Proposed Caching

In the code that resolves the URI into a QDataSet, we would first check
a cache to see if the data is available, and use the cached version if
available. Using this would tweak the freshness, and when new datasets
are cached, the least fresh would be removed from the cache to make room
for the new. Where things get complicated are:

  - data source caching. Some data sources provide their own caching,
    and we would have to account for this as well.
  - time series browse. Parts of the dataset may be cached, and it's
    essential that the caching would support this.
  - mutable data sets. Some implementations are mutable, and we would
    need to make sure legacy codes that cheat don't cause problems.

Caching to persistent storage. Some datasources only work on-line, such
as the das2server and TSDS data sources, and it's worth considering if
these should be cached as well to local storage as qstream files.

Another thing to consider with caching is using a WeakHashMap to keep
references to data that is otherwise being used. A WeakHashMap will
allow the datasets to a be garbage collected if no one is using them,
but would keep all the references to datasets in one place. This would
be quite easy to implement, because no management is needed to remove
stale items from the cache, and would have fixed the problem where
Reiner had two datasources that used the same URI.

# Sourceforge tickets having to do with memory consumption

Rocket data runs out of memory
<http://sourceforge.net/tracker/index.php?func=detail&aid=3032234&group_id=199733&atid=970682>

ascii parser stores multiple copies of the same thing
<http://sourceforge.net/tracker/index.php?func=detail&aid=2988422&group_id=199733&atid=970682>

LogConsole/logger.log prevents datasets from GarbageCollectd
<http://sourceforge.net/tracker/index.php?func=detail&aid=3479791&group_id=199733&atid=970682>

use CDF subsampling when necessary
<http://sourceforge.net/tracker/index.php?func=detail&aid=2987345&group_id=199733&atid=970682>

Finally, this 2009 ticket suggests it's time to start memory caching:
<http://sourceforge.net/tracker/index.php?func=detail&aid=2848360&group_id=199733&atid=970685>
Time to get going on this.

