Das2Streams and QStreams: Das2Streams are self-describing, streaming
format developed and used by the Plasma Wave Group at the University
of Iowa. "Streaming" is the requirement that at any point along the
stream, you have all the data you need have a valid and complete
stream. They are generally useful for serializing and deserializing
data in das2's internal data model, and Autoplot's QDataSet model.
The design goal is any dataset that can be represented in Autoplot
can be serialized into a das2Stream. "QStream" refers specifically
to a das2Stream with a QDataSet on it, and has the extension .qds.
Legacy das2Streams have a .d2s extension.
  - Mime type: application/x-das2stream
  - Extensions: .d2s .das2stream .qds
  - Example URLs:
    * [9 https://autoplot.org/data/proton_density.qds](https://autoplot.org/data/proton_density.qds)
    * [10 https://autoplot.org/data/proton_velocity_rtn.qds](https://autoplot.org/data/proton_velocity_rtn.qds)
  - Supports Formatting: yes, rank 1, 2, 3 to QStream
  - parameters
      - arg\_0 is the named parameter within the stream, if not
        specified then default parameter is used.
  - output parameters
      - **type**
          - **binary** means format to binary stream
