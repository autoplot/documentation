Purpose: Describe the QStream data format

Audience: das2 developers

# Introduction

Das2's design was that data was streamed out from a central server to
data-rendering clients. These were called Das2Streams and contained the
data in packets and metadata describing how each packet is to be parsed.
When Autoplot was developed, the limits of Das2's data model and the
das2streams become appearent quickly, and QDataSet and QStreams were
developed. Like the Das2Stream, data would be streamed to clients in
packets, but now data could have 3-D and 4-D dimensionality, and bundles
of data (T-\>Bx,By,Bz,N) could be transmitted.

The stream consists of packets of data and packet descriptors that
describe packet types. Each packet is tagged with an identifier that is
used to look up the packet type. This is a two-digit number within
delimiters that indicate the type. For example, "\[01\]" preceeds the
descriptor that defines the format for each packet, preceeded by ":01:".

# Stream Descriptor

`[00]LENGTH`<CONTENT>` where `  
`   LENGTH is six-digit content lenth`  
`   CONTENT is xml content.`

A description of the CONTENT portion follows below, but this describes
the course structure of the stream.

# Packet Descriptors

`[ID]LENGTH`<CONTENT>` where `  
`   ID is two-digit id from 01 to 99.  xx may be used when there will be no references to the packet descriptor.`  
`   LENGTH is six-digit content lenth`  
`   CONTENT is xml content.`

See packet types.

# Packets

`:ID:`<CONTENT>` where`  
`   ID is two-digit reference to a packet descriptor.  Note these are identifiers for stream semmantics, and not the dataset identifiers.`  
`   CONTENT is the data no longer than 1000000 bytes.  It is generally binary but can also be ascii encoded data in a special case.`

# Stream Descriptor XML Content

<stream dataset_id="DSID" byte_order="big_endian"/>  
`   DSID is the name of the default dataset to use.  This ID must be a Java-style identifier ([_a-zA-Z][_a-zA-Z0-9]*).  das2streams could only carry one dataset, so this is to preserve the discovery functionality of the stream.`  
`   byte_order is optional, and when the property is missing, little_endian is default.`

# Packet Descriptor XML

A schema should be written for this, but for now:

<packet>  
`   `<qdataset id="DSID" rank="N">`  (1 or more)`  
`       `<properties>`  (0 or 1)`  
`           `<property name="NAME" type="TYPE" value="" />`  (0 or more properties from QDataSet, or indexed property below)`  
`       `</properties>  
`       `<values encoding="ENCODING" length="INT_LIST" />`  (1, or inline values property below)`  
`   `</qdataset>  
</packet>

Selected properties:

  - qdataset
      - id="DSID" is the Java-style identifier. These are used to
        connect QDataSets to make science abstractions.
      - rank="N" specifies the number of indices used to access the
        data, and is the same as "rank" property in QDataSet.
  - qdataset.properties
      - these are properties used in the QDataSet data model, see
        <http://autoplot.org/QDataSet#DataSet_Properties>
      - Note DEPEND\_0 typically would not be used, but instead
        DEPENDNAME\_0.
  - qdataset.values
      - encoding="ENCODING" The format for each value, such as int4. See
        below.
      - length="INT\_LIST" comma-delineated list of dimension lengths.
        Rank 2 data will have one number that is number of elements for
        each record.

## indexed properties

QDataSets can have properties with an index. For example, to support a
table of different quantities, an index is used in the "bundle
descriptor".

`       `<properties index="0">  
`           `<property name="UNITS" type="units" value="us2000"/>  
`           `<property name="NAME" type="String" value="TimeMin"/>  
`       `</properties>

## inline values

Often it's easiest to just insert the values into the packetDescriptor.
This looks like:

`       `<values values="7.0,8.0,9.0"/>

These must be comma-separated list of doubles. (TODO: check this, it's
possible the units are used to parse.)

## encodings

Data is encoded with the encodings tag. Encoding identifiers include:

  - asciiNN NN-digit ascii field that is parsed as a double.
  - timeNN NN-digit ascii field that is parsed as an ISO8601 UT time.
  - int2, int4, int 8 Little-endian encoded integers. The stream can
    have a property that sets big-endian encoding.
  - float, real4 Four-byte Little-endian encoded reals. The stream can
    have a property that sets big-endian encoding.
  - double, real8 Four-byte Little-endian encoded reals. The stream can
    have a property that sets big-endian encoding.

# Under consideration

## packet lengths in packets

If the packet length was in each packet, then the stream could be
processed without any understanding of the content of the stream. Also,
a character different than the colon could be used to delimit the
packets, which we've wanted to replace for a while, because colons
appear in the data: 2001-02-02T00:01:00 :01:... So perhaps we would have
something like:

`[01]001023<1024 byte xml description of data>`  
`|01|000024<24 bytes of data>`

Note this paves the way for variable-length packets as well.

## Enumeration Units

Das2 allows for Enumeration units that are used to encode integer values
into meaningful strings. For example:

<property name="UNITS" type="enumerationUnit" value="default[1:ON::2:OFF]"/>

says that 1 is to be represented as "ON" and 2 is "OFF". This is
clumbsy, difficult to read, and quite limiting. Something like the
following declaration is better, perhaps a peer to the qdataset node:

<enumeration id="state">  
`   <value="1" label="ON"/>`  
`   <value="2" label="OFF"/>`  
</unit>

and then the dataset would have the property:

<property name="UNITS" type="enumeration" value="state"/>

# Example Streams

Links with the extension .qds are streams:
<http://papco.org:8080/hudson/job/autoplot-test013/ws/>

Stream containing an exception:
<http://papco.org:8080/hudson/job/autoplot-test013/ws/test013_exception.qds>

Rank 1 Temperature\[Time\]:
<http://www-pw.physics.uiowa.edu/~jbf/autoplot/data/qds/temperature.qds>

Rank 2 ds\[Time,En\]:
<http://papco.org:8080/hudson/job/autoplot-test013/ws/test013_spectrogram.qds>

Rank 2 no depends:
<http://papco.org:8080/hudson/job/autoplot-test013/ws/test013_test0_rank2.qds>

Rank 1 just timetags:
<http://papco.org:8080/hudson/job/autoplot-test013/ws/test013_test1.qds>

Rank 2 vector time series:
<http://papco.org:8080/hudson/job/autoplot-test013/ws/test013_test2.qds>

Rank 2 vector time series with multiple packet descriptors:
<http://papco.org:8080/hudson/job/autoplot-test013/ws/test013_test8.qds>

Events Data Set
<http://www-pw.physics.uiowa.edu/~jbf/autoplot/data/qds/BurstModeEvents_2016-08-26_2016-08-28.qds>

Rank 4 DataSet:
<http://www-pw.physics.uiowa.edu/~jbf/autoplot/data/qds/rank4.qds>
