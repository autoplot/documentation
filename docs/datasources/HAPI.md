# HAPI servers

HAPI (Heliophysics API) servers provide data using the standard API developed to address
the problem of diverse APIs for data servers in our field.  HAPI defines a standard
minimal set of operations a server needs to be useful, in hopes that many sites will use
the standards, perhaps in addition to the APIs they already provide.  

There are a quite a few of these servers which exist now, including CDAWeb and SSCWeb, and soon
the CFA and PDS-PPI.  

The dialog comes up with an initial selection of the known HAPI servers, a registry is kept
at https://github.com/hapi-server/servers/blob/master/all.txt.  These servers appear in the
droplist, as well as other servers which have been used in the past.  (This allows groups
to set up HAPI servers independently and privately, sharing the location of a HAPI server
among team members, for example.)  

Once the HAPI server is selected, it is queried for its available data sets, and the list is
presented on the left.  When a dataset is selected, then a list of parameters within the 
dataset is shown, and you can select individual parameters to load.  A time range is entered
and the parameters are loaded within the timerange.

Groups considering implementing a data server should look at the HAPI specification 
at https://github.com/hapi-server/data-specification/blob/master/hapi-3.0.0/HAPI-data-access-spec-3.0.0.md .
