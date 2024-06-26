Purpose: notes about the stream format we talked about at the RPWS
group.

Introduction: first das2streams, then qstreams. qstreams still weren't
clean and extensible. This attempts to fix the problems.

`[T|N|L] `  
`T: the type of packet.  For example, stream descriptor, packet descriptor, or data.`  
`N: the packet identifier.  numbers or zero-length string to indicate anonymous.  This must only be positive and less than 1000, or zero length.`  
`L: decimal length.  Number of bytes following the packet.  Zero is acceptable (heartbeat).  999999999 is limit.`

The type (T) of packet can be one of:

  - S, a stream header. What follows this will always be a valid stream.
    (This is the sync capability we revere but never implement.) Once a
    S is encountered, all Ss can be ignored. This will always be
    anonymous, so that streams have the magic number "\[S||" The
    identifier (N) indicates the scheme for the stream, e.g. das2stream
    or QStream.
  - H, a packet header. This is an xml description of things that will
    be on the stream.
  - h, a zipped packet header. This can be unzipped to become an H.
  - D, a data packet. This is data described by an H with the same
    identifier.
  - d, a zipped packet. This can be unzipped to become a D.
  - C, a comment packet. This is intended to provide non-essential
    metadata such as progress information, etc for a stream.
  - c, a zipped comment packet.

Resolutions about the S11 layer:

  - number of packet types should be kept to a minimum. Semantic layers
    will provide abstraction.
  - one type of compression should be implemented at this layer, since
    it's possible to do compression regardless of content.
  - stream header serves as a sync so it should be its own type.
  - packet headers describe packets.
  - comments are non-essential metadata that can always be removed, like
    stderr messages vs stdout.

That's the S11 layer.

Things to think about:

  - repeat count? This would enable multiple packets to be compressed
    together.

# Limits

Length of packet content, 0..999999999. (9 digits) Length of packet id,
0..999 (3 digits) Length of header packet, without content, is 1 + 1 + 1
+ 3 + 1 + 9 + 1 = 27 bytes. Characters of packet length, must parse as
integer, containing only 0..9 and spaces. Characters of packet id,
containing 0..9.

# Goals

With the old wiki, there was a list of about 12 things we wanted to
accomplish with streams.

  - transmit data
  - ac-hoc method for storing data, just like .idlsav files.
  - provide self-describing but readable format. (ascii format)
  - provide efficient means for transmitting data. (binary format,
    compression.)
  - allow client to sync up with the stream. (like telemetry stream)
  - allow metadata such as progress information to be inserted into the
    stream.
  - valid stream concatenated with valid stream is valid stream.
  - heartbeats or keep-alive messages: comments allow for this...

# Questions

  - Can properties be defined in the S packet, indicating stream
    properties?

` Chris answer:  Of course, the contents of S packets are defined by the`  
` protocol number.  Put whatever you like in there.`

# Proposal on Stream Syntax numbers

How about the following for a starter protocol index list:

  - 0 - Not a legal protocol ID. (Used to terminate a stream?)
  - 1 - Das1 Packets in this chucking format, stream would only have
    \[D\] packets, not \[H\] packets.
  - 2 - Das2 Packets in this chucking format
  - 3 - QStream Packets in this chunking format
  - 4 - Das2.2 server "in-band" queries
  - 100 - Chunked binary object transfer, a way to send a CDF file for
    example

? Also the 900 block is reserved for private use.
