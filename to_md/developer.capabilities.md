Purpose: document use of existing capabilities of DataSource objects.
This was motivated by the poorly-documented Updating capability.

# Overview

An Autoplot datasource implements a number of methods, such as
retrieving the dataset and metadata. It can also be "decorated" to have
additional capabilities. Instead of declaring a subclass and using Java
inheritance, we use a pattern where we can query the object to see if it
has additional capabilities. This document outlines the capabilities.

# TimeSeriesBrowse

The first and probably most important of these capabilities is
TimeSeriesBrowse. This allows clients to query for additional data. For
example, if I ask for 20120203.dat, I have the one file. But if I ask
for $Y$m$d.dat?timerange=2012-02-03, then its TimeSeriesBrowse
capability tells me I can generate URIs for other times and get data.

# Updating

This tells clients that they can listen for updates by registering a
listener.

# Caching

Often it is inexpensive or necessary to read more than the user asked
for, so Caching tells the client to ask it first if a dataset has
already been loaded. For example, when we run a Jython script, all of
the quantities calculated are stored in a cache, so for example, even
though we plot four parameters, the script is only run once.
