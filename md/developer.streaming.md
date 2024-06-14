Purpose: Define and discuss data streaming in Autoplot.

Audience: Developers and interested scientists.

# Introduction

Data streaming the term used to describe when the dataset is made
available immediately as it is processed, instead of requiring that the
entire dataset is processed before it can be accessed. For example,
consider two processes, |smooth(5) and |fft(). Once the first five
measurements are received by the smooth function, the first results can
be made available for the next processing steps. |fft(), on the other
hand, must be completely processed before any measurements are
available.

This applies to data sources as well. When reading a CSV file, once the
first record is read, it can be made available to other parts of the
system. Just as important is that the reader itself no longer needs to
store the data, which often makes it much more capable as well. Take as
a second example the aggregating data source. Once a granule is read in,
the reader could make the data available to a reader, freeing up its
storage. Now anything it aggregates, even if each source granule cannot
be cannot be streamed, can be streamed.

To state this explicitly: the term "streaming" means that data is
available as it is processed, not necessarily that each record is
immediately available.

The Radio and Plasma Wave Group's Das2Server is based on streaming,
where it can satisfy data requests simply be streaming the output of
readers which must also stream. The reader stream can be fed into a data
reducing (averaging) filter, and this output is also a stream.

# Streaming in Autoplot

Autoplot has been slow to use streaming, mostly because at some point
all the data will be in memory anyway, so the need is not so great.
However as Autoplot is used to support servers, the need has become more
immediate. For example, the HAPI Server Demonstration loads all the data
into memory and this is then sent out after the data load is complete.
When Autoplot is used to feed data into a Das2Server, it breaks up the
request into smaller granules, and these are sent out, streaming the
data but inefficiently.

Therefore, streaming is finally coming to Autoplot, in a number of
forms. First, Data Sources can support a Streaming capability, and
Autoplot may check to see if this capability is available. Also filters
may begin to support streaming, allowing multiple threads to satisfy
filtering requests.

# Streaming With Scripts

One thing I've only identified as a problem is how scripts would be
dealt with. For example, suppose you have a script that multiplies a
streaming source by -1. It would be nice if Autoplot could allow this
script to be streaming as well.

